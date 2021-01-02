# Flow Control
Controlling the sequence of execution of instructions is a powerful tool for creating programs. In this section the following constructs of C programing language are introduced.
1. if/else
2. whille
3. for

## if / else
One very intuitive way of controlling the flow of a program is to execute some instructions based on a condition. The `if` keyword helps checking the condition and the block of statements comming ater that are executed only if the condition provided to the if has been met (having a true value).

An `else` block can be used after a block of `if` statement. The instructions in the `else` block is executed only if the condition given to the `if` statement is valued as false. 

The code sinppet below demonstrates this.

```
/* Assume an air conditioner device that should turn on and off 
 * if the temperature read by thermostat is in some certain ranges.
  * */
#include <stdio.h>

int main(int argc, char *argv[]) {
    int temp;

    printf("temperatue:\n");
    scanf("%d\n", &temp);
    if (temp < 20) {
    	turn_on_heater();
    } else if (temp < 25) {
    	// make sure both heater and ac are off.
	turn_off_heater();
	turn_off_ac();
    }  eles {
        turn_on_ac();
    }
    
    return 0;
}
```

## While loop
The body of while loop is executed until the condition is evaluated as `true`.
```
#include <stdio.h>
#include <string.h> 
 
int main(int argc, char *argv[])
{
  unsigned char condition = 1;
  char cmd[32];
  while (condition) {
    fgets(cmd, 32, stdin);
    if (strcmp(cmd, "quit\n") == 0) {
      condition = 0;
    }
    /* execute the command and perform related operations.  ...    */ 
  }
  return 0; 
}
```

## For loop
```
for ( 1. initialization ;  2. condition; 4. operation ) {
  3. body
} 
```
A for loop has the syntax showed above. The body of the for loop is executed over and over until the condition is evaluated as `false` or `0`.

The steps of executing a for is loop as below:
1. First the initialization section is executed. If there is any variable definition, the scope of the variable will be the body of for loop. This means that the variable defined in for loop is undefined out side of the body of the loop (unless redefined).
2. After executing the initialization section the condition section (shown in code snippet below) is checked. If the condition is satisfactory, meaning it is `true` or `non-zero`, the execution of the loop begins from the first instruction in the body of the for loop. If condition is `false` then the loop is not executed at all and the flow of the program is moved to the next instruction after the loop block.
3. Assuming the loop condition was `true`, all the instructions in the loop are exectued (except if there is `continue` or `break` statements).
4. After reaching the end of the loop's block, the operation section in the loop declartion line is executed.
5. Then, the condition of the loop is checked, if `true` the loop is going to be executed again (jump to point 3). Otherwise the loop is terminated and the flow of the program is continued.

Example of a for loop counting the even numbers:
```
int count = 0;

for (int i = 0; i < 10; i++) {
  if (i % 2 == 0)
    count++;
}
```

We can write a for loop using only a while loop. This might help in understanding the steps of execution described above.
```
int count = 0;

// defining scope of for loop
{
   // 1. initialization and declaration
   int i = 0;
   // 2. condition
   while (i < 10) {
     // 3. loop body ....
     if (i % 2 == 0)
       count++;
     
     // last instruction the loop
     // 4. operation section in the for loop definition
     i++;
   }
}
```