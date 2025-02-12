# Introduction

A vector is a 1-dimensional array.
They may contain elements of different types.

## Creating Vectors

Vectors can be created via the `vector` function or by using its reader form `#()`

```lisp
(vector 1 t "foo" 'b) ; => #(1 T "foo" B)
#(2 nil "bar" a)     ; => #(2 NIL "bar" A)
```

Since they are arrays they can also be created with `make-array`:

```lisp
(make-array 3 :initial-element 'x) ; => #(X X X)
(make-array 3 :initial-contents '(a b c)) ; => #(A B C D)
```

## Vector Predicate

To check if object is a vector simply use the predicate `vectorp`.

## Accessing Elements

To access elements of a vector use `aref`, the indexes are zero-based:

```lisp
(aref #(1 2 3) 1) ; => 2
(aref #(a b c) 0) ; => A
```

