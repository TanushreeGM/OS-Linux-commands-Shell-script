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
<img width="158" height="89" alt="image" src="https://github.com/user-attachments/assets/17156c0d-7493-43fb-95dc-a1a2b35860c6" />





cat < file2
## OUTPUT
<img width="173" height="102" alt="image" src="https://github.com/user-attachments/assets/1f85e6f3-47d9-44a9-aca2-9417a2e9b279" />



# Comparing Files
cmp file1 file2
## OUTPUT
<img width="277" height="49" alt="image" src="https://github.com/user-attachments/assets/e6908279-a8e3-430c-9b9e-1c76b6a525fa" />


comm file1 file2
 ## OUTPUT
 <img width="233" height="127" alt="image" src="https://github.com/user-attachments/assets/6925ae0b-a526-422c-803d-c1fbd81fe944" />

 
diff file1 file2
## OUTPUT
<img width="198" height="154" alt="image" src="https://github.com/user-attachments/assets/2d270602-5855-48d4-9668-cd570105c381" />


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
<img width="176" height="65" alt="image" src="https://github.com/user-attachments/assets/278c6156-ec4d-45c6-a4ca-ee08fe9d3cc2" />





cut -d "|" -f 1 file22
## OUTPUT
<img width="208" height="91" alt="image" src="https://github.com/user-attachments/assets/5d115ff8-5bca-4973-a32f-b600e9c3b9db" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="205" height="73" alt="image" src="https://github.com/user-attachments/assets/d2e9dcc3-ab6f-4c80-bf00-8f5a750f6617" />


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
<img width="175" height="58" alt="image" src="https://github.com/user-attachments/assets/7aae16a4-0ffe-4409-b89d-40665c75fbc3" />



grep hello newfile 
## OUTPUT
<img width="174" height="51" alt="image" src="https://github.com/user-attachments/assets/2c6e10c8-b515-4830-9daf-434411b9265b" />






grep -v hello newfile 
## OUTPUT
<img width="194" height="53" alt="image" src="https://github.com/user-attachments/assets/dee937dd-eee9-4f14-94f7-6aaff645bea9" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="238" height="56" alt="image" src="https://github.com/user-attachments/assets/648a4fee-7d5e-4445-b7ae-765efa472384" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="261" height="56" alt="image" src="https://github.com/user-attachments/assets/31afa3f1-b800-499a-86c9-805e77111706" />



grep -R ubuntu /etc
## OUTPUT
<img width="859" height="512" alt="image" src="https://github.com/user-attachments/assets/b388c8d3-de0e-42b7-a82f-bb39fbaf545a" />



grep -w -n world newfile   
## OUTPUT
<img width="220" height="64" alt="image" src="https://github.com/user-attachments/assets/bf960b56-8fe9-4ef3-844c-9609b74de3b0" />



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
<img width="278" height="74" alt="image" src="https://github.com/user-attachments/assets/93214282-2c9e-42a4-9d5c-eaf775fbd8bc" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="283" height="60" alt="image" src="https://github.com/user-attachments/assets/cb9ba261-2e88-43d8-8af3-32cf714aef66" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="266" height="71" alt="image" src="https://github.com/user-attachments/assets/983364b5-b8dd-4127-99d1-dab469b17294" />





egrep '(^hello)' newfile 
## OUTPUT
<img width="225" height="63" alt="image" src="https://github.com/user-attachments/assets/123cdc63-627d-4f0b-ad09-de994f06a7f3" />



egrep '(world$)' newfile 
## OUTPUT
<img width="222" height="63" alt="image" src="https://github.com/user-attachments/assets/b23ec14f-c4ef-4b17-96ea-282eeff2e2a3" />




egrep '(World$)' newfile 
## OUTPUT
<img width="203" height="65" alt="image" src="https://github.com/user-attachments/assets/b55131dc-b2ba-49bc-956d-706cceab67da" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="233" height="79" alt="image" src="https://github.com/user-attachments/assets/81ee7ebe-ac3e-4111-b89c-20cd4b1a314a" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="205" height="54" alt="image" src="https://github.com/user-attachments/assets/690a9b38-7895-44e2-9c62-342c1073de55" />





egrep 'Linux.*world' newfile 
## OUTPUT
<img width="234" height="54" alt="image" src="https://github.com/user-attachments/assets/4b958982-5202-42ee-96b6-9df6ea88b53c" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="225" height="47" alt="image" src="https://github.com/user-attachments/assets/bc762bc6-f091-4db0-935f-349835f3832f" />


egrep l{2} newfile
## OUTPUT
<img width="192" height="70" alt="image" src="https://github.com/user-attachments/assets/d803a3e7-0644-498e-a215-57009e3c7414" />



egrep 's{1,2}' newfile
## OUTPUT 

<img width="208" height="74" alt="image" src="https://github.com/user-attachments/assets/3d0eb262-e9ea-4b61-b6f2-e28d66d35670" />


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

<img width="187" height="58" alt="image" src="https://github.com/user-attachments/assets/80cd9972-74d5-4379-bed6-a8e05cbadcb9" />



sed -n -e '$p' file23
## OUTPUT

<img width="205" height="48" alt="image" src="https://github.com/user-attachments/assets/36383a48-d2a4-4a2b-b671-75e775cf2f99" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="263" height="142" alt="image" src="https://github.com/user-attachments/assets/968bfd52-573a-4d45-ac50-9f8e974a6e00" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="245" height="134" alt="image" src="https://github.com/user-attachments/assets/6f6b7baf-9669-47ea-a291-2f283f97c875" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="265" height="149" alt="image" src="https://github.com/user-attachments/assets/51368724-3dc5-41d2-ade4-06c0d4687cfe" />



sed -n -e '1,5p' file23
## OUTPUT



<img width="222" height="112" alt="image" src="https://github.com/user-attachments/assets/52a3dbb5-f92f-4cdd-b225-256aa7fdc566" />





sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="246" height="74" alt="image" src="https://github.com/user-attachments/assets/c2d2dd19-5aa3-4940-ac65-35d9e485903a" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="262" height="76" alt="image" src="https://github.com/user-attachments/assets/a413a9f7-bcd8-4721-a543-ec27be1993e1" />


seq 10 
## OUTPUT
<img width="191" height="166" alt="image" src="https://github.com/user-attachments/assets/9f8df675-8529-41c1-8da8-4390065f16ef" />




seq 10 | sed -n '4,6p'
## OUTPUT
<img width="202" height="75" alt="image" src="https://github.com/user-attachments/assets/71f09ee0-5797-42ec-abfc-648116605ccd" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="240" height="74" alt="image" src="https://github.com/user-attachments/assets/3128dc2c-c096-4601-99d9-2aea062ed146" />

seq 3 | sed '2a hello'
## OUTPUT
<img width="213" height="90" alt="image" src="https://github.com/user-attachments/assets/b85f113b-e34f-4595-97a0-e23678aa54e6" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="231" height="76" alt="image" src="https://github.com/user-attachments/assets/59472eca-e565-4da5-9f69-c1a7d82c542a" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="242" height="75" alt="image" src="https://github.com/user-attachments/assets/a9d36382-be3d-4e52-bc28-52c6de253a2c" />



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="256" height="82" alt="image" src="https://github.com/user-attachments/assets/42a75583-ad2a-47f9-b1cb-041fce6fc10a" />





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

<img width="213" height="107" alt="image" src="https://github.com/user-attachments/assets/be4ccafe-d1c4-4078-9ecc-7027401b16dd" />


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
<img width="229" height="112" alt="image" src="https://github.com/user-attachments/assets/e84020a7-909d-4899-ab75-2e49b504808d" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="298" height="148" alt="image" src="https://github.com/user-attachments/assets/b20fd4fd-ee4f-4627-a056-e8c7fafb4c3d" />

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

<img width="262" height="76" alt="image" src="https://github.com/user-attachments/assets/46a16182-6b55-4eac-9f3a-ed4ef26fc614" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="306" height="83" alt="image" src="https://github.com/user-attachments/assets/4dbafb6c-4f64-499c-9909-b0a4ca4bce98" />




#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="435" height="482" alt="image" src="https://github.com/user-attachments/assets/2ee63861-8207-4823-96c4-f912a4db36b4" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="684" height="437" alt="image" src="https://github.com/user-attachments/assets/cfc60ad4-eb17-4fdb-af0f-c677d03fbe78" />


tar -xvf backup.tar
## OUTPUT
<img width="454" height="433" alt="image" src="https://github.com/user-attachments/assets/5629ecf8-b22f-4ae7-b677-c5700208464d" />
<img width="250" height="144" alt="image" src="https://github.com/user-attachments/assets/64f9f6a4-c158-43f2-909a-ecc5d519fac6" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="205" height="100" alt="image" src="https://github.com/user-attachments/assets/e1582159-8f96-4447-b65a-9a2a4aeda10f" />

 
gunzip backup.tar.gz
## OUTPUT
<img width="823" height="174" alt="image" src="https://github.com/user-attachments/assets/fa95bd1b-526d-4115-b831-e570a53ec02f" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="375" height="279" alt="image" src="https://github.com/user-attachments/assets/61b33489-bf7c-4e38-a30a-fe53ac239e30" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="246" height="162" alt="image" src="https://github.com/user-attachments/assets/3830973c-cd5e-45b5-8035-28f386e5276c" />


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
<img width="310" height="430" alt="image" src="https://github.com/user-attachments/assets/7cc405b1-05f1-4978-ad65-edb875a949c3" />

 
ls file1
## OUTPUT
<img width="159" height="55" alt="image" src="https://github.com/user-attachments/assets/131b51f0-be35-4365-a75a-478efd7d2457" />

echo $?
## OUTPUT
<img width="212" height="53" alt="image" src="https://github.com/user-attachments/assets/0cce1ae3-35d1-4b51-8faf-d94e87e19c22" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="297" height="158" alt="image" src="https://github.com/user-attachments/assets/0ab28c4a-cbc1-44c7-8263-30ed192ae3de" />

abcd
 
echo $?
 ## OUTPUT
<img width="289" height="171" alt="image" src="https://github.com/user-attachments/assets/a6b37578-ee59-482a-8088-aa9ae5a647bd" />


 
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
## OUTPUT

<img width="261" height="162" alt="image" src="https://github.com/user-attachments/assets/ec05d9b7-d2ce-40a4-b058-c16b897bfdcc" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="340" height="111" alt="image" src="https://github.com/user-attachments/assets/f29ba8d7-2b69-412d-a7ed-b5997c7f2f5a" />


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
