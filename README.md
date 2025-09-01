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
Mithun Kumar
Navadeeps
Adityas
^d
```
cat > file2
```
Sanjay
Hemanth
Kirthicksha
^d
```
### Display the content of the files
cat < file1
## OUTPUT
<img width="293" height="129" alt="Screenshot 2025-08-31 152110" src="https://github.com/user-attachments/assets/6d83d15c-a684-4d48-841b-64671e490fc0" />



cat < file2
## OUTPUT
<img width="422" height="120" alt="Screenshot 2025-08-31 152121" src="https://github.com/user-attachments/assets/07a3dbb5-b9f6-481b-8744-689ea86e3c78" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="347" height="77" alt="Screenshot 2025-08-31 152131" src="https://github.com/user-attachments/assets/8db633b4-7b08-4946-bfb0-b093ee6191b5" />

comm file1 file2
 ## OUTPUT

 <img width="388" height="281" alt="Screenshot 2025-08-31 152143" src="https://github.com/user-attachments/assets/d9415ac8-3c7b-4388-b8ff-dc974ac05b98" />

diff file1 file2
## OUTPUT

<img width="347" height="251" alt="Screenshot 2025-08-31 152153" src="https://github.com/user-attachments/assets/2b8c4140-df60-4814-a83f-6a5c4157befa" />

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

<img width="288" height="101" alt="Screenshot 2025-08-31 152355" src="https://github.com/user-attachments/assets/c08ffec3-7ea0-481c-b498-1ed653641fdc" />

cut -d "|" -f 1 file22
## OUTPUT

<img width="329" height="127" alt="Screenshot 2025-08-31 152604" src="https://github.com/user-attachments/assets/eeec2441-bcc2-4fe0-90ed-288b14d99fd1" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="320" height="126" alt="Screenshot 2025-08-31 152633" src="https://github.com/user-attachments/assets/d90997c6-0e01-4a4a-9bfd-fefb7b642443" />

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

<img width="294" height="77" alt="Screenshot 2025-08-31 152817" src="https://github.com/user-attachments/assets/3677cbc1-5c81-407a-9438-61a5e3a30cae" />


grep hello newfile 
## OUTPUT


<img width="273" height="77" alt="Screenshot 2025-08-31 152843" src="https://github.com/user-attachments/assets/a8427b02-dd96-440b-b8f6-bb0e06cbe304" />


grep -v hello newfile 
## OUTPUT

<img width="288" height="74" alt="Screenshot 2025-08-31 152920" src="https://github.com/user-attachments/assets/1077489e-c6a7-4811-b28b-18def260b0c7" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="391" height="102" alt="Screenshot 2025-08-31 152958" src="https://github.com/user-attachments/assets/c7b4545c-e96d-4a01-bc7a-63d745c2871c" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="436" height="81" alt="Screenshot 2025-08-31 153039" src="https://github.com/user-attachments/assets/0b6fb23e-a570-4c3e-ada5-3285caf6384c" />



grep -R ubuntu /etc
## OUTPUT

<img width="1498" height="847" alt="Screenshot 2025-08-31 153205" src="https://github.com/user-attachments/assets/3decaa77-786e-48c8-80b9-d3f7fddc739b" />


grep -w -n world newfile   
## OUTPUT
<img width="478" height="99" alt="Screenshot 2025-08-31 153319" src="https://github.com/user-attachments/assets/23b675f6-baee-4560-a841-42e20bb28eab" />


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

<img width="390" height="105" alt="Screenshot 2025-08-31 154446" src="https://github.com/user-attachments/assets/3ef29771-a3b2-4a68-bdc4-7b0c0e710232" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="378" height="105" alt="Screenshot 2025-08-31 154540" src="https://github.com/user-attachments/assets/0e4eb1b6-1a9a-44f0-aa38-9b7f3373038b" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="461" height="102" alt="Screenshot 2025-08-31 154641" src="https://github.com/user-attachments/assets/0c2fc00f-bd64-43b3-a0b5-4ce27afedacb" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="334" height="76" alt="Screenshot 2025-08-31 154728" src="https://github.com/user-attachments/assets/8231a7d5-4a93-4972-9825-feda03e122af" />


egrep '(world$)' newfile 
## OUTPUT

<img width="385" height="106" alt="Screenshot 2025-08-31 160711" src="https://github.com/user-attachments/assets/463407f9-2734-427b-9a2b-c91d1ed864fb" />



egrep '(World$)' newfile 
## OUTPUT
<img width="358" height="77" alt="Screenshot 2025-08-31 160736" src="https://github.com/user-attachments/assets/0c4c4aee-bb4e-4947-b85a-bd0b2c9f9dc8" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="420" height="123" alt="Screenshot 2025-08-31 160852" src="https://github.com/user-attachments/assets/82352e50-20dc-45f2-b025-1ed06761f25d" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="383" height="77" alt="Screenshot 2025-08-31 161659" src="https://github.com/user-attachments/assets/1a1dcf38-2a97-4e27-b20d-a432ae22720f" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="410" height="82" alt="Screenshot 2025-08-31 161737" src="https://github.com/user-attachments/assets/62ba2bea-1aa5-4ae5-a478-3e69bba456ef" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="357" height="82" alt="Screenshot 2025-08-31 161807" src="https://github.com/user-attachments/assets/5fa02749-dc12-4288-9439-4db5a2e755c5" />

egrep l{2} newfile
## OUTPUT

<img width="321" height="110" alt="Screenshot 2025-08-31 161849" src="https://github.com/user-attachments/assets/ac311c33-3beb-4c6c-835b-aa7ef95147ee" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="344" height="131" alt="Screenshot 2025-08-31 161929" src="https://github.com/user-attachments/assets/a75c3f90-e3df-43c4-83fd-b23861285cf3" />


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

<img width="312" height="78" alt="Screenshot 2025-08-31 162700" src="https://github.com/user-attachments/assets/3aefdf88-9665-427d-8c84-711122980258" />


sed -n -e '$p' file23
## OUTPUT

<img width="300" height="79" alt="Screenshot 2025-08-31 162803" src="https://github.com/user-attachments/assets/60fb0264-9778-4674-b972-b1beee987fb3" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="435" height="249" alt="Screenshot 2025-08-31 162845" src="https://github.com/user-attachments/assets/e974a47c-0672-4fec-8c10-266bdeaab878" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="388" height="253" alt="Screenshot 2025-08-31 162914" src="https://github.com/user-attachments/assets/6c68de91-8649-41cc-b645-979d8d251f2c" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="664" height="78" alt="Screenshot 2025-08-31 163020" src="https://github.com/user-attachments/assets/41c0b059-6d68-418f-8906-48211ef09858" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="366" height="179" alt="Screenshot 2025-08-31 163056" src="https://github.com/user-attachments/assets/a66a6686-44b0-477d-9943-eebd0268064d" />


sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="353" height="130" alt="Screenshot 2025-08-31 163134" src="https://github.com/user-attachments/assets/d2d20c50-5b1b-46a7-aa70-1689554181a6" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="422" height="100" alt="Screenshot 2025-08-31 163221" src="https://github.com/user-attachments/assets/48982e72-f02b-4b7e-a6fd-c8ded8f0a0fe" />


seq 10 
## OUTPUT

<img width="301" height="302" alt="Screenshot 2025-08-31 163243" src="https://github.com/user-attachments/assets/d1f4df8c-1115-48b6-8dbb-499250914eaf" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="306" height="127" alt="Screenshot 2025-08-31 163325" src="https://github.com/user-attachments/assets/23275b2a-dc06-4607-995b-6db35b8f6788" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="318" height="128" alt="Screenshot 2025-08-31 163405" src="https://github.com/user-attachments/assets/c8bee314-0216-4627-9e5e-6b30498808e1" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="320" height="153" alt="Screenshot 2025-08-31 163439" src="https://github.com/user-attachments/assets/da0be8db-2bec-418c-afcd-3317ffcb3631" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="334" height="129" alt="Screenshot 2025-08-31 163510" src="https://github.com/user-attachments/assets/4f7bda13-0090-417d-a3ac-f8baa53b3eab" />

seq 10 | sed '2,9c hello'
## OUTPUT

<img width="357" height="128" alt="Screenshot 2025-08-31 163550" src="https://github.com/user-attachments/assets/dcbc71d6-60f4-41bf-a640-ea788b49dd0e" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="372" height="129" alt="Screenshot 2025-08-31 163822" src="https://github.com/user-attachments/assets/44c10081-c165-4764-8704-e0909db0f7fe" />


sed -n '2,4{s/$/*/;p}' file23

<img width="383" height="131" alt="Screenshot 2025-08-31 163910" src="https://github.com/user-attachments/assets/47b7380b-6d8f-4e03-867a-2b5f7335daa1" />

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
<img width="331" height="184" alt="Screenshot 2025-08-31 164137" src="https://github.com/user-attachments/assets/a79cc115-8f3f-4647-9ce6-825d353262b9" />


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

<img width="322" height="177" alt="Screenshot 2025-08-31 164350" src="https://github.com/user-attachments/assets/a0c7307f-7d6f-4405-94bc-873252ad9d40" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="473" height="256" alt="Screenshot 2025-08-31 164507" src="https://github.com/user-attachments/assets/1d84b256-8d4d-41f2-8105-b8a7bb5c8616" />

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
<img width="441" height="127" alt="Screenshot 2025-08-31 164700" src="https://github.com/user-attachments/assets/05095586-0385-440d-8ec5-fccb05554a62" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="506" height="128" alt="Screenshot 2025-08-31 164742" src="https://github.com/user-attachments/assets/e6635c0a-b4e3-4714-b5f1-26a0c31cceb4" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="366" height="273" alt="Screenshot 2025-08-31 164819" src="https://github.com/user-attachments/assets/94900faa-9933-44d1-88e1-a4a8f93d218a" />


mkdir backupdir
 
mv backup.tar backupdir
<img width="636" height="277" alt="Screenshot 2025-08-31 164934" src="https://github.com/user-attachments/assets/d0678ee7-fb78-4480-8139-038f7939a2ce" />

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="591" height="107" alt="Screenshot 2025-08-31 165108" src="https://github.com/user-attachments/assets/22557ddb-a6c6-4ebc-8fb2-067254bda9e0" />

tar -xvf backup.tar
## OUTPUT
<img width="657" height="108" alt="Screenshot 2025-08-31 170337" src="https://github.com/user-attachments/assets/7c02672c-80bf-423a-860b-0ca49782d312" />

gzip backup.tar
<img width="524" height="74" alt="Screenshot 2025-08-31 170451" src="https://github.com/user-attachments/assets/b9c46927-c706-4b3c-a17f-417ba9522f57" />

ls .gz
## OUTPUT
<img width="545" height="75" alt="Screenshot 2025-08-31 170531" src="https://github.com/user-attachments/assets/4518cba4-aecc-4069-8302-84354f23482f" />
 
gunzip backup.tar.gz
## OUTPUT
<img width="471" height="74" alt="Screenshot 2025-08-31 170613" src="https://github.com/user-attachments/assets/4e960fef-6afb-4766-99fd-bef4b380d513" />

 
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
<img width="354" height="126" alt="Screenshot 2025-08-31 173253" src="https://github.com/user-attachments/assets/482567b5-c276-4f90-b655-938824738ef6" />


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
<img width="535" height="129" alt="Screenshot 2025-08-31 185331" src="https://github.com/user-attachments/assets/a2932fc9-5049-44cc-8002-83a7f7546607" />

 
ls file1
## OUTPUT
<img width="330" height="70" alt="Screenshot 2025-08-31 185402" src="https://github.com/user-attachments/assets/11fe3d0c-15ec-4240-a222-d717fca8f81b" />

echo $?
## OUTPUT 
<img width="289" height="74" alt="Screenshot 2025-08-31 185448" src="https://github.com/user-attachments/assets/67371631-9f08-45f1-95d5-cbe4b1aeba83" />

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

<img width="455" height="287" alt="Screenshot 2025-08-31 190313" src="https://github.com/user-attachments/assets/a941002e-697b-42cb-8838-f10fad0e6455" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="670" height="181" alt="Screenshot 2025-08-31 190413" src="https://github.com/user-attachments/assets/858f6626-351f-49e9-a441-5450de310765" />


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
<img width="642" height="303" alt="Screenshot 2025-08-31 191128" src="https://github.com/user-attachments/assets/62c464f0-410a-4786-acf4-73d5c2fae5f9" />

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

<img width="599" height="471" alt="Screenshot 2025-08-31 192829" src="https://github.com/user-attachments/assets/eb99ea52-d712-4818-a7bb-9e4f25c067b4" />


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
<img width="690" height="185" alt="Screenshot 2025-09-01 191447" src="https://github.com/user-attachments/assets/ef25341d-8fb7-4c4b-855f-66bb431550f4" />

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
<img width="622" height="151" alt="Screenshot 2025-09-01 192212" src="https://github.com/user-attachments/assets/c86c1e65-8073-4543-8b0a-199f3257b3e9" />

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
<img width="622" height="151" alt="Screenshot 2025-09-01 192212" src="https://github.com/user-attachments/assets/b879b637-cd54-4749-be7e-5b13609eaa64" />


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
<img width="622" height="151" alt="Screenshot 2025-09-01 192212" src="https://github.com/user-attachments/assets/e3da6377-bf3d-424b-a067-66124e87011f" />

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
 <img width="622" height="151" alt="Screenshot 2025-09-01 192212" src="https://github.com/user-attachments/assets/666e4775-603f-424c-90c2-127702c0a6b2" />

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
 <img width="622" height="151" alt="Screenshot 2025-09-01 192212" src="https://github.com/user-attachments/assets/30c36c54-f243-4832-8262-19ce15da3003" />

 
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
 
 <img width="622" height="151" alt="Screenshot 2025-09-01 192212" src="https://github.com/user-attachments/assets/c61fc222-7a48-4e13-afa5-582597be26b9" />

 
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
 <img width="653" height="299" alt="image" src="https://github.com/user-attachments/assets/e0fc7222-f2ea-4992-a243-74e6cd6e0c28" />

 
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
<img width="622" height="222" alt="image" src="https://github.com/user-attachments/assets/8bdd60e5-c26c-4993-9386-4c54dee37c60" />

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
<img width="622" height="222" alt="image" src="https://github.com/user-attachments/assets/d1355dbb-9f70-4cc0-b531-1b7943a95c85" />

 
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
 <img width="637" height="302" alt="image" src="https://github.com/user-attachments/assets/bcbfebde-bce3-42e9-802b-1239c199f129" />

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
<img width="653" height="299" alt="image" src="https://github.com/user-attachments/assets/e0fc7222-f2ea-4992-a243-74e6cd6e0c28" />
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
<img width="461" height="300" alt="image" src="https://github.com/user-attachments/assets/40ee67f3-d453-44ba-a327-62558bd6d875" />


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
<img width="400" height="226" alt="image" src="https://github.com/user-attachments/assets/3a0e0d5e-fdc0-4b1c-ad9c-6ba533de9a08" />

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
<img width="445" height="233" alt="image" src="https://github.com/user-attachments/assets/77776de6-949a-4a46-a2e0-59de1ef1d0ad" />

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

 <img width="435" height="376" alt="image" src="https://github.com/user-attachments/assets/98b3dd1c-6f7f-4384-8b01-8c9a6642cd14" />

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
 <img width="369" height="175" alt="image" src="https://github.com/user-attachments/assets/b136200d-7386-487a-b14e-b705e4865869" /> 

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
 <img width="390" height="230" alt="image" src="https://github.com/user-attachments/assets/e2c8d687-df10-42b4-9499-fa6bfeb74af5" />

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

<img width="412" height="158" alt="image" src="https://github.com/user-attachments/assets/381c8972-6d43-4ca1-bde6-8c0c1bdeb725" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="427" height="152" alt="image" src="https://github.com/user-attachments/assets/2c7ba546-f13a-4d12-99ec-0e3e55f18a26" />


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

 <img width="424" height="129" alt="image" src="https://github.com/user-attachments/assets/6b3fd3fe-fc9f-4ca4-8f51-f5d9be114993" />


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
 <img width="308" height="174" alt="image" src="https://github.com/user-attachments/assets/90e0690c-dd82-43da-9d17-c9c2f5e626e2" />

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
<img width="307" height="176" alt="image" src="https://github.com/user-attachments/assets/9216b73f-0c06-4fdc-b1bd-a4fd2a5b8f1f" />


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
 
 <img width="356" height="152" alt="image" src="https://github.com/user-attachments/assets/8ec272bc-545a-4086-8bf7-875903072587" />

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
 <img width="433" height="387" alt="image" src="https://github.com/user-attachments/assets/6b7d46e4-9965-40c5-a05e-bbfb6b0f90cb" />

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
<img width="754" height="180" alt="image" src="https://github.com/user-attachments/assets/0a7d142c-007b-43cd-86cc-94c5660c929c" />

<img width="396" height="124" alt="image" src="https://github.com/user-attachments/assets/3d8efde6-c264-471b-aaae-d34e9bf76fea" />

# RESULT:
The Commands are executed successfully.
