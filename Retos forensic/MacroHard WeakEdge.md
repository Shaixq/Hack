### Objetivos 

I've hidden a flag in this file. Can you find it? [Forensics is fun.pptm](https://mercury.picoctf.net/static/d3dd8cd51524d9fafcccd1b7d55f85e7/Forensics%20is%20fun.pptm)
### Solución 

``` bash
┌──(kali㉿kali)-[~/…/notas-hacking/Utils/Actividad10/MacroHard]
└─$ unzip Forensics_is_fun.pptm 
┌──(kali㉿kali)-[~/…/notas-hacking/Utils/Actividad10/MacroHard]
└─$ ls    
'[Content_Types].xml'   docProps   Forensics_is_fun.pptm   ppt   _rels


┌──(kali㉿kali)-[~/…/notas-hacking/Utils/Actividad10/MacroHard]
└─$ ls    
'[Content_Types].xml'   docProps   Forensics_is_fun.pptm   ppt   _rels
                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/notas-hacking/Utils/Actividad10/MacroHard]
└─$ grep -r pico           
                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/notas-hacking/Utils/Actividad10/MacroHard]
└─$ 
                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/notas-hacking/Utils/Actividad10/MacroHard]
└─$ cd ppt      
                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/Utils/Actividad10/MacroHard/ppt]
└─$ ls
presentation.xml  presProps.xml  _rels  slideLayouts  slideMasters  slides  tableStyles.xml  theme  vbaProject.bin  viewProps.xml
                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/Utils/Actividad10/MacroHard/ppt]
└─$ cd slideMasters 
                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/Actividad10/MacroHard/ppt/slideMasters]
└─$ ls
hidden  _rels  slideMaster1.xml
                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/Actividad10/MacroHard/ppt/slideMasters]
└─$ cat hidden     
Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q                                                                                                                                                                                                                           
┌──(kali㉿kali)-[~/…/Actividad10/MacroHard/ppt/slideMasters]
└─$ echo  " Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q " | tr -d " " | base64 -d 
flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}base64: invalid input
```

### Notas adicionales:

picoCTF{D1d_u_kn0w_ppts_r_z1p5}base64

### Referencias: