# Mockable.io para teste da Balança

## Simulação de Teste com Mockable.io
é uma plataforma online que permite criar rapidamente 
APIs simuladas (ou "mocks") para testar integrações de 
software ou desenvolver protótipos. Com o Mockable.io, você 
pode criar endpoints personalizados com respostas fictícias para 
simular o comportamento de uma API real.



## Como Criar uma API de Teste no Mockable.io usando JSON

Para simular uma API de teste no Mockable.io usando JSON, siga estas etapas:

<list type="decimal" start="1">
<li>  Acesso ao Mockable.io </li>
</list>
 <p>Acesse o site oficial do <a href="https://www.mockable.io/" > Mockable.io </a>
e faça login na sua conta. Se você ainda não tem uma conta, pode se registrar gratuitamente.</p>


<list type="decimal" start="2">
<li>  Criação de um Novo Mock
 </li>
</list>
 <p>No painel principal do Mockable.io, clique no botão "New Mock" ou "New REST Mock" para começar a criar um novo mock.</p>



<list type="decimal" start="3">
<li> Definição de Endpoints
</li>
</list>
Adicione um novo endpoint clicando no botão "Add Endpoint". Defina o método HTTP (por exemplo, GET, POST, PUT, DELETE) e o caminho do endpoint (por exemplo, /api/teste).

<list type="decimal" start="4">
<li> Adição de Respostas Simuladas
</li>
</list>
Para cada endpoint, adicione respostas simuladas clicando nele e configurando as respostas desejadas. Cada resposta pode ter seu próprio status HTTP, cabeçalhos e corpo de resposta em formato JSON.


<list type="decimal" start="5">
<li> Adição de Corpo de Resposta JSON
</li>
</list>
Para adicionar um corpo de resposta em formato JSON, clique no botão "Add Body" ou "Add Response" e selecione "JSON" como tipo de corpo. Insira o JSON desejado no editor fornecido.



<sample >
{
{
    "100-002-337": {
        "hnuid": "100-002-337",
        "className": "PC Interface",
        "modelName": "USB-Cable-Radio",
        "serial": 337,
        "versions": {
            "firmware": "1.2.0",
            "hardware": "1.0.0",
            "hnp": "1.4.4"
        }
    },
    "200-003-1881": {
        "hnuid": "200-003-1881",
        "className": "WL 108",
        "modelName": "10 t",
        "serial": 1881,
        "ready": true,
        "indication": "7000 kg",
        "load":4525,
        "zeroIndication": false,
        "motionIndication": false,
        "overloadIndication": false,
        "underloadIndication": false,
        "minloadIndication": false,
        "units": {
            "load": "kg",
            "temperature": "°C"
        },
        "division": 50,
        "capacity": 10000,
        "adjustmentCounter": 1,
        "firmwareChecksum": "1871h",
        "versions": {
            "legalyRelevantFirmware": "1.0.0",
            "legalyNotRelevantFirmware": "1.5.1",
            "hardware": "1.1.0",
            "hnp": "1.2.9"
        }
    },
    "200-003-1882": {
        "hnuid": "200-003-1882",
        "className": "WL 108",
        "modelName": "10 t",
        "serial": 1882,
        "ready": true,
        "indication": "2250 kg",
        "load":4525,
        "zeroIndication": false,
        "motionIndication": false,
        "overloadIndication": false,
        "underloadIndication": false,
        "minloadIndication": false,
        "units": {
            "load": "kg",
            "temperature": "°C"
        },
        "division": 50,
        "capacity": 19000,
        "adjustmentCounter": 1,
        "firmwareChecksum": "1871h",
        "versions": {
            "legalyRelevantFirmware": "1.0.0",
            "legalyNotRelevantFirmware": "1.5.1",
            "hardware": "1.1.0",
            "hnp": "1.2.9"
        }
} 
}

</sample>

<list type="decimal" start="6">
<li> Salvamento do Mock
</li>
</list>
Após configurar todos os endpoints e respostas, clique no botão "Save" ou "Save Changes" para salvar o seu mock.

<list type="decimal" start="7">
<li> Acesso ao URL do Mock
</li>
</list>
Acesse o URL fornecido para o seu mock e comece a fazer solicitações para testar a integração com a sua API simulada.
