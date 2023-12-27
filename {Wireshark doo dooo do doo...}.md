First download the file given in the question.
Then open wireshark and use the option open from the file.
There will be many http and tcp packets present in the file.
Now try searching all the packets.
In the http header most of the packets are kerberos encrypted.
But there are two files where only plain text is present.
Opening the first one will give the encrypted flag.

------------------------------------
Gur synt vf cvpbPGS{c33xno00_1_f33_h_qrnqorrs}
------------------------------------

Use rot13 to get the decrypted flag.

------------------------------------
Flag : The flag is picoCTF{p33kab00_1_s33_u_deadbeef}
------------------------------------
