# UML

# Class Diagram

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

# ER Diagram
```mermaid
erDiagram
    CUSTOMER }|..|{ DELIVERY-ADDRESS : has
    CUSTOMER ||--o{ ORDER : places
    CUSTOMER ||--o{ INVOICE : "liable for"
    DELIVERY-ADDRESS ||--o{ ORDER : receives
    INVOICE ||--|{ ORDER : covers
    ORDER ||--|{ ORDER-ITEM : includes
    PRODUCT-CATEGORY ||--|{ PRODUCT : contains
    PRODUCT ||--o{ ORDER-ITEM : "ordered in"
```

# Mermaid

[mermaid-js](https://mermaid-js.github.io/mermaid/#/classDiagram)

## Define a class

```mermaid
classDiagram
    class Animal
```

```
classDiagram
    class Animal
```

```mermaid
classDiagram
    Vehicle <|-- Car
```

```
classDiagram
    Vehicle <|-- Car
```

## Defining Members of a class

```mermaid
classDiagram
    class BankAccount
    BankAccount : +String owner
    BankAccount : +BigDecimal balance
    BankAccount : +deposit(amount)
    BankAccount : +withdrawal(amount)
```

```
classDiagram
    class BankAccount
    BankAccount : +String owner
    BankAccount : +BigDecimal balance
    BankAccount : +deposit(amount)
    BankAccount : +withdrawal(amount)
```

## Defining Relationship

|Type|Description|
|---|---|
|**<\|--**|Inheritance|
|***--**|Composition|
|**o--**|Aggregation|
|**<--**|Association|
|**--**|Link (Solid)|
|**<..**|Dependency|
|**<\|..**|Realization|
|**..**|Link (Dashed)|


```mermaid
classDiagram
    classA <|-- classB : Inheritance
    classC *-- classD : Composition
    classE o-- classF : Aggregation
    classG <-- classH : Association
    classI -- classJ : Link(Solid)
    classK <.. classL : Dependency
    classM <|.. classN : Realization
    classO .. classP : Link(Dashed)
```

```
classDiagram
    classA <|-- classB : Inheritance
    classC *-- classD : Composition
    classE o-- classF : Aggregation
    classG <-- classH : Association
    classI -- classJ : Link(Solid)
    classK <.. classL : Dependency
    classM <|.. classN : Realization
    classO .. classP : Link(Dashed)
```

# Reference
* https://en.wikipedia.org/wiki/Unified_Modeling_Language
* https://www.nextree.co.kr/p6753/amp
