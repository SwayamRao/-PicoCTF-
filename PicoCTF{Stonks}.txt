Description
I decided to try something noone else has before. I made a bot to automatically trade stonks for me using AI and machine learning. I wouldn't believe you if you told me it's unsecure! 
vuln.c // link to the source code
 nc mercury.picoctf.net 20195 // link to the working code

Solution :-
Downloading the source code 
command :- wget -o filename url
Viewing source code , we can exploit the user_buf and add some hexadecimal values which will print me the values present in stack.
using %x which is unsigned hex decimal I got 
ocip{FTC0l_I4_t5m_ll0m_y_y3n5406d06dÿÅ} which is not the flag.
it should be changed in terms of 4 characters in order to get the flag

ocip  pico
{FTC  CTF{
0l_I  I_l0
4_t5  5t_4
m_ll  ll_m
0m_y  y_m0
_y3n  n3y_
5406  6045
d06d  d60d
ÿÅ}   } gibrish
 
soo now we get the original flag :- picoCTF{I_l05t_4ll_my_m0n3y_6045d60d}