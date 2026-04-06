## Entry Info

- Date: 17.1.2026
- BGGP Challenge: 3,4,5,6 
- Name: dominikr
- Contact Info: Discord dominikr, github dominikfhnw
- Online Presence: -
- Writeup Link: https://github.com/dominikfhnw/viert/blob/bggp6-release1/README.md


## File Info

- Target File Type: Forth source code
- Target File Size: 130 bytes
- SHA256 Hash: c33db4ee8d91c4716b31b30da51bb38332e10f30e03cb2baaead9f79375b72e2

- Target File Type: compiled ELF32 program
- Target File Size: 154 bytes
- SHA256 Hash: f889f4694929bdbc34f85dd111c0aca3373b623c4bf7c1c0ea10f2bd33c183ad 

### File Contents

Source:
```
OiBzIHN5c2NhbGwzIDsKOiB6IHN0cmluZzAgOwpyZHJvcCBpIDUgcyAwIDU0IHNwQCA4IHMgMTg3
IHMgNjQgcyA2IHN3YXAgMzcgcyAwIHogIjZsLmFsIiB6ICItTCIgZHVwIHNwQCAwIHN3YXAgeiAi
L2Jpbi9jdXJsIiAxMSBzCg==
```
Cleartext:
``` Forth
: s syscall3 ;
: z string0 ;
rdrop i 5 s 0 54 sp@ 8 s 187 s 64 s 6 swap 37 s 0 z "6l.al" z "-L" dup sp@ 0 swap z "/bin/curl" 11 s
```


Compiled:
```
f0VMRgEAAAAAAAAAAAABAAIAAwAgAAEAIAABAAQAAAC+XgABAInnKfSpIAABAKyNiDcAAQD/4a/r
9FhQUDHA6+1U6+qsVgHG6+SLB+vurOvrWlhS6+ZYW1lazYDr3gATFwUfFwAXNgoXCB8Xux8XQB8X
BhoXJR8XAA0GNmwuYWwADQMtTAADChcAGg0KL2Jpbi9jdXJsABcLHw==
```


## Environment Info

### Target Software and Version

The source code targets `viert`, my own Forth compiler, which in turn implements my own Forth dialect. It could work in other Forth dialects, as long as you implement either the `creat/open/sendfile/execve/getppid/kill` words in said Forth, or if you you implement the lower-level `syscall3` word.

The compiled output targets i386 Linux systems.

### Environment Setup

To be able to compile the source, download the `viert` release specifically made for BGGP6 from https://github.com/dominikfhnw/viert/releases/tag/bggp6-release1. You will also need nasm and perl; and curl when actually running the program.

The main branch, or even the bggp6 branch are not guaranteed to compile the source, as the language still changes very often at this point in development.

## Additional Info

From here on you can follow the README.md: compile with
```
$ bash bggp6.fth
```
or the minified version:
```
rm -rf ./6 && LIT8=1 ASM="i swap dup" FULL= TOS_ENABLE=0 ./optim.sh minified.fth
```

If you run the first option (bggp6.fth) it should execute the output ELF `viert` with strace:
```
     0.000000 [  59] [00007ffff7ceb08b] execve("./viert", ["./viert"], 0x7fffffffddb8 /* 39 vars */) = 0
     0.000732 [  59] [0001005c] [ Process PID=208660 runs in 32 bit mode. ]
     0.000033 [   5] [0001005c] open("./viert", O_RDONLY) = 3
     0.000234 [   8] [0001005c] creat("6", 066) = 4
     0.000403 [ 187] [0001005c] sendfile(4, 3, NULL, 65646) = 154
     0.000343 [  64] [0001005c] getppid() = 208657
     0.000334 [  37] [0001005c] kill(208657, SIGABRTbggp6.fth: line 1: 208657 Aborted                 (core dumped) setarch -R strace -b execve -rni ./viert
dominik@VM:~/test2-viert$ Another #BGGP6 download!!!!!! Hi @binarygolf https://binary.golf/6
```
Here you can see how it clones itself (BGGP4), kills its parent (BGGP3), and downloads (BGGP5). Strace gets killed while executing, so this is why you see the curl output *after* strace.



You can also compile issue #150: 
```
$ echo "6 ." > print6.fth
$ LIT8=1 PLUS=1 FULL= TOS_ENABLE=0 ./optim.sh print6.fth && strace -rni ./viert
....
-rwxr-xr-x 1 dominik dominik 180 Jan 17 15:10 viert
+ exit 0
     0.000000 [  59] [00007e80a5eeb08b] execve("./viert", ["./viert"], 0x7fff8ddc7d98 /* 39 vars */) = 0
     0.000796 [  59] [00010083] [ Process PID=209357 runs in 32 bit mode. ]
     0.000039 [   4] [00010083] write(1, "6", 16) = 1
     0.000255 [   4] [00010083] write(1, " ", 1 ) = 1
     0.000286 [   4] [00010035] --- SIGSEGV {si_signo=SIGSEGV, si_code=SEGV_MAPERR, si_addr=NULL} ---
     0.007815 [   4] [????????] +++ killed by SIGSEGV (core dumped) +++
Segmentation fault (core dumped)
```
It segfaults because it's missing an exit() syscall. The size is quite big, because the whole itoa() code gets compiled into it.

A program which just does an exit(6) is much smaller at 69 bytes:
```
$ echo "6 bye" > bye6.fth
$ ASM="bye" FULL= TOS_ENABLE=0 ./optim.sh bye6.fth && strace -rni ./viert
...
-rwxr-xr-x 1 dominik dominik 69 Jan 17 15:15 viert
+ exit 0
     0.000000 [  59] [00007ec049ceb08b] execve("./viert", ["./viert"], 0x7fffdddd3158 /* 39 vars */) = 0
     0.000837 [  59] [0001003c] [ Process PID=209691 runs in 32 bit mode. ]
     0.000040 [   1] [0001003c] exit(6) = ?
     0.000476 [   1] [????????] +++ exited with 6 +++
```

## Verification 

- Reviewer: netspooky
- Review Date: 2026-04-06
- SHA256: f889f4694929bdbc34f85dd111c0aca3373b623c4bf7c1c0ea10f2bd33c183ad
- Score: 4966 [ Base: 3942 (4096 - 154) +256 (BGGP3) +256 (BGGP4) +256 (BGGP5) +256 (Writeup) ]
- Note: works as is, note that the score is based on the final compiled elf, not the forth source code!

```
$ ./bggp6-elf
Another #BGGP6 download!!!!!! Hi @binarygolf https://binary.golf/6
Connection to 10.127.1.113 closed.

$ sha256sum bggp6-elf
f889f4694929bdbc34f85dd111c0aca3373b623c4bf7c1c0ea10f2bd33c183ad  bggp6-elf

$ sha256sum 6
f889f4694929bdbc34f85dd111c0aca3373b623c4bf7c1c0ea10f2bd33c183ad  6
```

