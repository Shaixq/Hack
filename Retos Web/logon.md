### Objetivos 
The factory is hiding things from all of its users. Can you login as Joe and find what they've been looking at? `https://jupiter.challenges.picoctf.org/problem/13594/` ([link](https://jupiter.challenges.picoctf.org/problem/13594/)) or http://jupiter.challenges.picoctf.org:13594

### Solución 

``` bash
Agregar la extensión de cookies en el navegador y cambiar los permisos del usario, como a un administrador, cambiando el false a true
  //
Poner el link proporcionado y agregarle /flag -H "Cookie: admin=true" y nos muestra la bandera
```

### Notas adicionales:


picoCTF{th3_c0nsp1r4cy_l1v3s_d1c24fef}
### Referencias: