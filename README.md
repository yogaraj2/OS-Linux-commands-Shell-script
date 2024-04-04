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
![314966454-db8c1fbc-22ba-4f16-b6f2-1ea1e9da77cb](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/b7f546fa-4358-4013-a104-97fd773bdf04)

cat < file2

## OUTPUT
![314968728-8cccd0e6-2c17-4903-950a-ae3e8875485c](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/4fba90d4-0fb0-49ce-95d0-e3f3251fd076)

# Comparing Files
cmp file1 file2
## OUTPUT
 ![314970320-e9e9919f-9651-403a-be67-cd04aa78d578](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/dd3c9ace-6547-43db-9376-092b9d7ce36c)

comm file1 file2
 ## OUTPUT
![314973236-19a03beb-8998-4fc8-9330-fa4b0b100d0d](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/3bf10b6b-72c4-473a-b260-dfea58416ad1)

 
diff file1 file2
## OUTPUT
![314976645-88d613bd-33ca-41d2-9a5c-88a1ab184d93](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/3cfa2e65-8cab-4fdd-a12a-098c79a58e90)


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
![315049755-2e03daed-f504-479b-9030-c23924ff4530](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/c573c7f6-9f5a-4854-8606-073f45491398)

cut -d "|" -f 1 file22
## OUTPUT
![315050373-0a19cb91-b645-4687-87c0-086dcaa9d148](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/c4770f82-6188-41ac-a0aa-386a31d0210f)

cut -d "|" -f 2 file22
## OUTPUT
![315050613-3a75e4f1-6f49-4983-84b7-7277c7843eb6](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/9fee0b94-a3a0-4615-99c3-c1c6df894b85)


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
![315052424-568e5c3f-8266-4fe6-a01a-06efb74e8bab](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/a12d1c94-407e-4081-9550-681d1f459a8b)

grep hello newfile 

## OUTPUT
![315052582-930b95c8-1c24-41c5-84fe-5d747a497d47](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/b6e084b5-5db6-4a6f-8c2f-71410c86f1bb)


grep -v hello newfile 

## OUTPUT
![315052852-94afdf67-2e48-43ab-a1f9-42d9de23af1c](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/9753ef93-0103-4f2f-b6c6-7eeca5a50894)


cat newfile | grep -i "hello"

## OUTPUT

![315054165-f8535b1f-4cab-4a2d-b36d-8cec94fcfd03](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/713cd60f-e7f6-49f2-b237-f86c7c5d0f4e)

cat newfile | grep -i -c "hello"

## OUTPUT
![315054313-5aa8276f-bc86-4add-bc04-6d719669072a](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/32035f00-2cbe-4b3d-ba9f-ba76408fac1b)


grep -R ubuntu /etc

## OUTPUT
![315054860-f03dc186-49ae-4027-bcd5-d33892288b6b](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/f1f4063b-872c-4ef5-b564-4f6f71258a70)


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
![315057576-2e7b2e22-546d-4cf4-8c55-e004d07bc432](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/b1b1806d-7e8c-4be2-bf6d-ae6f68f8c16d)


egrep -w '(H|h)ello' newfile 
## OUTPUT
![315057612-9504c57c-c491-4984-91a8-0f6ffa3405b6](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/45807eb4-1895-42df-a17d-29b5be91f3d5)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![315057786-85c2ea71-e4c0-4527-ad4b-f999f7dd6836](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/d8b21ec4-5e48-4417-9b5d-0c2ca8c23467)


egrep '(^hello)' newfile 
## OUTPUT
![315057856-d30b7b1a-4ef2-4d3c-b102-5459fd72d99e](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/8ce4f7f0-dfcf-4e0c-8073-14aaaa1199c1)

egrep '(world$)' newfile 
## OUTPUT
![315057905-cab3a50b-2828-4b70-b0ac-dd9870c27d65](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/33f03fe5-06b8-4015-aa52-8c20c4f9234d)


egrep '(World$)' newfile 
## OUTPUT
![315057987-220b73d8-209c-467c-bf69-eeab592b9f55](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/1bb819a5-ab9f-4d04-bc47-06c9e5e27653)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![315058081-134dd96b-ec62-4534-94d8-2838128d5926](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/5f118111-b698-4aff-86c6-7f51a18ab6de)

egrep '[1-9]' newfile 
## OUTPUT
![315058148-9747fd78-a71e-4ac1-bc88-395c40c5a141](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/1ae7fa24-8a53-4911-821d-e1665720e38e)

egrep 'Linux.*world' newfile 
## OUTPUT
![315058212-61acfb3f-c1d8-4df0-8599-4f354a63eaf9](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/f5207be6-4e7b-4ad0-a08b-6cccdee0b727)


egrep 'Linux.*World' newfile 
## OUTPUT

![315058259-6eb50d28-7a75-4198-b114-cfb6fa1af3b6](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/1aa5ee2c-b200-4135-9d70-fe0c077570b4)

egrep l{2} newfile
## OUTPUT
![315058350-510bbc04-d288-4b3f-8ef6-6d8fa637c3a9](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/4d9b341a-e6a1-4293-8626-db2670e57542)


egrep 's{1,2}' newfile
## OUTPUT 
![315058512-fd9e79fe-ef41-4999-9f8d-7d49f8e7f6a5](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/4b872336-a8db-4739-a832-c704bdc290ba)


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
![315058621-454dec9b-25d6-4ff5-b527-7cd8dd066541](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/44a01fbe-422e-485a-a22f-3c2a500d6932)


sed -n -e '$p' file23
## OUTPUT
![315058651-2063ef33-c10f-4a08-a1c7-4c9a1fc21a50](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/709af281-77ce-4c2d-8838-3e70457475a4)


sed  -e 's/Ram/Sita/' file23
## OUTPUT
![315058815-d2f5b200-f89f-4fdf-83e2-cf5a5b034330](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/0e2004aa-11a2-425a-8ab3-f5cd99442e5a)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![315058862-78737b47-4c94-403f-993d-0dd4f06e4880](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/6b17f715-e898-445c-9dcf-8e931c010e3b)

sed  '/tom/s/5000/6000/' file23
## OUTPUT

![315059141-0057c0e2-4513-4a4f-acf6-0b892d784cce](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/7d74c34e-c552-4843-a075-63f9067aca24)


sed -n -e '1,5p' file23
## OUTPUT
![315059192-ad64fd5d-4327-48be-b161-6e0fe7af04ce](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/1ab92a40-ea52-4d36-a46f-420f361d58ac)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![315059241-00523d89-5158-4d01-a601-1089eedbff2d](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/2be25544-97f8-4630-b406-9f4776ee958b)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![315059353-8bc88352-7206-48e5-802a-d4f572d87354](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/2268f0e7-579a-4a55-8fe1-67bb74cd3ed1)

seq 10 
## OUTPUT
![315059428-13d56ab8-ca51-4c9f-8be7-3c2a4cb3b80c](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/44a7ea47-2616-4d0a-bae9-17da9e779169)

 
seq 10 | sed -n '4,6p'
## OUTPUT
![316232756-b1613ac9-b570-4cc6-b01e-74d904abd089](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/04dc11f3-6be0-4c27-a1bc-5be21f7278e1)


seq 10 | sed -n '2,~4p'
## OUTPUT



seq 3 | sed '2a hello'
## OUTPUT
![316233035-78951b7a-c375-44f5-b45f-ab68eade58b2](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/d234abfa-cda4-4fb2-8165-0dbfbbb9b26f)



seq 2 | sed '2i hello'
## OUTPUT
![316233047-091701a2-2116-4bae-a268-c92e9ce800b3](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/f5ec0595-dc0c-4d27-a7d2-7f5815ec056c)

seq 10 | sed '2,9c hello'
## OUTPUT
![316233167-a6ff0a5e-df58-471e-8d8c-ca343b04daef](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/586c40eb-e2a0-4ec0-86de-736a7cb32bf1)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![316233225-dfc01136-30c0-4c3d-8f0e-52cb7aac03a4](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/2bf29007-b112-461a-bfa0-fd4332cfa0be)


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
![316233304-6bbf7928-dc8d-4b9f-8056-4ab956946bd8](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/8d0bf1fe-9dce-4202-bf35-ac135b7778a2)


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
![316233316-f765bf07-13f9-4292-aef5-4aa2e0ede8c2](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/67cd139d-f8ea-433a-b959-13b9e8cbcc8a)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![316233342-9deef10f-f1a7-4210-962a-b9d0787cf39e](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/2c88ffa0-ff83-400a-83fd-51a1822881f4)


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
![316233381-eb1f8912-c34f-494c-84ea-743b7b308b5c](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/ccf8d42b-87c2-4a5a-8faf-c24a53024da5)


cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![316233393-b3ba8261-228d-446f-bfd7-96544a204a6d](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/073c27b4-adb7-4e3a-b901-d3828a715dbe)

#Backup commands
tar -cvf backup.tar *
## OUTPUT
![316233456-a19797ce-1a2c-4b81-b07c-e7c4eaa0a796](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/e12aad28-de23-40ee-9f2b-85d989c8e24c)

tar -tvf backup.tar
## OUTPUT
![318279303-14b7c4b4-e817-494e-b041-94451c249cc0](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/d2ad8a74-7544-4c51-b368-f846976d49ef)


tar -xvf backup.tar
## OUTPUT
![318279313-a5aa83f9-76ac-4c1b-9f35-f3f5504956ea](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/0449668b-ab2f-4bdd-aee6-19fd5ae8ff0e)

gzip backup.tar ls .gz

## OUTPUT
 ![318279416-2f1dc30a-7553-4b55-b754-3e0d6436a4e7](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/5a66b934-9a7b-4ea5-885d-9bd736a46d1f)
 
gunzip backup.tar.gz
## OUTPUT
![318279427-af1b8ee0-1a48-49d9-b2d3-8ce086d5f56d](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/18762b5d-f682-4bbb-8db6-f5010444fc09)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![318279460-ff31ddb0-00d1-43f0-9047-9fc9b8da9668](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/daa97438-0c15-4018-ad8e-f3e00efb84f7)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![318279467-93a6993f-f93c-415d-afd8-e06022abf92a](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/588ed472-4e89-471d-a11e-de8d15296821)


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
![318279493-5d31649b-d5ae-41bb-8518-b2860b8fae20](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/0c14a3e5-23c1-4da7-9813-6e123505567e)

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![318279567-2d40f2a5-10f4-45ff-a7a5-d1b7124aa2c4](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/f7dd3dc5-e458-40c5-b65c-f155aa31dc17)

abcd
 
echo $?
 ## OUTPUT
![318279578-23dff394-d5d4-4adb-82c2-bb10accba343](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/c842ce43-7d54-4ba3-b7ec-50da158c51ee)


 
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
![318279585-ac72d640-dba9-4cbc-b8d0-9ad5767096d4](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/8dba7800-b309-4d0c-99fc-dbc7d1651e60)


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
![318281323-f73e6164-481d-4aae-9a3c-08e87463930d](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/0c65c410-0709-44dc-bb09-5121ba7c0020)

![318281324-e7be2e48-d157-40a2-a0a1-b545e056004f](https://github.com/yogaraj2/OS-Linux-commands-Shell-script/assets/153482637/314d1e38-aa8a-4463-898d-533444575494)


# RESULT:
The Commands are executed successfully.
