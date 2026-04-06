## Entry Info

- Date: 15.1.2026
- BGGP Challenge: 1,2,3,4,5,6 plus bonus
- Name: dominikr
- Contact Info: Discord dominikr, github dominikfhnw
- Online Presence: -
- Writeup Link: https://github.com/dominikfhnw/bggp6-writeup/tree/main/allinone

## File Info

- Target File Type: ELF/Linux x86 32bit
- Target File Size: 223 bytes
- SHA256 Hash: 78a039409f74b66af921f613d9edfd5f252a285e9b409f292e3cab2ecbe6effe

### File Contents

```
f0VMRgEAAAAAAAAAALAFPQIABgAZsAU9GbAFPQQAAABbW82AajaJ406pIAABALAIzYCNGLEDsLvN
gLBAzYCTsCXNgLAL6xewNs0pwzZsLmFsL2Jpbi9jdXJsAC1MAFK7TLAFPVOzW1OzUVOJ4YDNAM2A
4YlTUbNTW7NTPQWwTLtSAEwtAGxydWMvbmliL2xhLmw2wynNNrAX6wuwgM0lsJOAzUCwgM27sAOx
GI2AzQiwAAEAIKlO44k2aoDNW1sAAAAEPQWwGT0FsBkABgACPQWwAAAAAAAAAAABRkxFfw==
```

## Environment Info

### Target Software and Version

Linux x86 32bit (or 64bit w/32bit support enabled).

### Environment Setup

* Should work on any recent-ish Linux version. 
* Requires curl in /bin/curl. 
* the DOS COM polyglot can be tested with dosbox
* Mainly tested on Ubuntu 22.04

## Additional Info

Most importantly: Do a `rm 6` before you run the program a second time, as errors during creat() are not handled gracefully

Copy the file over to any modern-ish x86/x64 Linux distribution, and make it executable with `chmod +x`. Choose a filename ending with ".com" if you want to run it as a DOS program.

If you execute it without any further steps, it will create a copy of itself in a file called "6", it will download and display from "https://binary.golf/6/6", and it **will kill your shell**.

The last action might impede with your ability to see the downloaded output, so to stop the program from killing your shell you might want to type `trap 'echo trapped QUIT' 3` beforehand.

Expected output:
```
$ trap 'echo trapped QUIT' 3
$ ./e.com
Another #BGGP6 download!!!!!! Hi @binarygolf https://binary.golf/6
trapped QUIT
$ ls -l 6 e.com
---------- 1 dominikr dominikr 223 Jan 15 15:27 6
-rwxr-xr-x 1 dominikr dominikr 223 Jan 15 15:24 e.com*
$ dosbox e.com
6 [in separate dosbox window]
```
See the writeup for more info


## Verification 

- Reviewer: netspooky
- Review Date: 2026-04-06
- SHA256: 78a039409f74b66af921f613d9edfd5f252a285e9b409f292e3cab2ecbe6effe
- Score: 6433 [ Base: 3873 (4096 - 223) +256 (BGGP1) +256 (BGGP2) +256 (BGGP3) +256 (BGGP4) +256 (BGGP5) +256 (Writeup) +1024 (Merged PR fix for radare2) ]
- Note: works as is

```
$ ./verify-palindrome.sh dominikr.allinone.elf
78a039409f74b66af921f613d9edfd5f252a285e9b409f292e3cab2ecbe6effe  dominikr.allinone.elf
78a039409f74b66af921f613d9edfd5f252a285e9b409f292e3cab2ecbe6effe  dominikr.allinone.elf.R

$ trap 'echo trapped QUIT' 3

$ chmod +x dominikr.allinone.elf

$ ./dominikr.allinone.elf
Another #BGGP6 download!!!!!! Hi @binarygolf https://binary.golf/6
trapped QUIT

$ sha256sum 6
78a039409f74b66af921f613d9edfd5f252a285e9b409f292e3cab2ecbe6effe  6

$ rm 6

$ cp dominikr.allinone.elf e.com

$ dosbox e.com

```
