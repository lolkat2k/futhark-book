Ideas for exercises.
==

Define the following functions:

```
-- Summation.
val sum [n]: (xs: [n]i32) -> i32

-- Taking product.
val product [n]: (xs: [n]i32) -> i32

-- Computing average - remember to not use i32 for intermediate
-- calculations!
val average [n]: (xs: [n]i32) -> i32

-- Dot product.
val dotprod [n]: (xs: [n]i32) -> (ys: [n]i32) -> i32

-- Multiply matrix with row vector.
val matvecmul_row [n][m]: (xss: [n][m]i32) -> (ys: [m]i32) -> [n]t

-- Multiply matrix with column vector.
val matvecmul_col [n][m]: (xss: [n][m]i32) -> (ys: [n]i32) -> [n][n]t

-- Multiply two matices.  Hint: You will need to use the 'transpose'
-- function.
val matmul [n][p][m]: (xss: [n][p]i32) -> (yss: [p][m]i32) -> [n][m]i32
```

Define some of the array utility functions:

https://futhark-lang.org/docs/futlib/array.html

Testing
--

Put the functions in one or more files.  If you define them with
`entry` instead of `let`, then you can easily add tests:

```
-- ==
-- entry: abs
-- input { 1 } output { 1 }
-- input { -1 } output { 1 }

entry abs (x: i32) = if x < 0 then -x else x
```

Run with `futhark-test`.
