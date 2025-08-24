
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
<img width="321" height="103" alt="image" src="https://github.com/user-attachments/assets/fce49d35-52cb-43cb-aede-b8e4b7b0bbc4" />


cat < file2
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 30 20_912384da](https://github.com/user-attachments/assets/26ae4355-d2f1-4315-9a86-49f6c9c469c7)


# Comparing Files
cmp file1 file2
## OUTPUT

 ![WhatsApp Image 2025-08-22 at 16 30 22_4104e7d7](https://github.com/user-attachments/assets/d10628ec-7895-444f-9916-9f8f5c17a602)

comm file1 file2
 ## OUTPUT
<img width="321" height="103" alt="image" src="https://github.com/user-attachments/assets/e496db6e-7060-42bc-a0e1-ec74f7dea44e" />

 
diff file1 file2
## OUTPUT
<img width="321" height="103" alt="image" src="https://github.com/user-attachments/assets/a89b9fc6-9809-40ff-8b15-60cad2eee718" />


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

![WhatsApp Image 2025-08-22 at 16 30 21_98583ea1](https://github.com/user-attachments/assets/1187085e-0eb9-4455-8a28-ad28fef591d4)




cut -d "|" -f 1 file22
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 30 18_33bb04d7](https://github.com/user-attachments/assets/650a7509-590c-4805-a0ce-0d09d2df4771)



cut -d "|" -f 2 file22
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 30 17_1ec2117b](https://github.com/user-attachments/assets/c027e408-bedb-4733-92ac-3ec6d49a699a)


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world

## OUTPUT

![WhatsApp Image 2025-08-22 at 16 30 19_8249b8b6](https://github.com/user-attachments/assets/1e950096-b1de-436b-9931-cff77c1b506c)

 
grep Hello newfile 
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 30 15_f265f735](https://github.com/user-attachments/assets/28ebbfd0-7c3e-401c-b79e-e640106ee32b)



grep hello newfile 
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 30 18_5cb3c023](https://github.com/user-attachments/assets/e5ca6ea8-04d9-4045-991a-1be7cc79336f)





grep -v hello newfile 
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 30 12_dc14b8ea](https://github.com/user-attachments/assets/ff923bd9-b7d6-4f09-820d-20618396980d)



cat newfile | grep -i "hello"
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 30 12_93cd5fd0](https://github.com/user-attachments/assets/fcade02f-6209-4797-8654-e8632c0b3e85)




cat newfile | grep -i -c "hello"
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 30 11_bd3a9b76](https://github.com/user-attachments/assets/5598c70c-a93f-456f-a865-a525f5ac9c0c)




grep -R ubuntu /etc
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 30 13_9b90eb6b](https://github.com/user-attachments/assets/a03931a3-337c-4160-b951-4fd77cea0b2c)



grep -w -n world newfile   
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 30 14_599460d3](https://github.com/user-attachments/assets/20f83574-d45d-4e59-bc79-17c155a2b105)


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

![WhatsApp Image 2025-08-22 at 16 30 09_741455b0](https://github.com/user-attachments/assets/84cb6af2-71ff-4f05-8b08-c48509df89dc)



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="321" height="103" alt="image" src="https://github.com/user-attachments/assets/0c8c2265-31ce-4ac8-9a5a-10e36db40134" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 30 10_0bdd498c](https://github.com/user-attachments/assets/005f1dea-c624-4330-9c1e-bac217b77dde)




egrep '(^hello)' newfile 
## OUTPUT
![WhatsApp Image 2025-08-22 at 16 30 08_0a2b8580](https://github.com/user-attachments/assets/d44f0279-0bd0-4e36-b182-6a3af93c4d9f)



egrep '(world$)' newfile 
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 30 07_c182082b](https://github.com/user-attachments/assets/fc5241ef-7f20-446b-8437-e40b09e4f056)



egrep '(World$)' newfile 
## OUTPUT
<img width="321" height="103" alt="image" src="https://github.com/user-attachments/assets/02dbbb99-4033-4c74-b0d3-229bef2cf25a" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 30 06_60937eaf](https://github.com/user-attachments/assets/60f5d5f9-33a1-4599-a984-673edf6b2109)



egrep '[1-9]' newfile 
## OUTPUT
<img width="321" height="103" alt="image" src="https://github.com/user-attachments/assets/b190fcfc-703f-4b89-bf2a-58fa95251552" />



egrep 'Linux.*world' newfile 
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 30 05_14ac1a16](https://github.com/user-attachments/assets/e5476133-2e75-4152-8bd2-775a5be2f749)


egrep 'Linux.*World' newfile 
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 30 04_094b08b9](https://github.com/user-attachments/assets/32e35072-1d71-4272-9ad6-201fc45ff618)


egrep l{2} newfile
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 30 01_817c2507](https://github.com/user-attachments/assets/2276dcca-968d-4947-b677-8e12972aadd9)



egrep 's{1,2}' newfile
## OUTPUT 

![WhatsApp Image 2025-08-22 at 16 30 02_abb4ee9e](https://github.com/user-attachments/assets/85301c09-d7cd-4b4c-9333-5adab2fb268c)


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

![WhatsApp Image 2025-08-22 at 16 30 04_451460a0](https://github.com/user-attachments/assets/6628631c-9b55-425b-987d-343801573b44)



sed -n -e '$p' file23
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 30 00_18ae89ff](https://github.com/user-attachments/assets/f8f4d0f5-0aea-4acf-ba28-507fa33cd9c2)



sed  -e 's/Ram/Sita/' file23
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 30 01_3c0db1b0](https://github.com/user-attachments/assets/77bb55c8-7403-4f50-8616-9efa0b95ebe7)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 29 58_013a8aa1](https://github.com/user-attachments/assets/00f18754-508d-46b1-91cf-b3a39051fb60)



sed  '/tom/s/5000/6000/' file23
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 29 59_cea8826e](https://github.com/user-attachments/assets/16811a6c-4daf-4ec5-a176-a1fbdd605119)



sed -n -e '1,5p' file23
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 29 54_c5405a01](https://github.com/user-attachments/assets/e97017e7-6b08-4095-bb2e-e54181208efe)



sed -n -e '2,/Joe/p' file23
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 29 57_3efc2a08](https://github.com/user-attachments/assets/78616a39-7fd2-4543-8938-9c37675262e0)





sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 29 56_358bea9d](https://github.com/user-attachments/assets/6a785cc6-dfd5-48ee-a349-5495da63e5d4)



seq 10 
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 29 58_bafd0b6a](https://github.com/user-attachments/assets/861e245d-954e-432b-b884-8f1f0bdaeb87)



seq 10 | sed -n '4,6p'
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 29 53_e0eca603](https://github.com/user-attachments/assets/4f293daa-c9b2-4432-baee-6d05104f549d)



seq 10 | sed -n '2,~4p'
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 29 52_dfe12338](https://github.com/user-attachments/assets/4e19e849-12c0-4bcd-a3eb-360f9d796407)



seq 3 | sed '2a hello'
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 29 54_be07ce98](https://github.com/user-attachments/assets/329f68f4-fe62-46c3-a5f0-9361e6949f6a)




seq 2 | sed '2i hello'
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 29 51_fb5dbd02](https://github.com/user-attachments/assets/dcb216e6-97a2-4094-8d7c-93585adc57dc)



seq 10 | sed '2,9c hello'
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 29 51_03c70845](https://github.com/user-attachments/assets/a17a5ac9-4658-4666-9f26-149be47ddfd8)



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 29 50_49845ec4](https://github.com/user-attachments/assets/dbf5c4cf-4dfa-4e31-868a-30c9934b072d)




sed -n '2,4{s/$/*/;p}' file23
## OUTPUT:

![WhatsApp Image 2025-08-22 at 16 29 49_6952b9a6](https://github.com/user-attachments/assets/12444d14-158f-4a7a-be4a-146de9a053cf)


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

![WhatsApp Image 2025-08-22 at 16 29 48_d3372b4f](https://github.com/user-attachments/assets/87b8e64c-a1f5-4d0f-b04b-cfe9500c068e)


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

![WhatsApp Image 2025-08-22 at 16 29 49_f1d94a6b](https://github.com/user-attachments/assets/3094bba1-11c3-430b-9be8-d3fc3cb999c6)




#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 
 ![WhatsApp Image 2025-08-22 at 16 29 47_391166f0](https://github.com/user-attachments/assets/b1ce1547-1b29-40e0-a794-6f4e1f8da460)


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
 
![WhatsApp Image 2025-08-22 at 16 29 46_d08d5f3d](https://github.com/user-attachments/assets/edb79654-577c-4ef7-9107-20dd390f7032)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 29 46_dc5daa86](https://github.com/user-attachments/assets/f4c30f7b-cc2d-424a-bcae-da882014a3d0)



#Backup commands
tar -cvf backup.tar *
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 29 43_eff81a46](https://github.com/user-attachments/assets/771cc725-e864-43b0-af02-fa8c50ce8a0a)


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 29 44_c573cbad](https://github.com/user-attachments/assets/140b005f-ad7d-4826-a775-d74e714e3213)


tar -xvf backup.tar
## OUTPUT
![WhatsApp Image 2025-08-22 at 16 29 42_7fc7f885](https://github.com/user-attachments/assets/ff60bcb4-96ee-4a57-b6b2-cb5f69c76a3d)


gzip backup.tar

ls .gz
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 29 41_7b2154a9](https://github.com/user-attachments/assets/c14114a9-f386-4fbb-aa13-6fb9b68dd1a6)

 
gunzip backup.tar.gz
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 29 40_39cc98ba](https://github.com/user-attachments/assets/cae51602-46f5-4bb7-8ec5-cf7bfef02bb3)


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 29 40_b4564739](https://github.com/user-attachments/assets/6168975e-8ac3-4988-b4dc-3c4ddc4edd0f)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 29 39_fea07e26](https://github.com/user-attachments/assets/d1ecf0d7-b62c-4b45-ab8f-212b413bbe84)


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

![WhatsApp Image 2025-08-22 at 16 29 38_6947bbd4](https://github.com/user-attachments/assets/ee6aac57-3328-4617-b4aa-dec04bdca23a)

 
ls file1
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 29 37_d75612ec](https://github.com/user-attachments/assets/a3a9dd7a-7540-49e7-a639-ea3171aa69e3)

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

 ![WhatsApp Image 2025-08-22 at 16 29 36_101e3225](https://github.com/user-attachments/assets/2a04609d-41c7-4ab0-898e-835c3de5f762)

abcd
 
echo $?
 ## OUTPUT
 
![WhatsApp Image 2025-08-22 at 16 29 34_dab634b8](https://github.com/user-attachments/assets/a93421c0-20d9-4d3e-9f5c-8a7a3f9d9510)


 
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
# OUTPUT

![WhatsApp Image 2025-08-22 at 16 29 35_abbd3e1e](https://github.com/user-attachments/assets/f87a75ec-232c-4adc-a19e-f320a8416d9a)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 29 33_cf806432](https://github.com/user-attachments/assets/8fa3afe8-e842-4454-be88-4cf8f4f21759)


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

![WhatsApp Image 2025-08-22 at 16 29 32_0bd04e3b](https://github.com/user-attachments/assets/b28e6388-2376-48d3-b21a-7241101ad21f)


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

![WhatsApp Image 2025-08-22 at 16 29 28_370f33f1](https://github.com/user-attachments/assets/a4fb02e3-70ae-44dc-a719-e18fea64c087)


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

![WhatsApp Image 2025-08-22 at 16 29 30_72eef822](https://github.com/user-attachments/assets/ba525a46-3ba6-4f2e-9284-d64742fdbc03)



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

![WhatsApp Image 2025-08-22 at 16 29 28_370f33f1](https://github.com/user-attachments/assets/a4fb02e3-70ae-44dc-a719-e18fea64c087)

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

![WhatsApp Image 2025-08-22 at 16 29 28_5689ec93](https://github.com/user-attachments/assets/cb9898e7-1878-443b-8a0f-9d2d7ac564e0)


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
<img width="321" height="103" alt="image" src="https://github.com/user-attachments/assets/d91d2044-1d40-44c3-9cc9-b6652497edaf" />



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


![WhatsApp Image 2025-08-22 at 16 29 27_8392b87c](https://github.com/user-attachments/assets/b97842f8-731a-4c70-8515-c3d95c9f40ef)

 
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


![WhatsApp Image 2025-08-22 at 16 29 26_74475173](https://github.com/user-attachments/assets/00266e9f-2dd3-43bc-b2ba-bc1a4f0ab08f)

 
 
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


![WhatsApp Image 2025-08-22 at 16 29 25_4d901ee7](https://github.com/user-attachments/assets/a5f7fbbd-970b-41fb-a6ee-fe26199362f1)

 
 
 
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


![WhatsApp Image 2025-08-22 at 16 29 24_b84a76cb](https://github.com/user-attachments/assets/adbaaf2c-2cdb-4b22-ba5c-75677136c8d4)

 
 
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


![WhatsApp Image 2025-08-22 at 16 29 23_115bce0d](https://github.com/user-attachments/assets/321e380f-9e18-4501-8cdb-61705781cdd4)

 
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

cat forin3.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin3.sh

## OUTPUT

![WhatsApp Image 2025-08-22 at 16 29 23_55fb3120](https://github.com/user-attachments/assets/f189eee9-084a-4b31-934d-0eda24165458)

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

![WhatsApp Image 2025-08-22 at 16 29 22_dbe1e202](https://github.com/user-attachments/assets/07ddbd07-6eb4-47e4-98e2-2638d1bd15b3)


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

![WhatsApp Image 2025-08-22 at 16 29 19_c6856f8e](https://github.com/user-attachments/assets/d9fc4b77-4ba4-4320-aad4-caaa7a4fe559)


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
 
![WhatsApp Image 2025-08-22 at 16 29 16_c277fa90](https://github.com/user-attachments/assets/d59f8472-3353-4716-8a8a-0307430ced08)

 
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

![WhatsApp Image 2025-08-22 at 16 29 15_04580913](https://github.com/user-attachments/assets/74b2d98b-cb6a-43d4-a2d9-416106178252)

 
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

![WhatsApp Image 2025-08-22 at 16 29 14_55d62ee8](https://github.com/user-attachments/assets/1f780362-1011-4d9b-9581-63c1bb5cf54d)

 
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

![WhatsApp Image 2025-08-22 at 16 29 12_f7429422](https://github.com/user-attachments/assets/2d130d26-af88-476e-9a09-89839f993391)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![WhatsApp Image 2025-08-22 at 16 29 11_5f5ff99b](https://github.com/user-attachments/assets/56b9f902-80e0-4c3c-bd2e-000140357809)



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
$ ./argshift.sh 1 2 3
## OUTPUT

![WhatsApp Image 2025-08-22 at 16 29 00_b143a1ba](https://github.com/user-attachments/assets/ebebde04-8aed-44eb-b9e2-0af71e0d8eaf)

 
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

![WhatsApp Image 2025-08-22 at 16 28 58_222eb4e2](https://github.com/user-attachments/assets/31c79d7c-c520-4ae5-87e4-c1c59416c5c5)

 
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
 
 ![WhatsApp Image 2025-08-22 at 16 28 57_f4e6b8c6](https://github.com/user-attachments/assets/7ab2ee42-7463-4bda-9447-ad6c9a6357f4)

 
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

![WhatsApp Image 2025-08-22 at 16 28 56_7510a7ef](https://github.com/user-attachments/assets/c5fe83c3-ea7c-4542-981a-f7a14556b35a)

 
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

![WhatsApp Image 2025-08-22 at 16 28 53_8b93a2e0](https://github.com/user-attachments/assets/8a08408a-f685-4900-bca1-3da9d8d4b1ec)


# RESULT:
The Commands are executed successfully.
