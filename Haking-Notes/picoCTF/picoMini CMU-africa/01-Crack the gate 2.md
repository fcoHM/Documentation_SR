
## Description
The login system has been upgraded with a basic rate-limiting mechanism that locks out repeated failed attempts from the same source. We’ve received a tip that the system might still trust user-controlled headers. Your objective is to bypass the rate-limiting restriction and log in using the known email address: **ctf-player@picoctf.org** and uncover the hidden secret.

Additional details will be available after launching your challenge instance.
## Solution
1. Intercept an attempt to login in with BurpSuite.
2. Craft a payload with several ips (19 in this case because there are 19 possible passwords) and with a Pitchfork attack we will iterate this ips in the header `X-Forwarded-For`.
	![](Pasted%20image%2020251005112425.png)
3. Craft a payload with the possible passwords:
![](Pasted%20image%2020251005112527.png)
4. Create a Grep Match by the keyword: *true*
![](Pasted%20image%2020251005112655.png)
5.  Do a Pitchfork attack and get the flag: `picoCTF{xff_byp4ss_brut3_f6cca7d4}`
![](Pasted%20image%2020251005112829.png)

## Additional notes
## References
https://www.typeerror.org/docs/http/headers/x-forwarded-for

