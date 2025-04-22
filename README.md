
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
![Screenshot from 2025-04-12 13-52-39](https://github.com/user-attachments/assets/7c6da32d-ef0b-4934-90a0-0ed9ef18667c)


cat < file2
## OUTPUT
![Screenshot from 2025-04-12 13-54-41](https://github.com/user-attachments/assets/2e51ec7b-1bdf-44dc-a783-5f11c351051c)

	


# Comparing Files
cmp file1 file2
## OUTPUT
![Screenshot from 2025-04-16 13-54-08](https://github.com/user-attachments/assets/fc75319a-dd0c-45ad-b772-b99d18aefdf4)


 
comm file1 file2
 ## OUTPUT
 ![Screenshot from 2025-04-16 13-54-44](https://github.com/user-attachments/assets/1c267c69-60a3-4d5e-aebf-98a514f3474a)


	

 
diff file1 file2
## OUTPUT

![Screenshot from 2025-04-16 13-55-45](https://github.com/user-attachments/assets/d2603ba3-7c6d-4056-bbc6-4af4c28568a0)




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


cut -c1-3 file22
## OUTPUT
![Screenshot from 2025-04-16 13-58-07](https://github.com/user-attachments/assets/b054d058-fb8b-4b84-bd06-7da3f171e373)

	


cut -d "|" -f 1 file22
## OUTPUT
![Screenshot from 2025-04-16 13-58-36](https://github.com/user-attachments/assets/306bc0e4-9f77-4695-9efb-0dd929527209)

	

cut -d "|" -f 2 file22
## OUTPUT
![Screenshot from 2025-04-16 13-59-12](https://github.com/user-attachments/assets/1551ddfb-7f92-415b-95a7-4fc5ec9360f8)

	

cat > newfile 
```
Hello world
hello world
^d
````
cat < newfile 
Hello world
hello world
 
grep Hello newfile
## OUTPUT
![Screenshot from 2025-04-16 14-04-42](https://github.com/user-attachments/assets/2b6e9277-7402-40a7-932b-aef9b757f4ff)

	

grep hello newfile
## OUTPUT
![Screenshot from 2025-04-16 14-05-04](https://github.com/user-attachments/assets/9321c36e-3b2f-4121-9c11-61d57fe78a1d)



grep -v hello newfile 
## OUTPUT
![Screenshot from 2025-04-16 14-05-28](https://github.com/user-attachments/assets/08f643ab-49a8-4581-95d4-abcce2698d09)

	


cat newfile | grep -i "hello"
## OUTPUT

![Screenshot from 2025-04-16 14-05-53](https://github.com/user-attachments/assets/d3f2414e-38aa-4b39-b1c8-8e8ffb55e74c)



cat newfile | grep -i -c "hello"
## OUTPUT
![Screenshot from 2025-04-16 14-06-25](https://github.com/user-attachments/assets/82292861-50fa-49c9-a7c6-612c58768761)

	


grep -R ubuntu /etc
## OUTPUT
![Screenshot from 2025-04-16 14-07-48](https://github.com/user-attachments/assets/9f13b10d-8825-4c1e-8dee-7393b2b4a959)


grep -w -n world newfile   
## OUTPUT
![Screenshot from 2025-04-16 14-08-24](https://github.com/user-attachments/assets/e2d1e731-b7f9-484e-a63f-18454058e1dc)

	

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
![Screenshot from 2025-04-16 14-09-12](https://github.com/user-attachments/assets/88b16e75-97fd-4fd9-ab41-983b97a5aead)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![Screenshot from 2025-04-16 14-09-33](https://github.com/user-attachments/assets/c429b507-c47a-4b73-a9cb-d9de60009eb5)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![Screenshot from 2025-04-16 14-09-57](https://github.com/user-attachments/assets/b5358100-1848-4b9d-88e4-2c1bac1534f6)




egrep '(^hello)' newfile 
## OUTPUT
![Screenshot from 2025-04-16 14-10-16](https://github.com/user-attachments/assets/c2200081-908f-40c3-9bfa-1676de5f3a71)



egrep '(world$)' newfile 
## OUTPUT
![Screenshot from 2025-04-16 14-10-36](https://github.com/user-attachments/assets/da86f15d-f49f-43b6-add3-0850dc638e60)



egrep '(World$)' newfile 
## OUTPUT
![Screenshot from 2025-04-16 14-10-56](https://github.com/user-attachments/assets/5c73c697-d1d7-4342-b447-9ec171f3dedd)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![Screenshot from 2025-04-16 14-11-20](https://github.com/user-attachments/assets/c1fd8b3e-8140-4ee9-8be8-6a9ffa0f466d)



egrep '[1-9]' newfile 
## OUTPUT
![Screenshot from 2025-04-16 14-11-47](https://github.com/user-attachments/assets/efce97e1-bb71-43ba-ae9d-ebdaf1c21104)



egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot from 2025-04-16 14-12-06](https://github.com/user-attachments/assets/e9032c76-4cac-447c-97d7-794054d68da8)


egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot from 2025-04-16 14-12-30](https://github.com/user-attachments/assets/a466e184-a4d3-46b7-8e72-7ca52a05d93e)


egrep l{2} newfile
## OUTPUT
![Screenshot from 2025-04-16 14-12-50](https://github.com/user-attachments/assets/b88cc0f7-b6c4-4789-9b99-fabe996cf6ed)



egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot from 2025-04-16 14-13-10](https://github.com/user-attachments/assets/ad734437-f47c-4ef4-8ecc-c51f31d0fcb1)


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
![Screenshot from 2025-04-16 14-14-00](https://github.com/user-attachments/assets/83ad914a-dd67-4fe2-8b46-0fd8e2570677)



sed -n -e '$p' file23
## OUTPUT
![Screenshot from 2025-04-16 14-14-21](https://github.com/user-attachments/assets/e8f706e5-8d2e-493b-bbcf-d0a95e52578a)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2025-04-16 14-14-40](https://github.com/user-attachments/assets/47ff459b-f17a-4cbd-bf49-dc15bd5a8e3c)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2025-04-16 14-14-58](https://github.com/user-attachments/assets/b4b309da-9627-4a21-9655-89dbaf26ab49)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Screenshot from 2025-04-16 14-15-19](https://github.com/user-attachments/assets/3e8088cc-7c41-444a-bc8e-2080397613c1)



sed -n -e '1,5p' file23
## OUTPUT
![Screenshot from 2025-04-16 14-15-39](https://github.com/user-attachments/assets/126b9548-440c-4667-862e-b42f6f7ab30f)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![Screenshot from 2025-04-16 14-15-57](https://github.com/user-attachments/assets/c52f2fc4-def2-4913-824c-d7e61e2beb49)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![Screenshot from 2025-04-16 14-16-15](https://github.com/user-attachments/assets/8de26e41-b51e-406f-9bf3-72c86852cad1)



seq 10 
## OUTPUT
![Screenshot from 2025-04-16 14-16-33](https://github.com/user-attachments/assets/a5989b39-86c0-4eea-b4e2-886b6f4ec172)



seq 10 | sed -n '4,6p'
## OUTPUT
![Screenshot from 2025-04-16 14-16-50](https://github.com/user-attachments/assets/d2bf894d-0d90-4d93-a595-494a3df070b9)



seq 10 | sed -n '2,~4p'
## OUTPUT
![Screenshot from 2025-04-16 14-21-14](https://github.com/user-attachments/assets/c151241a-3c93-4aaf-ad4d-3f6ef09ddc44)



seq 3 | sed '2a hello'
## OUTPUT
![Screenshot from 2025-04-16 14-21-34](https://github.com/user-attachments/assets/301a95b5-64a3-428f-a407-3fa9c149d2b8)



seq 2 | sed '2i hello'
## OUTPUT
![Screenshot from 2025-04-16 14-21-54](https://github.com/user-attachments/assets/cb4498db-4a57-4bbc-9fb7-afb824cbd8ca)


seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot from 2025-04-16 14-22-20](https://github.com/user-attachments/assets/7d2a10c3-d366-476a-a1ef-c7ba1d781787)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![Screenshot from 2025-04-16 14-22-40](https://github.com/user-attachments/assets/c4641a84-b93a-4083-b40b-787280d78b05)



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![Screenshot from 2025-04-16 14-22-57](https://github.com/user-attachments/assets/201b357f-58ac-4717-8028-d8848dd16c65)


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
![Screenshot from 2025-04-16 14-23-57](https://github.com/user-attachments/assets/c164d304-c849-413e-800b-08907a30b15c)


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
![Screenshot from 2025-04-16 14-24-36](https://github.com/user-attachments/assets/6c99dc60-6382-48ac-8170-a819b68a673f)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT 
 ![Screenshot from 2025-04-16 14-25-01](https://github.com/user-attachments/assets/cd106e4d-5063-4aa9-824d-d4f03c660190)


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
![Screenshot from 2025-04-16 14-26-13](https://github.com/user-attachments/assets/c432a42d-076c-42ea-ae40-211e178f5a6a)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![Screenshot from 2025-04-16 14-26-31](https://github.com/user-attachments/assets/8f005f4e-e38d-4a13-8e36-ce5306eb9330)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![Screenshot from 2025-04-16 14-27-48](https://github.com/user-attachments/assets/64c4ee80-6d30-4fd9-8276-06bf00c94f78)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
tar -xvf backup.tar
## OUTPUT
![alt text](<Screenshot from 2025-04-17 13-47-40.png>)

gzip backup.tar

ls .gz
## OUTPUT
![alt text](<Screenshot from 2025-04-17 13-49-37.png>)
 
gunzip backup.tar.gz

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![Screenshot from 2025-04-16 14-32-29](https://github.com/user-attachments/assets/9a1bdfd0-1900-4ecd-98b5-70fc0f731ec5)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![Screenshot from 2025-04-16 14-33-17](https://github.com/user-attachments/assets/c182ec01-d7d8-4eec-99c8-d87944e209ee)


cat>scriptest.sh 
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
![Screenshot from 2025-04-16 14-34-43](https://github.com/user-attachments/assets/60b9f873-e688-482e-8107-3ea69925bc36)

 
ls file1
## OUTPUT
![Screenshot from 2025-04-16 14-35-04](https://github.com/user-attachments/assets/098c2d28-6e8e-476d-a043-660db3e267c9)

echo $?
## OUTPUT 
![Screenshot from 2025-04-16 14-35-22](https://github.com/user-attachments/assets/9561078f-c9db-4165-a8d1-ac3dfc8223a5)



 
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
![Screenshot from 2025-04-16 14-40-45](https://github.com/user-attachments/assets/e4d1765e-32cc-4912-8978-1b4dbfdd4d6c)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![Screenshot from 2025-04-16 14-41-16](https://github.com/user-attachments/assets/251dfe19-ca51-49af-8f16-40b96a8927cb)


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
![Screenshot from 2025-04-16 14-43-01](https://github.com/user-attachments/assets/3a2dd276-414a-40e1-abac-b386f4dfee4b)


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
![Screenshot from 2025-04-16 14-48-21](https://github.com/user-attachments/assets/e5568804-02d8-4c2e-bcb6-03799190e02e)



# using numeric test comparisons
cat > iftest.sh 
```bash
#!/bin/bash
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
## OUTPUT
![Screenshot from 2025-04-16 14-49-22](https://github.com/user-attachments/assets/d1366212-4c66-426a-83f5-32e977c5b86d)


# check if a file
cat > ifnested.sh 
```bash
#!/bin/bash
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
## OUTPUT
![Screenshot from 2025-04-16 14-50-53](https://github.com/user-attachments/assets/c047a06b-c944-4396-91e5-d9361bca4c47)

# looking for a possible value using elif
cat elifcheck.sh 
```bash
#!/bin/bash
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
![Screenshot from 2025-04-16 14-51-59](https://github.com/user-attachments/assets/3f0f7c06-797e-4b8c-ad11-613240bd85ba)


# testing compound comparisons
cat> ifcompound.sh 
```bash
#!/bin/bash
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
![Screenshot from 2025-04-16 14-52-53](https://github.com/user-attachments/assets/0d7a7599-a4d4-4ec8-b78a-cf0204651830)

# using the case command
cat >casecheck.sh 
```bash
#!/bin/bash
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
## OUTPUT 
 ![Screenshot from 2025-04-16 14-53-59](https://github.com/user-attachments/assets/c0f59447-37d8-4154-a633-b697e468a5b6)

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
## OUTPUT

![Screenshot from 2025-04-16 14-54-56](https://github.com/user-attachments/assets/5526dd92-8d29-403a-b796-0302a9fa17d4)

 
cat untiltest.sh 
```bash
\#using the until command
#!/bin/bash
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh

## OUTPUT 
 ![Screenshot from 2025-04-16 14-56-03](https://github.com/user-attachments/assets/e40c70b7-da06-4d90-8f94-09adadf586b7)

 
 
cat forin1.sh 
```bash
#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh

## OUTPUT
![Screenshot from 2025-04-16 14-57-04](https://github.com/user-attachments/assets/6b538fef-a725-4a0c-8449-d0adcd304861)

 
cat forin2.sh 
```bash
#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh

## OUTPUT
![Screenshot from 2025-04-16 14-58-16](https://github.com/user-attachments/assets/087fb2cf-dc58-4673-8317-e5db45d7b133)

 
 
cat forin3.sh 
```bash
#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
## OUTPUT
![Screenshot from 2025-04-16 14-59-38](https://github.com/user-attachments/assets/955f2f47-4a46-4fc8-a3b3-c93e948571a8)


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
![alt text](<Screenshot from 2025-04-17 13-02-49.png>)

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

![alt text](<Screenshot from 2025-04-17 13-07-46.png>)

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
![alt text](<Screenshot from 2025-04-17 13-08-49.png>)

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
![alt text](<Screenshot from 2025-04-17 13-09-48.png>)
 
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
![alt text](<Screenshot from 2025-04-17 13-11-15.png>)

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forcontinue.sh 
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
![alt text](<Screenshot from 2025-04-17 13-13-57.png>)

 
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
![alt text](<Screenshot from 2025-04-17 13-15-10.png>)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![alt text](<Screenshot from 2025-04-17 13-16-12.png>)


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
![alt text](<Screenshot from 2025-04-17 13-17-30.png>)
 
 ./funcex.sh 1 2
![alt text](<Screenshot from 2025-04-17 13-18-03.png>)
 
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
![alt text](<Screenshot from 2025-04-17 13-19-12.png>)
 
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
 ![alt text](<Screenshot from 2025-04-17 13-25-50.png>)
 
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
![alt text](<Screenshot from 2025-04-17 13-30-07.png>)
 
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
![alt text](<Screenshot from 2025-04-17 13-34-33.png>)

# RESULT:
The Commands are executed successfully.
