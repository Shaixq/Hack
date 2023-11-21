### Objetivos 
Can you get the flag?Download this [binary](https://artifacts.picoctf.net/c/87/gdbme).Here's the test drive instructions:

- `$ chmod +x gdbme`
- `$ gdb gdbme`
- `(gdb) layout asm`
- `(gdb) break *(main+99)`
- `(gdb) run`
- `(gdb) jump *(main+104)`
### Solución 

```

┌─────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┐
│    0x5555555552c7 <main>           endbr64                                                                                                                                                                              │
│    0x5555555552cb <main+4>         push   %rbp                                                                                                                                                                          │
│    0x5555555552cc <main+5>         mov    %rsp,%rbp                                                                                                                                                                     │
│    0x5555555552cf <main+8>         sub    $0x50,%rsp                                                                                                                                                                    │
│    0x5555555552d3 <main+12>        mov    %edi,-0x44(%rbp)                                                                                                                                                              │
│    0x5555555552d6 <main+15>        mov    %rsi,-0x50(%rbp)                                                                                                                                                              │
│    0x5555555552da <main+19>        mov    %fs:0x28,%rax                                                                                                                                                                 │
│    0x5555555552e3 <main+28>        mov    %rax,-0x8(%rbp)                                                                                                                                                               │
│    0x5555555552e7 <main+32>        xor    %eax,%eax                                                                                                                                                                     │
│    0x5555555552e9 <main+34>        movabs $0x4c75257240343a41,%rax                                                                                                                                                      │
│    0x5555555552f3 <main+44>        movabs $0x4362383846336235,%rdx                                                                                                                                                      │
│    0x5555555552fd <main+54>        mov    %rax,-0x30(%rbp)                                                                                                                                                              │
│    0x555555555301 <main+58>        mov    %rdx,-0x28(%rbp)                                                                                                                                                              │
│    0x555555555305 <main+62>        movabs $0x6630624760433530,%rax                                                                                                                                                      │
│    0x55555555530f <main+72>        movabs $0x4e64646267353361,%rdx                                                                                                                                                      │
│    0x555555555319 <main+82>        mov    %rax,-0x20(%rbp)                                                                                                                                                              │
│    0x55555555531d <main+86>        mov    %rdx,-0x18(%rbp)                                                                                                                                                              │
│    0x555555555321 <main+90>        movb   $0x0,-0x10(%rbp)                                                                                                                                                              │
│    0x555555555325 <main+94>        mov    $0x186a0,%edi                                                                                                                                                                 │
│B+  0x55555555532a <main+99>        call   0x555555555110 <sleep@plt>                                                                                                                                                    │
│    0x55555555532f <main+104>       lea    -0x30(%rbp),%rax                                                                                                                                                              │
│    0x555555555333 <main+108>       mov    %rax,%rsi                                                                                                                                                                     │
│    0x555555555336 <main+111>       mov    $0x0,%edi                                                                                                                                                                     │
│    0x55555555533b <main+116>       call   0x555555555209 <rotate_encrypt>                                                                                                                                               │
│    0x555555555340 <main+121>       mov    %rax,-0x38(%rbp)                                                                                                                                                              │
│    0x555555555344 <main+125>       mov    0x2cc5(%rip),%rdx        # 0x555555558010 <stdout@@GLIBC_2.2.5>                                                                                                               │
│    0x55555555534b <main+132>       mov    -0x38(%rbp),%rax                                                                                                                                                              │
│    0x55555555534f <main+136>       mov    %rdx,%rsi                                                                                                                                                                     │
│    0x555555555352 <main+139>       mov    %rax,%rdi                                                                                                                                                                     │
│    0x555555555355 <main+142>       call   0x5555555550f0 <fputs@plt>                                                                                                                                                    │
│    0x55555555535a <main+147>       mov    $0xa,%edi                                                                                                                                                                     │
│    0x55555555535f <main+152>       call   0x5555555550c0 <putchar@plt>                                                                                                                                                  │
│    0x555555555364 <main+157>       mov    -0x38(%rbp),%rax                                                                                                                                                              │
│    0x555555555368 <main+161>       mov    %rax,%rdi                                                                                                                                                                     │
└─────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┘
multi-thre No process In:                                                                                                                                                                                     L??   PC: ?? 
(gdb) break *(main+99)
Breakpoint 1 at 0x132a
(gdb) run
Starting program: /home/kali/Documents/CiberSeguridad/notas-hacking/Utils/Actividad16/gdbme
[Thread debugging using libthread_db enabled]
Using host libthread_db library "/lib/x86_64-linux-gnu/libthread_db.so.1".

Breakpoint 1, 0x000055555555532a in main ()
(gdb) jump *(main+104)
Continuing at 0x55555555532f.
picoCTF{d3bugg3r_dr1v3_7776d758}
(gdb) ior 1 (process 11572) exited normally]


```

### Notas adicionales:

picoCTF{d3bugg3r_dr1v3_7776d758}
### Referencias: