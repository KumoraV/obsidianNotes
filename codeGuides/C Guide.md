WHEN USING PART OF SOMEONE"S CODE, CREDIT THE WEBSITE IN THE COMMENTS
WHEN USING PART OF SOMEONE"S CODE, CREDIT THE WEBSITE IN THE COMMENTS
WHEN USING PART OF SOMEONE"S CODE, CREDIT THE WEBSITE IN THE COMMENTS
Make each command on a differnet line, dont combine commands on the same line. It's messy and hard to read.

Make a pointer = type *a;
Type is the type of variable: int, char, long, etc...
*a means a pointer with name a.

& infront of variable = give me the address of
* in front of pointer = give me whatever is at this address.


Allocate Memory blocks~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
malloc : type *name = (cast_type*)malloc(byte_size);  Ex. int *name = (int*)malloc(n*sizeof(int));
calloc : int *a = (cast_type*)calloc(n, sizeof(int));    This initalizes all the elments 0.
realloc : int *b = (int*)realloc(a, 2*n*sizeof(int));    This copys and pastes the old block, plus changes the size.
free(a); = Free memory block
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
scanf("%lf", &outerD); 
^What does ^^&^^ mean: & before the variable name means to assign it
The % means that this is a variable.
The lf means its a long float.
The & means give me the address of.
outerD is the variable that contains the input.
The first % matches with the first variable, the second with the second, and so on.

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
printf("The Rim Area of the washer is %-10.5lf\n", area);
The - means to left justify. This means to put the number close to the left text, with just a single space inbetween.
The "%" means that this is a variable.
The 10. means 10 numbers long, including the dot.
the 5 means 5 decimal numbers long.
lf means it's a long float.
\n means new line.
area means what the %10.5lfn variable is.
To write a literal % instead of a command %, you would write %%. Same for \, you would do \\.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
&& = and ~~~~ if (a < 20 && b < 30)
|| = or
! = not (called "bang") ~~~~~~ 


Comment out line = //
Comment out multiple lines = /* ~~~~~~~~
                                ~~~~~~
			     */

Show all of highlighted: shift + 8. Press I to cancel.


~~~~~~~~~~~~~/////////~~~~~~~~~~~////~~~~/~~~~~~~/~~~~~~~~~~~~

int main( int argc, char *argv[] )
argc = argument count
argv = argument value, the argument you're entering
argv[] = you don't know how big the arrary is
*argv = An array to pointers, the star is declaring it as an array of pointers to character arrays.
Always make argc and argv a useful name to give them meaning and make it more readable.
Every number in a command argument is a string, never a number.

If asked for command line input, make sure you DO NOT USE interactive command, which is where you
enter your own input into the command line. Instead, use argc, command line argument.

"""number=atoi(argv[index]);""""
atoi = ascii to integer, make the char 5 into the int 5
~~~~~~~~~~~~~~~~~////~~~~~~~~~~~//////////~~~~~~~~~~~~~~~~~~~~
:

for loop: for(ind = 0; ind < 4; ++ind) ~~~ Make ind 0, while ind is less than 4, continue loop and add one to ind)
Array: int arrayofint[4] = {2, 4, 6, 8);
       char arrayofchar[4] = {'2', '4', '6', '8'};

int tuple[3][4] =         ~~~~ Makes a multiple dimesonal array thats row x coloum. [1][2] is 6.
	{ {0, 1, 2, 3}
	  {4, 5, 6, 7}
	  {8, 9, 10, 11} }

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Get input interactiverly using fgets:
fgets("newVariable", "Length", "inputFile,normallystdin")
fgets(fgetsStr, 100, stdin);
ALWAYS replace the newvariable's second to last char into \0. (fgetsStr[strlen(fgetsStr-1]="\0"

Compine strs:
strcat("first str", "secondstring);
stringconcatanate adds the second string to the first string.

Search for string and print everything from it and after:
strstr("stringtosearchin","stringtosearchfor");


Forks:
pid_t pid; : A vairable type that describes how many bits you need for an integer.
pid = fork(); : Makes another instance, a child program, that starts running below this line.

execvp ("new program", "whattopassthrough); :This overwrites the current program with the new program and passes through a command.
execvp ("./daughter", theargs);

Exit,break,continue:
exit(#);
break; : To stop the loop and fall through. (Stop loop and continute after loop).
continue; : Continue loop


Structs:::::::
Struct is a data type that holds other variables of different data types:

struct grades
{ char *name;
  int final;
  int midterm;
  int extra;
};

struct grades CSIT231;
CSIT231.name ="Chris";
CSIT231.final =97;
CSIT231.midtem =87;
CSIT231.extra=10;

struct grades *pCSIT231;    : Pointer to CSIT231

struct grades CSIT[30];     : Array of 30 big, im assigning the bottom to the 4th value.
CSIT[4].name ="Chris";
CSIT[4].final =97;
CSIT[4].midtem =87;
CSIT[4].extra=10;

To get the value of a struct, you would use ::::
pCSIT231->final  : If using pointers
or
CSIT231.midterm
