# Data Types in C programming language
* The exact size of the data types are compiler specific.
* The `sizeof()` can be used for retrieving the amount of memory a variable acquire.

|Name            |Size (byte)     |
|:---------------|:----------------:|
|[unsigned] char              |1|
|[unsigned] short             |2|
|[unsigned] int                 |4|
|[unsigned] long              |8|
|[unsigned] long long      |8|
|[unsigned] float              |4|
|[unsigned] double          |8|

## Signed/Unsigned Data:
Lets explain unsigned concept with an example.
Consider a data type which uses 4 bits for representing numeric values. if we defince a variable called `num` with this data type, it could have values in range of  [-8, 7]. The memory state and interpreted value can be as shown below.

``` 
bit:   3     2    1    0
      [ 0 ][ 0 ][ 0 ][ 0 ] = 0
      [ 0 ][ 0 ][ 0 ][ 1 ] = 1
      [ 0 ][ 0 ][ 1 ][ 0 ] = 2
      [ 0 ][ 0 ][ 1 ][ 1 ] = 3
      [ 0 ][ 1 ][ 0 ][ 0 ] = 4
                   .
                   .
                   .
      [ 0 ][ 1 ][ 1 ][ 1 ] =  7
      [ 1 ][ 0 ][ 0 ][ 0 ] = -8
      [ 1 ][ 0 ][ 0 ][ 1 ] = -7
      [ 1 ][ 0 ][ 1 ][ 0 ] = -6
      [ 1 ][ 0 ][ 1 ][ 1 ] = -5
      [ 1 ][ 1 ][ 0 ][ 0 ] = -4
                   .
                   .
                   .
```

if we define the `num` as an **unsigned** data type then the interpretation of values will be as below. (values are in range [0, 15])
``` 
bit:   3     2    1    0
      [ 0 ][ 0 ][ 0 ][ 0 ] = 0
      [ 0 ][ 0 ][ 0 ][ 1 ] = 1
      [ 0 ][ 0 ][ 1 ][ 0 ] = 2
      [ 0 ][ 0 ][ 1 ][ 1 ] = 3
      [ 0 ][ 1 ][ 0 ][ 0 ] = 4
                   .
                   .
                   .
      [ 0 ][ 1 ][ 1 ][ 1 ] = 7
      [ 1 ][ 0 ][ 0 ][ 0 ] = 8
      [ 1 ][ 0 ][ 0 ][ 1 ] = 9
      [ 1 ][ 0 ][ 1 ][ 0 ] = 10
      [ 1 ][ 0 ][ 1 ][ 1 ] = 11
      [ 1 ][ 1 ][ 0 ][ 0 ] = 12
                   .
                   .
                   .
```

## More Reading
1. Boolean & Conditional Expressions
2. Structs
3. Pointers
