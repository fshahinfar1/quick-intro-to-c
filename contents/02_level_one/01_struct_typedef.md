# Struct and Typedef

## Syntax: Defining a Struct
```
/* In this program a rectangle is 
 * represented on a 2d screen
 * */
#include <stdio.h>

/* defining a struct for holding values
 * representing a point on a 2d screen
 * */
struct point {
    int x; // position along x axis
    int y; // position along y axis
};

// define a type `point_t` (a.k.a. struct point)
typedef struct point point_t;

/* define a struct representing a rectangle
 * on its position on a 2d screen
 * */
struct rectangle {
    unsigned int width;
    unsigned int height;
    point_t top_left_corner;
};

// impl
....
```

## Initialization of Struct
```
int main (int argc, char *argv[])
{
    // notice the full data type name is 
    // `struct rectange`
    struct rectangle rect_1;
    
    // now that we have allocated memory for
    // rect_1. we can populate the structure.
    rect_1.width = 10;
    rect_1.height = 5;
    
    // we can use both `point_t` or 
    // the full name `struct point` to define
    // a variable of type point.
    // notice that we can initialize structs
    // with this initializer syntax too.
    struct point =  {
      .x = 7,
      .y = -6
    };
    
    ...
    
    return 0;
}
```


