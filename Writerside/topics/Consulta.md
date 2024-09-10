# Consulta

![image_20.png](image_20.png)

### Consultar Infrações

Esta tela apresenta uma visão geral das infrações registradas no sistema, permitindo ao usuário consultar, filtrar e exportar dados de infrações para análise ou auditoria. Abaixo estão descritos os principais elementos e funcionalidades da tela.

---

####  Filtros de Consulta

No topo da tela, você pode filtrar as infrações com base em:
- **Data da Infração**: Definir o intervalo de tempo da infração a ser consultada, utilizando as colunas "De" e "Até" para determinar o início e o fim das datas.
- **Horário da Infração**: Definir o intervalo de horário das infrações que você deseja consultar.
- **Mais Filtros**: Ao clicar neste botão, outros filtros específicos podem ser disponibilizados, permitindo uma busca mais detalhada de acordo com outros parâmetros do sistema.

#### Botões de Ação

- **Filtrar**: Executa a pesquisa com base nos parâmetros definidos pelos filtros.
- **Limpar**: Restaura os campos de filtro aos seus valores padrão, removendo qualquer critério de busca previamente aplicado.

---

####  Tabela de Resultados

A tabela abaixo exibe os resultados da consulta de infrações, contendo as seguintes colunas:

- **ID**: Identificador único de cada infração no sistema.

- **Sequencial**: Indica o número sequencial de cada infração na ordem de processamento.

- **AIT**: Número do Auto de Infração de Trânsito (AIT) correspondente à infração registrada.

- **Data**: Exibe a data e o horário exatos em que a infração foi registrada.

- **Placa Veículo**: A placa do veículo que cometeu a infração, permitindo identificar o infrator.

- **Tipo Infração**: Descreve o tipo da infração cometida. Neste exemplo, o tipo de infração mostrado é "Cronotacógrafo".

- **Enquadramento**: Indica o código ou o artigo do regulamento que foi infringido pelo veículo.

- **Status Processamento**: Indica o status atual do processamento da infração:
    - **Processada** (em verde): Significa que a infração foi processada corretamente pelo sistema.
    - **Descartada** (em vermelho): Significa que a infração foi descartada durante o processo de validação ou auditoria.

- **Usuário Triagem**: Nome ou identificador do usuário responsável por realizar a triagem ou auditoria daquela infração.

- **Exportado**: Indica se a infração foi ou não exportada para um arquivo externo ou sistema. Um ícone ou texto correspondente deve aparecer nesta coluna para mostrar o status de exportação.

- **Ações**: Botão que permite **visualizar** mais detalhes sobre a infração específica. Ao clicar no ícone "olho", uma nova janela ou seção pode ser aberta com informações adicionais.

---

#### Funcionalidades Principais

- **Consulta Detalhada**: O usuário pode utilizar os diversos filtros para restringir os resultados e encontrar infrações com base em parâmetros como data, horário, placa do veículo, tipo de infração e status.

- **Visualização de Detalhes**: Ao clicar no botão "olho" na coluna **Ações**, é possível acessar detalhes adicionais sobre cada infração, como imagens capturadas (se aplicável), mais informações sobre o veículo e o motorista, ou outros dados específicos da infração.

- **Status de Processamento e Auditoria**: O sistema permite que os usuários acompanhem o status de cada infração, sabendo se ela foi processada corretamente ou se foi descartada, além de poder identificar o usuário que fez a triagem.

