https://play.picoctf.org/events/77/challenges/530?category=4&page=1
## Description
Hi, intrepid investigator! 📄🔍 You've stumbled upon a peculiar PDF filled with what seems like nothing more than garbled nonsense. But beware! Not everything is as it appears. Amidst the chaos lies a hidden treasure—an elusive flag waiting to be uncovered. Find the PDF file here [Hidden Confidential Document](https://challenge-files.picoctf.net/c_saffron_estate/ccc0d441aa5e523d76f4cddf3e8ef48763cb19abcc171a69ec743a958db3ee33/confidential.pdf) and uncover the flag within the metadata.
## Solution
1. We check the metadata of the pdf file and the author is in base64:
	![](Pasted%20image%2020251005115133.png)
2. Decode the text `echo cGljb0NURntwdXp6bDNkX20zdGFkYXRhX2YwdW5kIV84N2JlNjBjMH0= | base64 -d` and we found the flag `picoCTF{puzzl3d_m3tadata_f0und!_87be60c0}`

## Additional notes
## References

