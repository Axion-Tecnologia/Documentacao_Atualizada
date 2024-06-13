# Webhooks

## Introdução
A seção de webhooks no sistema AXHUB permite aos usuários configurar URLs que receberão notificações sobre eventos específicos, facilitando a integração com outros serviços ou sistemas. Esta documentação fornece uma visão detalhada da interface e orientações passo a passo para configurar e gerenciar webhooks.

### Interface de Configuração de Webhooks
#### Descrição Geral
A interface de configuração de webhooks é projetada para facilitar a criação, edição e gerenciamento de webhooks no sistema. Abaixo, detalhamos cada componente da interface:

1. **Botão "Novo"**
    - **Descrição:** Inicia o processo de criação de um novo webhook.
    - **Ação:** Clicando neste botão, o usuário é levado para a tela de configuração onde pode definir os detalhes do webhook, como nome, URL e evento.

2. **Botão "Excel"**
    - **Descrição:** Permite exportar ou importar a lista de webhooks em formato Excel.
    - **Ação:** Clicando neste botão, o usuário pode escolher entre baixar um arquivo Excel com os dados dos webhooks configurados ou importar um arquivo Excel para adicionar múltiplos webhooks de uma vez.

3. **Campo de Busca**
    - **Descrição:** Permite filtrar os webhooks com base em URL ou evento.
    - **Ação:** O usuário digita o termo de busca e clica na lupa para filtrar a lista de webhooks exibida.

4. **Colunas da Tabela**
    - **Nome:** Exibe o nome dado ao webhook.
    - **Código:** Mostra o código identificador do webhook.
    - **URL:** Exibe a URL configurada para o webhook.
    - **Evento:** Indica o evento que aciona o webhook.
    - **Ativo:** Informa se o webhook está ativo ou inativo.
    - **Ações:** Contém botões para editar ou excluir o webhook.

## Passo a Passo para Configurar um Webhook

### Criar um Novo Webhook

1. Clique no botão "Novo".
2. Preencha os campos obrigatórios:
    - **Nome:** Dê um nome descritivo ao webhook.
    - **URL:** Insira a URL que receberá as notificações.
    - **Evento:** Selecione o evento que acionará o webhook.
    - **Ativo:** Marque se o webhook deve estar ativo imediatamente.
3. Clique em "Salvar" para criar o webhook.

### Editar um Webhook

1. Na lista de webhooks, clique no ícone de edição na coluna "Ações" correspondente ao webhook que deseja editar.
2. Faça as alterações necessárias.
3. Clique em "Salvar" para aplicar as mudanças.

### Excluir um Webhook

1. Na lista de webhooks, clique no ícone de lixeira na coluna "Ações" correspondente ao webhook que deseja excluir.
2. Confirme a exclusão na janela de confirmação que aparece.

## Exportar e Importar Webhooks

### Exportar Webhooks

1. Clique no botão "Excel".
2. Selecione a opção de exportar. O sistema irá baixar um arquivo Excel contendo os dados dos webhooks configurados.

### Importar Webhooks

1. Clique no botão "Excel".
2. Selecione a opção de importação.
3. Escolha o arquivo Excel contendo os webhooks que deseja importar e clique em "Importar".

## Considerações Finais

- **Segurança:** Certifique-se de que a URL configurada para o webhook está protegida e pronta para receber as solicitações.
- **Testes:** Após configurar um webhook, realize testes para garantir que os eventos estão sendo enviados corretamente.

---

Essa documentação deve fornecer uma visão clara e detalhada sobre como usar a interface de configurações de webhooks no sistema AXHUB. Caso haja atualizações na interface ou novas funcionalidades, revise e atualize a documentação conforme necessário.