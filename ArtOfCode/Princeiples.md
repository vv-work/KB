# Principles


## Reusable Abstraction Principle

**RAP** (**R**eusable,**A**bstraction,**P**rinciple)
[Article RAP](http://codemanship.co.uk/parlezuml/blog/?postid=934)

## S.O.L.I.D

### Single Responsibility Principle

### Open/Closed Principle

### Liskov Substitution

### Interface Sugregation

### Dependency Injection

```csharp
public class Bar
{
    ISomeService _service;

    public Bar(ISomeService service)
    {
        _service = service;
    }

    public void DoSomething()
    {
        var foo = new Foo(_service);
        foo.DoSomething();
        ...
    }
}
```

## TDD