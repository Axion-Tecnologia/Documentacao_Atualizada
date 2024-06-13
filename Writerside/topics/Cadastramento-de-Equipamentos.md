# Monitoramento de Equipamentos

## Introdução

O AxManager é um sistema desenvolvido para monitorar o status de diversos equipamentos, fornecendo informações detalhadas sobre suas operações e contratos associados. A seguir, detalhamos o processo de cadastramento de operações, contratos, e equipamentos no sistema.

## Cadastramento da Operação

Para cadastrar os contratos, é necessário cadastrar primeiro o Grupo de Equipamentos na seção "Equipamentos".

![GrupodeEquipamento.png](GrupodeEquipamento.png)

### Órgão

Um Órgão refere-se à entidade governamental ou institucional responsável por gerir os contratos.

- **Nome:** DEPARTAMENTO ESTADUAL DE INFRAESTRUTURA RODOVIÁRIA

### Empresa

A Empresa é a entidade contratada pelo Órgão para fornecer ou gerir os equipamentos.

- **Nome:** [Nome da Empresa]
- **CNPJ:** [CNPJ da Empresa]
- **Cidade:** [Cidade]
- **Estado:** [Estado]
- **Endereço:** [Endereço]
- **Telefone:** [Telefone]
- **CEP:** 49085-380

### Contrato

O Contrato é o acordo formal entre a Empresa e o Órgão, definindo os termos de fornecimento e gestão dos equipamentos.

- **Nome:** [Nome do Contrato]
- **Empresa:** [Nome da Empresa]
- **Órgão:** DEPARTAMENTO ESTADUAL DE INFRAESTRUTURA RODOVIÁRIA
- **Data de Início:** [Data de Início]
- **Data de Término:** [Data de Término]
- **Grupos de Equipamentos:** [Grupos de Equipamentos]

### Configuração do Contrato

A Configuração do Contrato refere-se às especificações técnicas e administrativas necessárias para o gerenciamento do contrato no AxManager.

- **Nome da Conta:** [Nome da Conta]
- **Chave da Conta:** [Chave da Conta]
- **URL Storage:** [URL de Armazenamento]
- **Contrato:** [Nome do Contrato]
- **Usar Azure Local:** [Sim/Não]

## Equipamento

Equipamento é o hardware específico que será monitorado pelo AxManager. O cadastramento de um novo equipamento envolve definir seu fabricante, modelo e tipo.

### Fabricantes

Os Fabricantes são as empresas que produzem os equipamentos.

- **Nome:** [Nome do Fabricante]
- **Código do Fabricante:** [Código do Fabricante]
- **Slug:** [Slug]
- **Agrupador Sequencial:** [Agrupador Sequencial]

### Modelo

O Modelo é a especificação particular de um equipamento fornecido por um fabricante.

- **Marca:** [Marca]
- **Modelo:** [Modelo]
- **Portaria:** [Portaria]
- **Número da Portaria:** [Número da Portaria]
- **Fabricante de Equipamento:** [Nome do Fabricante]

### Tipo

O Tipo refere-se à categoria do equipamento.

- **Nome:** [Nome do Tipo]

## Operações

Operações são as atividades específicas realizadas com os equipamentos ao longo do tempo.

- **Novo Operação:** [Nome da Operação]
- **Código:** [Código da Operação]
- **Data de Início:** [Data de Início]
- **Data de Fim:** [Data de Fim]
- **Data de Aceite:** [Data de Aceite]
- **Data de Homologação:** [Data de Homologação]
- **Data de Instalação:** [Data de Instalação]
- **Selecione o Grupo:** [Seleção do Grupo]

---

Se precisar de mais alguma alteração ou inclusão de detalhes, é só avisar!