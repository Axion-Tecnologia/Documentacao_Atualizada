# Aferições

Vamos documentar a funcionalidade "Aferições" do Axhub com base nas imagens fornecidas.

#### Visão Geral
A funcionalidade "Aferições" no Axhub é usada para gerenciar e registrar informações relacionadas às aferições de equipamentos. Esta seção permite a visualização detalhada, edição e gerenciamento dos dados de aferições, incluindo informações sobre o número do Inmetro, lacre, laudo, e datas relevantes.

#### Tela de Listagem de Aferições
- **Objetivo:** Exibir uma lista completa de todas as aferições registradas no sistema.
- **Componentes Principais:**
    - **Número Inmetro:** Número de registro no Inmetro associado ao equipamento.
    - **Número de Série:** Identificação única do equipamento.
    - **Número Laudo:** Identificação do laudo técnico relacionado à aferição.
    - **Número do Lacre:** Número do lacre de segurança do equipamento.
    - **Data de Aferição:** Data em que a aferição foi realizada.
    - **Data de Emissão:** Data em que o laudo da aferição foi emitido.
    - **Data de Vencimento:** Data de validade da aferição, indicando quando uma nova aferição será necessária.

- **Ações Disponíveis:**
    - **Editar:** Permite ao usuário editar os detalhes da aferição selecionada.
    - **Excluir:** Remove a aferição do sistema.

#### Tela de Edição de Aferições
- **Objetivo:** Facilitar a atualização dos dados de uma aferição específica.
- **Campos Disponíveis:**
    - **Número de Série:** Identificação única do equipamento.
    - **Número do Inmetro:** Número de registro do equipamento no Inmetro.
    - **Número do Laudo:** Identificação do laudo técnico relacionado à aferição.
    - **Número do Lacre:** Número do lacre de segurança do equipamento.
    - **Data de Aferição:** Data em que a aferição foi realizada.
    - **Data de Emissão:** Data de emissão do laudo da aferição.
    - **Data de Vencimento:** Data de validade da aferição.
    - **Tipo de Aferição:** Tipo de aferição realizada, por exemplo, "Aferição Eventual".
    - **Equipamento:** Seleção do equipamento relacionado à aferição.

#### Seção de Faixas Associadas
- **Objetivo:** Gerenciar as faixas associadas à aferição em questão.
- **Componentes Principais:**
    - **Operação:** Ações relacionadas à gestão de faixas, como adicionar ou remover uma faixa.
    - **Faixa:** Seleção da faixa específica associada à aferição.
    - **Adicionar:** Permite adicionar uma nova faixa à lista de faixas associadas.
    - **Excluir:** Remove uma faixa específica da lista de faixas associadas.
    - **Upload de Arquivos:** O usuário pode arrastar e soltar arquivos relacionados à aferição para associá-los ao registro.

#### Fluxo de Uso
1. **Visualização:** O usuário acessa a tela de listagem de aferições, onde pode ver todas as aferições registradas, com a possibilidade de filtragem e ordenação conforme necessário.
2. **Edição:** Clicando no ícone de edição, o usuário pode acessar a tela de edição de aferições, onde é possível atualizar as informações do equipamento, laudo, lacre, e as datas relevantes.
3. **Gestão de Faixas:** Dentro da tela de edição, o usuário pode associar ou remover faixas específicas à aferição, garantindo que todas as faixas relevantes estejam corretamente vinculadas ao equipamento aferido.
4. **Salvamento:** Após realizar as alterações desejadas, o usuário deve clicar no botão "Salvar" para confirmar e registrar as mudanças no sistema.

