
# Criptografia de Arquivos com Certificado Digital


## **Objetivo**

Este documento descreve o processo de **criptografia de arquivos** utilizando um modelo de **criptografia híbrida** (AES + RSA), adotado pelas empresas integradoras para garantir a **confidencialidade** dos arquivos enviados à Axion Tecnologia.

---

## **Metodologia Utilizada**

- A criptografia simétrica com **AES (Advanced Encryption Standard)** é utilizada pela sua eficiência no tratamento de **grandes volumes de dados**.
- A segurança da **criptografia assimétrica RSA (2048 bits)** é utilizada para proteger a chave simétrica usada no processo.
- O processo híbrido assegura que **somente a Axion**, detentora da **chave privada** correspondente ao certificado digital, poderá acessar os dados criptografados.

---

## **Passo a Passo: Criptografia de Arquivo**

### **1. Preparação do Certificado Digital**

- A Axion fornecerá um **certificado digital contendo a chave pública** que deverá ser utilizada pelas empresas integradoras para criptografar os arquivos.

---

### **2. Geração da Chave AES e IV**

- O algoritmo **AES-256** será utilizado para criptografar os dados.
- Será gerada uma **chave simétrica de 256 bits** e um **vetor de inicialização (IV)** de 16 bytes.

---

### **3. Criptografia da Chave AES com RSA**

- A chave AES e o IV são criptografados utilizando a **chave pública do certificado digital da Axion**, com **RSA de 2048 bits**.
- Isso garante que somente a Axion poderá **descriptografar essas informações**, utilizando sua **chave privada** correspondente.

---

### **4. Criptografia dos Dados**

- O conteúdo do arquivo (ex: imagem) é **dividido em blocos** e criptografado utilizando o **AES** com a chave e IV gerados.
- A saída é um novo arquivo contendo:
    - **256 bytes da chave AES criptografada**
    - **16 bytes do IV**
    - **Dados do arquivo criptografados com AES**
- O cabeçalho do arquivo resultante ocupará **exatamente 272 bytes**.

---

## **Segurança Garantida**

Este método assegura:

- **Confidencialidade** dos dados em trânsito.
- Proteção contra interceptações.
- **Segurança na troca de informações** sensíveis entre as partes.

---

## **Material de Apoio**

📎 **Encrypt – Csharp.zip**  

---

