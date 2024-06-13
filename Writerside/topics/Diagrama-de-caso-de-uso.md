# Diagrama de Caso de Uso
<code-block lang="plantuml" >
@startuml
skinparam rectangle {
    BackgroundColor LightSkyBlue
    BorderColor DarkBlue
    RoundCorner 15
}
skinparam actor {
    BackgroundColor LightBlue
    BorderColor DarkBlue
}
skinparam usecase {
    BackgroundColor LightYellow
    BorderColor DarkGoldenRod
    RoundCorner 15
}
@startuml
skinparam rectangle {
    BackgroundColor LightSkyBlue
    BorderColor DarkBlue
    RoundCorner 15
}
skinparam actor {
    BackgroundColor LightBlue
    BorderColor DarkBlue
}
skinparam usecase {
    BackgroundColor LightYellow
    BorderColor DarkGoldenRod
    RoundCorner 15
}
left to right direction

title Diagrama de Caso de Uso

actor Administrador as Admin
actor Usuário as User

rectangle "Sistema AxCross" {
rectangle "Abas" {
usecase "Veículos Monitorados" as Veiculos_Monitorados
usecase "Equipamentos" as Equipamentos
usecase "Monitoramento Online" as Monitoramento_Online
usecase "Relatórios" as Relatorios
}
rectangle "Cadastros Operação" {
usecase "Equipamento" as Cadastro_Equipamento
usecase "Faixa" as Cadastro_Faixa
usecase "Grupo de Equipamentos" as Cadastro_Grupo
}
rectangle "Veículos Monitorados" {
usecase "Dashboard" as Dashboard_VM
usecase "Veículos Monitorados" as Veiculos_Monitorados_VM
}
rectangle "Monitoramento Online" {
usecase "Mapa de Equipamento" as Mapa_Equipamento
}
rectangle "Relatórios" {
usecase "Relatório de Passagens" as Relatorio_Passagens
usecase "Relatório de Mapeamento de Rotas" as Relatorio_Rotas
usecase "Relatório de Rastreamento de Placas" as Relatorio_Placas
usecase "Relatório de Veículos Monitorados" as Relatorio_Veiculos
}

User --> Veiculos_Monitorados
    User --> Equipamentos
    User --> Monitoramento_Online
    User --> Relatorios
    Veiculos_Monitorados --> Dashboard_VM
    Veiculos_Monitorados --> Veiculos_Monitorados_VM
    Monitoramento_Online --> Mapa_Equipamento
    Relatorios --> Relatorio_Passagens
    Relatorios --> Relatorio_Rotas
    Relatorios --> Relatorio_Placas
    Relatorios --> Relatorio_Veiculos
}

rectangle "Configurações" {
rectangle "Alterações" {
usecase "Configurações do Sistema" as Configuracoes_Sistema
}
rectangle "Controle de Acessos" {
usecase "Usuários" as Usuarios
usecase "Perfis de Acesso" as Perfis_Acesso
usecase "Permissões" as Permissoes
usecase "Logs de Acesso" as Logs_Acesso
}
Admin --> Configuracoes_Sistema
Admin --> Usuarios
Admin --> Perfis_Acesso
Admin --> Permissoes
Admin --> Logs_Acesso
}

@enduml



</code-block>