IF YOU DO A WHICH FOR a command, and it doesn't show up but you know it is a command,
that means that it's build in to the shell, just as the "." command.
File ends with .sh
At the top, have #!/bin/bash, so it knows you want to run bash.
You can just bin/java, bin/python, etc.
./"filename" : run script, AFTER you give yourself permission to run it.
. ./"filename" : Run a script without making it an execuble. Makes a copy of the shell, and runs.

ALWAYS UPPERCASE the variable names so you can differinate them from commands

$1, $2, $#, etc... : This is the value on the argument line, which is inputted by the user.
echo Hello world $VARIABLE : Print out the text and the variable.
# : Comment

VARIABLENAME=variabledata : Make a variable; no spaces between =.
let VARIABLENAME=number : Make a number variable.
let "NAME"=$NAME+$NAME : Add numbers.

$"VARIABLENAME" : use the variable

read VARIABLENAME : Take input from user and assign it to variablename.

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
* = ALL FILES, this will effect ALL FILES, even the files in folder
"char"* , i*, a*, etc.. : ALL FILES starting with that character.

? : Single character. Example:
ls hi?.txt : Will give you all the files that have something in the dollar sign place.
hi1.txt ; hi2.txt ; hij.txt ; will print out, BUT NOT hi.txt

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

test : Tells you the truth value of the command after it. 0 = true. 1 = False. 2 = Error
OLD WAY:
test 1 -eq 1 : equals sign. Is 1 equal to one.
test 1 -gt 2 : Is 1 greater than 2.
1 -eq 1 -a 2 -eq 3 : "-a" is the "and" command.
NEW BETTER WAY: 
((1==1))
((1>))
((1==1 && 2==3))
((1==1))&&((2==3))
((1==1 || 2==3))
echo $? : Check the truth value of the previous test.

test -z VARIABLE = Check if the variable is Null, or empty. 0 for empty, 1 for in use.
test ! -z VARIABLE = "!" is the opposite

test -n "VARIABLE" = -n checks if it has a string, you NEED quotes "" around the variable.
test "%TEACHER" == "$PROF" : Check if both variables have the same string

~~~~~~~~~~~~~~~~~How if loops work: ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

if (( $AGE > 18 ))
then
  echo "Wow! You're an adult!"
  return
else
  echo "You're not an adult yet!"
fi
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

kill -9 = Unconditional kill, will kill program NO MATTER WHAT, even if you disable kill.
