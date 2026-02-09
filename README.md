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

<img width="339" height="152" alt="544094863-2e7977f7-aef5-4d53-bca0-fa88e74418e0" src="https://github.com/user-attachments/assets/752331a5-372a-490e-b740-543f5a900629" />

cat < file2
## OUTPUT

<img width="317" height="173" alt="544094923-b386e68d-6da9-4187-a62f-0d30d8a65400" src="https://github.com/user-attachments/assets/7132c2d2-9e83-4962-8c53-26b7950653c1" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="372" height="73" alt="544095180-800b7fe1-f9c9-48c3-9ebc-b0db5a1bd2ec" src="https://github.com/user-attachments/assets/42f81b8c-e8e3-4b8c-9f83-0888b192cf8c" />

comm file1 file2
 ## OUTPUT
<img width="348" height="225" alt="544095221-b830dd54-aea1-49fe-9085-54ecd735cea1" src="https://github.com/user-attachments/assets/cfa4de76-ec11-46b2-9b98-a78f395ca3de" />

diff file1 file2
## OUTPUT
<img width="331" height="276" alt="544095276-e3b84279-7ac7-482d-9af3-fbc6cdb2c6ca" src="https://github.com/user-attachments/assets/e548104d-7b4a-45fe-b54f-3c45db94893b" />

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

<img width="317" height="123" alt="544095891-7bd1dac6-577b-44b1-a7dd-30b418bd0fc0" src="https://github.com/user-attachments/assets/f3fb6535-c06d-4eab-a718-c989ca8bd6c5" />


cut -d "|" -f 1 file22
## OUTPUT
![Alt text](<img/cut -d "|" -f 1 file22.png>)


cut -d "|" -f 2 file22
## OUTPUT
<img width="318" height="121" alt="544095950-f5573262-d5e7-42ce-ac9e-d6d6521da576" src="https://github.com/user-attachments/assets/894dc073-e266-4941-a289-384cb741be70" />


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

<img width="318" height="75" alt="544096032-5f35a486-09b5-4648-9fe9-afba845c67af" src="https://github.com/user-attachments/assets/2e15a8fa-a9b4-4b57-a789-9c13932789e3" />

grep hello newfile 
## OUTPUT

<img width="323" height="73" alt="544106537-3f55253a-f718-4bba-9773-35dc7643d90a" src="https://github.com/user-attachments/assets/d41201d9-10ec-442c-8e40-076323afeadb" />



grep -v hello newfile 
## OUTPUT
<img width="325" height="72" alt="544096322-0836f8e0-cc59-44cb-9e1c-876d912d1120" src="https://github.com/user-attachments/assets/769d2aae-198a-4710-b575-f633f71cd089" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="360" height="96" alt="544096367-6036caa8-f00d-4df2-99c2-1ba7173ecbcd" src="https://github.com/user-attachments/assets/92b8de08-2765-4c6d-8e80-e7ac545ee934" />


cat newfile | grep -i -c "hello"
## OUTPUT
<img width="393" height="75" alt="544097735-4e47d2bc-c3cf-4d79-8040-ddcad7b6c925" src="https://github.com/user-attachments/assets/10e7de53-557d-4f00-baed-05f6d2befcd0" />


grep -R ubuntu /etc
## OUTPUT

<img width="944" height="123" alt="544097777-c7c82e4e-27e2-4405-b168-d7c6e493dc76" src="https://github.com/user-attachments/assets/8a30d8a0-1a10-4f4f-bce9-6c3dcb5327ee" />


grep -w -n world newfile   
## OUTPUT
<img width="320" height="98" alt="544097830-a996ab96-d18c-4758-8c38-1d1bb7c2b5b8" src="https://github.com/user-attachments/assets/f2df44e7-8919-4fe7-b0f4-0fbc52343220" />


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
<img width="372" height="99" alt="544097888-9577f493-8a19-4d79-9b18-daf1e5d3d2c6" src="https://github.com/user-attachments/assets/c2f0fc23-cc8b-4ce5-b9c1-39f92a7d9246" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="353" height="101" alt="544097920-57c18488-5ed5-4c3d-aa43-40a99d52a4bc" src="https://github.com/user-attachments/assets/e7f9a27b-baee-4332-b5fd-d500bce663f2" />

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="394" height="98" alt="544097962-7934d737-b846-41c6-8114-e22619b8c5d3" src="https://github.com/user-attachments/assets/9f7a7fab-3e30-4d45-a1d7-336434f28533" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="318" height="75" alt="544098155-b942ccea-0610-4066-9234-11c750d3d71c" src="https://github.com/user-attachments/assets/5c29a808-6a1a-4afd-8e95-b0d9f5ef7ef8" />

egrep '(world$)' newfile 
## OUTPUT

<img width="315" height="98" alt="544098153-fe42c534-8f6d-49e4-ab5b-57fea69e2376" src="https://github.com/user-attachments/assets/e3ebede4-1bdc-46db-a65d-a2f48f531243" />


egrep '(World$)' newfile 
## OUTPUT


<img width="330" height="70" alt="544098156-d1f4a04a-a54f-4fb9-856c-c3e75e230952" src="https://github.com/user-attachments/assets/6fc72d23-7d04-4158-8a8c-f2a39224b63b" />

egrep '((W|w)orld$)' newfile 
## OUTPUT


<img width="368" height="121" alt="544098154-042735d6-6f41-4907-a0f3-bed805f44a7f" src="https://github.com/user-attachments/assets/e8d81409-feaa-4c17-8bad-61767369b806" />

egrep '[1-9]' newfile 
## OUTPUT
<img width="318" height="75" alt="544098160-ab776fb8-8431-49df-9b95-bebd7c6a000e" src="https://github.com/user-attachments/assets/7a497ae7-d6ad-4629-b5b7-0f3bc56ee398" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="354" height="74" alt="544098194-ef8e9831-94b9-4980-ac42-dbbee5fd778f" src="https://github.com/user-attachments/assets/20d34eb4-3c66-483b-b444-c50fa4977fe6" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="348" height="71" alt="544098270-c2538f7f-a0a9-455d-9cfe-a5ad701792cd" src="https://github.com/user-attachments/assets/793b7ac0-7771-4a0f-8a11-afb2b190ae11" />


egrep l{2} newfile
## OUTPUT
<img width="321" height="98" alt="544098305-6c93838d-6cee-4eb3-a14e-f87c63ae3ddc" src="https://github.com/user-attachments/assets/d04cda27-5681-47d7-98bf-fca8375b3613" />

egrep 's{1,2}' newfile
## OUTPUT 

<img width="326" height="123" alt="544098332-0ea0d3fb-b2b5-457f-bc08-28f346dd3ec2" src="https://github.com/user-attachments/assets/6fcd7e59-47d4-4c2d-9849-c36851f2de5e" />

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

<img width="319" height="76" alt="544098432-d8dca06b-458b-4b5b-8b0b-3a7d58b57b9e" src="https://github.com/user-attachments/assets/49874325-0f9b-4794-b4f7-758a078923de" />

sed -n -e '$p' file23
## OUTPUT

<img width="314" height="75" alt="544098485-400a8174-8c3b-4505-b587-4027250ebb91" src="https://github.com/user-attachments/assets/2180d474-86cb-4dde-bdca-15ae1a843ca0" />

sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="354" height="252" alt="544098513-8eb927e8-82a7-4e55-bcf1-234f3f03eefb" src="https://github.com/user-attachments/assets/259b5003-b298-4416-a1f1-3d0e280ae0c3" />

sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="369" height="250" alt="544098550-8856b12d-e913-40d3-bb56-b38bcab45d09" src="https://github.com/user-attachments/assets/4f7ddc72-eaef-4510-a36d-917a75c037c8" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT


<img width="395" height="248" alt="544098585-b8556ad2-1627-451f-a561-b133a46ee556" src="https://github.com/user-attachments/assets/51525862-4fce-45f6-8a31-786a08d1dbed" />
sed -n -e '1,5p' file23
## OUTPUT
<img width="329" height="176" alt="544098626-c3ef56f2-c022-47c5-a93a-cba46dcdb797" src="https://github.com/user-attachments/assets/d25a068a-16d1-420b-a084-6d590d49e73f" />


sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="350" height="123" alt="544098681-f7433fd8-c068-48df-8e16-f32f6b7b3e51" src="https://github.com/user-attachments/assets/4b18fa88-4fe6-40d4-9fea-2f3dcdb9a831" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="384" height="100" alt="544098718-de0b2f7c-7a9f-4d4b-ab66-b346548b47ee" src="https://github.com/user-attachments/assets/93a354f4-30c8-4b2c-8da8-83df77d7f43e" />


seq 10 
## OUTPUT
<img width="317" height="297" alt="544098740-2c02cc29-60b7-49a9-b779-d33e3b79f166" src="https://github.com/user-attachments/assets/ab42a2e6-4c07-4343-b2fe-6cca0a59e76a" />

seq 10 | sed -n '4,6p'
## OUTPUT

<img width="318" height="123" alt="544098810-007f20a9-1861-4de0-a113-0d7e7306947f" src="https://github.com/user-attachments/assets/99a202f3-6f65-49df-bf0a-c0faa3895248" />

seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="318" height="120" alt="544098918-c716b7af-a893-415b-92e5-0e421a9b811e" src="https://github.com/user-attachments/assets/577a2667-965a-4030-8618-68a1246cb90e" />

seq 3 | sed '2a hello'
## OUTPUT


<img width="318" height="149" alt="544098953-0189f04b-ae62-4cc1-b185-c712b01cf767" src="https://github.com/user-attachments/assets/cd4ab05c-e58d-4d73-85eb-61eb5eb12a09" />

seq 2 | sed '2i hello'
## OUTPUT

<img width="311" height="123" alt="544098993-bed808da-445f-4f59-b727-045384e853a7" src="https://github.com/user-attachments/assets/ebfa10ad-4b63-4139-b61a-0700e24d5e89" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="326" height="119" alt="544099032-c93c7f84-d9e5-4df8-95b4-17024de0eb15" src="https://github.com/user-attachments/assets/6eeb86b4-8f39-49e1-99a8-0016833e1c26" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


<img width="326" height="119" alt="544099174-c5747cfc-0d58-4f25-8b38-7e67002fa876" src="https://github.com/user-attachments/assets/7d97fb7f-37dc-49a5-862c-3e2f63516380" />

sed -n '2,4{s/$/*/;p}' file23
## OUTPUT


<img width="363" height="126" alt="544099636-f095acf5-7bc5-423c-9afe-b0195dcbd5ef" src="https://github.com/user-attachments/assets/dfc5a645-e936-46ee-a0ab-1a31ed847a55" />

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

<img width="335" height="175" alt="544099736-fa71f8a1-99b2-4275-9e4c-a28478b83315" src="https://github.com/user-attachments/assets/f457edf5-bdd4-4c29-9cb7-7466b94203d5" />

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

<img width="336" height="173" alt="544099824-5090bd2f-927a-47eb-86a5-f33d6c20e8a1" src="https://github.com/user-attachments/assets/93f5b0ad-1169-4a6a-ae47-59aed6c5ec2c" />

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT


<img width="424" height="249" alt="544100330-e5ba5758-9ada-473d-a74f-b4579ad764f5" src="https://github.com/user-attachments/assets/fad80479-7360-4377-affb-64d633d21868" />

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


 <img width="343" height="123" alt="544100433-2737eb22-f8b3-420a-aaa4-e435a277c895" src="https://github.com/user-attachments/assets/4aa6466c-5f92-4f50-a6fb-f8cec8c5feba" />

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="474" height="125" alt="544100513-a10dbb18-0827-4e47-ac92-fd19cbfb7324" src="https://github.com/user-attachments/assets/160aa404-e6e6-47c5-a03f-136a0b271f79" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT


<img width="333" height="249" alt="544100621-5136a8d1-6929-411a-8f85-ccacaf6af491" src="https://github.com/user-attachments/assets/d615ede0-2fb6-4056-8e49-61057dbbdf65" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="619" height="250" alt="544100740-f78bc145-7cf9-4f9f-adb8-c9d1f068f972" src="https://github.com/user-attachments/assets/85fcb31a-45ee-4079-af9a-298a067a912d" />


tar -xvf backup.tar
## OUTPUT
<img width="424" height="249" alt="544100987-67802543-0f30-4a6a-b690-caf2bd2e2d31" src="https://github.com/user-attachments/assets/6b00b807-189c-4c7a-892d-54e557e8f9ff" />


gzip backup.tar

ls .gz
## OUTPUT
 
<img width="424" height="249" alt="544100987-67802543-0f30-4a6a-b690-caf2bd2e2d31" src="https://github.com/user-attachments/assets/eb816b40-94fe-4ae8-b808-abf9db988e88" />


gunzip backup.tar.gz

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘;exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="435" height="98" alt="544101057-7d9ba61b-4849-40b0-b6d9-19a992e2757e" src="https://github.com/user-attachments/assets/579e3e2c-6d60-44d9-938c-404b2c31cc7d" />


cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="449" height="127" alt="544101161-d6041a32-66f1-4cac-b12f-e3d2d1cf8438" src="https://github.com/user-attachments/assets/fdb07a2b-862f-4882-872a-c17952e333c0" />

cat < scriptest.sh 
```bash
#!/bin/sh
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
```

cat scriptest.sh 
```bash
#!/bin/sh
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


<img width="619" height="447" alt="544101532-95afbef6-9891-4101-bc8f-1e0dc0cfe3b1" src="https://github.com/user-attachments/assets/76751e7b-ba57-4242-82c2-1b955d95d3ff" />

ls file1
## OUTPUT

<img width="423" height="72" alt="544101680-20b07bb4-6cd3-4dcf-b237-bc043c0a8d02" src="https://github.com/user-attachments/assets/524c3c48-629b-4f6a-a8a2-1bb34e117b78" />

echo $?
## OUTPUT 


<img width="423" height="74" alt="544101847-c040f2cd-4784-4e18-97e5-145b153468ac" src="https://github.com/user-attachments/assets/54739345-a070-4e28-bc60-36f11f9ffe09" />

./onebash:./one: Permission denied
 
echo $?
## OUTPUT 
 
<img width="423" height="74" alt="544101847-c040f2cd-4784-4e18-97e5-145b153468ac" src="https://github.com/user-attachments/assets/03848fec-0a17-42af-b32a-6f5211aba802" />


abcd
 
echo $?
 ## OUTPUT

<img width="468" height="148" alt="544101906-f0c2ab54-4937-4a9c-9b57-d33afd8f75b6" src="https://github.com/user-attachments/assets/b2eb3252-4cdc-4f21-8fcc-cefc41c77dae" />

 
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
#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```

## output
<img width="427" height="272" alt="544101971-4b114bad-977a-492f-8d38-479f1c19f56e" src="https://github.com/user-attachments/assets/41123f02-43c7-438e-bc2f-decef60ca00d" />

chmod 755 strcomp.sh 
./strcomp.sh 
## OUTPUT

<img width="609" height="100" alt="544102032-f3035968-5d85-47db-bc7d-471693101433" src="https://github.com/user-attachments/assets/e8187afd-d6d2-4753-8f3d-dcf173a2b2c8" />


# check file ownership
cat < psswdperm.sh 
```bash
#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
```

cat psswdperm.sh 
```bash
#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT

<img width="457" height="76" alt="544102102-1f169cdb-1173-42f8-b8ca-e948a4ec5bde" src="https://github.com/user-attachments/assets/beeec484-68f3-4b93-9b46-e32da2bc863b" />


# check if with file location
cat>ifnested.sh 
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
```
cat ifnested.sh 
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
```

./ifnested.sh 
## OUTPUT

<img width="423" height="75" alt="544102126-a8ad56d1-f2c9-4e29-b08b-59c6290183cb" src="https://github.com/user-attachments/assets/0fa78bbe-d88d-496a-b2d7-8c2e8b6204fb" />


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
```


cat iftest.sh 
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
```

chmod 755 iftest.sh
 
./iftest.sh 
## OUTPUT

<img width="609" height="125" alt="544102225-d6dc7f84-10fb-4b2b-85a2-41bdeeb1f07b" src="https://github.com/user-attachments/assets/d2da702b-18a1-4c5c-85bc-e03f5d7f51bd" />

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
```

cat ifnested.sh 
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
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
## OUTPUT

<img width="633" height="150" alt="544102353-bba1cb74-10f5-45d8-b09f-ad0aa8460a1b" src="https://github.com/user-attachments/assets/787d4e83-1236-417d-9ad9-545a0ae03bbe" />


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

chmod 755 elifcheck.sh
 
./elifcheck.sh 
## OUTPUT

<img width="629" height="105" alt="544102352-679ee9db-caa5-486c-92a0-124c57938de7" src="https://github.com/user-attachments/assets/b5092a35-d5fc-4b36-8d03-9319ae378bcf" />


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
chmod 755 ifcompound.sh
./ifcompound.sh 
## OUTPUT
<img width="644" height="103" alt="544102387-c5598b37-07e6-47a8-abae-52f6f7df7384" src="https://github.com/user-attachments/assets/b1b1a7b4-93e0-46e5-9a05-437f13f206e7" />


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

<img width="423" height="77" alt="544102761-fa308ca1-d584-40b0-a7cf-2475b6cb8a89" src="https://github.com/user-attachments/assets/7798b971-e301-4382-a195-9cfe45b9ee7d" />


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
chmod 755 whiletest.sh
 
./whiletest.sh
 ## OUTPUT

 <img width="441" height="304" alt="544103021-902a9aab-cbc9-431b-b0db-42f35575df01" src="https://github.com/user-attachments/assets/48d3d2f1-20a5-4b6c-80be-91f2eb0e72f0" />

 
cat untiltest.sh 
```bash
#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
$ ./untiltest.sh
 ## OUTPUT

<img width="504" height="175" alt="544103185-2107a5cb-ee3f-4970-9f0a-f8ecd0214c46" src="https://github.com/user-attachments/assets/2e5c516a-03ac-4176-b09d-3b8a4c82500b" />


cat forin1.sh 
```bash
#!/bin/bash
#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
$ ./forin1.sh
## OUTPUT

<img width="603" height="249" alt="544103293-1201b51e-595c-401d-847f-835b64d35171" src="https://github.com/user-attachments/assets/8ac5bdff-75b4-434d-931f-014bb30aa544" />

 
cat forin2.sh 
```bash
#!/bin/bash
# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
## OUTPUT

<img width="605" height="177" alt="544103389-7960c912-841c-4670-926d-5a7b83ce1ab8" src="https://github.com/user-attachments/assets/6782a37e-e961-426b-a863-b26f931ad12f" />


cat forin3.sh 
```bash
#!/bin/bash
# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ chmod 755 forin3.sh
$ ./forin3.sh 
## OUTPUT
<img width="605" height="177" alt="544104038-684c0a81-0911-4c21-84a2-d8caa9b29a91" src="https://github.com/user-attachments/assets/fb80eefc-06b9-4e67-9ada-50eb63e6729d" />


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
$ ./forin1.sh
## OUTPUT
<img width="618" height="252" alt="544104167-224f380b-5b3c-42be-9103-1354e6615504" src="https://github.com/user-attachments/assets/fffff408-db71-4886-91e9-ac995fd64e84" />


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

$ cat > cities
```
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam
```
./forinfile.sh
## OUTPUT
<img width="615" height="252" alt="544104272-0a4e07d8-589c-43a7-b2cd-8a80b959bdb9" src="https://github.com/user-attachments/assets/9a781d0a-f0a0-4ae1-9ac7-f2b3573d606a" />



cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
```
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT
<img width="417" height="223" alt="544104615-cd2e159f-396b-493d-94af-36be0f3b3e9c" src="https://github.com/user-attachments/assets/e81319f4-1702-44f6-90ba-ab325e07235d" />


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
<img width="422" height="175" alt="544104461-165137f4-54f0-4216-8ed9-b052db5d6f05" src="https://github.com/user-attachments/assets/757968eb-918c-4a85-ac76-8718a95b34f0" />

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


<img width="428" height="76" alt="544104766-48f94dfc-c96c-44ec-8fc5-0f24df6997cc" src="https://github.com/user-attachments/assets/2b18c95f-0000-406e-900e-b190089a7a0c" />

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


<img width="414" height="353" alt="544104933-c3d9cd71-8567-42f1-b84d-9f0ece5fea77" src="https://github.com/user-attachments/assets/c4e1102b-0008-4923-a529-888fabebd189" />

cat > forcontinue.sh 
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
 <img width="414" height="353" alt="544105220-96e74f97-1b90-4252-95e5-2352d3f0aa3a" src="https://github.com/user-attachments/assets/b61f53ea-d719-4f0b-bf8a-221426068942" />


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

<img width="442" height="100" alt="544105758-ba66c427-7f94-471b-8eed-0ac9bccb27f4" src="https://github.com/user-attachments/assets/1bd686c1-803d-443d-b3fc-8a47bbeab0b4" />


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


<img width="451" height="101" alt="544105759-60d6dbca-9704-473b-91ae-d42f1c76fb66" src="https://github.com/user-attachments/assets/4429fcfd-fdb0-4fec-ab8f-7ecbaa1b0786" />

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
$ chmod 755 funcex.sh
$ ./funcex.sh 

## OUTPUT
 
<img width="423" height="74" alt="544105907-bc569fa9-dd5c-42e9-bd92-379876c993cc" src="https://github.com/user-attachments/assets/3d252ae9-0d20-49f4-bfaa-22358c60398b" />

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
<img width="420" height="124" alt="544097359-2c579ffb-7109-4b3a-bd84-cfd37f634895" src="https://github.com/user-attachments/assets/ff52160b-a66f-4714-8e12-f430605cf54d" />


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
$ chmod 777 argshift1.sh

$ ./argshift1.sh 1 2 3
## OUTPUT
<img width="419" height="124" alt="544097084-90e682d6-0f0e-4dcd-9dc0-72c174a23774" src="https://github.com/user-attachments/assets/11cf9341-8803-4a3d-b4ea-1a16afd35522" />


 
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
 
<img width="418" height="401" alt="544096898-8f87fa6d-374c-49ef-9755-a2df935acc76" src="https://github.com/user-attachments/assets/eb052b75-31e0-44de-8644-bb4203d429cb" />

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
<img width="433" height="126" alt="544096657-93ab60fe-a7c5-4174-a9ab-7681ebac708e" src="https://github.com/user-attachments/assets/e7cac7e0-60a3-4443-8880-08dadbdc8b22" />


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
$chmod 755 palindrome.sh

$./palindrome.sh
## OUTPUT 

<img width="433" height="126" alt="544096657-93ab60fe-a7c5-4174-a9ab-7681ebac708e" src="https://github.com/user-attachments/assets/42c94475-6f6a-4620-bc06-b8a5264cfd0d" />


# RESULT:
The Commands are executed successfully.
