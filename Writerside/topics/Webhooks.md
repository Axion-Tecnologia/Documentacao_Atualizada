# Webhooks

## Manual de Integração AxHub via Webhook

O AxHub ativamente conecta-se a serviços externos informando eventos importantes via Webhooks. Com eles, seu serviço externo fica informado sempre que determinada ação acontecer.

### Habilitando Webhooks

No AxHub, acesse o menu “Configurações” e no submenu “Webhooks”. Na lista de Webhooks, clique no botão “Novo”, preencha o campo com a “URL” do serviço no qual você deseja receber eventos, selecione o “Tipo do Evento”, selecione as “Operações” e marque o campo “Transacional” (*) se deseja validar o envio, e em seguida clique em Salvar.

<tip>
Ao criar um novo Webhook, faremos uma chamada do tipo POST para a URL informada no campo e esperamos receber uma resposta de status 200 caso o campo “Transacional” esteja marcado.
</tip>

### Tipos de Envios

**0 - Lote de Importação:**
Este evento ocorre sempre que um novo lote de importação de passagens, infrações ou imagens de teste chega ao sistema. Este evento não envia os dados do conteúdo do lote, mas somente as informações do cabeçalho do lote.

**1 - Passagem:**
Este evento ocorre sempre que uma nova passagem chega ao AxHub. Especificamente para este evento de passagem, todas elas são disparadas, seja com ou sem imagens.

**2 - Passagem com Imagem:** 
Este evento se limita a uso interno da Axion, pois não é enviada a imagem em Base64, mas somente o caminho da imagem no storage para integração interna entre nossos sistemas internos. Ocorre sempre que uma nova passagem chega ao AxHub sendo disparado somente para passagens com imagens.

**3 - Passagem com Imagem Base64:**
Este evento é para integração com sistemas externos, pois a imagem é enviada no corpo da mensagem em Base64. Ocorre sempre que uma nova passagem chega ao AxHub sendo disparado somente para passagens com imagens.

**4 - Infração:**
É disparado sempre que uma nova infração chega ao AxHub.

**5 - Imagem de Teste:**
É disparado sempre que uma nova imagem de teste chega ao AxHub.

### Envio Transacional

O envio transacional aguarda o retorno da requisição para validar se o cliente recebeu o registro. O envio não transacional ignora o resultado do envio.

Caso o envio falhe, o serviço agenda o reenvio por mais 10 tentativas em um determinado intervalo de tempo. Após todas as tentativas falharem, o envio é cancelado.

### Objeto Evento

```json
{
  "TipoEvento": 3,
  "Payload": "{}",
  "DataCriacao": "2024-06-12T11:50:16.8966199-03:00",
  "DataAtualizacao": "2024-06-12T11:50:16.8966202-03:00",
  "CodigoWebhook": 1
}
```

### Evento

| Campo           | Obrigatório | Tipo     | Observações                                                                                                                                                    |
|-----------------|-------------|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TipoEvento      | Sim         | Int      | 0 - Lote de Importação<br>1 - Passagem<br>2 - Passagem com Imagem<br>3 - Passagem com Imagem Base64<br>4 - Infração<br>5 - Imagem de Teste                     |
| Payload         | Sim         | String   | Objeto serializado em String referente ao tipo do evento.<br>O Payload pode ser do tipo:<br>• Lote Importação<br>• Passagem<br>• Infração<br>• Imagem de Teste |
| DataCriacao     | Não         | DateTime | Data e hora da criação do evento                                                                                                                               |
| DataAtualizacao | Não         | DateTime | Data e hora da última tentativa de envio                                                                                                                       |
| CodigoWebhook   | Não         | Int      | Código do cadastro de Webhooks                                                                                                                                 |

### Payload Passagem

```json
{
  "Id": 0,
  "DataHoraPassagem": "2024-06-12T11:49:00",
  "CodigoEquipamento": "T1001",
  "PlacaVeiculo": "AAA0A00",
  "VelocidadeMedida": 84,
  "VelocidadeConsiderada": 77,
  "TamanhoVeiculo": 4,
  "QuantidadeEixo": 2,
  "MarcaVeiculo": "",
  "ModeloVeiculo": "",
  "CorVeiculo": "",
  "ArrivalDateTime": "2024-06-12T11:50:08.623",
  "Faixa": {
    "Codigo": "T1001-1",
    "NumeroFaixa": 1,
    "Latitude": -5.0938720703125,
    "Longitude": -42.7659530639648,
    "Municipio": "Teresina",
    "SentidoFaixa": "LESTE - OESTE FAIXA 1"
  },
  "Imagens": [{
    "NomeArquivo": "T1001-2024-06-12-11-49-00.JPG",
    "CodigoTipoImagem": "1",
    "ImagemBase64": ""
  }],
  "ClassificacaoVeiculo": {
    "Codigo": "",
    "Descricao": ""
  }
}
```

### Campos do Payload Passagem

| Campo                               | Obrigatório   | Tipo     | Observações                            |
|-------------------------------------|---------------|----------|----------------------------------------|
| Id                                  | Sim           | Int      |                                        |
| DataHoraPassagem                    | Sim           | DateTime | Formato: yyyy-MM-ddTHH:mm:ss.fffzzz    | 
| CodigoEquipamento                   | Sim           | String   | Código do cadastro de equipamentos     |
| PlacaVeiculo                        | Não           | String   |                                        |
| VelocidadeMedida                    | Não           | Int      | Velocidade em Km/h                     |
| VelocidadeConsiderada               | Não           | Int      | Velocidade em Km/h                     |
| TamanhoVeiculo                      | Não           | Double   | Tamanho em metros                      |
| QuantidadeEixo                      | Não           | Int      |                                        |
| MarcaVeiculo                        | Não           | String   |                                        |
| ModeloVeiculo                       | Não           | String   |                                        |
| CorVeiculo                          | Não           | String   |                                        |
| ArrivalDateTime                     | Não           | DateTime | Formato: yyyy-MM-ddTHH:mm:ss.fffzzz    |
| **Faixa**                           | Sim           | Object   |                                        |
| &nbsp;&nbsp;&nbsp;Codigo            | Sim           | String   | Código do cadastro de faixas           |
| &nbsp;&nbsp;&nbsp;NumeroFaixa       | Sim           | Int      |                                        |
| &nbsp;&nbsp;&nbsp;Latitude          | Não           | Double   |                                        |
| &nbsp;&nbsp;&nbsp;Longitude         | Não           | Double   |                                        |
| &nbsp;&nbsp;&nbsp;Municipio         | Não           | String   |                                        |
| &nbsp;&nbsp;&nbsp;SentidoFaixa      | Não           | String   |                                        |
| **Imagens**                         | Não           | Array    |                                        |
| &nbsp;&nbsp;&nbsp;NomeArquivo       | Sim           | String   |                                        |
| &nbsp;&nbsp;&nbsp;CodigoTipoImagem  | Não           | String   | Código do cadastro de tipos de imagens |
| &nbsp;&nbsp;&nbsp;ImagemBase64      | Sim           | String   | Imagem no formato Base64               |
| **ClassificacaoVeiculo**            | Não           | Object   |                                        |
| &nbsp;&nbsp;&nbsp;Codigo            | Não           | String   | Código do cadastro de classificações   |
| &nbsp;&nbsp;&nbsp;Descricao         | Não           | String   |                                        |