
# Veículos Monitorados

### Visão Geral
O módulo de **Relatórios** do AxCross é uma ferramenta essencial para o monitoramento e análise detalhada de dados de tráfego e veículos. Ele oferece insights críticos para a gestão de infraestruturas de tráfego, permitindo aos administradores tomar decisões informadas com base em dados precisos e em tempo real.


#### 1. Veículos Monitorados
- **Descrição**: A seção de **Veículos Monitorados** fornece uma visão abrangente dos veículos registrados no sistema. Isso inclui veículos em monitoramento ativo e aqueles que têm ocorrências específicas associadas.
- **Funcionalidades**:
    - **Adicionar Veículo Monitorado**:
        - **Placa do Veículo**: Campo de texto obrigatório para inserir a placa do veículo. Este é o identificador principal do veículo no sistema.
        - **Habilitado**: Checkbox para ativar ou desativar o monitoramento do veículo. Isso é útil para suspender temporariamente o monitoramento sem remover o veículo do sistema.
        - **Tipo de Ocorrência**: Menu suspenso para selecionar o tipo de ocorrência relacionado ao veículo, como excesso de velocidade, entrada não autorizada, etc. Esta classificação ajuda a filtrar e analisar dados por tipo de evento.

#### 2. Tipos de Ocorrências
- **Descrição**: esta funcionalidade permite a criação e personalização dos tipos de ocorrências que o sistema deve monitorar. Isso inclui a configuração de novos tipos de eventos e a edição dos existentes.
- **Funcionalidades**:
    - **Adicionar Tipo de Ocorrência**:
        - **Código**: campo obrigatório para um identificador único do tipo de ocorrência. Isso facilita a referência e a filtragem de ocorrências nos relatórios.
        - **Nome**: nome descritivo que identifica claramente o tipo de ocorrência. Isso é exibido em relatórios e alertas.
        - **Cor**: Seleção de cor para a visualização de ocorrências nos gráficos e dashboards. As cores ajudam a diferenciar visualmente os tipos de ocorrência.
        - **Emitir Alerta Sonoro**: Checkbox para definir se um alerta sonoro deve ser emitido quando essa ocorrência é registrada, alertando operadores em tempo real sobre eventos críticos.

#### 3. Alertas
- **Descrição**: O sistema de alertas é projetado para notificar os usuários sobre eventos importantes ou anomalias detectadas. Isso inclui a configuração de alertas baseados em tipos de ocorrências específicas.
- **Funcionalidades**:
    - **Configurar Alerta**:
        - **Nome**: Campo obrigatório para o nome do alerta, usado para identificação e gestão dos alertas.
        - **Desabilitar**: Opção para desativar o alerta temporariamente, sem excluí-lo. Isso é útil durante períodos de manutenção ou ajustes.
        - **Tipo de Ocorrência**: Seleção do tipo de ocorrência que aciona o alerta. Permite focar em eventos específicos.
        - **Tipo de Notificação**: Escolha do método de notificação (por exemplo, Email, SMS, notificações in-app), permitindo personalizar como os alertas são entregues.
        - **Destinatário**: Definição de quem receberá o alerta. Pode incluir múltiplos destinatários, como equipes de segurança ou gerentes de tráfego.
        - **Equipamentos**: Seleção de equipamentos específicos associados ao alerta, permitindo monitorar e responder a eventos em dispositivos ou locais específicos.

#### 4. Classificações de Veículos
- **Descrição**: Esta seção permite a classificação de veículos em diferentes categorias, como automóveis, caminhões, ônibus, etc. Isso ajuda a organizar os dados e facilita a análise específica por tipo de veículo.
- **Funcionalidades**:
    - **Adicionar Classificação de Veículo**:
        - **Nome**: Campo obrigatório para o nome da classificação, que será usado para identificar e agrupar veículos no sistema.

### Considerações Finais
- **Personalização**: O AxCross permite uma personalização robusta para se adaptar às necessidades específicas de diferentes usuários e cenários. Isso inclui a personalização de tipos de ocorrência, alertas e classificações de veículos.
- **Escalabilidade e Integração**: O sistema é escalável e pode ser integrado com outros sistemas e sensores, aumentando sua utilidade em ambientes complexos de tráfego e infraestrutura.
- **Segurança e Conformidade**: As funcionalidades de monitoramento e alertas são desenhadas para cumprir com normas de segurança e privacidade, assegurando que os dados sejam usados de maneira ética e protegida.

