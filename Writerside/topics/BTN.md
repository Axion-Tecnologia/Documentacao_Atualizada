# Diagrama de caso de uso Axton

Este tipo de diagrama é muito útil para entender as principais funcionalidades do sistema, identificar os atores envolvidos e suas interações, e comunicar de forma clara e concisa os requisitos funcionais do sistema para os diferentes stakeholders envolvidos no projeto.


<code-block lang="plantuml">
@startuml
skinparam packageStyle rectangle
skinparam usecase {
    BackgroundColor LightBlue
    BorderColor DarkBlue
}
left to right direction
actor Suporte as U
rectangle "AxTon Application" {
usecase "Instalar MongoDB" as InstallMongo
usecase "Instalar MongoDB Compass" as InstallCompass
usecase "Instalar AxTon Setup" as InstallAxTon
usecase "Conectar ao MongoDB" as ConnectMongo
usecase "Criar Banco de Dados" as CreateDB
U --> InstallMongo
U --> InstallCompass
U --> InstallAxTon
U --> ConnectMongo
U --> CreateDB
}
@enduml


newpage

@startuml
skinparam packageStyle rectangle


left to right direction
actor "Usuário" as User
package "Sistema de Pesagem Axton" {
package "Configurações" {
usecase "Sistema" as ManageSystem
usecase "Usuários" as ManageUsers
usecase "Locais" as ManageLocations
usecase "Classificações" as ManageClassifications
usecase "Sequenciais de Infração" as ManageInfractionSequentials
usecase "Sequenciais de Exportação" as ManageExportSequentials
}
package "Operação" {
usecase "Iniciar Pesagem" as StartWeighing
}
User --> ManageSystem
User --> ManageUsers
User --> ManageLocations
User --> ManageClassifications
User --> ManageInfractionSequentials
User --> ManageExportSequentials
User --> StartWeighing
}
@enduml

</code-block>