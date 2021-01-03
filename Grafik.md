<!--
author:   Sebastian Zug & André Dietrich
email:    sebastian.zug@informatik.tu-freiberg.de & andre.dietrich@informatik.tu-freiberg.de
version:  0.0.4
language: de
narrator: Deutsch Female

import:  https://raw.githubusercontent.com/liascript-templates/plantUML/master/README.md

-->

# Grafische Darstellungen


                        {{0-1}}
*******************************************************************************
1. ASCII basierte Grafiken

<!-- style="display: block; margin-left: auto; margin-right: auto; max-width: 315px;" -->
``` ascii
                           .--->  F
  A       B     C   D     /
  *-------*-----*---*----*----->  E
           \            ^ \
            v          /   '--->  G
             B --> C -'
```

<!-- style="display: block; margin-left: auto; margin-right: auto; max-width: 315px;" -->
```    ascii
  +------+   +-----+   +-----+   +-----+
  |      |   |     |   |     |   |     |
  | Foo  +-->| Bar +---+ Baz |<--+ Moo |
  |      |   |     |   |     |   |     |
  +------+   +-----+   +--+--+   +-----+
                ^         |
                |         V
  .-------------+-----------------------.
  | Hello here and there and everywhere |
  '-------------------------------------'
```

*******************************************************************************

                         {{1-2}}
*******************************************************************************

2. PlantUML-Grafiken

```text @plantUML.png
@startuml

abstract class AbstractList
abstract AbstractCollection
interface List
interface Collection

List <|-- AbstractList
Collection <|-- AbstractCollection

Collection <|- List
AbstractCollection <|- AbstractList
AbstractList <|-- ArrayList

class ArrayList {
  Object[] elementData
  size()
}

enum TimeUnit {
  DAYS
  HOURS
  MINUTES
}

annotation SuppressWarnings

@enduml
```

*******************************************************************************

                         {{2-3}}
*******************************************************************************

3. Interaktive PlantUML-Grafiken

Diese können Sie zur Laufzeit verändern und damit Anpassungen vornehmen. Die Änderungen werden lokal gespeichert.

```text @plantUML.png
@startuml
ditaa

+---------+  /--------\   +-------+
| cBLU    +--+cAAA    +---+Version|
|         |  |  Data  |   |   V3  |
|    +----+  |  Base  |   |cRED{d}|
|    |cPNK|  |     {s}|   +-------+
|    |    |  \---+----/
+----+----+   
@enduml
```
@plantUML.eval(png)


*******************************************************************************
