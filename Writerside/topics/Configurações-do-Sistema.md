# Configurações do Sistema
---

#### **Visão Geral**
As Configurações do Sistema são a parte mais importante do Axhub, pois permitem a administração centralizada de parâmetros críticos que afetam o funcionamento de toda a plataforma. Este módulo abrange desde a configuração de integração com serviços externos até o ajuste de parâmetros específicos para a operação do sistema.

---

#### **Acesso às Configurações do Sistema**

1. **Caminho**:
    - Para acessar as configurações do sistema, vá para **Administração > Configurações do Sistema** no menu principal.

2. **Permissões**:
    - Somente administradores ou usuários com permissões elevadas devem ter acesso a esta seção, dado o impacto potencial das alterações feitas aqui.

---

#### **Seções das Configurações do Sistema**

##### 1. **Configurações Gerais**

- **Prazo para Triagem**: Define o número de dias para realizar a triagem de infrações. O valor padrão é `20` dias.
- **Tipo de Integração para Exportação**: Escolha o tipo de integração para exportação, como `ExportacaoInfraçaoInmetro`.
- **Limite de Infrações por Lote de Exportação**: Defina o número máximo de infrações que podem ser exportadas por lote. O valor padrão é `100`.
- **Tipo de Imagem do Lado Esquerdo/Direito**: Especifique os tipos de imagem que aparecerão nas listas de triagem/auditoria.
- **Exibir Quantidade em Auditoria no Painel Sinótico**: Opção para exibir a quantidade de auditorias no painel.
- **Exigir Agente para Auditoria**: Habilite se for necessário que um agente aprove auditorias de imagens válidas.
- **Tempo de Análise da Imagem**: Define o tempo em minutos para a análise de imagens.
- **Timeout Heartbeat**: Tempo em minutos que define quando o equipamento está offline.
- **Tempo de Infração Duplicada**: Define o tempo, em segundos, para que infrações com o mesmo veículo e equipamento sejam consideradas duplicadas.
- **Limite de Horas para Importação de Infrações**: Define o tempo limite em horas para a importação de novas infrações.
- **Exibir Alertas para Velocidades Superiores a**: Defina o limite de velocidade (em Km/h) para exibir alertas.
- **Motivo de Descarte Padrão**: Escolha o motivo padrão para o descarte de infrações.
- **Conta de Envio de SMS**: Defina a conta de SMS para envio de notificações.

##### 2. **Configurações do Órgão Autuador**

- **Código da Entidade**: Código da empresa ou entidade que presta o serviço de monitoramento.
- **Nome da Entidade**: Nome da entidade responsável pelo monitoramento.
- **Nome do Órgão Autuador**: Especifica o nome do órgão responsável pela autuação.
- **Endereço do Órgão Autuador**: Endereço completo do órgão.
- **Telefone do Órgão Autuador**: Número de telefone de contato.
- **CNPJ do Órgão Autuador**: Cadastro Nacional de Pessoa Jurídica do órgão.
- **Logo do Órgão Autuador**: Permite o upload ou alteração do logotipo do órgão autuador.

##### 3. **Configurações de Integração com Power BI**

- **Authentication Type**: Define o tipo de autenticação para integração com o Power BI, como `ServicePrincipal`.
- **URL Power BI Service Api Root**: Especifique a URL raiz para a API do Power BI.
- **Authority Url**: URL da autoridade de autenticação, geralmente `https://login.microsoftonline.com/organizations`.
- **Application Id**: ID da aplicação registrada no Azure AD para integração com Power BI.
- **Application Secret**: Chave secreta para a aplicação registrada.
- **Scope**: Defina o escopo de permissões para a integração, como `https://analysis.windows.net/powerbi/api/.default`.

---

#### **Salvamento e Validação**

1. **Salvar Configurações**:
    - Após ajustar os parâmetros necessários, clique em **Salvar** no topo da tela para aplicar as mudanças.
    - Certifique-se de revisar todas as seções antes de salvar para evitar inconsistências.

2. **Validação**:
    - O sistema pode exigir validações adicionais para certos campos (como senhas e tokens), e informará o usuário em caso de falha.

---

#### **Solução de Problemas Comuns**

1. **Problema**: Configurações não são salvas corretamente.
    - **Solução**: Verifique se todos os campos obrigatórios estão preenchidos e se os valores são válidos. Certifique-se de que não há problemas de conexão com o banco de dados ou serviços externos.

2. **Problema**: Integração com Power BI falha.
    - **Solução**: Confirme que os detalhes de autenticação (Application Id, Secret, Authority Url) estão corretos e que a aplicação está devidamente configurada no Azure AD.

---

#### **Considerações Finais**

- As Configurações do Sistema são cruciais para o funcionamento do Axhub. Alterações devem ser feitas com cautela e apenas por pessoal autorizado.
- Revisões regulares dessas configurações são recomendadas para garantir que o sistema continue operando de maneira eficiente e conforme as exigências regulatórias.

---

Se precisar de mais detalhes ou ajuda com outra parte do sistema, estou aqui para ajudar!