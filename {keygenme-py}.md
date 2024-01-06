I first saw the code where we need to input a character in order to start the operation.
And after analyzing the code the option which was related to flag was c.
I first found out that the length of flag would be key_full_template_trial.
{which was obvious}
Then I found that the dynamic part was going through the if case.
Then I copied the condition from the if statement to get the last dynamic part of the flag.

#code starts from here
bUsername_trial = b"ANDERSON"

print(hashlib.sha256(bUsername_trial).hexdigest()[4]) 
print(hashlib.sha256(bUsername_trial).hexdigest()[5])
print(hashlib.sha256(bUsername_trial).hexdigest()[3])
print(hashlib.sha256(bUsername_trial).hexdigest()[6])
print(hashlib.sha256(bUsername_trial).hexdigest()[2])
print(hashlib.sha256(bUsername_trial).hexdigest()[7])
print(hashlib.sha256(bUsername_trial).hexdigest()[1])
print(hashlib.sha256(bUsername_trial).hexdigest()[8])


Then add the result in the static part to obtain the overall flag 

------------------------------------------------
 Flag : picoCTF{1n_7h3_|<3y_of_01582419}
------------------------------------------------