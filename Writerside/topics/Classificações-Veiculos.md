# Classificações Veiculos

![image_32.png](image_32.png)

A funcionalidade "Classificações dos Veículos" no Axhub é responsável por gerenciar as diferentes classificações de veículos, como motocicletas, automóveis, ônibus, caminhões, entre outros. Essa funcionalidade permite que os usuários adicionem, visualizem, editem e excluam classificações de veículos, associando parâmetros específicos como comprimento mínimo e máximo, peso bruto total (PBT), e a unidade veicular padrão (UVP).

#### Tela de Listagem de Classificações
- **Objetivo:** Exibir uma lista de todas as classificações de veículos cadastradas no sistema.
- **Componentes Principais:**
    - **Código:** Código identificador da classificação do veículo.
    - **Descrição:** Descrição da classificação do veículo (ex: Motocicleta, Automóvel).
    - **Comprimento Mínimo:** Comprimento mínimo do veículo, configurado de acordo com o tamanho detectado pela câmera.
    - **Comprimento Máximo:** Comprimento máximo do veículo, também configurado conforme a detecção pela câmera.
    - **PBT:** Peso Bruto Total do veículo.
    - **UVP:** Unidade Veicular Padrão.
    - **Ações:** Permite ao usuário editar ou excluir uma classificação existente.

#### Tela de Edição de Classificações
![image_33.png](image_33.png)

Permitir a edição e atualização dos parâmetros classificativos de uma categoria de veículo específica.

- **Código:** Código único da classificação do veículo.
- **Descrição:** Nome ou tipo da classificação (ex: Automóvel, Caminhão).
- **Comprimento Mínimo do Veículo:** Define o menor comprimento permitido para a classificação, baseado na configuração da câmera.
- **Comprimento Máximo do Veículo:** Define o maior comprimento permitido para a classificação.
- **PBT (Peso Bruto Total):** O peso total permitido para o veículo dessa classificação.
- **Label Rede Neural:** Rótulo utilizado pela rede neural para classificar o veículo dentro dessa categoria.
- **UVP (Unidade Veicular Padrão):** Unidade padrão para o veículo dentro do sistema.


