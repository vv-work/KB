# Motoko

##Questions

- [ ]  Question on dhall. 
	- How to correctly  reference on GitHub

- [ ] Order (how to use how to crate) 
    - Lyamda methods.

- [ ]  Unit testing ?
    - how to correctly right unitt test
    - Sutites,Matchers, Testables? 
- [ ] Async/Await testing

- [ ] Iter ( toChar)?

- [ ] Array freezing/unfizing usage of buffers.
	
## Modules 

Are files basically

```motoko
import Counter "../src/Counter";
import Counter "Counter";
import Result "mo:base/Counter";
import {map,find,field, fold = fold} "mo:base/Array";


module some{}
module {}

```
## Folder Structure

```motoko

root
|
--src
|
--test
|
--example

```

## Vessel 

**Vessel** - Is a package manager for motoko specificely

`vessel init`

`$bin\vessel --version` or `vessel --version`

**Dhall**-  is a programmable configuration language that you can think of as: JSON + functions + types + imports

`vessel.dhall`

```dhall
{
	dependencies = [ "base" ], 
	compiler = Some "0.6.2" 
}

```

`package-set.dhall`

```dhall
let upstream = https://github.com/dfinity/vessel-package-set/releases/download/mo-0.6.21-20220215/package-set.dhall sha256:b46f30e811fe5085741be01e126629c2a55d4c3d6ebf49408fb3b4a98e37589b
let Package =
    { name : Text, version : Text, repo : Text, dependencies : List Text }

let
  -- This is where you can add your own packages to the package-set
  additions =
    [] : List Package

let
  {- This is where you can override existing packages in the package-set

     For example, if you wanted to use version `v2.0.0` of the foo library:
     let overrides = [
         { name = "foo"
         , version = "v2.0.0"
         , repo = "https://github.com/bar/foo"
         , dependencies = [] : List Text
         }
     ]
  -}
  overrides =
    [] : List Package

in  upstream # additions # overrides
```

#### Run vessel check

`$(vessel bin)/moc $(vessel sources) --check` - check our files


`$(vessel bin)/moc -r test/zeroTest.mo` - check our files


### Import package 

To import pckage we need :

1. In `package-set.dhall` define package `array` and github link
2. In `main.mo` define `import mo:arra/Array`

 

## Field visability    	

- `private` - enclosing object 
- `public` 
- `system` - actor field


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
Classes  - is part of the module but is seprate class each one by one.

If using Cllass make sure that output is  *stable*!!!


