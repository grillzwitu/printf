## _printf
This is repository is an implementation of printf by Taremowei Appah and Girum Ajebe, this implementation demonstartes the use of structs, typedefs, function pointers,variadic functions, write, as well as basic functions and loops in __C__. The files in this repository are compiled with __gcc -Wall -Wextra -Werror -pedantic -Wno-format *.c__, and they demonstrate how __printf__ works for various data types given the specifier. The files include;

- __holberton.h__: A header file containing are function prototypes used for the implementation of printf.

- ___putchar.c__: A function to print characters to stdout.

- __printf.c__: Prints a formatted string to stdout.

- __format_specifiers.c__: Contains the functions that implement the printing of a data type listed in the ___printf__ function pointer __f_list__. The functions contained include;
  * __print_char__: Prints a character to stdout.
  * __print_string__: Prints a string to stdout.
  * __print_percent__: Prints __%__ to stdout.
  * __print_integer__ Prints an integer to stdout.

- __print_number__: The function used with the __print_integer__ function to print numbers.

- __parser.c__: A functions that recieves the main string and all other arguments needed for ___printf__ to print a formatted string to stdout. It is called in __printf__ and serves as the ___printf__ engine. It iterates through __f_list__ and calls the functions pointed to by __sym__ which are located in __format_specifiers.c__, and gives instructions regarding the general behaviour of ___printf__.

- __man_3_printf__: A man page for ___printf__.

- __test__: A directory containng a __main.c__ file to test ___printf__. An illustration of the ___printf__ function is illustrated below. It is important that the __main.c__ is in the same directory as the ___printf__ and its other supporting functions. and the program is compiled with the command __gcc -Wall -Wextra -Werror -pedantic -Wno-format *.c__. The illustration is as follows: 

alex@ubuntu:~/c/printf$ cat main.c

#include <limits.h>  
#include <stdio.h>  
#include "holberton.h"

/\*\*  
 \* main - Entry point  
 \*  
 \* Return: Always 0  
 \*/  

int main(void)
\{

	int len;
	int len2;


	len = _printf("Let's try to printf a sentence.\n");
	len2 = printf("Let's try to printf a sentence.\n");
     
	_printf("Length:[%d, %i]\n", len, len);
	printf("Length:[%d, %i]\n", len2, len2);
	_printf("Negative:[%d]\n", -9999);
	printf("Negative:[%d]\n", -9999);
	_printf("Character:[%c]\n", 'H');
	printf("Character:[%c]\n", 'H');
	_printf("String:[%s]\n", "I am a string !");
	printf("String:[%s]\n", "I am a string !");
	len = _printf("Percent:[%%]\n");
	len2 = printf("Percent:[%%]\n");
	_printf("Len:[%d]\n", len);
	printf("Len:[%d]\n", len2);
	return (0);
\}

alex@ubuntu:~/c/printf$ gcc -Wall -Wextra -Werror -pedantic -Wno-format *.c  
alex@ubuntu:~/c/printf$ ./printf  
Let's try to printf a simple sentence.  
Let's try to printf a simple sentence.  
Length:\[39, 39\]  
Length:\[39, 39\]  
Negative:\[\-9999\]  
Negative:\[\-9999\]  
Character:\[H\]  
Character:\[H\]  
String:\[I am a string !\]  
String:\[I am a string !\]  
Percent:\[%\]  
Percent:\[%\]  
Len:\[12\]  
Len:\[12\]  
