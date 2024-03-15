
Downloading the source code <br>
command :- `wget -o filename url`<br>
Viewing source code , we can exploit the user_buf and add some hexadecimal values which will print me the values present in stack.
using %x which is unsigned hex decimal I got <br>
`ocip{FTC0l_I4_t5m_ll0m_y_y3n5406d06dÿÅ}` which is not the flag.<br>
it should be changed in terms of 4 characters in order to get the flag

ocip -> pico

{FTC -> CTF{

0l_I -> I_l0

4_t5 -> 5t_4

m_ll -> ll_m

0m_y -> y_m0

_y3n -> n3y_

5406 -> 6045

d06d -> d60d

ÿÅ}  -> } gibrish
 
soo now we get the original flag

----------------------------------------
Flag :- picoCTF{I_l05t_4ll_my_m0n3y_6045d60d}
----------------------------------------