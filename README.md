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


strcat(s,t) copies the string t to the end of s:

int this program we have used mgetline function i have useed this before also which takes the line and read it
till the end of file.
and the function mystrcat reads the line untile it is 0
and then the value of t is combined with s \\(*s=*t)!='\0'.
and the new string is combined.

simple version of strncmp,strncpy,srncat:
mystrlen assigns the address of s to p in char *p = s and then goes one character at a time, till it reaches 0. When it is at the end of the word, it subtracts the current address s with intial address p, which thus returns the len of string.

mystrncpy copies n characters of source string to destination. It does this by copying or overwriting one character a time from source to destination and keeps track of count n. When source is exhausted or n characters are copied, it checks if there further characters in destination, if it exists, it goes past them without over-writing and then closes the string by 0.




 strend returns 1 if string t occurs at the end of the string s:
The primary part of this program is the strend function, which takes two character pointers, s and t. It calculates the length of t and stores in the variable len. And then, we back off till the last characters in both s and t.
And then we look for the match from the end. This is checked in this while loop. While the len is > 0, check if s and t are same and back off one character at a time.
If the string t exhausts, that is, it’s length, len becomes 0, then we known that string t occurs at the end of string s and we return 1. Otherwise, we return 0.

mystrncat, takes three arguments, str1, str2 and dest. It concatenates n characters from str2 to str1 into a new string dest. It does this by copying all characters from str1 to dest and then keeps a track of count n, and copies n characters of str2 to dest. After copying n characters, it closes the dest string by 0 character.

mystrncmp, compares the lhs string with rhs string. It compares one character at a time and as long as both characters are same, it keeps going and if the lhs is exhaused before n characters are compared, it means we still satisfy the criteria and we return 0. Otherwise, it returns the difference between lhs character and rhs character, which will be 0 if they are equal, negative if lhs is smaller than rhs or positive value if lhs is greater than rhs.




expr, evaluate rpn from command line:
The main function has a signature now, that is int main(int argc, char *argv[]), that is it takes the command line args, argc for count of the args and argv is the array which stores the arguments.
input will be stored in the array agrv as strings. In this program, we go about by getting each argument from argv and then giving that as the input to our RPN calculator,

If we find an operand, using the push function, we push it to the stack and when we find a operator in the input, we pop() the two operands out of the stack and do the operation.
