# [Plant UML](https://plantuml.com/ko/)

PlantUML 은 다이어그램을 빠르게 작성하기 위한 오픈 소스 프로젝트입니다.

## Ditaa Diagram

PlantUML now can generate diagrams other than UML. In such cases the usual `@startuml` does not make sense anymore. So now we allow diagrams start with `@startXYZ` and finish with `@endXYZ`, where `XYZ` can change with the type of diagram and can be any characters (including spaces).

This means that plugin developers are encouraged to change their code to recognize `@start` instead of `@startuml`.

DITAA diagrams are usually formatted as @startditaa...@endditaa.

### Ditaa
[Ditaa (DIagrams Through Ascii Art)](http://ditaa.sourceforge.net/) is an Open Source project that allows to generate general diagrams from a text descriptions. The idea is close to **PlantUML**, and it may be useful for documentation to generate other diagrams than UML.

So last version of **PlantUML** allows this :

```java
@startuml
ditaa
+--------+   +-------+    +-------+
|        +---+ ditaa +--> |       |
|  Text  |   +-------+    |diagram|
|Document|   |!magic!|    |       |
|     {d}|   |       |    |       |
+---+----+   +-------+    +-------+
    :                         ^
    |       Lots of work      |
    +-------------------------+
@enduml
```
