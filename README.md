# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT

<img width="186" alt="os 1" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/cabbbbf8-edbc-423f-b2fd-9b554ebcb6fb">


cat < file2
## OUTPUT
<img width="158" alt="os 2" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/ddfac777-1c3b-4f3d-a7a7-d340013f7bfc">


# Comparing Files
cmp file1 file2
## OUTPUT


comm file1 file2
 ## OUTPUT
<img width="114" alt="os 3" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/8e2fb210-00d5-4cfa-a247-3daf4d43e665">

 
diff file1 file2
## OUTPUT
<img width="356" alt="os4" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/bc967684-feda-415f-acc9-63475c7ada5b">


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT

<img width="113" alt="os 5" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/05a637c2-3fa5-4e99-8c2b-0754383606d9">



cut -d "|" -f 1 file22
## OUTPUT

<img width="155" alt="os 6,7,8" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/99c14dd1-d293-48d4-88d5-5f58a0dfecdc">


cut -d "|" -f 2 file22
## OUTPUT

<img width="155" alt="os 6,7,8" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/58574bf5-65cc-4c1b-b0ae-b5bd2f50c2f3">

cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT

<img width="140" alt="os 9" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/b65f5c56-9fad-4ac3-973d-e5dae9290ee4">


grep hello newfile 
## OUTPUT

<img width="616" alt="os 10,11,12,13,14" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/988232cc-e5f7-446e-8435-4fe40ce64cba">

grep -v hello newfile 
## OUTPUT

<img width="616" alt="os 10,11,12,13,14" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/988232cc-e5f7-446e-8435-4fe40ce64cba">

cat newfile | grep -i "hello"
## OUTPUT




cat newfile | grep -i -c "hello"
## OUTPUT




grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="187" alt="17" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/bbe880e2-1417-4b4d-90c6-8e1a3ec93ff3">



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="184" alt="18" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/05883e8f-e378-4113-afb4-f417046ec28e">



egrep '(^hello)' newfile 
## OUTPUT

<img width="143" alt="19" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/45fdeb70-c1ad-4c81-921f-2f9a565d2f7d">


egrep '(world$)' newfile 
## OUTPUT

<img width="140" alt="20" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/d38f1eed-72c1-4b2d-89be-a60982cd4297">


egrep '(World$)' newfile 
## OUTPUT
<img width="140" alt="21" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/cbd6a237-2899-4c0a-be69-207b33a320b7">


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="173" alt="22" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/b9efc4c6-a492-4117-8444-9cbe0ee9a7d3">



egrep '[1-9]' newfile 
## OUTPUT

<img width="131" alt="23" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/0e282f25-ab75-49dd-98ee-0a567a592385">


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="134" alt="24" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/a606278c-2758-4bfa-90d0-2ef403b1b78f">


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="144" alt="25" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/a51f6e88-5fff-49cb-b7ca-175e33eb3857">

egrep l{2} newfile
## OUTPUT

<img width="109" alt="26" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/30aa7a3d-ac7c-45ae-9c87-00a5c4b2402e">


egrep 's{1,2}' newfile
## OUTPUT 
<img width="133" alt="27" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/f6866b3e-ba6e-44cd-a39b-ecd51f0b6946">


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT



sed -n -e '$p' file23
## OUTPUT



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="185" alt="29" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/37bfe2d1-d9dd-4ebc-bdf2-b81f539e3029">


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="217" alt="30" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/1832cf84-5ecd-41dd-ad45-9c3ea0ff843d">



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="178" alt="31" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/de3bc4a3-de17-4c35-b82d-17cd7da8836e">


sed -n -e '1,5p' file23
## OUTPUT

<img width="158" alt="32" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/0eb0aba7-4fba-4f76-906a-f91e67d47656">


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="149" alt="33" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/0e5b828b-2170-4a07-89f2-203d0f667a42">



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


<img width="152" alt="34" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/47fa830f-601c-4557-98dd-a52c23a1b14e">

seq 10 
## OUTPUT

<img width="117" alt="35" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/46e4c01d-8936-487e-bc80-e06cd97e6b52">


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="115" alt="36" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/d361f670-4ff3-472b-aeb6-f2cb591c0a01">


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="133" alt="37" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/4ce1fb02-75b2-43b0-aca2-4de7e4c000ad">


seq 3 | sed '2a hello'
## OUTPUT

<img width="125" alt="38" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/d989ba89-8a57-4582-916a-1024cc840fea">


seq 2 | sed '2i hello'
## OUTPUT
<img width="130" alt="39" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/709ba924-945c-4d01-b334-102079425b13">


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="155" alt="40" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/6ec608b6-ea07-4ac2-9bfd-bbdd47d9c9a8">


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="179" alt="41" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/c6db5c63-3df1-495c-93e0-3e3fc1aea7bc">


sed -n '2,4{s/$/*/;p}' file23


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT

<img width="150" alt="42" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/a16d83f9-782e-4369-a337-99028f610eec">


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="170" alt="43" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/bc56461f-9ef1-4505-a8ef-3ab45d748607">

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT

<img width="153" alt="44" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/ad598f93-72b5-4937-a876-7277c7a6df80">

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="227" alt="45" src="https://github.com/NaveenKumarV2005/OS-Linux-commands-Shell-script/assets/151476286/71ad6809-a838-4034-8ec0-59a837150757">


#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT

# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT



# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT


# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT

# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 
cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 
 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 
 
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 
cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 

 
 ./funcex.sh 1 2

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
 
 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
 
cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 


# RESULT:
The Commands are executed successfully.
