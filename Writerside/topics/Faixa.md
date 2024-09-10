# Faixa

![image_28.png](image_28.png)

A funcionalidade "Faixa" no Axhub permite aos usuários visualizar, editar e gerenciar faixas relacionadas ao tráfego, com informações específicas como código, número da faixa, sentido, e endereço. Esta seção da aplicação é crucial para o gerenciamento das faixas e sua localização precisa.

#### Tela de Listagem de Faixas
- **Objetivo:** Exibir uma lista de todas as faixas cadastradas.
- **Componentes Principais:**
    - **Código:** Identificação única da faixa.
    - **Faixa:** Número que identifica a faixa dentro de uma determinada via.
    - **Sentido:** Direção do tráfego na faixa (por exemplo, Centro/Bairro).
    - **Endereço:** Localização completa da faixa, incluindo logradouro, bairro, município, e coordenadas (latitude e longitude).
    - **Ações:** Permite ao usuário editar ou excluir uma faixa existente.

#### Criação  de Faixa
![image_29.png](image_29.png)

-  Permitir a edição detalhada das informações de uma faixa específica.
- **Campos Disponíveis:**
    - **Código:** Identificação única da faixa. Este campo é preenchido automaticamente e não é editável.
    - **Número da Faixa:** Identifica o número da faixa dentro da via.
    - **Sentido:** Direção do tráfego na faixa.
    - **Código do Logradouro:** Código associado ao logradouro.
    - **CEP:** Código Postal relacionado ao endereço da faixa.
    - **Endereço Completo:**
        - **Logradouro:** Nome da rua ou avenida onde a faixa está localizada.
        - **Número:** Número específico do logradouro, se aplicável.
        - **Complemento:** Informação adicional sobre o endereço.
        - **Bairro:** Nome do bairro onde a faixa está localizada.
        - **Município:** Cidade onde a faixa se encontra.
        - **Código do Município:** Código identificador do município.
        - **UF:** Unidade Federativa (estado) onde a faixa está localizada.
    - **Coordenadas Geográficas:**
        - **Latitude:** Coordenada geográfica de latitude da faixa.
        - **Longitude:** Coordenada geográfica de longitude da faixa.

#### Fluxo de Uso
1. **Visualização:** O usuário acessa a tela de listagem de faixas, onde pode visualizar todas as faixas cadastradas, filtrando e ordenando conforme necessário.
2. **Edição:** Ao clicar no ícone de edição na coluna "Ações", o usuário é redirecionado para a tela de edição da faixa, onde pode atualizar as informações de localização e características da faixa.
3. **Salvamento:** Após realizar as alterações, o usuário clica no botão "Salvar" para atualizar as informações da faixa no sistema.


