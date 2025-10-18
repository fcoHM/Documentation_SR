
## Description
You’re given a seemingly ordinary JPG image. Something is tucked away out of sight inside the file. Your task is to discover the hidden payload and extract the flag. Download the jpg image [here](https://challenge-files.picoctf.net/c_saffron_estate/10a2b19b0ab78b3de382d27358555a459e77fcf083d5da577bef1ad29b714576/img.jpg).

## Solution
1. Read its metadata and found in comment the following base64 `c3RlZ2hpZGU6Y0VGNmVuZHZjbVE9` code, we decode it and we find this once we decode it says `steghide:cEF6endvcmQ=`.
2. Then we re-decode the encoded part `cEF6endvcmQ=` and we found the key to use in a stenography decoder, key: `pAzzword`.
3. We upload the image and key to a decoder and we found the flag:

![](Pasted%20image%2020251005134042.png)

![](Pasted%20image%2020251005134025.png)


Flag: `picoCTF{h1dd3n_1n_1m4g3_f051f2e8}`
## Additional notes
## References
https://futureboy.us/stegano/decinput.html
