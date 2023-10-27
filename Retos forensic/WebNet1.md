### Objetivos 

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.


### Solución 

```
┌──(kali㉿kali)-[~]
└─$ strings vulture.jpg -n15 
picoCTF{honey.roasted.peanuts}
 )/'%'/9339GDG]]}
 )/'%'/9339GDG]]}
%&'()*456789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz
&'()*56789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz



```

### Notas adicionales:
Utilizamos wireshark para desencriptar los paquetes y notamas que hay una imagen que se esta descargando la esxportamos y trabajamos con ella para obtener la bendera

picoCTF{honey.roasted.peanuts}
### Referencias:
