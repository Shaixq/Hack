### Objetivos 
How about some hide and seek heh?Look at this image [here](https://artifacts.picoctf.net/c/239/atbash.jpg).
### Solución 

```

┌──(kali㉿kali)-[~]
└─$ apt-get install steghide
E: Could not open lock file /var/lib/dpkg/lock-frontend - open (13: Permission denied)
E: Unable to acquire the dpkg frontend lock (/var/lib/dpkg/lock-frontend), are you root?
                                                                                                                   
┌──(kali㉿kali)-[~]
└─$ pip install steghide 
Defaulting to user installation because normal site-packages is not writeable
ERROR: Could not find a version that satisfies the requirement steghide (from versions: none)
ERROR: No matching distribution found for steghide
                                                                                                                   
┌──(kali㉿kali)-[~]
└─$ 






┌──(kali㉿kali)-[~]
└─$ sudo apt-get install steghide -y
[sudo] password for kali: 
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
E: Unable to locate package steghide
                                                                                                                   
┌──(kali㉿kali)-[~]
└─$ apt-get install steghide        
E: Could not open lock file /var/lib/dpkg/lock-frontend - open (13: Permission denied)
E: Unable to acquire the dpkg frontend lock (/var/lib/dpkg/lock-frontend), are you root?
                                                                                                                   
┌──(kali㉿kali)-[~]
└─$ sudo apt install steghide       
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
E: Unable to locate package steghide
                                                                                                                   
┌──(kali㉿kali)-[~]
└─$ which steghide
steghide not found
                                                                                                                   

┌──(kali㉿kali)-[~]
└─$ echo "deb http://http.kali.org/kali kali-rolling main non-free contrib" | sudo tee /etc/apt/sources.list
deb http://http.kali.org/kali kali-rolling main non-free contrib
                                                                                                                   
┌──(kali㉿kali)-[~]
└─$ sudo apt-get update
Get:1 http://kali.download/kali kali-rolling InRelease [41.2 kB]
Get:2 http://kali.download/kali kali-rolling/main amd64 Packages [19.5 MB]
Get:3 http://kali.download/kali kali-rolling/main amd64 Contents (deb) [45.9 MB]                                  
Get:4 http://kali.download/kali kali-rolling/non-free amd64 Packages [226 kB]                                     
Get:5 http://kali.download/kali kali-rolling/non-free amd64 Contents (deb) [913 kB]                               
Get:6 http://kali.download/kali kali-rolling/contrib amd64 Packages [122 kB]                                      
Get:7 http://kali.download/kali kali-rolling/contrib amd64 Contents (deb) [285 kB]                                
Fetched 67.0 MB in 54s (1,250 kB/s)                                                                               
Reading package lists... Done
                                                                                                                   
┌──(kali㉿kali)-[~]
└─$ sudo apt-get install steghide -y                                                              
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following additional packages will be installed:
  libmcrypt4 libmhash2
Suggested packages:
  libmcrypt-dev mcrypt
The following NEW packages will be installed:
  libmcrypt4 libmhash2 steghide
0 upgraded, 3 newly installed, 0 to remove and 1014 not upgraded.
Need to get 311 kB of archives.
After this operation, 907 kB of additional disk space will be used.
Get:1 http://kali.download/kali kali-rolling/main amd64 libmcrypt4 amd64 2.5.8-7 [72.6 kB]
Get:2 http://kali.download/kali kali-rolling/main amd64 libmhash2 amd64 0.9.9.9-9 [94.2 kB]
Get:3 http://kali.download/kali kali-rolling/main amd64 steghide amd64 0.5.1-15 [144 kB]
Fetched 311 kB in 33s (9,320 B/s)
Selecting previously unselected package libmcrypt4.
(Reading database ... 398533 files and directories currently installed.)
Preparing to unpack .../libmcrypt4_2.5.8-7_amd64.deb ...
Unpacking libmcrypt4 (2.5.8-7) ...
Selecting previously unselected package libmhash2:amd64.
Preparing to unpack .../libmhash2_0.9.9.9-9_amd64.deb ...
Unpacking libmhash2:amd64 (0.9.9.9-9) ...
Selecting previously unselected package steghide.
Preparing to unpack .../steghide_0.5.1-15_amd64.deb ...
Unpacking steghide (0.5.1-15) ...
Setting up libmhash2:amd64 (0.9.9.9-9) ...
Setting up libmcrypt4 (2.5.8-7) ...
Setting up steghide (0.5.1-15) ...
Processing triggers for libc-bin (2.37-6) ...
Processing triggers for man-db (2.11.2-3) ...
Processing triggers for kali-menu (2023.4.3) ...
                                                                                                                   
┌──(kali㉿kali)-[~]
└─$ cd Downloads 
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads]
└─$ steghide info atbash.jpg 
"atbash.jpg":
  format: jpeg
  capacity: 2.4 KB
Try to get information about embedded data ? (y/n) y
Enter passphrase: 
  embedded file "encrypted.txt":
    size: 31.0 Byte
    encrypted: rijndael-128, cbc
    compressed: yes
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads]
└─$ steghide extract -sf atbash.jpg -xf datos.txt
Enter passphrase: 
wrote extracted data to "datos.txt".
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads]
└─$ cat datos.txt                  
krxlXGU{zgyzhs_xizxp_1u84w779}
                                                                                                                    


```

### Notas adicionales:

picoCTF{atbash_crack_1f84d779}
### Referencias: