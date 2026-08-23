classDiagram
    %% Associazioni principali
    CityMayor --> City : gestisce
    City --> Grid : 1 rappresentata da
    City --> CityState : possiede
    Grid --> Block : composta da
    Block "1" --> "1" Stats : ha

    
  %% Definizione Attributi CityState
    class CityState {
        Strategy
        Tick
        Polution
        Money
        Happines
        Population
        Energy
        Workers
    }

    %% Definizione Attributi Stats
    class Stats {
        Polution
        Money
        Happines
        Population
        Energy
        Operative
    }

    %% Albero di Ereditarietà (Livello 1)
    Block <|-- Infrastructure
    Block <|-- Building
    Block <|-- Empty

    %% Albero di Ereditarietà Infrastrutture (Livello 2)
    Infrastructure <|-- PowerPlant
    Infrastructure <|-- Road
    Infrastructure <|-- Park

    %% Albero di Ereditarietà Edifici (Livello 2)
    Building <|-- Residential
    Building <|-- Factory
    Building <|-- Commertial
