# examples

## subgraph label spacing

from https://github.com/mermaid-js/mermaid/issues/1209

### original

```mermaid
flowchart LR
subgraph Internet
  D[Client]
end
```

### patern 1

```mermaid
flowchart LR
subgraph subg [ ]
  style subg fill:none,stroke:none
  subgraph Internet
    D[Client]
  end
end
```

### patern 2

```mermaid
flowchart LR
classDef subgraph_padding fill:none,stroke:none

subgraph subg [ ]
  subgraph Internet
    D[Client]
  end
end

class subg subgraph_padding
```

## escape

from https://stackoverflow.com/questions/28121525/mermaid-cli-how-do-you-escape-characters

`a---b---other`

```mermaid
flowchart LR
a---b---other
```

`a---b--- other`

```mermaid
flowchart LR
a---b--- other
```

`a---b---dummy["other"]`

```mermaid
flowchart LR
a---b---dummy["other"]
```

## tree style

```mermaid
flowchart TB
    a---b
    a---c
        c---d
        c---e
```

```mermaid
flowchart LR
    a---b
    a---c
        c---d
        c---e
```

```mermaid
flowchart TB
    a---b
    a---c
        c---d
        c---e
            e-->a
```

## classDiagram

from https://mermaid-js.github.io/mermaid/#/classDiagram

```mermaid
 classDiagram
      Animal <|-- Duck
      Animal <|-- Fish
      Animal <|-- Zebra
      Animal : +int age
      Animal : +String gender
      Animal: +isMammal()
      Animal: +mate()
      class Duck{
          +String beakColor
          +swim()
          +quack()
      }
      class Fish{
          -int sizeInFeet
          -canEat()
      }
      class Zebra{
          +bool is_wild
          +run()
      }
```

## sequenceDiagram

from https://mermaid-js.github.io/mermaid/#/sequenceDiagram?id=sequencenumbers

```mermaid
sequenceDiagram
    autonumber
    Alice->>John: Hello John, how are you?
    loop Healthcheck
        John->>John: Fight against hypochondria
    end
    Note right of John: Rational thoughts!
    John-->>Alice: Great!
    John->>Bob: How about you?
    Bob-->>John: Jolly good!
```

## entityRelationshipDiagram

from https://mermaid-js.github.io/mermaid/#/entityRelationshipDiagram?id=attributes

```mermaid
erDiagram
    CAR ||--o{ NAMED-DRIVER : allows
    CAR {
        string registrationNumber
        string make
        string model
    }
    PERSON ||--o{ NAMED-DRIVER : is
    PERSON {
        string firstName
        string lastName
        int age
    }
```

## pie

from https://mermaid-js.github.io/mermaid/#/pie?id=example

```mermaid
pie
    title Key elements in Product X
    "Calcium" : 42.96
    "Potassium" : 50.05
    "Magnesium" : 10.01
    "Iron" :  5
```