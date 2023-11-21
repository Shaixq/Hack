### Objetivos 
We have recovered a [binary](https://jupiter.challenges.picoctf.org/static/31c9b832d036a10daeef52d8b4290ef0/rev) and a [text file](https://jupiter.challenges.picoctf.org/static/31c9b832d036a10daeef52d8b4290ef0/rev_this). Can you reverse the flag.
### Solución 

```
┌──(kali㉿kali)-[~]
└─$ wget https://jupiter.challenges.picoctf.org/static/31c9b832d036a10daeef52d8b4290ef0/rev
--2023-11-07 16:10:46--  https://jupiter.challenges.picoctf.org/static/31c9b832d036a10daeef52d8b4290ef0/rev
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16856 (16K) [application/octet-stream]
Saving to: ‘rev’

rev                          100%[==============================================>]  16.46K  --.-KB/s    in 0.002s  

2023-11-07 16:10:47 (10.6 MB/s) - ‘rev’ saved [16856/16856]

                                                                                                                    
┌──(kali㉿kali)-[~]
└─$ wget https://jupiter.challenges.picoctf.org/static/31c9b832d036a10daeef52d8b4290ef0/rev_this
--2023-11-07 16:11:06--  https://jupiter.challenges.picoctf.org/static/31c9b832d036a10daeef52d8b4290ef0/rev_this
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 24 [application/octet-stream]
Saving to: ‘rev_this’

rev_this                     100%[==============================================>]      24  --.-KB/s    in 0s      

2023-11-07 16:11:07 (23.2 MB/s) - ‘rev_this’ saved [24/24]

                                                                                                                    
┌──(kali㉿kali)-[~]
└─$ cat rev_this 
picoCTF{w1{1wq85jc=2i0<}   

flag = ""

with open("rev_this","rb") as data:
        for i in range(8):
                flag += chr(data.read(1)[0])
        for i in range(8, 23):
                if (i & 1) == 0:
                        flag += chr(data.read(1)[0] - 5)
                else:
                        flag += chr(data.read(1)[0] + 2)
        flag += chr(data.read(1)[0])
print("Flag: {}".format(flag))

```

### Notas adicionales:
picoCTF{r3v3rs37ee84d27}
### Referencias: