# Operações

#### **Objetivo:**
O módulo de **Operações** permite a gestão e o monitoramento de operações associadas a equipamentos, incluindo a configuração de parâmetros, acompanhamento de status, e geração de relatórios. Esta ferramenta é essencial para garantir a conformidade dos equipamentos e para facilitar o acompanhamento das operações realizadas.

#### **Componentes Principais:**

1. **Visão Geral das Operações:**
   - **Tabela de Operações:** Exibe uma listagem detalhada de todas as operações cadastradas. Os principais campos incluem:
      - **Equipamento:** Identificação do equipamento envolvido na operação.
      - **Instalação:** Data de instalação do equipamento.
      - **Início da Operação:** Data de início da operação.
      - **Fim da Operação:** Data de término da operação.
      - **Dt. Aceite:** Data de aceite da operação.
      - **Dt. Homologação:** Data de homologação da operação.
      - **Homologado:** Indica se a operação foi homologada.
      - **Monitorado:** Indica se a operação está sendo monitorada.
   - **Ações:**
      - **Editar:** Permite a edição dos detalhes da operação.
      - **Excluir:** Remove a operação do sistema.
      - **Visualizar:** Permite visualizar os detalhes da operação.

2. **Monitoramento de Operações:**
   - **Filtros de Pesquisa:**
      - **Início da Operação e Fim da Operação:** Permitem definir o intervalo de tempo para o qual as operações serão exibidas.
      - **Operador:** Filtra as operações por operador responsável.
      - **Operação:** Seleção da operação específica.
   - **Lista de Operações Ativas:** Exibe operações em andamento com detalhes como hora de início, operador, e status atual.

3. **Detalhamento da Operação:**
   - **Dashboard:** Exibe um resumo geral da operação, com gráficos e indicadores-chave, como:
      - **Infração x Triagem:** Relaciona infrações captadas pelo equipamento durante a operação e o status de triagem das mesmas.
      - **Aproveitamento OCR:** Indica a eficiência do OCR nas últimas 48 horas, mostrando a porcentagem de leituras bem-sucedidas.
   - **Dados da Operação:**
      - **Data da Instalação e Data de Homologação:** Registra as datas essenciais relacionadas à instalação e homologação do equipamento.
      - **Equipamento:** Identificação do equipamento em operação.
      - **Tarja Padrão:** Seleção da tarja padrão associada à operação.
      - **Tipos de Fiscalizações:** Seleção das fiscalizações aplicáveis, como Monitoramento Online, Cronotacógrafo, ou Fuga de Balança.
      - **Tipos de Infrações:** Seleção das infrações que devem ser monitoradas durante a operação.
      - **Gerar Infração de Passagem:** Permite a configuração para gerar infrações automaticamente com base em passagens captadas.
   - **Documentos da Operação:**
      - **Upload e Gestão de Documentos:** Interface para upload de documentos relacionados à operação e consulta dos documentos já armazenados.

#### **Procedimentos Operacionais:**

1. **Configuração de Operações:**
   - Navegue até a página de **Operações** e clique em **Novo** para criar uma nova operação.
   - Preencha os campos obrigatórios como **Data de Instalação**, **Data Inicial** e **Equipamento**.
   - Configure os parâmetros de fiscalização e infrações de acordo com as necessidades da operação.
   - Após revisar as informações, clique em **Salvar** para iniciar a operação.

2. **Monitoramento e Acompanhamento:**
   - Use os filtros na página de **Monitoramento** para rastrear operações em andamento.
   - Verifique o **status** das operações, identificando rapidamente se há necessidade de intervenção ou ajuste.
   - Acesse o **Dashboard** para uma visão geral das atividades, incluindo a eficiência do OCR e o status das infrações captadas.

3. **Gestão de Documentos e Finalização:**
   - Acesse a aba **Documentos** para anexar e gerenciar todos os documentos relacionados à operação.
   - Utilize a funcionalidade de **Exportar** para gerar relatórios detalhados ao término da operação, garantindo que todas as atividades estejam documentadas e acessíveis para auditoria.

Essa documentação visa assegurar que todos os usuários do módulo de Operações tenham um guia claro e detalhado de como configurar, monitorar e finalizar operações de forma eficiente.