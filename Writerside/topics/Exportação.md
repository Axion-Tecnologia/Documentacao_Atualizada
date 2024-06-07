# Exportação de Dados
A função de exportação no software de pesagem de caminhões permite que os dados coletados durante o processo de pesagem sejam transferidos para outros sistemas ou armazenados em formato legível para futuras referências. Esta seção detalha os principais elementos exportados e os procedimentos para realizar uma exportação bem-sucedida.

## Dados Exportados
Os seguintes dados são incluídos no arquivo de exportação:


| A                             | B          | D           | E                            |
|-------------------------------|------------|-------------|------------------------------|
| Endereço, Número, Complemento | NumeroAIIP | Data e Hora | Placa                        |


<deflist collapsible="true">
    <def title="Endereço Completo_A" collapsible="true" default-state="expanded">
O campo "Endereço Completo" representa a totalidade das informações relacionadas à localização do usuário, incluindo o endereço, número e complemento. Esses detalhes são extraídos do cadastro do usuário associado à pesagem do caminhão.</def>
</deflist>
<deflist collapsible="true">
<def title="Numero AIP_B" collapsible="true" default-state="expanded">
O campo "NumeroAIIP" é um número único associado à Autorização de Instalação de Instrumento de Pesagem (AIP), que é um documento oficial que autoriza a instalação e uso da balança para fins de pesagem de veículos.</def>
</deflist>
<deflist collapsible="true">
    <def title="Data e Hora_D" collapsible="true" default-state="expanded">
O campo "Data e Hora" registra a data e o horário exato em que a pesagem do caminhão foi realizada. Isso ajuda a rastrear e registrar o momento preciso em que os dados foram coletados.</def></deflist>

<deflist collapsible="true">
    <def title="Placa_E" collapsible="true" default-state="expanded">
O campo "Placa" se refere à placa de identificação do caminhão que está sendo pesado. Essa informação é essencial para identificar o veículo específico e associar os dados de pesagem corretamente. </def>
</deflist>

#### Soma do PBT

| AL   | AM   | AN   | AO | AP     |
|------|------|------|----|--------|
| 1300 | 2300 | 1600 | 2C | -68313 |

<deflist collapsible="true">
    <def title="Excesso PBT_AL" collapsible="true" default-state="expanded">
O campo "Excesso PBT" indica a quantidade de peso excedente em relação ao Peso Bruto Total (PBT) permitido legalmente para o veículo. Esse valor é calculado subtraindo o PBT legal do PBT medido durante a pesagem.
<br>
<code-block lang="tex" >
    \begin{equation}
\text { PBT Excesso }  =\text { PBT Constatado	}- \text {PBT Considerado}  
\end{equation}
</code-block>
</def>
</deflist>

<deflist collapsible="true">
    <def title="Excesso Dos Eixo Medido_AM" collapsible="true" default-state="expanded">
O campo "Excesso dos eixos Medido" refere-se ao peso excedente em relação ao peso permitido para um eixo específico do veículo, conforme medido durante a pesagem. Esse valor é calculado subtraindo o peso legal do eixo do peso real medido.
<code-block lang="tex" >
    \begin{equation}
\text { Excesso de Todos os Eixo }  =\text { Excesso Eixo1 }  
 + \text { Excesso Eixo2 }  
\end{equation}
</code-block>
</def>
</deflist>
<deflist collapsible="true">
    <def title="PBT Regulamentado_AN" collapsible="true" default-state="expanded">
O campo "PBT Legal" representa o Peso Bruto Total (PBT) máximo permitido por lei para o veículo, determinado conforme as regulamentações de trânsito e de segurança rodoviária. 
<br>
<code-block lang="tex" >
    \begin{equation}
\text { PBT Regulamentado }  =\text { Eixo Regulamentado }  
 + \text { Eixo Regulamentado  }  
\end{equation}
</code-block>
</def>

<def title="Classificação_AO" collapsible="true" default-state="expanded">
O campo "Classificação" categoriza o resultado da pesagem com base em critérios específicos, como a conformidade com os limites de peso legalmente estabelecidos ou a necessidade de ações corretivas.</def>
</deflist>
<deflist collapsible="true">
    <def title="Infração_Ap" collapsible="true" default-state="expanded">
O campo "Infração" indica se houve violação das regulamentações de peso durante a pesagem do veículo. Isso pode incluir informações sobre multas, penalidades ou outras consequências associadas à infração.</def></deflist>


#### Soma dos Eixos

| AQ | AR    | AS    | AT   | AU   | Av | AW   | AY    | Ax    | AZ |
|----|-------|-------|------|------|----|------|-------|-------|----|
| E1 | 9050  | 6000  | 6750 | 2300 | E2 | 9050 | 10000 | 11250 | 0  |

<deflist collapsible="true">
    <def title="Grupo de Eixo_AQ_AV" collapsible="true" default-state="expanded">
O campo "Grupo de Eixo" identifica a qual grupo específico de eixos do veículo pertence à medição realizada. Isso ajuda na organização e na análise dos dados de pesagem por grupos de eixos, facilitando a compreensão dos resultados. </def>
</deflist>

<deflist collapsible="true">
    <def title="Eixo Constatado_AR_AW" collapsible="true" default-state="expanded">
O campo "Eixo Constatado" representa o peso real ou observado de um eixo específico do veículo, medido durante o processo de pesagem. </def>
</deflist>

<deflist collapsible="true">
    <def title="Eixo Regulamentado_AS_AY" collapsible="true" default-state="expanded">
O campo "Eixo Regulamentado" indica o limite de peso permitido por lei para um determinado grupo de eixos do veículo, conforme estabelecido pelas regulamentações de trânsito e de segurança rodoviária. </def>
</deflist>

<deflist collapsible="true">
    <def title="Eixo Considerado_AT_AX" collapsible="true" default-state="expanded">
O campo "Eixo Considerado" é o peso máximo permitido legalmente para um grupo de eixos específico do veículo, considerando qualquer carga adicional que possa ser tolerada dentro dos limites regulamentares. </def>
</deflist>

<deflist collapsible="true">
    <def title="Excesso de Eixo_AU_AZ" collapsible="true" default-state="expanded">
O campo "Excesso de Eixo" representa a quantidade de peso excedente em relação ao limite regulamentado para um grupo de eixos específico do veículo. Esse valor é calculado subtraindo o peso regulamentado do peso real ou observado do eixo. 
<br>
<code-block lang="tex" >
    \begin{equation}
\text { Excesso de Eixo }  =\text { Eixo Constatado }  
 - \text { Eixo Considerado }  
\end{equation}
</code-block>
</def>
</deflist>

## Regulamentação de Pesos para Fiscalização de Veículos

Conforme a regulamentação estabelecida pelo Conselho Nacional de Trânsito (Contran), os veículos ou combinações de veículos com peso bruto total regulamentar igual ou inferior a 50 toneladas devem ser fiscalizados apenas quanto aos limites de peso bruto total ou peso bruto total combinado, exceto em casos específicos estabelecidos pelo Contran.

### Limites de Peso Regulamentados

<list>
<li>
Peso Regulamentado Máximo para Considerar Infrações de PBT/Eixo: 50.000 kg (cinquenta mil quilogramas)
</li>
<li>
Peso Regulamentado Mínimo para Considerar Infrações de PBT, Eixo e PBT/Eixo: 50.050 kg (cinquenta mil e cinquenta quilogramas)
</li>
</list>



### Códigos de Enquadramento para Infrações
Os códigos de enquadramento para infrações relacionadas ao peso dos veículos são os seguintes:

<list>
<li>
Código de Enquadramento para PBT: -68311
</li>
<li>
Código de Enquadramento para Eixo: -68312
</li>
<li>
Código de Enquadramento para Eixo/PBT: -68313
</li>
</list>
