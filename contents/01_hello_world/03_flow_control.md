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