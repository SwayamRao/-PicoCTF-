lvl 16 : In this lvl we need to use nmap to first discover the ports which will send us the desired ouput. 
For this we use command : nmap -sV -T4 localhost -p 31000-32000

description about the command : 
      -sV is used to detect version 
      -T4 is an aggresive post scanning technique 
      -p is used to give the ports u want to do the scanning in 

This command would take some time to run roughly 90-130 secs.
You would get a output like this

PORT      STATE SERVICE     VERSION
31046/tcp open  echo
31518/tcp open  ssl/echo
31691/tcp open  echo
31790/tcp open  ssl/unknown
31960/tcp open  echo
We can use port 31790 to get the output.

Now we have to use ssl as previously did to get the output.
The output is an RSA private key.

Now we have to make a new directory "tmp" as we cannot use the home directory.
Follow the following commands :

bandit16@bandit:~$ mkdir /tmp/random_key
bandit16@bandit:~$ cd /tmp/random_key
bandit16@bandit:/tmp/random_key$ touch private.key
copy paste the private RSA key to private.key
bandit16@bandit:/tmp/random_key$ vim private.key

bandit16@bandit:/tmp/random_key$ chmod 400 private.key

chmod 400 is an important step here as this modifies the bits.
{ It would be better to go through this topic once. }

chmod sets permissions so that User / owner can read, can't write and can't execute. Group can't read, can't write and can't execute. Others can't read, can't write and can't execute.

then we use ls -l to see the required changes 

-r-------- 1 bandit16 bandit16 xxxx Xxx xx xx:xx private.key

{ output should be something like this . }

now this would act as our password for username "bandit17" 
command used : ssh bandit17@localhost -i private.key -p 2220

-p is used to specify port for which we are trying ssh connection 
-i is used to specify the file name
You will get the bandit17 username access.

