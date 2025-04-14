
# Assinatura Digital com Certificado Digital


---

## **Objetivo**

Este documento descreve o processo de **assinatura digital** aplicado aos arquivos trocados entre a Axion Tecnologia e as empresas integradoras, com o objetivo de garantir a **integridade** e **autenticidade** das informações transmitidas.

---

## **Fluxo do Processo**

### **1. Criação da Assinatura Digital**

As empresas integradoras deverão:

- Gerar uma assinatura digital para cada arquivo utilizando a **chave privada** de seu **certificado digital**.
- Aplicar a função **hash SHA-256** combinada com **Padding PKCS#1** ao conteúdo do arquivo.
- Assinar o hash resultante com a **chave privada**, obtendo assim a assinatura digital.
- Codificar a assinatura gerada em **Base64**, facilitando o envio e armazenamento.

---

### **2. Distribuição da Chave Pública**

Para que a Axion possa verificar os arquivos recebidos:

- As empresas integradoras deverão fornecer a **chave pública** do certificado digital utilizado para assinar os arquivos.
- A chave pública **pode ser compartilhada livremente**, pois serve apenas para **verificação da assinatura** e não permite falsificações.

---

### **3. Verificação da Assinatura Digital**

Ao receber os arquivos:

- A Axion utilizará a **chave pública** fornecida pela integradora para **verificar a assinatura digital**.
- Se a verificação for bem-sucedida, isso indica que o arquivo **não foi alterado** após sua assinatura.
- Qualquer modificação no conteúdo invalida a assinatura, garantindo assim a **proteção contra alterações indevidas**.

---

## Segurança Garantida

Esse processo assegura que:

- Os arquivos não foram modificados após serem assinados.
- A origem do conteúdo pode ser autenticada com base no certificado digital.
- A troca de dados entre a Axion e as empresas integradoras permanece **segura e confiável**.

---

## **Material de Apoio**

O exemplo de implementação da assinatura digital está disponível no arquivo em anexo:

📎 **Sign – Csharp.zip**

---
