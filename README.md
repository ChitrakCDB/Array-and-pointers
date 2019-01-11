# Array-and-pointers


Get next integer from input:
The function getint(int *) which takes a pointer to an integer as the argument.
We also use getch and ungetch as two functions, from chapter 4, which work on buf of BUFSIZE sharing a global variable called bufp.
ungetch function returns the character read to buf while getch tries to read that character to our program and if no character is present, 
it uses getchar to get the character.
In this program, we declare an array of size of 1000, and we send each digit of the array to getint using a call like getint(&array[n]). 
Our intention is to load the characters in array with a valid integer format like +/-1234EOF, 
that is + or - 1234 and ending with EOF character.
And if we get any invalid input.
ex:abc
    %**
Then the program will immediately end.
with some garbage values.


Get next float from input:
the program is similar to next integer program but instead of integer we are 
getting float values.
