# Data Types in C programming language
* The exact size of the data types are compiler specific.
* The `sizeof()` can be used for retrieving the amount of memory a variable acquire.

|Name            |Size (byte)     |
|:---------------|:----------------:|
|[unsigned] char           |1|
|[unsigned] short          |2|
|[unsigned] int            |4|
|[unsigned] long           |8|
|[unsigned] long long      |8|
|[unsigned] float          |4|
|[unsigned] double         |8|

* Other than specified data types there are:
    1. pointer to a `<data type>`
    2. array of a specific `<data types>`
* These two types although related to other data types, are two different types.
* Size of a pointer data type is defined by the system architecture. For example in a 32-bit system the memory addresses are defined by 32-bits or 4 bytes hence the `sizeof(<pointer data type>) = 4 // bytes`.
* Size of an array data types is depndent on its number of elements. It can be calculated as `sizeof(<data type>) * number_of_elements //bytes`.

## Some useful types defined in standard headers
### stdbool.h
By includeing `<stdboo.h>` the `bool`, `true`, and `false` values are defined and can be used in source code. If this header is not included three mentioned values does not exist. For checking what is defined in `stdbool.h` check [here](https://pubs.opengroup.org/onlinepubs/9699919799/).

### stdint.h
A useful way of defining values is specifying their exact width in the type. this can be acheived by includeing `<stdint.h>` header. By including this the following data types are defined:

```
+ int8_t,  uint8_t
+ int16_t, uint16_t
+ int32_t, uint32_t
+ int64_t, uint64_t
```

The details of defined macros and constants in this header file is available [here](https://pubs.opengroup.org/onlinepubs/9699919799/).

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
