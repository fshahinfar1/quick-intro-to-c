# Operators
The defined operators in C language can have either:
    1. one operand (unary operators)
    2. two operands (binary operators)
    3. three operands (ternary operators)

The operators can be categorized by:
    1. Arithmetic
    2. Relational
    3. Logical
    4. Bitwise
    5. Assign
    6. Others

The list of operators are:

**1) Arithmetic**

| Type | Symbol | Description |
|:---:|:----:|:----------:|
|Binary|\*|Multiplication `a * b`|
|Binary|/|Division `a / b`|
|Binary|+|Addition `a + b`|
|Binary|-|Subtraction `a - b`|
|Binary|%|Returns the remainder of divison of `a` by `b`|

**2) Relational**

|Type|Symbol|Description|
|:---|:----:|:----------|
|Binary|==|Equality|
|Binary|!=|Inequality|
|Binary|>|Greater than|
|Binary|<|Less than|
|Binary|>=|Greater than or Equal|
|Binary|<=|Less than or Equal|

**3) Logical**

|Type|Symbol|Description|
|:---|:----:|:----------|
|Binary|&&|Logical And|
|Binary|\|\||Logical Or|
|Binary|!|Logical Not|

**4) Bitwise**

|Type|Symbol|Description|
|:---|:----:|:----------|
|Binary|&|And|
|Binary|\||Or|
|Binary|~|Not|
|Binary| << [n: an integer] |shift left by n, insert 0 at right when shifting|
|Binary| >> [n: an integer] |shift right by n, insert 0 at left when shifting|

**5) Assign**

|Type|Symbol|Description|
|:---|:----:|:----------|
|Binary|=|Assign value from rigth side value (rvalue) to left side value (lvalue)|
|Binary|`<arithmatic op>`=|Assign result of applying the op on the current value of lvalue and rvalue to the lvalue e.g. `x += y // x = x + y`|
|Binary|`<bitwise op>`=|Same as above but with bitwise operators|

**6) Others**

|Type|Symbol|Description|
|:---|:----:|:----------|
|Unary|sizeof()|Is evaluated to the number of bytes the data type (or data type of a variable) requires|
|Unary|&|Is evaluated to the memory address of the variable|
|Unary|\*|Is evaluated by fetching value from the memory. The variable value is treated as a memory address and value from that memory address is fetched|
|Ternary|(condition) ? `<true-value>` : `<false-value>`||

