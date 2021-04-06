# Unit Testing

## NSubsititue

```powershell
 Install-Package NSubstitute.Analyzers.CSharp -Version 1.0.14
 ```

### Usage

**Create**

```csharp
_calculator = Substitute.For<ICalculator>();
```

**Return**

```csharp
_calculator.Add(1, 2).Returns(3);
Assert.That(_calculator.Add(1, 2), Is.EqualTo(3));
```

**Events**
```csharp
bool eventWasRaised = false;
_calculator.PoweringUp += () => eventWasRaised = true;

_calculator.PoweringUp += Raise.Event<Action>();
Assert.That(eventWasRaised);
```

**Check if was a call** 
```csharp
_calculator.Add(1, 2);
_calculator.Received().Add(1, 2);
_calculator.DidNotReceive().Add(5, 7);
```

**Any**

```csharp
_calculator.Add(10, -5);
_calculator.Received().Add(10, Arg.Any<int>());
_calculator.Received().Add(10, Arg.Is<int>(x => x < 0));
```