# ConsolePrettify
A simple tool for making good UI in C console apps.

## How to Use
Download or clone this repository. Copy `prettify_functions.c` and `ConsolePrettify.h` into your project folder and add `#include "ConsolePrettify.h"` in your C files.

Make sure the new files are correctly linked in your IDE/compiler.

## Available Functions

Function | Description
--- | --- 
`prettify_textcolor(color)` | Changes the text color
`prettify_textbox(specifier, variable, color)` | Displays an input field and reads user input
`prettify_textbox_password(variable, mask, color)` | Displays an input field with masking eg. *****

_**NOTE**: Please use `prettify_textcolor()` for all colored text in your program._.

## Available Colors
use any of these constants as the color arguments of prettify functions
Color | Value
--- | --- 
RED | 12
GREEN |  10
LIGHT_BLUE | 11
YELLOW | 6
LIGHT_YELLOW | 14
BLUE | 9
PURPLE | 5
WHITE | 15
CYAN | 3
GRAY | 7
DARK_GRAY | 8

___
## Examples

```c
int num;
char password[25];

printf("THIS IS A TEXTBOX");
prettify_textbox("%i", &num, YELLOW);

printf("\nTHIS IS A PASSWORD TEXTBOX");
prettify_textbox_password(password, '+', BLUE);
```
Output:

![Output](images/output1.png)