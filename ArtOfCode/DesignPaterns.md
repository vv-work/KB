# Design Patterns

List

Creational
    - Abstract Factory
    - Builder 
    - Factory Method
    - Prototype
    - Singelton
Stractural
    - Adapter
    - Bridge
    - Composite
    - Decoretor
    - Facade
    - Flyweight
    - Proxy
Behavioural
    - Cahain Of Responsabiliteis
    - Command
    - Iterator
    - Mediator
    - Memento
    - Observer
    - State 
    - Strategy
    - Template Method
    - Visitor




#Creational

#Stractural


#Behavioural


##Command

Undo & Redo 
    Just add Execute&UnExecute in order 
    to be able use do undo.

Stracture
        Invoker
            ctor(Icommand c)
        ICommand
        -ctor(Data d)
        - Exectute()
        - UnExecute()
        ConcrateCommand
        - Exectute()
            {Reciever.Action()}
        Reciever
            Action()  

# Other

## Hamble Object Pattern
I was chalanage I was checking the 
Notes but unfortenetly they have reference to article I don't have.

Just simple from MonoBahaviour you call object. 
And it call MonoBehaviour back.
