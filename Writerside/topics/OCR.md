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


- **Câmera Zoom**: Câmeras do tipo zoom devem ser configuradas na seção de câmeras.

- **Câmera Panorâmica**: Câmeras panorâmicas também devem ser configuradas na seção de câmeras.


##  Cameras
![Imagem do WhatsApp de 2024-08-21 à(s) 14.35.35_c2743db8.jpg](Imagem_do_WhatsApp_de_2024-08-21_à(s)_14.35.35_c2743db8.jpg)

<warning>Para que a configuração das câmeras seja realizada, é necessário que as câmeras estejam ligadas e com o IP devidamente configurado.</warning>

- **Escolha a Camera a Configurar** 

- **IP**: Endereço IP da câmera.

  
#### **Tipo de Câmera Manual**: Selecione o tipo como **ONVIF**.
- **Conecte a Câmera**: Certifique-se de conectar a câmera antes de iniciar a configuração.
- **Caminho para Configuração**: Acesse **Edit Connections > Ethernet > Camera > Editing Wired Connection 1> Method : Manual**.
- 

![image_11.png](image_11.png)

- **Método de Configuração**: Defina o **Method** como **Manual**.
- **Adicionar um IP**:
    - A maioria dessas câmeras utiliza o IP **192.168.1.20**.
    - Pressione **Enter** para confirmar o IP.
    - Em **Netmask**, insira **24** e pressione **Enter** novamente.
- **Salvar Configurações**: Após realizar os ajustes, clique em **Save** para salvar as configurações.

#### **Tipo de Câmera**: Selecione o tipo como **Pulmatronix**.

- A câmera deve ter um IP automático que corresponda ao mesmo IP da rede de internet, por exemplo, na rede da internet Starlink
  ![686c0921-4878-4733-bf6d-237c56c95864.jpg](686c0921-4878-4733-bf6d-237c56c95864.jpg)
- Insira o **Admin** e a **Senha** da câmera, conforme fornecido no manual do equipamento.
- **Altere o IP da câmera para** **192.168.1.201** para garantir a configuração correta.
- **Caminho para Configuração**: Acesse **Edit Connections > Ethernet > Camera > Editing Wired Connection 1> Method : Automatic**.

- **Protocolo**: Escolha o tipo de câmera a ser configurada.

- **Resolução Saída Largura**: Define a largura da resolução de saída da imagem capturada

- **Resolução Saída Altura**:Define a altura da resolução de saída da imagem capturada.

- **Detecção Percentual Movimento**: Define o percentual mínimo de movimento necessário para que a câmera detecte uma mudança
- 
- **Altura Ideal Placa**: Configuração para a altura ideal da placa em pixels na imagem capturada

- **Percentual Variação Nova Placa** Define o percentual de variação permitido para reconhecer uma nova placa.


#### **Tipo de Câmera**: Selecione o tipo como **Radar**.


### **Opções de Configuração**:

**Identificar Placa Na Imagem**: 
**Exibir Imagem Ao Vivo**: 
**Gravar Imagem Ao Vivo**: 
**Debug Detecção Veículo**: 

- **Testar Conexão Câmera**: Botão para testar a conexão da câmera com as configurações definidas.

<warning>Para que a detecção da câmera funcione corretamente, é necessário que a câmera esteja configurada e que a URL de conexão seja inserida corretamente.</warning>

- **URL Conexão**: URL gerada automaticamente para conexão com a câmera, que inclui o IP, porta e parâmetros de streaming.

Url da Camera ONVIF
  ```
  rtsp://admin:@192.168.1.10:554/H264?ch=1&subtype=0
  ```
Url da Camera Pulmatronix
  ```
  rtsp://admin:@192.168.0.201:554/H264?ch=1&subtype=0
  ```
- **Configurar Detecção**:Botão para configurar as opções avançadas de detecção da câmera.
![image_12.png](image_12.png)

##  Conexões
![Imagem do WhatsApp de 2024-09-03 à(s) 08.51.55_e59ae757.jpg](Imagem_do_WhatsApp_de_2024-09-03_à(s)_08.51.55_e59ae757.jpg)
- **API Key**: Chave de autenticação para acessar o serviço OCR principal.
- **URL Servidor OCR - Principal**: Endereço IP e porta do servidor principal que realiza o reconhecimento óptico de caracteres.
- **URL Servidor OCR - Secundario**: Endereço IP e porta de um servidor secundário de OCR para redundância.
- **URL BD Placas**: Configuração da URL de conexão ao banco de dados de placas, incluindo o host, porta, usuário e senha.
- **URL Servidor OpenALPR**: Endereço da API do serviço OpenALPR para reconhecimento de placas veiculares.
- **API Key OpenALPR**: Chave de autenticação para acessar o serviço OpenALPR.
- **URL Servidor Plate Recognizer**: Endereço da API do serviço Plate Recognizer para o reconhecimento de placas.
- **API Key Recognizer**: Chave de autenticação para o serviço Plate Recognizer.


## Diretorios
![Imagem do WhatsApp de 2024-09-03 à(s) 08.52.08_e8f3b17f.jpg](Imagem_do_WhatsApp_de_2024-09-03_à(s)_08.52.08_e8f3b17f.jpg)

- **Diretório Imagem Teste**: Local onde são armazenadas imagens de teste para o sistema de OCR.

- **Diretório Capturas**: Contém imagens capturadas, possivelmente de uma câmera ou outra fonte de entrada.

- **Diretório Passagens**: Provavelmente armazena imagens relacionadas a veículos em trânsito ou passagens de leitura automática.

- **Diretório Sem Placas**: Armazena imagens que foram identificadas como não contendo placas, ou onde as placas não foram detectadas corretamente.

- **Diretório Leituras**: Pode armazenar imagens que estão sendo processadas ou que já foram lidas pelo sistema OCR.

- **Diretório Imagem**: Um diretório geral que contém todas as imagens ou serve como ponto de acesso principal para imagens.

- **Diretório Imagens Ao Vivo**: Armazena imagens capturadas em tempo real, provavelmente de um feed ao vivo.

- **Diretório Debug**: Contém imagens usadas para fins de depuração, possivelmente usadas para ajustar ou testar o sistema de OCR.

- **Diretorio Arquivo Contagem**: Pode conter imagens ou dados relacionados à contagem de algum tipo, como o número de veículos ou leituras processadas.

![Imagem do WhatsApp de 2024-09-03 à(s) 08.52.21_f92fa54d.jpg](Imagem_do_WhatsApp_de_2024-09-03_à(s)_08.52.21_f92fa54d.jpg)


##  Configurações de OCR

A aba "OCR" permite configurar diversos parâmetros relacionados à leitura de placas utilizando sistemas de OCR (Reconhecimento Óptico de Caracteres). A seguir, estão descritos os campos e opções disponíveis:

1. **Engine OCR Local**: Seleciona o mecanismo de OCR local a ser utilizado para leitura de placas. Opções disponíveis incluem diferentes motores OCR que podem estar instalados no sistema, como "AXION".

2. **Engine Segunda Leitura OCR**: Define o segundo mecanismo de OCR a ser utilizado para uma segunda leitura de placas. Este campo permite configurar uma redundância para melhorar a acurácia da leitura, com opções como "PLATERECOGNIZER".

3. **Qtde Máxima Frames OCR Por Passagem**: Determina a quantidade máxima de frames (quadros de vídeo) que serão processados pelo OCR durante a passagem de um veículo. Exemplo: "30" frames.

4. **Qtde Frames Sem Placa Após Primeira Placa**: Configura o número de frames que podem ser processados sem detectar uma placa, após a primeira leitura bem-sucedida. Exemplo: "2" frames.

5. **Atraso Consulta Veículo**: Especifica o atraso (em segundos) para a consulta de um veículo após sua detecção inicial. Este valor é útil para evitar leituras duplicadas ou incorretas. Exemplo: "20" segundos.

6. **Tempo Máximo Consulta Servidor OCR**: Define o tempo máximo (em segundos) para realizar uma consulta ao servidor OCR. Se o tempo exceder este limite, a consulta é interrompida. Exemplo: "5" segundos.

#### Opções de Leitura de Placas (Checkboxes)

- **Realizar Leitura Placa Local**: Ativa a leitura de placas utilizando o OCR local configurado.

- **Realizar Leitura Placa Servidor**: Habilita a leitura de placas utilizando um servidor OCR remoto.

- **Realizar Leitura Placa OPENALPR**: Configura a leitura de placas através do motor OCR OPENALPR.

- **Ler Apenas Primeira Placa**: Quando ativada, apenas a primeira placa detectada será lida e processada.

- **Habilitar Filtro Sharpen**: Ativa um filtro de nitidez (sharpen) para melhorar a qualidade da imagem antes da leitura OCR.

- **Realizar Leitura Placa PlateRecognizer**: Utiliza o motor OCR PlateRecognizer para a leitura de placas.

- **Realizar Leitura Placa Segunda Engine Caminhões**: Configura uma segunda leitura de OCR específica para caminhões utilizando um motor secundário.

- **Realizar Leitura Placa Segunda Engine Diurno**: Ativa uma segunda leitura de OCR durante o dia utilizando um motor secundário.

- **Realizar Leitura Placa Segunda Engine Noturno**: Ativa uma segunda leitura de OCR durante a noite utilizando um motor secundário.

- **Descartar Caminhões Sem Placa**: Configura o sistema para descartar a leitura de caminhões que não possuam uma placa detectável.

- **Descartar Sem Classe Sem Placa**: Configura o sistema para descartar veículos sem classificação e sem placa detectável.

##  Agendamento
![Imagem do WhatsApp de 2024-09-03 à(s) 08.52.40_23a0a221.jpg](Imagem_do_WhatsApp_de_2024-09-03_à(s)_08.52.40_23a0a221.jpg)

A aba "Agendamento" permite configurar os horários de operação das câmeras, ajustando parâmetros como o tempo de abertura do obturador (shutter), o nível de exposição, o ganho e o modo de operação (dia/noite). A seguir estão descritos os campos e opções disponíveis:

1. **IP**: Este campo lista o endereço IP das câmeras que estão configuradas para o agendamento. Cada linha representa uma câmera específica identificada pelo seu endereço IP.

2. **Hora Início**: Define a hora de início do agendamento para a câmera correspondente. Este é o horário em que as configurações especificadas (shutter, nível, ganho, modo) começam a ser aplicadas. O formato de hora é "HH:MM".

3. **Hora Fim**: Define a hora de término do agendamento para a câmera correspondente. Este é o horário em que as configurações especificadas deixam de ser aplicadas. O formato de hora é "HH:MM".

4. **Shutter**: Configura o tempo de abertura do obturador da câmera (em milissegundos). Um valor mais alto aumenta o tempo de exposição, o que pode ser útil em condições de pouca luz, mas pode resultar em imagens borradas se houver movimento.

5. **Nível**: Ajusta o nível de exposição da câmera. Este parâmetro pode influenciar a luminosidade da imagem capturada.

6. **Ganho**: Configura o ganho da câmera, que é utilizado para amplificar o sinal de vídeo em condições de baixa luz. Um ganho mais alto pode resultar em imagens mais claras, mas também pode aumentar o ruído na imagem.

7. **Modo**: Define o modo de operação da câmera para o agendamento específico. As opções disponíveis são "DAY" (Dia) e "NIGHT" (Noite), que ajustam automaticamente a câmera para otimizar a captura de imagens de acordo com a luz ambiente.

### Tabela de Agendamento

A tabela permite configurar múltiplos agendamentos para cada câmera, ajustando os parâmetros conforme necessário para diferentes horários do dia ou condições de iluminação. Por exemplo:

- **192.168.0.201** está configurada para operar no modo "DAY" das 06:00 às 10:00 com um shutter de 60 ms, nível de 20, e ganho de 70.
- **192.168.0.202** alterna entre o modo "DAY" e "NIGHT" dependendo do horário configurado, ajustando os parâmetros como o shutter e ganho conforme a luz ambiente muda.

 