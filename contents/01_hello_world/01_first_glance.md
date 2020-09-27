# First glance on a C program
A simple program has been provided below.
Its purpose is to demonstrate the syntax used for 
1. Including other libraries and source codes
2. Introduce the concept of main function
3. Show variable decleration and assignment
4. Introduce the inline and multiline comments

```
/* In C you use directive "#include" to inform the complier that
 * you want to add a file to your source code.
 * this directive simply copies the file mentioned in front of it
 * and place it at the position the directive has been writen
 * */
#include <stdio.h>

/* For includeing you can use two syntax shown below:
 * 1. #include <name of the file>
 * 2. #include "name of the file or relative path to the file"
 * In the case of using <...> compiler will look for the file name
 * in the systems predifined directories. But when "..." is used you can
 * use a relative path the file
 * */
 #include "../include/my_utility_library.h" // relative address to the file 

int main()
{
    /* for defining a variable:
     * <data-type> <variable-name>;
     */
    int a = 10;
    int b = 20;
    int c;
    c = a + b; 
    return 0;
}
```

# More Reading
1. Header Files
2. Data Types
3.  Memory Allocation from Stack and Heap
