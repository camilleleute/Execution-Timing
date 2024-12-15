# A1 - Execution Timing

## Reference Materials
STM32L4xxxx Reference Manual (RM) – Clock System, GPIO
NUCLEO-L4x6 Users Manual (UM) – Pin Diagram (L476RG/L4A6ZG)

## Instructions 
### LED Counter
Connect 4 LEDs to GPIO pins PC0, PC1, PC2, and PC3. (LED and 150 Ω resistor)
Write a program that repeatedly counts 0 to 15, outputting the count to the 4 LEDs
Include a software delay (empty for loop) between counts to make the counting visible
### Measure Execution Timing
In a new project, add the code listing below (ExecutionTime.c) to main.c to replace the auto-generated main(). This code should only replace the main() function. Keep the other functions that are auto-generated with a blank project. 
Set up an oscilloscope or logic analyzer to catch a single pulse on 2 separate channels to collect accurate timing.
Notice PC0 is toggled before and after the TestFunction subroutine and PC1 is toggled before and after the arithmetic operation instruction.
Change var_type and TestFunction(num) type to test the various variable types and operations listed in Table A1.1. 
Run the code and fill in the table with the timing results obtained. To measure how long it takes to enter the subroutine (Subroutine call), look at the difference between PC0 going high and PC1 going high. You do not need to find this time for each arithmetic function, use the simple           test_var = num for filling in the table. To time the arithmetic functions, use the width of PC1

## Data type and function call
### Timing Function
uint8_t
int32_t
int64_t
float
double
### Subroutine Call
test_var = num
test_var = num + 1
test_var = num * 3
test_var = num / 3
test_var = num * num
test_var = num % 10
test_var = pow(num, 3)
test_var = sqrt(num)
test_var = sin(num)

## Deliverables
- Demonstrate your working LED counter program to the instructor or lab assistant
- Submit your properly formatted C source code file for the LED counter.
- Fill out the execution timing table on Canvas
