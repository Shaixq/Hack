#### Description

Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:45028/](http://mercury.picoctf.net:45028/)

### Solución 

``` bash
┌──(kali㉿kali)-[~]
└─$ curl -I  http://mercury.picoctf.net:45028/
HTTP/1.1 200 OK
flag: picoCTF{r3j3ct_th3_du4l1ty_775f2530}
Content-type: text/html; charset=UTF-8

```

### Notas adicionales:

picoCTF{r3j3ct_th3_du4l1ty_775f2530}