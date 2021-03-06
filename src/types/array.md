# Array types

> **<sup>Syntax</sup>**\
> _ArrayType_ :\
> &nbsp;&nbsp; `[` [_Type_] `;` [_Expression_] `]`

An array is a fixed-size sequence of `N` elements of type `T`. The array type
is written as `[T; N]`. The size is an expression that evaluates to a
[`usize`].

Examples:

```rust
// A stack-allocated array
let array: [i32; 3] = [1, 2, 3];

// A heap-allocated array, coerced to a slice
let boxed_array: Box<[i32]> = Box::new([1, 2, 3]);
```

All elements of arrays are always initialized, and access to an array is
always bounds-checked in safe methods and operators.

> Note: The [`Vec<T>`] standard library type provides a heap-allocated resizable
> array type.

[_Expression_]: expressions.html
[_Type_]: types.html#type-expressions
[`Vec<T>`]: ../std/vec/struct.Vec.html
[`usize`]: types/numeric.html#machine-dependent-integer-types
