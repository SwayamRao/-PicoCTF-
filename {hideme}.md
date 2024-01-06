I first downloaded the flag given in the question.
Then I used the forencially website to extract the string inside the photo.
But there was nothing present except the content secret present in secret folder.
So I used a hex editor and then using the magic bits and saw 'PK' which is a zip file.
So I used binwalk to extract the files and got the flag.
reading resource for list signatures : https://en.wikipedia.org/wiki/List_of_file_signatures 

---------------------------
Flag : picoCTF{Hiddinng_An_imag3_within_@n_ima9e_8210824}
---------------------------
