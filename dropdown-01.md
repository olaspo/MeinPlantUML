@startuml
skinparam classAttributeIconSize 0

class Sektor {
    +name: String
    +unterkategorien: List
}

class Kontinent {
    +name: String
}

class Land {
    +name: String
}

class Bundesland {
    +name: String
}

class Landkreis {
    +name: String
}

class Gemeinde {
    +name: String
    +schluessel: String
    +adresse: String
    +email: String
    +status: String
    +lat: Float
    +lng: Float
}

Sektor "1" -- "0.." Kontinent : enthält >
Kontinent "1" -- "1.." Land : enthält >
Land "1" -- "0.." Bundesland : enthält >
Bundesland "1" -- "1.." Landkreis : enthält >
Landkreis "1" -- "1.." Gemeinde : enthält >

@enduml
