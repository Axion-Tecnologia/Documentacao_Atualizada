# Auditoria


#### **Objetivo:**
O módulo de **Auditoria de Infrações** é utilizado para revisar, corrigir e validar as infrações registradas. Essa funcionalidade é essencial para garantir que as infrações processadas sejam corretas e que erros ou inconsistências sejam devidamente ajustados.

#### **Componentes Principais:**

1. **Filtro de Pesquisa:**
    - **Data da Infração:** Permite ao usuário definir um intervalo de datas para filtrar as infrações.
    - **Mais Filtros:**
        - **Grupo de Equipamentos:** Filtra as infrações por grupos específicos de equipamentos.
        - **Equipamento:** Seleção de um equipamento específico para análise.
        - **Faixa:** Permite filtrar infrações por faixa de rodagem.
        - **Operação:** Filtro por tipo de operação realizada.
        - **Motivo Descarte:** Filtra as infrações baseando-se nos motivos de descarte pré-definidos.
        - **Número da Infração:** Busca direta pelo número da infração.
        - **Tipo de Infração:** Filtro que permite selecionar o tipo de infração.

2. **Listagem de Infrações:**
    - **Data da Infração:** Exibe a data em que a infração foi registrada.
    - **Prazo:** Mostra o tempo restante para a validação da infração.
    - **Validadas:** Indica o número de infrações já validadas.
    - **Não Validadas:** Mostra a quantidade de infrações que ainda não foram validadas.
    - **Processadas:** Exibe o número de infrações processadas.
    - **Descartadas:** Indica o número de infrações descartadas.

3. **Processamento de Infrações:**
    - **Visualização da Imagem:** A tela exibe a imagem capturada do veículo, junto com detalhes como local, data, hora, e velocidade.
    - **Formulário de Edição:**
        - **Placa:** Verificação e possível correção da placa do veículo.
        - **Motivo:** Seleção do motivo da infração ou correção do motivo.
        - **Classificação do Veículo:** Inclusão de detalhes do veículo, como marca/modelo, tipo, cor, município, etc.
    - **Ações:** O usuário pode processar a infração, alterar os dados ou consultar o histórico e detalhes adicionais.

#### **Procedimentos Operacionais:**

1. **Filtragem e Identificação de Infrações:**
    - Utilize os filtros disponíveis para identificar infrações que necessitam de auditoria. Ajuste os parâmetros como datas, equipamentos, e tipos de infrações para refinar a busca.
    - A lista de infrações será exibida conforme os critérios definidos.

2. **Revisão e Validação de Infrações:**
    - Selecione uma infração na lista para abrir a tela de auditoria.
    - Verifique a imagem e os dados do veículo. Se necessário, corrija as informações no formulário de edição.
    - Se a infração for válida, selecione o motivo adequado e confirme os detalhes do veículo. Caso contrário, utilize o motivo de descarte apropriado.
    - Pressione "Processar" para confirmar a validação ou "Alterar" se precisar ajustar alguma informação.

3. **Finalização e Relatórios:**
    - Após a auditoria, a infração é marcada como validada, processada ou descartada, conforme aplicável.
    - Relatórios podem ser gerados com base nas auditorias realizadas para análise posterior.

