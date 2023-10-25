### Description
Decode this [message](https://jupiter.challenges.picoctf.org/static/d6fcea5e3c6433680ea4f914e24fab61/message.wav) from the moon
### Solución 

``` bash
└─$ sstv -d message.wav -o result.png
[sstv] Searching for calibration header... Found!    
[sstv] Detected SSTV mode Scottie 1
[sstv] Decoding image...                                            [####################################################################################################] 100%
[sstv] Drawing image data...
[sstv] ...Done!
```

### Notas adicionales:

picoCTF{beep_boop_im_in_space}