In this lvl we need to manipulate the corrupted file so that it gives us the flag.<br>For that we first use online tool `hexedit` and see the struture of the image.<br>We then use online tool called `Photopea` to extract the image. <br>
We cane see that the image shows us a fake flag.<br>Now we increase the height of the image by changing the height value of the image using hexedit and then will view it in photopea, For that replace `32 01` to `6e 04` and save and view the image.<br>

----
Flag : picoCTF{qu1t3_a_v13w_2020}
----