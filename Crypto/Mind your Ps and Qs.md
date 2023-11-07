### Objetivos 
In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/b9ddda080c56fb421bf30409bec3460d/values)
### Solución 

```
└─$ python3
Python 3.11.4 (main, Jun  7 2023, 10:13:09) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> from Crypto.Util.number import inverse, long_to_bytes
>>> q = 650809615742055581459820253356987396346063
>>> p = 2434792384523484381583634042478415057961
>>> n = 1584586296183412107468474423529992275940096154074798537916936609523894209759157543
>>> e = 65537
>>> c = 964354128913912393938480857590969826308054462950561875638492039363373779803642185
>>> tn = (p-1) * (q-1)
>>> d = inverse(e, tn)
>>> m = pow(c,d,n)
>>> long_to_bytes(m)
b'picoCTF{sma11_N_n0_g0od_73918962}'
>>> 




```

### Notas adicionales:
Decrypt my super sick RSA:
c: 964354128913912393938480857590969826308054462950561875638492039363373779803642185
n: 1584586296183412107468474423529992275940096154074798537916936609523894209759157543
e: 65537

### Referencias: