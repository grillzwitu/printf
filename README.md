## _printf
This is repository is an implementation of printf by Taremowei Appah and Girum Ajebe, this implementation demonstartes the use of structs, typedefs, function pointers,variadic functions, write, as well as basic functions and loops in __C__. The files in this repository are compiled with __gcc -Wall -Wextra -Werror -pedantic -Wno-format *.c__, and they demonstrate how __printf__ works for various data types given the specifier. The files include;

- __holberton.h__: A header file containing are function prototypes used for the implementation of printf.

- ___putchar.c__: A function to print characters to stdout.

- __printf.c__: Prints a formatted string to stdout.

- __format_specifiers.c__: Contains the functions that implement the printing of a data type listed in the ___printf__ function pointer __f_list__. The functions contained include;
  __print_char__: Prints a character to stdout.
  __print_string__: Prints a string to stdout.
  __print_percent__: Prints __%__ to stdout.
  __print_integer__ Prints an integer to stdout.

- __print_number__: A helper function used with the __print_integer__ function.

- __parser.c__: A functions that recieves the main string and all other arguments needed for ___printf__ to print a formatted string to stdout. It is called in __printf__ and serves as the ___printf__ engine. It iterates through __f_list__ and calls the functions pointed to by __sym__ which are located in __format_specifiers.c__, and gives instructions regarding the general behaviour of ___printf__.

- __test__: A directory containng a __main.c__ file to test ___printf__
