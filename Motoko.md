# Motoko

## Unit testing

 [Motoko color repo](https://github.com/ByronBecker/motoko-color) Repo with unit tests setup to start making the unit test on local machine
`make test` - to run the unit tests in that repo

## Vessel

[Github repo](https://github.com/dfinity/vessel)

`$(vessel bin)/moc $(vessel sources) -wasi-system-api main.mo`

For motoko non-dfx projects.
`$(vessel bin)/moc` - command to start working with a prject or something

## Let Declaration

`let <pat> = <exp>`
- `<exp>` has type `T`
- `<pat>` has type `T`

`let` is *immutable*

```motoko


```

## Var Declation

**VAR** is *mutable* declaration `var <id> (: <typ>)? = <exp>`

- If the annotation `(:<typ>)?` is present, then `T == <typ>`.
    	
## Type decalartion

`  type Person = { first : Text; last : Text };`

The declaration type `<id> <typ-params>? = <typ>` declares a new type constructor `<id>`, with optional type parameters `<typ-params>` and definition `<typ>`.

The declaration type `C < X0 <: T0>, …​, Xn <: Tn > = U` is well-formed provided:

