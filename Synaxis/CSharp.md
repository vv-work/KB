## LINQ

```cs
var lowNums = from num in numbers
              where num < 5
              select num;
```

## async/await

## Serialization


```puml
@startuml

class Animal {
    Say()
}
class Dog{
    Say(string s)
    Jump()
}

Animal *-- Dog 


@enduml
```puml
## Resources
[Book]()