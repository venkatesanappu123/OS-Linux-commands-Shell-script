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
![Screenshot 2025-03-24 090253](https://github.com/user-attachments/assets/61faabae-c3ff-4a47-9270-2a0a5163fc49)

cat < file2
## OUTPUT
![Screenshot 2025-03-24 090307](https://github.com/user-attachments/assets/41625b67-a462-4537-9980-91156dc57ee2)
# Comparing Files

cmp file1 file2
## OUTPUT
![Screenshot 2025-03-24 090516](https://github.com/user-attachments/assets/25a3de27-e425-4b26-b14c-65a8cc919c70)

comm file1 file2
 ## OUTPUT
![Screenshot 2025-03-24 090621](https://github.com/user-attachments/assets/3addcf3c-ae2a-4ec5-a32a-6cebf364a9b0)

diff file1 file2
## OUTPUT

![Screenshot 2025-03-24 090735](https://github.com/user-attachments/assets/b1bdb900-4acc-4c7d-abef-9706c75f33ad)

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

![Screenshot 2025-03-24 091157](https://github.com/user-attachments/assets/a165e9c6-bb02-432a-8627-8008d14004ba)



cut -d "|" -f 1 file22
## OUTPUT

![Screenshot 2025-03-24 091345](https://github.com/user-attachments/assets/1ea1e32c-8c50-4e46-b1b0-ed4342a567a7)



cut -d "|" -f 2 file22
## OUTPUT

![Screenshot 2025-03-24 091429](https://github.com/user-attachments/assets/24b9bad5-9549-4843-9c7b-f9f7cb82c14c)

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

![Screenshot 2025-03-24 092337](https://github.com/user-attachments/assets/f3c5585a-fa48-406c-8779-060d8e91c9d6)


grep hello newfile 
## OUTPUT

![Screenshot 2025-03-24 092427](https://github.com/user-attachments/assets/c9ad6276-0d25-4a99-827e-d790fe81e86c)



grep -v hello newfile 
## OUTPUT

![Screenshot 2025-03-24 092525](https://github.com/user-attachments/assets/c7fcefb1-7db5-4733-bf30-a005e2fbdc11)


cat newfile | grep -i "hello"
## OUTPUT

![Screenshot 2025-03-24 092611](https://github.com/user-attachments/assets/d1558c95-9bdf-4e24-906a-06d5ca656b70)



cat newfile | grep -i -c "hello"
## OUTPUT

![Screenshot 2025-03-24 092700](https://github.com/user-attachments/assets/d95610bb-5376-4b66-a110-fc29a93e8b35)


grep -R ubuntu /etc
## OUTPUT


![Screenshot 2025-03-24 092938](https://github.com/user-attachments/assets/84458767-f5e9-4a39-b8d2-d0149028c96d)


grep -w -n world newfile   
## OUTPUT

![Screenshot 2025-03-24 093037](https://github.com/user-attachments/assets/2e92a618-dd03-4c66-921e-83198ee5fb6c)


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

![Screenshot 2025-03-24 094541](https://github.com/user-attachments/assets/6242b4df-686c-4f83-a82c-5574e9b1a405)



egrep -w '(H|h)ello' newfile 
## OUTPUT

![Screenshot 2025-03-24 094633](https://github.com/user-attachments/assets/154e8f56-f313-485e-93e3-1a6576383add)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![Screenshot 2025-03-24 094723](https://github.com/user-attachments/assets/38f4f296-ef36-4661-9cca-359b9bbc25fa)



egrep '(^hello)' newfile 
## OUTPUT

![Screenshot 2025-03-24 094755](https://github.com/user-attachments/assets/69d14737-9cd7-4d41-bfe3-3bdc6a4e89a0)


egrep '(world$)' newfile 
## OUTPUT

![Screenshot 2025-03-24 094850](https://github.com/user-attachments/assets/a356a64b-3d9b-4f41-9deb-4908e5e65cd7)



egrep '(World$)' newfile 
## OUTPUT


![Screenshot 2025-03-24 094923](https://github.com/user-attachments/assets/17aae12c-13d0-4e2f-ac76-ae8ef43b04d1)



egrep '((W|w)orld$)' newfile 
## OUTPUT

![Screenshot 2025-03-24 095026](https://github.com/user-attachments/assets/f391dc63-e918-4fe0-9d60-013a56bc692f)



egrep '[1-9]' newfile 
## OUTPUT

![Screenshot 2025-03-24 095055](https://github.com/user-attachments/assets/271c2fc0-8757-48be-95f7-e822cce258c9)


egrep 'Linux.*world' newfile 
## OUTPUT

![Screenshot 2025-03-24 095130](https://github.com/user-attachments/assets/4775db24-6c03-4063-9206-953e8244e6a1)

egrep 'Linux.*World' newfile 
## OUTPUT

![Screenshot 2025-03-24 095222](https://github.com/user-attachments/assets/dd71cc3c-7233-493d-8a62-a1721f5e372b)


egrep l{2} newfile
## OUTPUT

![Screenshot 2025-03-24 095251](https://github.com/user-attachments/assets/60044efb-3deb-4b22-aed5-7b71aae448dc)


egrep 's{1,2}' newfile
## OUTPUT 

![Screenshot 2025-03-24 095328](https://github.com/user-attachments/assets/d40c057b-121a-4516-8162-c901fd68ada4)


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
```


sed -n -e '3p' file23
## OUTPUT
![Screenshot 2025-04-07 083534](https://github.com/user-attachments/assets/406e9ce5-5ba8-47ed-b99f-03220fb3ab1e)



sed -n -e '$p' file23
## OUTPUT
![Screenshot 2025-04-07 083633](https://github.com/user-attachments/assets/c8598db1-61b8-413e-b5e7-2a9fc36b067b)




sed  -e 's/Ram/Sita/' file23
## OUTPUT
![Screenshot 2025-04-07 083809](https://github.com/user-attachments/assets/d9e3808b-da58-4301-8675-d34e93e889a3)




sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![Screenshot 2025-04-07 084016](https://github.com/user-attachments/assets/e382e631-5b3e-433c-9c27-aa2a9b171eed)




sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Screenshot 2025-04-07 084358](https://github.com/user-attachments/assets/a2cb395c-73ce-4bfe-810c-f04b54382698)



sed -n -e '1,5p' file23
## OUTPUT
![Screenshot 2025-04-07 084719](https://github.com/user-attachments/assets/5ae6361b-5d11-4828-80a9-97c489103a67)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![Screenshot 2025-04-07 085032](https://github.com/user-attachments/assets/91362ef1-bab3-4bbe-862a-38c9b4afa16f)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![Screenshot 2025-04-07 085349](https://github.com/user-attachments/assets/33f31b9b-13e5-4e83-8bd8-2ddeb5e88e5e)




seq 10 
## OUTPUT
![Screenshot 2025-04-07 085435](https://github.com/user-attachments/assets/7405e6aa-2cb2-4c37-83b3-63ebb25fc187)



seq 10 | sed -n '4,6p'
## OUTPUT
![Screenshot 2025-04-07 085543](https://github.com/user-attachments/assets/b8381808-0889-43c2-a547-b8e78aede636)



seq 10 | sed -n '2,~4p'
## OUTPUT
![Screenshot 2025-04-07 085856](https://github.com/user-attachments/assets/56d217c9-71c0-4a90-807a-cecd71a4ea26)



seq 3 | sed '2a hello'
## OUTPUT
![Screenshot 2025-04-07 090030](https://github.com/user-attachments/assets/da0c093f-f9cf-4096-8516-59227b031004)



seq 2 | sed '2i hello'
## OUTPUT
![Screenshot 2025-04-07 090138](https://github.com/user-attachments/assets/b61f97d1-9397-478c-b481-d1d10b1e8f84)



seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot 2025-04-07 090405](https://github.com/user-attachments/assets/15a2aeb8-7665-463c-8994-a40b3451a58b)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![Screenshot 2025-04-07 090529](https://github.com/user-attachments/assets/12b3d37d-03a0-412a-aab6-e1497e86536a)



sed -n '2,4{s/$/*/;p}' file23
![Screenshot 2025-04-07 090925](https://github.com/user-attachments/assets/6c64c8d2-63e1-4c5a-886c-a12e0c575448)


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
![Screenshot 2025-04-07 091340](https://github.com/user-attachments/assets/c57f5c47-ef51-4843-9fc2-142b55e1601a)


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
![Screenshot 2025-04-07 092013](https://github.com/user-attachments/assets/0bc4ac82-73c8-4642-8e38-4992c3f47d10)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Screenshot 2025-04-07 092607](https://github.com/user-attachments/assets/2be721a1-90ab-4f0a-b4be-f6e16ab298b1)

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
![Screenshot 2025-04-07 093021](https://github.com/user-attachments/assets/f7f7b053-379f-4afa-8910-a592b3fc5b6c)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



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
