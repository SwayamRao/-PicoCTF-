In this level we first got the credentials for the username and password.
Then we need to use burpsuite to intercept the requests.
First there were no nothing suspecious but when we first forward the request we get a suspecious get request which might be base64 encoded.
cGljb0NURntwcm94aWVzX2Fs This was what I found on the first request.
After decoding it using codechef or base64 decoder we get 
picoCTF{proxies_al
I got another base64 encoded request which was bF90aGVfd2F5X2QxYzBiMTEyfQ
which was l_the_way_d1c0b112}.
So I combined both the flags to get main flag. 

-----------------------------
Flag : picoCTF{proxies_all_the_way_d1c0b112}
-----------------------------
