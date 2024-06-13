# Configurações do Sistema 

## Introdução

A seção de Configurações do Sistema no AXHUB permite aos administradores ajustar várias preferências e parâmetros para garantir que o sistema opere conforme as necessidades específicas da organização. Esta documentação detalha cada opção disponível nesta seção.

## Configurações Gerais

### Prazo para Triagem
- **Descrição:** Define o prazo em dias para a realização das triagens.
- **Valor Padrão:** 20 dias.

### Tipo de Integração para Exportação
- **Descrição:** Especifica o método de integração utilizado para a exportação de dados.
- **Valor Padrão:** ExportacaoInfracaoInmetro.
- **Opções Disponíveis:** Podem variar conforme configurações do sistema.

### Limite de Infrações por Lote de Exportação
- **Descrição:** Define a quantidade máxima de infrações por lote de exportação. Se deixado vazio, não haverá limite.
- **Valor Padrão:** 100 infrações.

### Base de Dados Consulta de Veículo
- **Descrição:** Nome da base de dados utilizada para a consulta de veículos.
- **Valor Padrão:** apiplacas.

### Base de Dados Consulta Exportação
- **Descrição:** Nome da base de dados utilizada para a consulta na exportação.
- **Valor Padrão:** derse.

### Exibir Quantidade em Auditoria no Painel Sinótico
- **Descrição:** Opção para exibir a quantidade de auditorias no painel sinótico.
- **Opções:** Ativado/Desativado.

## Triagem

### Possui Auditoria?
- **Descrição:** Define se o sistema possui auditoria para a triagem.
- **Opções:**, sim, /Não.

### Requer Código do Agente para Auditoria de Imagens Válidas?
- **Descrição:** Especifica se é necessário o código do agente para a auditoria de imagens válidas.
- **Opções:** Sim ou Não.

### Exigir Modelo/Marca na Triagem
- **Descrição:** Define se é necessário exigir o modelo e a marca na triagem.
- **Opções:** Sim ou Não.
- **Valor Padrão:** Sim.

### Exigir Marca/Modelo com Código Externo
- **Descrição:** Define se é necessário exigir a marca e o modelo com um código externo.
- **Opções:** Sim ou Não.
- **Valor Padrão:** Sim.

### Exibir Imagem de Perfil
- **Descrição:** Define se deve exibir a imagem de perfil durante a triagem.
- **Opções:** Sim ou Não.
- **Valor Padrão:** Sim.

### Tipo de Imagem do Lado Esquerdo
- **Descrição:** Especifica o tipo de imagem que aparecerá no lado esquerdo nas telas de triagem/auditoria.
- **Opções:** Variam conforme configurações do sistema.
- **Valor Padrão:** ZT.

### Tipo de Imagem do Lado Direito
- **Descrição:** Especifica o tipo de imagem que aparecerá no lado direito nas telas de triagem/auditoria.
- **Opções:** Variam conforme configurações do sistema.
- **Valor Padrão:** P1.

## Tempo e Limites

### Tempo de Análise de Imagem
- **Descrição:** Tempo para analisar imagens nas telas de triagem/auditoria.
- **Valor Padrão:** 5 minutos.

### Timeout Heartbeat
- **Descrição:** Tempo sem heartbeat que determina que o equipamento está offline.
- **Valor Padrão:** 5 minutos.

### Tempo de Infração Duplicada
- **Descrição:** Tempo considerado para infrações com o mesmo veículo, equipamento e enquadramento.
- **Valor Padrão:** 1 segundo.

### Percentual de Discrepância
- **Descrição:** Percentual de margem a ser considerado na verificação de discrepância.
- **Valor Padrão:** 30%.

### Limite de Horas para Importação de Infração
- **Descrição:** Quantidade limite de horas para aceitar novas infrações.
- **Valor Padrão:** 720 horas.

### Limite de Horas para Importação de Passagens
- **Descrição:** Quantidade limite de horas para aceitar novas passagens.
- **Valor Padrão:** 720 horas.

### Exibir Alerta para Velocidades Superiores a
- **Descrição:** Define a velocidade a partir da qual alerta serão exibidos.
- **Valor Padrão:** 100 km/h.

### Quantidade de Enquadramentos de Cronotacógrafo
- **Descrição:** Quantidade mínima de enquadramentos configurados para infrações do tipo cronotacógrafo.
- **Valor Padrão:** 2 enquadramentos.

### Motivo de Descarte Padrão
- **Descrição:** Seleciona o motivo de descarte que estará configurado na triagem como padrão.
- **Valor Padrão:** 001 - OK.

### Limite Tempo Interrupção
- **Descrição:** Tempo para geração de interrupção sem o envio de dados.
- **Valor Padrão:** 1 hora.

### Limite Tempo Equipamento Conjugado
- **Descrição:** Limite de tempo (minutos) para equipamentos conjugados.
- **Valor Padrão:** 3 minutos.

## Classificação e Notificações

### Habilita Classificação por IA
- **Descrição:** Ativa ou desativa a classificação por inteligência artificial.
- **Opções:** Ativado/Desativado.
- **Valor Padrão:** Ativado.

### Conta do Envio de SMS
- **Descrição:** Conta ou SID do serviço de SMS.
- **Campo:** Texto.

### Token para Envio do SMS
- **Descrição:** Token do serviço de SMS.
- **Campo:** Texto.

## Fator de Medição

### Opções Disponíveis
- **Infração:** Ativado/Desativado.
- **Passagem:** Ativado/Desativado.
- **Imagem de Teste:** Ativado/Desativado.
- **Índice de OCR:** Ativado/Desativado.

---

Esta documentação cobre detalhadamente as opções de configuração disponíveis na interface de Configurações do Sistema do AXHUB. Se houver atualizações ou novas funcionalidades, revise e atualize esta documentação conforme necessário.