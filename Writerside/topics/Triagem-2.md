# Triagem
#### **Objetivo:**
O módulo de **Triagem de Infração** permite a análise e o processamento de infrações relacionadas ao uso de Infração em veículos. Esta funcionalidade é crucial para garantir que as infrações sejam identificadas, processadas e classificadas adequadamente.
#### **Componentes Principais:**

1. **Filtro de Pesquisa:**
    - **Data da Passagem:** Permite ao usuário selecionar um intervalo de datas para filtrar as passagens a serem triadas.
    - **Mais Filtros:**
        - **Grupo de Equipamentos:** Filtra as passagens por grupo de equipamentos.
        - **Equipamento:** Seleção de um equipamento específico para análise.
        - **Faixa:** Seleção da faixa de rodagem.
        - **Operação:** Filtro por tipo de operação realizada.
        - **Motivo Descarte:** Permite filtrar por motivos de descarte pré-definidos.
        - **Número da Infração:** Permite a busca direta pelo número da infração.

2. **Listagem de Infrações:**
    - **Data da Infração:** Mostra a data em que a infração foi registrada.
    - **Prazo:** Indica o tempo restante para o processamento da infração.
    - **Triagem/Reavaliação:** Mostra a quantidade de registros na fila de triagem ou reavaliação.
    - **Descartes/Processados:** Exibe o número de infrações descartadas e processadas.

3. **Processamento de Passagem:**
    - **Detalhes da Passagem:** Exibe a imagem capturada do veículo, juntamente com informações como placa, data e hora da passagem, local, e código do equipamento.
    - **Formulário de Processamento:**
        - **Placa:** Confirmação da placa do veículo.
        - **Motivo:** Seleção do motivo da infração ou confirmação de que a passagem está correta.
        - **Classificação do Veículo:** Identificação da categoria e outras características do veículo (marca/modelo, tipo, cor, etc.).
    - **Ações:** O usuário pode optar por processar a passagem ou avaliar posteriormente.

#### **Procedimentos Operacionais:**

1. **Filtragem e Identificação de Infrações:**
    - Utilize os filtros disponíveis para identificar infrações que precisam ser processadas. Defina os parâmetros, como datas e equipamentos, para refinar a busca.
    - A lista de infrações será atualizada de acordo com os critérios definidos.

2. **Processamento de Infrações:**
    - Selecione uma infração da lista para abrir a tela de processamento.
    - Verifique a imagem e os dados do veículo. Se necessário, corrija as informações no formulário de processamento.
    - Se a infração for válida, escolha o motivo apropriado e classifique o veículo. Caso contrário, utilize o motivo de descarte adequado.
    - Pressione "Processar" para confirmar a triagem ou "Avaliar Depois" se precisar de mais tempo para analisar.

3. **Finalização e Relatórios:**
    - Após o processamento, a infração é marcada como processada ou descartada, e movida para o histórico, conforme aplicável.
    - Relatórios podem ser gerados a partir dos dados de triagem, para análise posterior.

