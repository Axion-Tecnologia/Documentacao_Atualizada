# Diagrama dos Contratos


<code-block lang="plantuml">
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
center header
Diagrama dos Contratos
end header

left to right direction
rectangle  {
rectangle  {
usecase "Crono" as Crono 
}
rectangle  {
usecase "Triagem" as Triagem
}
rectangle  {
usecase "OCR" as OCR
}


' Define os contratos de Crono
rectangle  {
usecase "ITPS" as ITPS
usecase "IMEPI" as IMEPI
usecase "IMEQPB" as IMEQPB
usecase "INMEQMA" as INMEQMA
usecase "IMETROPA" as IMETROPA
usecase "IBAMETRO" as IBAMETRO
}

' Define os contratos de Triagem
rectangle  {
usecase "DERSE" as DERSE
usecase "SMTT" as SMTT
usecase "SMTRR" as SMTRR
usecase "STRANS" as STRANS
usecase "BHTRANS" as BHTRANS
usecase "SETRANS" as SETRANS
usecase "DETRANMA" as DETRANMA
}
' Define os contratos de OCR
rectangle  {
usecase "ECONOMIA" as ECONOMIA

}

rectangle  {
usecase "AxCross" as AxCross

}

' Define os relacionamentos
Crono --> ITPS
Crono --> IMEPI
Crono --> IMEQPB
Crono --> INMEQMA
Crono --> IMETROPA
Crono --> IBAMETRO

Triagem --> DERSE
Triagem --> SMTT
Triagem --> SMTRR
Triagem --> STRANS
Triagem --> BHTRANS
Triagem --> SETRANS
Triagem --> DETRANMA

OCR --> ECONOMIA

ECONOMIA --> AxCross
DERSE --> AxCross
SETRANS --> AxCross
SMTT --> AxCross
@enduml


</code-block>