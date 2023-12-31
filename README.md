# Class Diagram Drawing Tools

# What is class diagram?

📘 [**簡單理解 UML 類別圖**](https://misomiso43.medium.com/%E7%B0%A1%E5%96%AE%E7%90%86%E8%A7%A3-uml-%E9%A1%9E%E5%88%A5%E5%9C%96-f0b32a3272c)

# Free Tools

## [MIRO](https://miro.com/)

### Result Image

![MIRO.jpg](MIRO.jpg)

### Features

- Real time collaboration

### Pros

- Free to edit color, font and line style of elements
- Free to edit  text alignment
- Can import images
- Draw instantly online

### Cons

- No function of string replacement

## **[Mermaid](https://mermaid.js.org/)**

### Result Image

![Mermaid.png](Mermaid.png)

### Code

```
---
title: Pets in Pikas' Garden
---
classDiagram
    note "author : Pikas\ntool : Mermaid"
    Animal <|-- Duck
    Animal <|-- Fish
    Animal <|-- Lion
    Animal : +int age
    Animal : +bool hungry
    Animal : +String gender
    Animal : +List~List~int~~ DNA
    Animal : +getSpecies()$ List~String~
    Animal: +sleep()*
    <<Abstract>> Animal

    class Duck{
      +String color
      +swim()
      +catch(Fish) bool
      +sleep() 
    }
    Duck "1" ..> "1" Fish : hungry = False if catch()

    class Fish{
      -int sizeInFeet
      -edible() bool
      +catch(Fish) bool
      +sleep()
    }
    Fish "1" <..> "1" Fish : hungry = False if catch()

    class Lion{
      +bool is_wild
      +catch(Duck) bool
      +run()
      +sleep()
    }
    note for Lion "From Afirca"
    Duck "1" <.. "1" Lion : hungry = False if catch()

    class Pond{
        +List~Fish~ fishes
        +add_fish(Fish)
    }
    Pond "1" --> "0..*" Fish

    class Cleaner{
        +String name
        +clean(Pond)
    }
    Cleaner "2..3" *-- "1" Pond

    class Trainer{
        +String name
        +train(Animal)
    }
    Trainer "1" o-- "0..*" Duck
    Trainer "1" o-- "0..*" Lion : Log\n-----------------------\n +List< List< String>> record\n---------------------------\n+undo()
```

### Features

- Draw w/ code

### Pros

- A code corresponds to a diagram
- Draw instantly online

### Cons

- Messy Lines
- Hard to draw association classes
- Cannot move anything
- Cannot change the color of any class

## **[PlantUML](https://plantuml.com/zh/)**

### Result Image

![PlantUML.png](PlantUML.png)

### Code

```
@startuml
title Pets in Pikas' Garden
note "author : Pikas\ntool : PlantUML" as nt1

abstract class Animal {
  + int age
  + bool hungry
  + String gender
  + List<List<int>> DNA
  + List<String> getSpecies()
  + sleep()
}

class Duck {
  + String color
  + swim()
  + bool catch(Fish)
}

class Fish{
  - int sizeInFeet
  - bool edible()
  + bool catch(Fish)
}

class  Lion{
  + bool is_wild
  + bool catch(Duck)
  + run()
}

note right of Lion: From Afirca

class Pond {
  + List<Fish> fishes
  + add_fish(Fish)
}

class Cleaner {
  + String name
  + clean(Pond)
}

class Trainer {
  + String name
  + train(Animal)
}

Animal <|-- Duck
Animal <|-- Fish
Animal <|-- Lion

Duck "1" ..> "1" Fish : hungry = False if catch()
Duck "1" <.. "1" Lion : hungry = False if catch()

Fish "1" <..> "1" Fish : hungry = False if catch()

Pond "1" --> "0..*" Fish

Cleaner "2..3" *-- "1" Pond

Trainer "1" o-- "0..*" Duck
Trainer "1" o-- "0..*" Lion : "Log\n---------\n +List< List< String>> record\n---------------------------\n+undo()"
@enduml
```

### Features

- Draw w/ code

### Pros

- A code corresponds to a diagram
- Draw instantly online

### Cons

- Very difficult to draw association classes
- Cannot move anything
- Cannot change the color of any class
- Unknown error occurred. Server response not received.

## **[Draw.io](https://app.diagrams.net/)**

### Result Image

![Untitled](Drawio.png)

### Features

- Lots of diagram element templates
- Real time collaboration if Google Drive is available

### Pros

- Support italics
- Support underlines
- Support bold
- Many fonts

### Cons

- Ugly UI

### Tutorial

- [流程圖最佳工具(for Free)：Draw.io最佳實作的５個小技巧 - jimmy-wang - Medium](https://medium.com/jimmy-wang/%E6%B5%81%E7%A8%8B%E5%9C%96%E6%9C%80%E4%BD%B3%E5%B7%A5%E5%85%B7-for-free-draw-io%E6%9C%80%E4%BD%B3%E5%AF%A6%E4%BD%9C%E7%9A%84%EF%BC%95%E5%80%8B%E5%B0%8F%E6%8A%80%E5%B7%A7-82955e410e47)

## [Visual Paradigm Online](https://online.visual-paradigm.com/drive/#diagramlist:proj=0&dashboard)

### Result Image

![Untitled.png](VisualParadigm.png)

### Features

- Real time collaboration

### Pros

- Lots of templates
- Various diagram are available
- Many fonts

### Cons

- Malfunctioned “Find & Replace”
- Cannot add attribute/method by pressing ENTER
- Cannot edit existing arrows
- Hard to edit size of class blocks
- Unintuitive arrow direction
- Hard to draw association classes
- Things deleted may pop out at unexpected place & timing
- Bad saving
- Bad deleting
- Error message “Unknown error occurred. Server response not received.” often appears
- Big watermark

## **[Excalidraw](https://excalidraw.com/)**

### Result Image

![excalidraw.png](excalidraw.png)

### Features

- Real time collaboration

### Pros

- Free to edit color, font and line style of elements
- Free to edit  text alignment
- Can import images
- Draw instantly online

### Cons

- No italics
- No underlines
- No bold
- Simple arrows only
- Straight arrows only
- No function of string replacement

## **[tldraw](https://www.tldraw.com/)**

### Result Image

![tldraw.png](tldraw.png)

### Features

- Real time collaboration

### Pros

- Can import images
- Free to edit color, font and line style of elements
- Draw instantly online
- Beautiful curves

### Cons

- No italics
- No underlines
- No bold
- No solid arrow
- No function of string replacement

## **[StarUML](https://staruml.io/)**

### Result Image

![StarUML.jpg](StarUML.jpg)

### Features

- Use `[]` to represent **2D array** & **custom class array** instead of `<>`
- Use `Ctrl` to drag the canvas
- Duplicated class block changes with the original one

### Pros

- Free to edit color and font of elements
- Offline
- Can import images

### Cons

- Annoying watermark if unregistered (free ver.)
- Installation is necessary
- Hard to add first attribute/operation
- Not easy to move lines
- No bold
- No function of string replacement
