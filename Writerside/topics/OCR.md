# OCR
Após configurar o Axsync, é necessário ajustar as configurações do OCR para a captura de imagens, no OCR Configurator

<warning>
É necessário criar a Operação no AxHub para a entrega das passagens.</warning>


##  Equipamento
![Imagem do WhatsApp de 2024-08-20 à(s) 10.26.00_145c0c49.jpg](Imagem_do_WhatsApp_de_2024-08-20_à(s)_10.26.00_145c0c49.jpg)

- **Código do Equipamento**: Deve ser cadastrado exatamente igual no AxHub para garantir que a legenda da imagem seja exibida corretamente.![image_10.png](image_10.png)
- **Local**: Refere-se ao endereço onde o equipamento está instalado.
- **Nome da Via**: Refere-se ao endereço da Faixa onde o equipamento está instalado.
### Opção de Configuração
 1. Debug Passagens
 2. Consultar Tipo de Veículo
 3. Gerar Imagem Teste
 4. Realizar Identificação Jidosha
 5. Realizar Identificação OPENALPR
 6. Gravar Movimento Sem Veículos
 7. Acionar Iluminador Apenas Com Movimento

##  Faixas

![Imagem do WhatsApp de 2024-08-20 à(s) 10.26.10_5e641ee3.jpg](Imagem_do_WhatsApp_de_2024-08-20_à(s)_10.26.10_5e641ee3.jpg)

- **Escolha da Faixa a Configurar**: Refere-se à configuração da faixa selecionada na operação. Cada operação pode incluir várias faixas de equipamento.
- **Status**: Indica o status da faixa.
<warning> Atenção: Apenas uma faixa pode estar ativa por vez. </warning>

- **Código**: Número da faixa registrada no AxHub.
- **Descrição**: Sentido da faixa registrada no AxHub.
<warning> Atenção: Não utilize barras, apenas traços são permitidos.</warning>

- **Sentido de Captura**: Será afastado ou aproximado para melhorar a qualidade da captura da imagem.





##  Cameras
![Imagem do WhatsApp de 2024-08-21 à(s) 14.35.35_c2743db8.jpg](Imagem_do_WhatsApp_de_2024-08-21_à(s)_14.35.35_c2743db8.jpg)

O painel de configuração de câmeras permite ajustar diversos parâmetros para o funcionamento correto da câmera e a captura de imagens para OCR. A seguir, detalhamos cada campo de configuração:

1. **Escolha a Câmera a Configurar**:
    - Selecione a câmera que deseja configurar a partir da lista disponível.

2. **IP**:
    - Endereço IP da câmera. No exemplo, o IP configurado é `192.168.1.10`.

3. **Protocolo**:
    - Protocolo utilizado pela câmera para comunicação.`PUMATRONIX`, `ONVIF`.

4. **Resolução Saída Largura**:
    - Define a largura da resolução de saída da imagem capturada. Exemplo: `752`.

5. **Resolução Saída Altura**:
    - Define a altura da resolução de saída da imagem capturada. Exemplo: `480`.

6. **Detecção Percentual Movimento**:
    - Define o percentual mínimo de movimento necessário para que a câmera detecte uma mudança. Exemplo: `10`.

7. **Altura Ideal Placa**:
    - Configuração para a altura ideal da placa em pixels na imagem capturada. Exemplo: `300`.

8. **Percentual Variação Nova Placa**:
    - Define o percentual de variação permitido para reconhecer uma nova placa. Exemplo: `0.10`.

9. **Opções de Configuração**:
    - **Identificar Placa Na Imagem**: Permite a identificação da placa na imagem capturada.
    - **Exibir Imagem Ao Vivo**: Exibe a imagem ao vivo da câmera.
    - **Gravar Imagem Ao Vivo**: Habilita a gravação da imagem ao vivo.
    - **Debug Detecção Veículo**: Habilita o modo de depuração para detecção de veículos.

10. **Testar Conexão Câmera**:
    - Botão para testar a conexão da câmera com as configurações definidas.

11. **Configurar Detecção**:
    - Botão para configurar as opções avançadas de detecção da câmera.

12. **URL Conexão**:
    - URL gerada automaticamente para conexão com a câmera, que inclui o IP, porta e parâmetros de streaming. Exemplo:
      ```
      rtsp://admin:@192.168.1.10:554/H264?ch=1&subtype=0
      ```
##  Conexões
![Imagem do WhatsApp de 2024-09-03 à(s) 08.51.55_e59ae757.jpg](Imagem_do_WhatsApp_de_2024-09-03_à(s)_08.51.55_e59ae757.jpg)

## Diretorios
![Imagem do WhatsApp de 2024-09-03 à(s) 08.52.08_e8f3b17f.jpg](Imagem_do_WhatsApp_de_2024-09-03_à(s)_08.52.08_e8f3b17f.jpg)
##  Ocr
![Imagem do WhatsApp de 2024-09-03 à(s) 08.52.21_f92fa54d.jpg](Imagem_do_WhatsApp_de_2024-09-03_à(s)_08.52.21_f92fa54d.jpg)
##  Agendamento
![Imagem do WhatsApp de 2024-09-03 à(s) 08.52.40_23a0a221.jpg](Imagem_do_WhatsApp_de_2024-09-03_à(s)_08.52.40_23a0a221.jpg)