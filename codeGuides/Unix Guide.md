WHEN USING PART OF SOMEONE"S CODE, CREDIT THE WEBSITE IN THE COMMENTS
WHEN USING PART OF SOMEONE"S CODE, CREDIT THE WEBSITE IN THE COMMENTS
WHEN USING PART OF SOMEONE"S CODE, CREDIT THE WEBSITE IN THE COMMENTS

Daemon (Prononuced demon): Processes running in the background waiting for your command, usually at the end of the line as "d". Ex. "sshd"
Do not put quotations mark, they are indications for you to insert text.
class files: cd /var/tmp/CSIT231_FA22/

ALL variables WILL be written in ALL UPPERCASE. This is to differniate variables from commands.
$ means the end of something.
./ means the dir you are in. This can be changed to have another dir.
~/ means the home dir. Can be changed for a different dir.
| command = pipe commands. This will take the output of the first command and make it the input of the second command.
Exit command = ctrl+c
-c = create
-v = verify
-t = test
* = everything

Check version of unix: uname -a
Check history of commands: history
Find something: grep "~~~"

See contents: ls
See hidden files: ls -a
See file information: ls -l
See inode value/ primary key of all primary files: ls -i
See file type: file "filename"
See all file and acesses information: stat "filename"
See where you are: pwd

Home dir: cd
Home dir 100% : cd ~
Current dir: cd .
Move back a dir: cd ..
Go to dir located in current: cd "dirname"
Go to root: cd /
Go to dir: cd "/name/name/dirname"


/////////////MAKE, DELETE, COPY, MOVE/////////////////
Make dir: mkdir "dirname"
Remove dir: rmdir "dirname"

Just make file: echo > "filename".txt
Make file and edit w/ vi: vi "filename"
Make file and edit w/ nano: nano "filename"
Remove file: rm "filename"

Copy file to different dir: cp "filename" "destination dir"/
Make a copy to same dir: cp "filename" "newname"
Rename file: mv "filename" "newname"
Move file: mv "filename" "destination dir"/
Move and rename file: mv "filename" "destination dir"/"newname"

Overwrite or make txt in file: echo "text" > "filename"
Add txt to bottom of file: echo "text" >> "filename"
Print file: cat "filename"
"tee" command: Send a command both ways, like a T pipe.
echo "txt" | tee -a FDU.txt  ::: -a means append, so it adds to bottom of file

Save stdout to file: 1 > "name" :::: 
Save stderr to file: 2 > "name  :::: EX. grep -QQQ Knights FDU.txt 2> FDUTeaneck.txt (Gets a sentence that contains Knights from FDU.txt and sends the error to FDUTeaneck.txt. Change the 2 to 1 to send the normal output to it.
EX... (grep Knights FDU.txt; grep -QQQ Knights FDU.txt) 1> FDUTeaneck.txt 2> FDUTeaneck.err  (This sends the first command to 1 and the second command to 2.
Send the output to nowhere: "^^^^above text before the redirect" 1>/dev/null 2>/dev/null
Or above^^ : >/dev/null 2>&1
///////////////////////////////////////////////////////////////////



Check if files are the same: cksum "first file" "second file"

Compile file: gcc ".c filename" -o "new filename"
Run compiled file located at current dir: ./"filename"
Run compiled file located at home dir: ~/"filename"
Show the return code of the file you ran: echo $?
Run file using input from a file: ./"codename" < "filenametogetinputfrom"  (The < means "get from". This means that run file and get input from the other file. > means go to.)

Check disc cpace (Disc free): df
Easy to read disc free: df -h  (-h means human readable)
Disc inode sapce: df -i   (i for inode)
Disc used: du
Disc used but check only a certain amount of directories: du -d "#"  (The number is how many directories deep from the current directory you want to check)
Sort du by alphabetical: du | sort
Sort du by numerial: du | sort -n   (n for numerical)
Sort by the coloumn: du | sort -k "#ofcoloumn"  (k for coloumn)

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Example of piping: IMPORTANT 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Sort file content: cat "filename" | sort
Above but no duplicates: cat "filename" | sort | uniq
Above but count how many duplicates there are: cat "filename" | sort | uniq -c  (c for count)
Above but sorts the duplicates: cat "filename" | sort | uniq -c | sort -n
Above but sort the other way: cat "filename" | sort | uniq -c | sort -nr  (nr for numberical reverse)

I can continue piping the above command to make something that I want.
I can add | wc -c, |sort -n, |uniq, etc, how many times I want to get the result I want.
This goes for EVERY command, this is EXTREMELY POWERFUL to work in unix.
wc by line : wc -l
wc by character: wc -c
wc by word: wc -w
grep: find something : grep "txt"
Show everything except for: grep -v "text"
Search for multiple things: egrep "text|text"
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Look at all files in directory, also in other directories in current dir: find .
Find files ending in something: find . | grep \"ending"$
Count files found: find . | grep \."ending"$ | wc -l    (wc for word count)
Find something: grep "~~~"


show file page by page: cat "filename" | more
show first part of file: head -4 lab1.c   (this is an example)
show last part of file: tail -"#oflines" "filename"

Important~~---~-~----~~~----~~~---
Show the bottom of the file as it's being written to: tail -f "filename"
Exit above command: ctrl+c
~~---~~---~-~~~~--~---~~~~~~~~~~~-



/////TAR AND ZIP///// [Always test your zips and tars (-t) being untarring)
Make tar file: tar -cvf "newdirDestitantion&newname" "dirOfFiles"
	Example of above: tar -cvf ~/zip/dropbox.zip ./*
Make zip from tar: gzip "tarName"

Unzip: unzip or gunzip "zipFile.tar.gz"
TEST untar: tar -tvf "tarName.tar"  (Be careful when the file starts with "/" and not a "."; A slash will put the file exactaly where it was previously, not the current location that the tar is in.
Untar: tar -xvf "tarName.tar"
/////////////////////////////////////////////////////////////

Show variables of current shell: set
Show global variables: env
Make variable: "VariableName"="variableContent"
Show variable: echo $"variableName
Make variable into global: export "variableName"
Above but make a variable: export "variableName"="variableContent"

Show shells: ps
Show all processes running: ps -ef
Make shell: bash
Exit current shell: exit

////////TRANSFER from turing to your pc and back ///////////
Use winSCP or:
In pc cmd, transfering files
From turing to pc: fallasaguec1@turing.cs.montclair.edu:~/"filename" .
From pc to turing: scp "filename" fallasaguec1@turing.cs.montclair.edu:~/"filename or new name"
/////////////////////////////////////////////////////////////////

To rule while loops in bash:

-While true
>do (IMPORTANT, to start)
>date
>sleep 5
>done (IMPORTATN, to end)
  etc.......
or

while true; do date; sleep 5; done >> timecapture.txt &  (the & runs in background, the >> redirects the output to the file).



Commands in background and forground::::

& : The & means to run the command/process in the background.
jobs : Check the commands running 
fg "job number": Move job in background to the forground.
bg "job number": Move job to background
Suspend job : ctrl+z
Continute job: bg "number"
Kill : ctrl+c
Kill from elsewhere: kill "pid"
Pause : ctrl+z

nohup ./"filename": No hangup, even if you close your turing session, the background commands will still keep running.

echo $? : Check exit status code; This is the the exit your program got to. Ex.. exit(3) = 3, exit(478) = 478, etc...
$$ : Pid of command you ran with it.
$0 : Name of program that ran with it.
echo $! : The last program that was put in the background.

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
cal,date, time

date : Show date
date "+%s" : Show the time since unix epoch time, since janurary 1 1970.
cal : Show calender
cal 07 2001 : Show the entered month and year
date -d"@#######" : Make the epoch number into the date.
date -d"03/15/2003 14:03" +"&s"  : Make the date and time into epoch/unix time.
date -d"3 days" : Show the date in three days. Can be replaced with month year.
date -d"4 months ago : Above but show the date ago.


Printing out literal lines:: The $ is a reserved symbol, Also for $1, *, etc...
echo give me $100
> give me 00

echo give me \$100
> give me $100

echo 'give me $100'  :  ' ' is a literal symbol. " " is a grouping symbol and makes it a single variable.
> give me $100

echo give me '$'100
> give me $100


Grave symbols``or```Back quotes```or```Back ticks (OLD, DONT use anymore, use next syntax)
This symbol is around a command.
HOSTNAME = `hostname` : The result of `hostname` will be put into HOSTNAME

NEW AND BETTER WAY:
SERVER = $(hostname)


ROOT User commands::~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

sudo : Stands for super user. Temperarly makes the current user have root privileges.
sudo su : Switch user into root.
su "user" : Switch user into entered user

Menmoic: Something that stands in for a value. (x in place instead of the actual password)
root id = 0

chgrp "user" "file" : Change the group privileges of a file to a different group.
chown "user" "file" : Change the owner of the file.
chown "user:group" "file" : Change both the owner and group of a file.

PRIVILEGE TYPE
File type|User(owner) privilege|Group privilege|Other privilege
     -            rwx                 rwx             rwx
-rwxrwxrwx : This is the privilege type for the users. Read, write, execute.
r=4; w=2; x=1
u is user; g is group; o is other

-rw-r--r-- 
user=6; group=4; other=4::::: This is a 644 file.

NEVER REMOVE READ AND EXECUTE PRIVELEGE FROM USER, YOU CAN'T GET THE FILE BACK

chmod u-w "filename" : Change privilege type of someone. Ex: g+w; go-wx; u-wx; etc..
chmod 664 "filename" : Above but using numbers. ex: 644; 722; etc...

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
A router never sounds out a broadcast.
DNS (Domain Name System) : A type of phonebook that has all the domains and it's assosiated ip adress.

ping "domain name or ip address": Will ping that adress and recieve infor about ttl and time and ip adress.
nslookup "domain name" : Shows the ip adress of the domain.
nslookup "ip address" : A reverse lookup that looks at the domain name.
set debug: While in nslookup, go into debug mode. Has more info, like ttl. ttl is seconds. Time To Live
Emphemeral port

CIDR: how many bits is assosited to the ip adress, 255.255.255.0/24, it's the /24.
ifconfig : Look at infomation about your network, ip, mac, netmask, etc...
arp -a : Look at the ip and mac address of local network
arp -d "ip adreess" : Delete ip adress and mac from the arp chart

208.216.181.15:80 ::: The last number is the port number 1- 1024 are reservred for well know ports.
This tells which application to send the data to. 80 is reservred for web server ports. 
These are not permanent, and a new port number gets open every time an application sends a request, such as a new google tab, and asking something on the tab.
These are also called sockets.

netstat: Look at what you're connected to
netstat -ant : Look at the only ports you're connect to. -t is only look at tcp. -n is makes the domain name into ip
netstat::: If the Recv-Q is not greater than 0, it cant keep up.
netstat::: The Send-Q 
netstat::: 0.0.0.0:* means it will accept any ip adrress and star* means any ephemeral port.

ssh "ip" : Connect to that ip address
curl "domain name or ip" : Get html of that page. Screen scraping.

tcpdump: listen and show all packets being send to you
tcpdump port 22: Listen to things coming from port 22. 

LAB 8:::
./server 38299
./client turing.cs.montclair.edu 38299


dos2unix * : Converts all the dos files in your directory to unix files.

awk '/Sharon/' datafile: Prints any line that has Sharon in the file datafile
awk '/Sharon/ {print $1, $2}' datafile : Prints above, but only the first and second field
comma, is the field sepreator.
The filed sepreator is WHITE SPACE.

awk '$8>9' datafile: Prints out all the lines that the field 8 have a number greater than 9

OFS - Output field sepreater
FS - Input field sepreater
????????????
awk -F'[|]' '{print $1,$4}' datebook | awk '{print $3}'| awk -F'[/]' '{print $1}'

GOOD AWK TOPICS TO STUDY:::
special for loop
if-then-else in awk
OFS
BEGIN and END

sed -n '1, 4p' datebook - print out, without repeating, lines 1 to 4. $p is end of file
sed -n '/^Zippy/, /^Popeye/p' databook - Print the lines from Zippy to Popeye
sed '/Pinhead/d' datebook - Print everything put delete lines with Pinhead

sed -i '/Pinhead/d' datebook - In place editing. Acutally edit the file is -i.

sed 's/|/:/' datebook - Subsitutue (the first s), the first "|" by ":".
sed 's/|/:/g' datebook - Subsitutue (the first s), all (the g means global) "|" by ":".