https://play.picoctf.org/events/77/challenges/525?page=1
## Description
A friendly program wants to greet you… but its goodbye might say more than it should. Can you convince it to reveal the flag? connect to the challenge instance `nc saffron-estate.picoctf.net 52174`. You can Download the program file [here](https://challenge-files.picoctf.net/c_saffron_estate/32203434ff8bd03bc7b333c2531d5f33424f12623b5846b67f92f12485f9712d/vuln). And source [code](https://challenge-files.picoctf.net/c_saffron_estate/32203434ff8bd03bc7b333c2531d5f33424f12623b5846b67f92f12485f9712d/vuln.c)
## Solution
1. Looking at the source code we can see that this is a stack buffer overflow.
	![](Pasted%20image%2020251005143513.png)
	We need to craft a payload that overflows the variable "buffer" to be able to write in the "c" that is used in system(), the function that executes commands.
2. We use this payload:
	```pwnedbyfercat *```
		name will cointain 10 bytes \[pwnedbyfer\] and c will contail \[cat \*\] :
		![](Pasted%20image%2020251005143839.png)
3. Flag: `picoCTF{0v3rfl0w_c0mm4nd_a9259e7a}` 
## Additional notes
## References
https://en.wikipedia.org/wiki/Stack_buffer_overflow

