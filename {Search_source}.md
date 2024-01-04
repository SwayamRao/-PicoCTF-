First we get a hint which is the developer has kept the flag in the source code.
After visiting the website we can obviously conclude that it would take ages to go and find the flag in individual pages.
Therefore here we use terminal that will search the flag in few seconds through the entire website.
So we first download the source code using 'wget -m <url>' option to get the source code.
Then we use grep to get the flag.
Command : grep -nr picoCTF .
Here -nr means it will search each line recursively which means it will go through all the directory and file and . is used to mention present directory.
After this u will get the flag easily.
-------------------------------------
Flag : picoCTF{1nsp3ti0n_0f_w3bpag3s_587d12b8}
-------------------------------------
