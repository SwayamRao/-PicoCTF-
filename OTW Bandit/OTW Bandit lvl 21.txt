lvl 21 : For this lvl first we need to understand about daemons.
It is basically a program which runs continuosly in the background.
{For better understanding reading this would be useful : https://www.techtarget.com/whatis/definition/daemon}
Now , cron is also a daemon, to check this we use command :
whatis cron
Then it would be helpful to understand the crontable which basically tells us about the cron schedules.
The shortform of crontable is used which is crontab.
Now coming back to the question 

First we list out the things using command : 
 ls /etc/cron.d/

Then we use cat command to see whats inside the cronjob_bandit22 using command : 
 cat /etc/cron.d/cronjob_bandit22

We can see that the file is running a shell script which is cronjob_bandit22.sh which is executed every second.
{The 1st * represnt the command to execute every second and the secound represnts about hour and soo on. }
{Reading material for the above : https://www.howtogeek.com/devops/what-is-a-cron-job-and-how-do-you-use-them/}

Then we sould see what the cronjob is actually doing using command : 
 cat /usr/bin/cronjob_bandit22.sh

Note: All executable files are present in /usr/bin

then we see that it is creating a file called t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv {which might be differnt for your case}
So the password is getting stored there 
There to view the password use command : cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv

Password : WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff
 

