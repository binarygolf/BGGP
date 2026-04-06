## Entry Info

- Date: 17.1.2026
- BGGP Challenge: 5+6 or 4+6, depending on CLI arguments
- Name: dominikr
- Contact Info: Discord dominikr, github dominikfhnw
- Online Presence: -
- Writeup Link: https://github.com/dominikfhnw/bggp6-writeup/tree/main/download

## File Info

- Target File Type: ELF/Linux x86 32bit
- Target File Size: 45 bytes
- SHA256 Hash: bcd347dcf92545d711ef8d8a11b33ae10711bc6bd87d81f867f0dce9106f21a4

### File Contents

```
f0VMRgEAAAAAAAAAALALPQIAAwAZsAs9GbALPQQAAABeWYnhjRS0W82AIAAB
```

## Environment Info

### Target Software and Version

Linux x86 32bit (or 64bit w/32bit support enabled).

### Environment Setup

* Should work on any recent-ish Linux version. 
* Requires curl in /bin/curl. 
* Mainly tested on Ubuntu 22.04

## Additional Info

Copy the file over to any modern-ish x86/x64 Linux distribution, and make it executable with `chmod +x`.

BGGP5+6
```
$ ./argv /bin/curl -L https://binary.golf/6/6
Another #BGGP6 download!!!!!! Hi @binarygolf https://binary.golf/6
```

BGGP4+6:
```
$ ./argv /bin/cp -v argv 6
'argv' -> '6'
```

See the writeup for more info

## Verification 

- Reviewer: netspooky
- Review Date: 2026-04-06
- SHA256: bcd347dcf92545d711ef8d8a11b33ae10711bc6bd87d81f867f0dce9106f21a4
- Score: 4819 [ Base: 4051 (4096 - 45) +256 (BGGP4) +256 (BGGP5) +256 (Writeup) ]
- Note: works as is

```
$ chmod +x dominikr.dl.args.elf32

$ ./dominikr.dl.args.elf32 /bin/curl -L https://binary.golf/6/6
Another #BGGP6 download!!!!!! Hi @binarygolf https://binary.golf/6

$ ./dominikr.dl.args.elf32 /bin/cp dominikr.dl.args.elf32 6

$ ls -lah 6 dominikr.dl.args.elf32
-rwxrwxr-x 1 user user 45 Apr  6 13:18 6
-rwxrwxr-x 1 user user 45 Apr  6 13:14 dominikr.dl.args.elf32

$ sha256sum dominikr.dl.args.elf32
bcd347dcf92545d711ef8d8a11b33ae10711bc6bd87d81f867f0dce9106f21a4  dominikr.dl.args.elf32
```
