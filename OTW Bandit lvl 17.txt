lvl 17 : There are two ways that i found out 
1. is using diff command 
command used diff passwords.new passwords.old 
2. is using piping 
cat passwords.new passwords.old | sort | uniq -u

but when you use both of the ways you will get two outputs.
The difference between the two ways is that the first output would be present in passwords.new as mentioned in the question. 
So the two passwords are :
hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
p6ggwdNHncnmCNxuAt0KtKVq185ZU7AW

So the password is : hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg