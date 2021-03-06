## `purescript-elm-basics`

This is a Purescript port of the `Basics` module from [Elm's core library](https://github.com/elm-lang/core/blob/master/src/Basics.elm). This library only defines a few values, the rest are available from Purescript libraries or the [Prelude](https://github.com/purescript/purescript/tree/master/prelude).

This library is intended to help port [Elm](http://elm-lang.org/) libraries and programs to [Purescript](http://purescript.org/).


### Installation and Usage

`bower install purescript-elm-basics`

`import Elm.Basics`


### `Elm.Basics` Module Contents

Please also see the detailed [Module Documentation](docs/Elm/Basics.md).

* The built-in type `Number` is used instead of `Float`

* `degrees`, `radians`, `turns` are functions with type `Number -> Number`

* `clamp :: Number -> Number -> Number -> Number`

* `<|` and `|>` are provided and synonymous with `$` and `#`


### Not Included

The other types and values from Elm's `Basics` all have Purescript analogues and can be `import`ed from their respective modules, so they were not included. Here's a short migration guide:


#### `Prelude`

* `==`, `/=`, `<`, `>`, `<=`, `>=`, `+`, `-`, `*`, `/`, `negate`, `not`, `&&`, `||`, `++`, `otherwise`, `flip` can be imported from Purescript's `Prelude`

*  `<<` and `>>` become  `<<<` and `>>>` from `Prelude`

* `toString` is superseded by the `show` method of the `Show` typeclass from [Prelude](https://github.com/purescript/purescript-prelude/blob/master/docs/Prelude.md#show)

* `identity` becomes `id`, and `always` becomes `const`, from `Prelude`

* `Order` becomes `Ordering` and is used with the `compare` method of the `Ord` typeclass from [Prelude](https://github.com/purescript/purescript-prelude/blob/master/docs/Prelude.md#ordering)

* `xor` becomes `.^.` from the `Bits` type class, of which there is an instance for `Num`


#### `Math`

* `max`, `min`,  `round`, `floor`, `abs`, `sqrt`, `e`, `pi`, `cos`, `sin`, `tan`, `acos`, `asin`, `atan`, `atan2` are in module `Math` from [purescript-math](https://github.com/purescript/purescript-math)

* `ceiling` becomes `ceil`, and `^` becomes `pow` in `Math`


#### `Data.Tuple`

* `fst`, `snd`, `curry`, `uncurry` are in `Data.Tuple` from [purescript-tuples](https://github.com/purescript/purescript-tuples)

#### `Data.Int`

* `toNumber` (to be used instead of `toFloat`), as well as `floor`, `ceil`, `round` and others are in `Data.Int` from [purescript-integers](https://github.com/purescript/purescript-integers)


#### `Global`

* `isNaN` and `isFinite` (negated `isInfinite`) available from [purescript-globals](https://github.com/purescript/purescript-globals)


### TODO

* `//`, `rem`, `%`, `logBase`, `truncate`

* `toPolar`, `fromPolar`
