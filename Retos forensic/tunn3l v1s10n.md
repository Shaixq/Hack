### Objetivos 

#### Description

We found this [file](https://mercury.picoctf.net/static/01be2b38ba97802285a451b94505ea75/tunn3l_v1s10n). Recover the flag.
### Solución 

``` bash
wget https://mercury.picoctf.net/static/01be2b38ba97802285a451b94505ea75/tunn3l_v1s10n
--2023-10-27 17:48:41--  https://mercury.picoctf.net/static/01be2b38ba97802285a451b94505ea75/tunn3l_v1s10n
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2893454 (2.8M) [application/octet-stream]
Saving to: ‘tunn3l_v1s10n’

tunn3l_v1s10n         100%[=========================>]   2.76M  2.83MB/s    in 1.0s    

2023-10-27 17:48:42 (2.83 MB/s) - ‘tunn3l_v1s10n’ saved [2893454/2893454]

                                                                                        
┌──(kali㉿kali)-[~]
└─$ file tunn3l_v1s10n 
tunn3l_v1s10n: data
                                                                                        
┌──(kali㉿kali)-[~]
└─$ hexeditor tunn3l_v1s10n 
                                                                                                                    
┌──(kali㉿kali)-[~]
└─$ mv tunn3l_v1s10n tunn3l_v1s10n.bmp
                                                                                                                    
┌──(kali㉿kali)-[~]
└─$ hexeditor tunn3l_v1s10n           
                                                                                                                    
┌──(kali㉿kali)-[~]
└─$ hexeditor tunn3l_v1s10n.bmp 
                                                                                                                    
┌──(kali㉿kali)-[~]
└─$ hexeditor tunn3l_v1s10n.bmp
                                                                                                                    
┌──(kali㉿kali)-[~]
└─$ hexeditor tunn3l_v1s10n.bmp
                                                                                                                    
┌──(kali㉿kali)-[~]
└─$ open tunn3l_v1s10n.bmp 

```

### Notas adicionales:



### Referencias: