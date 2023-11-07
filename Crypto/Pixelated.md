### Objetivos 
I have these 2 images, can you make a flag out of them? [scrambled1.png](https://mercury.picoctf.net/static/49743139fb7c10765dbf462d40987d2a/scrambled1.png) [scrambled2.png](https://mercury.picoctf.net/static/49743139fb7c10765dbf462d40987d2a/scrambled2.png)

### Solución 

```
┌──(kali㉿kali)-[~/Downloads]
└─$ cd /opt                                                               
                                                                                                                   
┌──(kali㉿kali)-[/opt]
└─$ sudo wget http://www.caesum.com/handbook/Stegsolve.jar -O stegsolve.jar
--2023-11-07 13:53:31--  http://www.caesum.com/handbook/Stegsolve.jar
Resolving www.caesum.com (www.caesum.com)... 216.234.165.33
Connecting to www.caesum.com (www.caesum.com)|216.234.165.33|:80... connected.
HTTP request sent, awaiting response... 200 OK
Length: 312271 (305K) [application/x-java-archive]
Saving to: ‘stegsolve.jar’

stegsolve.jar                100%[=============================================>] 304.95K   170KB/s    in 1.8s    

2023-11-07 13:53:33 (170 KB/s) - ‘stegsolve.jar’ saved [312271/312271]

                                                                                                                   
┌──(kali㉿kali)-[/opt]
└─$ sudo  chmod +x stegsolve.jar                                           
                                                                                                                   
┌──(kali㉿kali)-[/opt]
└─$ cd ..  
                                                                                                                   
┌──(kali㉿kali)-[/]
└─$ cd   
                                                                                                                   
┌──(kali㉿kali)-[~]
└─$ 

┌──(kali㉿kali)-[~]
└─$ cd Downloads 
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads]
└─$ java -jar /opt/stegsolve.jar 
Picked up _JAVA_OPTIONS: -Dawt.useSystemAAFontSettings=on -Dswing.aatext=true





```

### Notas adicionales:
picoCTF{2a4d45c7}


### Referencias: