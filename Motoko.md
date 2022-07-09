# Motoko

##Questions

- [ ] Order (how to use how to crate) 
    - Lyamda methods.

- [ ]  Question on dhall. 

- [ ]  Unit testing ?
    - how to correctly right unitt test
    - Sutites,Matchers, Testables? 
- [ ] Async/Await testing

- [ ] Iter ( toChar)?

- [ ] Array freezing/unfizing usage of buffers.
	
    	

## Unit testing

 [Motoko color repo](https://github.com/ByronBecker/motoko-color) Repo with unit tests setup to start making the unit test on local machine
`make test` - to run the unit tests in that repo

## Vessel

[Github repo](https://github.com/dfinity/vessel)

`$(vessel bin)/moc $(vessel sources) -wasi-system-api main.mo`

For motoko non-dfx projects.
`$(vessel bin)/moc` - command to start working with a prject or something

## Variable declation 

if u declare variable through the `let` you would not be able to latter change it or use incide of the loop

### Let Declaration

`let <pat> = <exp>`
- `<exp>` has type `T`
- `<pat>` has type `T`

`let` is *immutable*

```motoko


```

### Var Declation

**VAR** is *mutable* declaration `var <id> (: <typ>)? = <exp>`

- If the annotation `(:<typ>)?` is present, then `T == <typ>`.
    	
## Type decalartion

`  type Person = { first : Text; last : Text };`

The declaration type `<id> <typ-params>? = <typ>` declares a new type constructor `<id>`, with optional type parameters `<typ-params>` and definition `<typ>`.

The declaration type `C < X0 <: T0>, …​, Xn <: Tn > = U` is well-formed provided:


## Making a loop 

### For loop 

```motoko
    for(i in Iter.range(0,size-1)){
      Debug.print(i);
    };
```

### Labeled loop

```Motoko

label l loop {
  i += 1;
  Debug.print(" I am in the fucking loop"); 
  Debug.print(debug_show(i));
  if(i >= 10)
    break l;
}
```

### while loop

```Motoko
     public func OurLoop() {

        var i = 0;
        while(i < 10) {
        i += 1;
        Debug.print(" I am in the fucking loop"); 
        Debug.print(debug_show(i));
        }
    };
```

### 

Actor - is a class canister( I get a canister 
Modules -  Set of functions or even a class or variables
Classes  -

If using Cllass make sure that output is  *stable*!!!


