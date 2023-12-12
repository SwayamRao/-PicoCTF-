lvl 19 : This level can be tackled by knowing about the privilages in linux

use command : ls -l     to know about the privilages about the file.

We can notice that the file has an s.
s stands for setuid. It will be present only in executable files.
setuid is used to set permissions for owner/user only.
Similar to setuid we have setgid, which by now you might have guessed it , sets permissions for Groupid.

then use :
          ls /etc/bandit_pass
to get list

then use 

./bandit20-do cat /etc/bandit_pass/bandit20
to get the Password { Here we access as Bandit20 to get the Password }

Password : VxCazJaVykI6W36BkBU0mJTCM8rR95XT


To understand this level , lets first understand whats really happening.
Basically the file Bandit20.do is given an s instead of x and when we do ls -l we can deduce that
the file can only be run with the permissions of user Bandit20 but we are Bandit19 therefore we cannot read the Password.
So we access as Bandit20 and cat the password to get the password.