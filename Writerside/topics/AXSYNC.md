# Configuração AXSYNC
Para que uma operação seja executada no Axhub, é necessário configurar o AxSync. Siga estes passos para configurar o AxSync e permitir que operações sejam executadas no Axhub:


### Criar Pasta
Crie uma pasta chamada "Axion.AxSync" no LinuxLite.

### Colocar Executáveis
Na pasta "Axion.AxSync", coloque os seguintes arquivos necessários para o funcionamento do aplicativo:

- `app.exe` (ou qualquer outro nome que o aplicativo tenha)
- `setting.json`
- `axion.services`
- `sqlite` (ou quaisquer outros arquivos necessários)

### Trocar Nome do Equipamento no JSON
Para trocar o nome do equipamento no arquivo JSON, siga estas etapas:

1. Abra o arquivo 'setting.json' com um editor de texto.
2. Localize o campo que define o nome do equipamento.
3. Substitua o nome atual pelo novo nome do equipamento.
4. Salve as alterações no arquivo JSON.

### Baixar o .NET 7
Execute os seguintes comandos no terminal para instalar o .NET 7:

```shell
wget https://packages.microsoft.com/config/ubuntu/22.04/packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
rm packages-microsoft-prod.deb
sudo apt-get update
sudo apt-get install -y aspnetcore-runtime-7.0
```

### Criar Arquivo de Autostart do Serviço
Crie o arquivo de serviço para o AxSync:

```shell
sudo nano /etc/systemd/system/AxSync.service
```

<warning>
<p>Atenção: Substitua 'USUARIOLINUX' pelo usuário da máquina nos comandos abaixo.</p>
</warning>

### Colar as Configurações no Arquivo AxSync.service
Aperte `Ctrl+O` para salvar e `Ctrl+X` para sair do editor. Cole o código abaixo:

```shell
[Unit]
Description=Serviço de Envio de Imagens para o AxHUB
[Service]
WorkingDirectory=/home/linuxlite/Axion.AxSync/
ExecStart=/home/linuxlite/Axion.AxSync/Axion.AxSync.Service
Restart=always
# Reiniciar serviço após 10 segundos se o serviço dotnet falhar:
RestartSec=10
KillSignal=SIGINT
SyslogIdentifier=log.axsync
User=linuxlite
TimeoutStopSec=30
[Install]
WantedBy=multi-user.target
```

## Configuração Passo a Passo do OCR das Câmeras

### Configurações do Sistema

**Descrição**

O OCR (Reconhecimento Óptico de Caracteres) é um software responsável por capturar as passagens de veículos por meio da leitura das placas. Ele deve ser configurado corretamente para funcionar com uma câmera conectada à máquina LinuxLite e um módulo de rede.

### Verifique a Conexão da Câmera

1. No LinuxLite, vá até a seção de conexões de rede.
2. Clique em "Editar Conexão" e altere apenas o IP da câmera.
    - Caminho: Ipv4 Settings
        - Método: Mude para "Manual"
        - Clique no botão "Adicionar" em Endereços.
        - Exemplo de IP: `192.168.1.20`
    - Em Ethernet, o método deve ser sempre "Automático".

3. Faça um teste:

```shell
ping 192.168.1.20
```

### Cadastramento do Equipamento

1. **Código do Equipamento:** [Equipamento Cadastrado no AxHub]
2. **Local:** [Endereço]
3. **Nome da Vila:** [Nome da Vila]

### Faixas

1. **Código da Faixa:** [Equipamento Cadastrado no AxHub]
2. **Descrição:** [Sentido da Faixa]

### Câmeras

1. **IP:** Coloque o IP definido da câmera.
2. **URL de Conexão:** Troque apenas o IP da conexão estabelecida.

<warning>
Atenção: Se o OCR não estiver configurado corretamente, as passagens não serão enviadas para o AxHub.
</warning>

## Inicializando a Aplicação

```shell
chmod +x /home/linuxlite/Axion.AxSync/Axion.AxSync.Service
sudo systemctl start AxSync.service
sudo systemctl enable AxSync.service
sudo systemctl status AxSync.service
```

<warning>
Verifique a câmera para garantir que esteja funcionando corretamente para capturar as passagens. Sem a câmera, o AxSync não conseguirá enviar as passagens para o AxHub.
</warning>

## Lista de Comandos Úteis

1. **Procurar Processo em Execução:**
   ```shell
   ps aux | grep Axion
   ```

2. **Listar Todos os Processos:**
   ```shell
   ps -ef
   ```

3. **Matar Processo:**
   ```shell
   sudo kill NUMEROPROCESSO(PID)
   ```

4. **Recarregar Configurações do Autostart:**
   ```shell
   sudo systemctl daemon-reload
   ```

## Erros Recorrentes

<warning>
<p>
Erro: Unknown command verb status AxSync.service.
</p>
</warning>

### Resolução:
Verifique sempre a chave token do fabricante no Axhub. Caso esteja incorreta, substitua a chave atualizada no campo API Key do sistema.

### Exemplo de Configuração JSON

```json
{
  "Logging": {
    "LogLevel": {
      "Default": "Error"
    }
  },
  "DeviceSettings": {
    "DeviceManufacturer": "AxRadar",
    "DeviceCode": "PA602C",
    "HeartbeatInterval": "00:10:00",
    "InfractionCodes": {
      "Speeding": [ "74550", "74630", "74710" ],
      "EvasionBalance": [ "60682" ],
      "RestrictedCirculation": [ "57463" ],
      "StopOverCrosswalk": [ "56732" ],
      "AdvanceRedLight": [ "60503" ],
      "ExclusiveLane": {
        "ExclusiveLanePublicTransportation": [ "75870" ],
        "RightExclusiveLane": [ "56810" ],
        "LeftExclusiveLane": [ "56900" ],
        "TargetLane": [ "57030" ]
      },
      "ProhibitedTurn": {
        "Return": [ "59910" ],
        "RightTurn": [ "60411" ],
        "LeftTurn": [ "60412" ]
      }
    }
  },
  "ApiSettings": {
    "ApiKey": "04953762da404159938197711bb9b3d3",
    "ApiEndpoint": "https://imetropa.axhub-api.axion.ws"
  },
  "AxRadarSettings": {
    "RootImageFolder": "/home/linuxlite/appOCR/Imagens/",
    "ImagesFolder": "/home/linuxlite/appOCR/Imagens/Capturas",
    "TestImagesFolder": "/home/linuxlite/appOCR/Imagens/ImagemTeste"
  },
  "VelsisSettings": {
    "SendPassageImage": true,
    "PassageImageTypes": [ "ZT", "ZF" ],
    "RootImageFolder": "D:\\VSRadarFixoLaser",
    "InfractionImageFolder": "D:\\VSRadarFixoLaser\\Exporta\\",
    "PassageImageFolder": "D:\\VSRadarFixoLaser\\ExportaImagensPassagem",
    "PassageTxtFolder": "D:\\VSRadarFixoLaser\\Exporta"
  }
}
```

### Verifique o Comando

#### Arquivo de Configuração do Serviço

```shell
[Unit]
Description=Serviço de Envio de Imagens para o AxHUB
[Service]
WorkingDirectory=/home/USUARIOLINUX/Axion.AxSync/
ExecStart=/home/USUARIOLINUX/Axion.AxSync/Axion.AxSync.Service
Restart=always
# Reiniciar serviço após 10 segundos se o serviço dotnet falhar:
RestartSec=10
KillSignal=SIGINT
SyslogIdentifier=log.axsync
User=USUARIOLINUX
TimeoutStopSec=30
[Install]
WantedBy=multi-user.target
```

#### Atalhos de Teclado no Linux

Para salvar e sair do editor, pressione `CTRL + O` para salvar e `CTRL + X` para sair.

### Comandos para Executar

```shell
chmod +x /home/linuxlite/Axion.AxSync/Axion.AxSync.Service
sudo systemctl start AxSync.service
sudo systemctl enable AxSync.service
sudo systemctl status AxSync.service
```
Claro, aqui está a parte solicitada revisada e melhorada:

---

## Verificação das Passagens no Axhub

1. **Preparar a Câmera:**
    - Posicione a câmera para capturar as passagens dos veículos, garantindo que ela esteja configurada para enviar os dados ao Axhub.

2. **Iniciar o OCR:**
    - Na área de trabalho, clique no arquivo Start.sh para iniciar o OCR.

3. **Verificar as Imagens Enviadas:**
    - Navegue até a pasta `linuxLite/imagens/enviadas`.
        - Se a pasta `enviadas` estiver presente e contiver imagens, isso indica que as imagens estão sendo enviadas para o Axhub.
        - Se a pasta `enviadas` não estiver presente ou estiver vazia, as imagens permanecerão como pendentes até que a configuração seja corrigida.

4. **Verificar Passagens no AxHub:**
    - No AxHub, vá para a seção de operações.
    - Selecione o equipamento cadastrado no OCR e clique em "Editar".
    - No Dashboard, verifique a seção "OCR nas Últimas 48 Horas" para confirmar se as passagens estão sendo recebidas e processadas corretamente.
