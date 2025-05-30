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
![Screenshot from 2025-05-27 10-08-43](https://github.com/user-attachments/assets/263b1251-05b3-4f70-8438-d83453aa4a6a)



cat < file2
## OUTPUT
![Screenshot from 2025-05-27 10-09-51](https://github.com/user-attachments/assets/e717d76d-38b5-4873-bf2f-b79f266776fd)



# Comparing Files
cmp file1 file2
## OUTPUT
 ![Screenshot from 2025-05-27 10-10-16](https://github.com/user-attachments/assets/c8712b92-779d-4a5d-a224-da2f68f959f7)

comm file1 file2
 ## OUTPUT
![Screenshot from 2025-05-27 10-15-18](https://github.com/user-attachments/assets/20b9fd11-b42f-4d20-ac4c-05a2eeb4018d)

 
diff file1 file2
## OUTPUT

![Screenshot from 2025-05-27 10-48-51](https://github.com/user-attachments/assets/ecb41e25-2c10-4377-9864-b684764d74a8)



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

![Screenshot from 2025-05-27 10-56-16](https://github.com/user-attachments/assets/adf22e1b-5fca-4f7b-86d6-8dcbc1b1f3e9)




cut -d "|" -f 1 file22
## OUTPUT

![Screenshot from 2025-05-27 10-56-28](https://github.com/user-attachments/assets/7118e45c-4999-4870-a4d2-fcc5120a3d64)



cut -d "|" -f 2 file22
## OUTPUT

![Screenshot from 2025-05-27 10-56-35](https://github.com/user-attachments/assets/e3a4a494-b033-46cd-ab4a-a4d19583122b)


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

![Screenshot from 2025-05-27 11-10-59](https://github.com/user-attachments/assets/427fa46d-05a7-4a22-899a-b5fe628986bb)



grep hello newfile 
## OUTPUT

![Screenshot from 2025-05-27 11-11-45](https://github.com/user-attachments/assets/ecd601c9-5596-49b2-864f-8dffbb52bd78)




grep -v hello newfile 
## OUTPUT


![Screenshot from 2025-05-27 11-11-49](https://github.com/user-attachments/assets/5ec33602-bd5a-4296-9345-f185bb9d11db)


cat newfile | grep -i "hello"
## OUTPUT

![Screenshot from 2025-05-27 11-11-57](https://github.com/user-attachments/assets/222ce81b-1066-4c55-a771-f6e7940fb4ad)




cat newfile | grep -i -c "hello"
## OUTPUT

![Screenshot from 2025-05-27 11-12-05](https://github.com/user-attachments/assets/034a20d2-4d0e-44d2-893c-534d69ebdb17)




grep -R ubuntu /etc
## OUTPUT

![Screenshot from 2025-05-27 11-13-09](https://github.com/user-attachments/assets/426c2245-58da-4b3a-8899-40303e49ef4f)



grep -w -n world newfile   
## OUTPUT

![Screenshot from 2025-05-27 11-14-14](https://github.com/user-attachments/assets/397f5b81-5695-4e13-8fc5-b37398ff868e)


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


![Screenshot from 2025-05-27 11-15-55](https://github.com/user-attachments/assets/380c5173-90b5-407c-a10c-8b6a57cd11f8)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![Screenshot from 2025-05-27 11-16-08](https://github.com/user-attachments/assets/3de42034-adcd-4983-bbaf-835ef4016cb5)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![Screenshot from 2025-05-27 11-16-53](https://github.com/user-attachments/assets/adfaecd5-aadc-4b10-81f8-d327b52718e4)




egrep '(^hello)' newfile 
## OUTPUT

![Screenshot from 2025-05-27 11-17-14](https://github.com/user-attachments/assets/fdc222a3-9381-480f-a22a-964a67504408)



egrep '(world$)' newfile 
## OUTPUT

![Screenshot from 2025-05-27 11-18-09](https://github.com/user-attachments/assets/c79da18f-a10d-4b7d-b902-fafdb6b8e95d)



egrep '(World$)' newfile 
## OUTPUT

![Screenshot from 2025-05-27 11-18-29](https://github.com/user-attachments/assets/188cb8d3-41c4-495a-8fcf-5ea96c032897)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![Screenshot from 2025-05-27 11-18-44](https://github.com/user-attachments/assets/c6f6c378-b21e-4d9e-ba0a-fd18d07c37f0)



egrep '[1-9]' newfile 
## OUTPUT

![Screenshot from 2025-05-27 11-19-00](https://github.com/user-attachments/assets/96ee6890-9d31-41bf-bdf4-be8ffc6380e7)



egrep 'Linux.*world' newfile 
## OUTPUT

![Screenshot from 2025-05-27 11-19-17](https://github.com/user-attachments/assets/e801a103-8920-48b6-9d53-5ee5b252df3c)


egrep 'Linux.*World' newfile 
## OUTPUT

![Screenshot from 2025-05-27 11-19-27](https://github.com/user-attachments/assets/4257d131-7495-4c4d-a756-42d9321ca7ca)


egrep l{2} newfile
## OUTPUT

![Screenshot from 2025-05-27 11-19-48](https://github.com/user-attachments/assets/3ae58761-3ac1-4b23-92f9-ca71cb7a1115)



egrep 's{1,2}' newfile
## OUTPUT 

![Screenshot from 2025-05-27 11-20-50](https://github.com/user-attachments/assets/5dd8a0ce-f60d-4826-ba2b-d1f87066494c)


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


![Screenshot from 2025-05-27 11-22-01](https://github.com/user-attachments/assets/3edb3b53-91c9-4f01-9a10-750c7616ba56)


sed -n -e '$p' file23
## OUTPUT

![Screenshot from 2025-05-27 11-22-12](https://github.com/user-attachments/assets/b7ad013a-8a95-4fb4-9814-9d32bcb56fbc)



sed  -e 's/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2025-05-27 11-22-32](https://github.com/user-attachments/assets/206231f2-efb9-4a23-911e-47443b435c0d)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![Screenshot from 2025-05-27 11-22-46](https://github.com/user-attachments/assets/6fdbf901-4621-40e2-bf35-37bc2017bfa9)



sed  '/tom/s/5000/6000/' file23
## OUTPUT

![Screenshot from 2025-05-27 11-22-58](https://github.com/user-attachments/assets/11b89339-e48b-47cf-909b-21995f7ae9ec)



sed -n -e '1,5p' file23
## OUTPUT


![Screenshot from 2025-05-27 11-23-15](https://github.com/user-attachments/assets/43f1a72c-7eef-455f-8a02-2b6ace08cf79)


sed -n -e '2,/Joe/p' file23
## OUTPUT


![Screenshot from 2025-05-27 11-23-33](https://github.com/user-attachments/assets/cf2caeed-4dc1-45db-ba0c-0ad289f94d3e)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![Screenshot from 2025-05-27 11-23-49](https://github.com/user-attachments/assets/2110f342-49a1-4642-82c5-10e20e8e57ce)



seq 10 
## OUTPUT

![Screenshot from 2025-05-27 11-24-08](https://github.com/user-attachments/assets/3486ea5e-053a-4697-9b6c-97f27dde4bad)



seq 10 | sed -n '4,6p'
## OUTPUT

![Screenshot from 2025-05-27 11-24-21](https://github.com/user-attachments/assets/eb80eca0-4b0b-42aa-9492-e7a2b1f6d743)



seq 10 | sed -n '2,~4p'
## OUTPUT


![Screenshot from 2025-05-27 11-24-34](https://github.com/user-attachments/assets/1b91e6d0-ff7e-4f87-b8b6-bae378c8427d)


seq 3 | sed '2a hello'
## OUTPUT

![Screenshot from 2025-05-27 11-24-49](https://github.com/user-attachments/assets/7809ae73-85e7-483f-beb1-54f3c16684ac)



seq 2 | sed '2i hello'
## OUTPUT

![Screenshot from 2025-05-27 11-25-04](https://github.com/user-attachments/assets/ff9be09f-4b4a-4c9c-9fd9-dd48af10a004)


seq 10 | sed '2,9c hello'
## OUTPUT

![Screenshot from 2025-05-27 11-25-17](https://github.com/user-attachments/assets/8a81423e-64a9-4e4c-b0d4-0c2b076d8e73)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![Screenshot from 2025-05-27 11-25-30](https://github.com/user-attachments/assets/99116047-36cb-4a26-9f79-81e7d03a8fa6)



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

![Screenshot from 2025-05-27 11-25-52](https://github.com/user-attachments/assets/448aa3b2-81c8-4d36-9076-bc89ff61aa17)


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

![Screenshot from 2025-05-27 11-26-48](https://github.com/user-attachments/assets/96678d91-ec1b-4786-b330-06fc04f3d84c)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

![Screenshot from 2025-05-27 11-27-19](https://github.com/user-attachments/assets/cd917f8e-cdbc-49e5-a97c-eb9228eeacdc)

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

![Screenshot from 2025-05-27 11-27-41](https://github.com/user-attachments/assets/25882c17-e50e-4b3d-aaf6-afb4b59c4a58)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![Screenshot from 2025-05-27 11-29-28](https://github.com/user-attachments/assets/850058f3-dfd7-45b3-9726-2a54019d5173)



#Backup commands
tar -cvf backup.tar *
## OUTPUT



mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


![Screenshot from 2025-05-27 11-38-30](https://github.com/user-attachments/assets/d0e590b5-6ff5-48e9-8b32-0932807719f9)



tar -xvf backup.tar
## OUTPUT

![Screenshot from 2025-05-27 11-39-55](https://github.com/user-attachments/assets/56c93fd0-8870-484f-aa04-f1a02f61a82c)


gzip backup.tar

ls .gz
## OUTPUT

 ![Screenshot from 2025-05-27 11-41-54](https://github.com/user-attachments/assets/3f1e693b-8247-41d7-b894-c7a680962c72)

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

![Screenshot from 2025-05-27 11-48-44](https://github.com/user-attachments/assets/76ed54ba-06c5-4f7b-82f8-01dd548a71d7)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![Screenshot from 2025-05-27 11-49-52](https://github.com/user-attachments/assets/b6a0a18d-dd17-424d-b8c3-5c1fef927812)


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

![Screenshot from 2025-05-27 11-51-26](https://github.com/user-attachments/assets/ace7820e-9e20-467a-9a1f-f762cb0116ee)

 
ls file1
## OUTPUT

![Screenshot from 2025-05-27 11-52-20](https://github.com/user-attachments/assets/711ac0dd-662f-41dc-b5d0-8a68a78349a8)

echo $?
## OUTPUT 

![Screenshot from 2025-05-27 11-52-53](https://github.com/user-attachments/assets/8f6fc957-bd34-4891-8938-87c0d117e971)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

![Screenshot from 2025-05-27 11-54-42](https://github.com/user-attachments/assets/b889688c-ac80-4096-92a8-0315349aab0b)

 
abcd
 
echo $?
 ## OUTPUT


![Screenshot from 2025-05-27 11-55-16](https://github.com/user-attachments/assets/eabd1551-5c2d-4acf-9b95-86990aaaf378)

 
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
chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![Screenshot from 2025-05-27 11-56-34](https://github.com/user-attachments/assets/68904b47-a2ce-4539-a21c-9c2cb0c74c78)



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

![Screenshot from 2025-05-27 12-01-26](https://github.com/user-attachments/assets/c71460d8-918c-49ed-b19a-a35e7390e0ab)


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

![Screenshot from 2025-05-27 12-26-16](https://github.com/user-attachments/assets/f42fb0a5-6296-4616-9c59-ce79d51a76af)



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
## OUTPUT

![Screenshot from 2025-05-27 12-27-40](https://github.com/user-attachments/assets/396d35cd-b818-4d5c-b001-acafead6713f)

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
## OUTPUT

![Screenshot from 2025-05-27 12-28-59](https://github.com/user-attachments/assets/06bcfdf0-0224-4364-b4b4-1bbea15e89b2)


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

![Screenshot from 2025-05-27 12-30-27](https://github.com/user-attachments/assets/e0bd28c1-23b9-42fc-8103-bd4ced6ddfc5)



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

![Screenshot from 2025-05-27 12-31-39](https://github.com/user-attachments/assets/15e30aa1-537a-4372-a880-7fd523c50aa5)


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
## OUTPUT
![Screenshot from 2025-05-27 12-32-54](https://github.com/user-attachments/assets/255802cb-041a-407d-b35e-91b60b1679fe)

 
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

![Screenshot from 2025-05-27 12-35-21](https://github.com/user-attachments/assets/6686cb44-9443-4868-bfd1-794ac0b77067)

 
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
## OUTPUT

![Screenshot from 2025-05-27 12-38-41](https://github.com/user-attachments/assets/61ba5117-7c50-431c-b6f7-17f04a07e17f)

 
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
## OUTPUT 

![Screenshot from 2025-05-27 12-39-47](https://github.com/user-attachments/assets/bbcf6dd6-106c-48e9-8b1d-40b623acfa22)

 
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
## OUTPUT

![Screenshot from 2025-05-27 12-40-42](https://github.com/user-attachments/assets/7131b4ac-c75c-403f-89b0-0c07bda4738a)


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
## OUTPUT

![Screenshot from 2025-05-27 12-42-11](https://github.com/user-attachments/assets/6d44e82b-cc43-4c51-8501-89a43d024b2f)


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
## OUTPUT

![Screenshot from 2025-05-27 12-46-52](https://github.com/user-attachments/assets/6bbf31fe-a0b0-43e5-b683-4de08df0882c)


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

![Screenshot from 2025-05-27 12-49-29](https://github.com/user-attachments/assets/7c76148a-4b56-4da4-b7a6-3d4f86997550)



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
![Screenshot from 2025-05-27 12-46-52](https://github.com/user-attachments/assets/58996af9-5463-4685-b45b-9c98efb378b8)


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
![Screenshot from 2025-05-27 12-49-29](https://github.com/user-attachments/assets/0347f13d-3c59-4332-bc2b-0ab5aa5858fa)




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
![Screenshot from 2025-05-27 12-50-45](https://github.com/user-attachments/assets/7f8e85ec-f11f-42f4-beab-be410f4f5054)




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
 ![Screenshot from 2025-05-27 12-51-34](https://github.com/user-attachments/assets/6d8aa191-ce7c-416f-a078-3a45d128b9b4)


 
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
$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
## OUTPUT
![Screenshot from 2025-05-27 12-54-03](https://github.com/user-attachments/assets/37d1aa17-9029-46b7-bbfb-2b98b54757b4)


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
![Screenshot from 2025-05-27 12-55-21](https://github.com/user-attachments/assets/50fb582b-9492-48d9-b42f-24905146e16c)


 
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
![Screenshot from 2025-05-27 12-56-19](https://github.com/user-attachments/assets/0e4e38a6-32ee-4dbf-acb1-7f7833fdd0c7)



 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 
$ ./exread1.sh 
## OUTPUT
![Screenshot from 2025-05-27 12-57-07](https://github.com/user-attachments/assets/541132eb-a77a-48ac-b84f-0402657f2890)





 
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
./funcex.sh 
./funcex.sh 1 2 

## OUTPUT
![Screenshot from 2025-05-27 12-58-37](https://github.com/user-attachments/assets/446e0c50-97e0-4f57-b6b5-aa58ec8f4197)


 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh
$ ./argshift.sh 1 2 3
## OUTPUT
![Screenshot from 2025-05-27 12-58-57](https://github.com/user-attachments/assets/94cf663e-2713-4889-8673-c8b2da160718)


 
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
$ ./argshift.sh 1 2 3
## OUTPUT
![Screenshot from 2025-05-27 12-59-37](https://github.com/user-attachments/assets/1df82689-e0b9-4f5e-bf6b-1d1b6fe11629)

 
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
./argshift.sh 1 2 3
## OUTPUT
![Screenshot from 2025-05-27 13-00-28](https://github.com/user-attachments/assets/86436ef9-f846-4c7b-ae83-5b053edfb659)


 
 
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
./argshift.sh 1 2 3
## OUTPUT 

![Screenshot from 2025-05-27 13-01-26](https://github.com/user-attachments/assets/5a119263-cf89-4d5e-8427-44c23abf62d0)


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

![Screenshot from 2025-05-27 13-03-14](https://github.com/user-attachments/assets/e83efe08-3697-4659-8bb2-4eff4d090d24)


 
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
![Screenshot from 2025-05-27 13-04-33](https://github.com/user-attachments/assets/8e4ae741-60a0-4ebc-8861-cd3224736010)



# RESULT:
The Commands are executed successfully.
