# Configuração Axton

## MongoDB
O MongoDB é um banco de dados NoSQL (Not Only SQL), de código aberto e orientado a documentos. 
Ele difere dos bancos de dados relacionais tradicionais, como o MySQL ou o PostgresSQL, em sua abordagem de armazenamento 
e recuperação de dados.

### Intalações﻿

<deflist collapsible="true">
    <def title="Instalação do MongoDB" collapsible="true" default-state="expanded">
Acesse o link <a href="https://www.mongodb.com/try/download/community">MongoDB Community Server</a> e siga as instruções para baixar e instalar o MongoDB em seu sistema operacional. </def>
</deflist>
<deflist collapsible="true">
    <def title="Instalação do MongoDB Compass" collapsible="true" default-state="expanded">
Baixe e instale o <a href="https://www.mongodb.com/try/download/community"></a> MongoDBCompass. </def>
</deflist>

<deflist collapsible="true">
    <def title="Instalação do Aplicativo AxTon Setup" collapsible="true" default-state="expanded">
O aplicativo AxTon Setup será fornecido pelo suporte. Certifique-se de ter o arquivo de instalação disponível. </def>
</deflist>

## Configurações no MongoDB
#### Conexão com MongoDB

<list type="decimal" start="1">
<li>Abra o MongoDB Compass.
<list type="alpha-lower" >
<li>Na aba "New Connection", clique em "Connect".
</li>
</list>
</li>
</list>

<warning>
Observação: Certifique-se de ter instalado o MongoDB e o MongoDB Compass corretamente para evitar erros de conexão, como "connect ECONNREFUSED 127.0.0.1:27017 mongo".
</warning>


## Criar um Novo Banco de Dados
<list type="decimal" start="1">
<li>Na aba "New Connection", clique em "Connect".</li>
</list>

<sample  title="Mongo">
Database Name: AxTon
Collection Name: User

</sample>

<list type="decimal" start="2">
<li>Clique em "Create Database".</li>
</list>

## Configurações do AxTon

<list type="decimal" start="1">
<li> Entre no AxTon usando as credenciais de login padrão:
<list type="alpha-lower" >
</list>
</li>
</list>
<sample>
Usuário: User
Senha: Pass
</sample>
<warning>
Observação: Certifique-se de ter instalado o MongoDB, MongoDB Compass e criado o banco de dados corretamente.</warning>

<list type="decimal" start="2">
<li> Configuração do Sistema: 
<list type="alpha-lower" >
<li>Insira o código dos equipamentos. 
</li>
<li>Insira as classificações no arquivo AxTon.classifications.JSON 
<tip>
    Observação: somente com suporte (AxTon.classifications.JSON) vai ser disponibilizado
</tip>
</li>

<li>Insira os dados do órgão HAENNI - URL do Servidor.
<tip>
Observação: Certifique-se de ter importado o JSON corretamente para evitar erros na hora da pesagem</tip>

</li>
</list>
</li>
</list>


##### 3. Tipo de Exportação
#### ATraffic:
1. **Formato de Exportação:** Excel (.xlsx)
2. **Método de Exportação:** Os dados serão exportados localmente no formato de planilha Excel.
3. **Detalhes Adicionais:** Esta opção é ideal quando há necessidade de manipulação ou análise dos dados localmente, oferecendo a flexibilidade de edição, visualização e compartilhamento conforme necessário.
#### Axhub:
1. **Formato de Exportação:** Direto para o Axhub (plataforma de integração)
2. **Método de Exportação:** Os dados são exportados diretamente para o sistema Axhub.
3. **Restrição Importante:** Quando selecionado o tipo de exportação "Axhub", os dados exportados não poderão ser deletados do sistema. Esta opção é utilizada para integrações automáticas e seguras, garantindo que os dados enviados ao Axhub permaneçam inalterados e disponíveis para uso contínuo na plataforma.

