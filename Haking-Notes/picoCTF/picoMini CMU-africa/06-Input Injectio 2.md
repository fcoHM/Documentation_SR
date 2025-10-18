https://play.picoctf.org/events/77/challenges/526?category=6&page=1
## Description
This program greets you and then runs a command. But can you take control of what command it executes? Connect to the program with netcat: `nc saffron-estate.picoctf.net 58119`. You can Download the program file [here](https://challenge-files.picoctf.net/c_saffron_estate/c22363524d7386b905cd485b62934708b299f9ab4dc2598cabb5d2e00c185e1c/vuln). And source [code](https://challenge-files.picoctf.net/c_saffron_estate/c22363524d7386b905cd485b62934708b299f9ab4dc2598cabb5d2e00c185e1c/vuln.c)
## Solution
1. We can observe this is a buffer overflow also. The allocation of memory doesn't look so adjacent. But our goal is to overwrite the variable shell using buffer overflow.
	![](Pasted%20image%2020251005152603.png)
2. Calculate the differences between address and craft a payload to just fill this difference (48 Bytes), after 48 bytes the variable shell allocation starts and we can start to overwrite it.
	```pwnedbyferpwnedbyferpwnedbyferpwnedbyferpwnedbyf[command]```

	1. First I listed all the files with `ls`
	2. Then I read the flag with `cat<flag.txt`

	![](../../Pasted%20image%2020251005152258.png)
We get the flag: `picoCTF{us3rn4m3_2_sh3ll_ac817f49}`
## Additional notes
## References

