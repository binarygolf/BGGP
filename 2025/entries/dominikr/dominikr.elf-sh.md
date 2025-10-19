## Entry Info

- Date: 18.10.2025
- BGGP Challenge: 2 & 6
- Name: dominikr
- Contact Info: discord @dominikr, github dominikfhnw
- Online Presence: -
- Writeup Link: https://gist.github.com/dominikfhnw/5cf86ce2c7b539a910f6c26307d0a5ab (still tbd)


## File Info

- Target File Type: ELF/Linux x86 32bit, and shellscript
- Target File Size: 64 bytes
- SHA256 Hash: 62ad69b736a11f1a385061130b7784e2a0d7ccc57555dfa536025139110a4d4a

### File Contents

_Please encode the file as Base64_

```
f0VMRjtleGl0IDYKajbrBAIAAwCwBOsgDEAgACAAAAABAAAAAAAAAABAIAABAEFBQAAAAEAAAACJ
4UJDzYDr+w==
```

## Environment Info

### Target Software and Version

Linux x86 32 bit (tested with 6.6 kernel), and shellscript/bash (tested with 5.1.16), and other shells

### Environment Setup

_Description of Target Software's Environment (Platform/OS, Setup Instructions, etc.)_

The ELF should work on any x86 Linux distro from the last few years (must support ELF, so has to be newer than ~1995), including x86_64 with 32-bit support enabled

The following shells are supported for the shellscript polyglot:
* busybox ash
* zsh
* ksh93 
* mksh 
* yash 
* dash 
* posh 
* csh 
* tcsh 
* bash version 5.1 and before

The following shells are NOT supported:
* bash version 5.2 and above

Primarily tested on Ubuntu 22.04 LTS, and bash 5.1.16

## Additional Info

_Here attach any additional information about the file, including supporting notes, screenshots, videos, console output, etc._

The ELF binary prints "6" and returns with exit code 2, fulfilling both the requirements from BGGP2 and BGGP6:
```
$ strace -rni ./bin
     0.000000 [  59] [000073ab39eeef3b] execve("./bin", ["./bin"], 0x7ffc1cdf2448 /* 24 vars */) = 0
     0.006834 [  59] [0020403e] [ Process PID=14392 runs in 32 bit mode. ]
     0.000030 [   4] [0020403e] write(1, "6", 16) = 1
     0.000142 [   1] [0020403e] exit(2) = ?
     0.000087 [   1] [????????] +++ exited with 2 +++
```

The shellscript returns with exit code 6, and prints a message about not finding a binary called `ELF` or similar (exact message depends on shell being used and locale):
```
$ dash -x ./bin
+ ELF
./bin: 1: ELF: not found
+ exit 6
```
Bash has heuristics to differentiate shell scripts from binary files, so the first 'line' of the ELF binary (i.e. up to the first newline) must not contain any null bytes. That is, up to bash version 5.2, where an explicit check for ELF files was added. Bummer, I did not know that when I wrote the first submission entry. More info will follow in the writeup.

bash 5.2 has stopped any ELF/shellscript shenanigans, due to this change: https://github.com/bminor/bash/blame/master/general.c#L724

## Verification 

- Reviewer: netspooky
- Review Date: 2025-10-19
- SHA256: 62ad69b736a11f1a385061130b7784e2a0d7ccc57555dfa536025139110a4d4a
- Score: 4032
- Note: works as is, tested on Ubuntu 22.04 and bash 5.1.16(1)-release


