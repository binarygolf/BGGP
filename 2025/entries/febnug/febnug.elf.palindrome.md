## Entry Info

- Date: 25/10/2025
- BGGP Challenge: 1 & 6
- Name: febnug 
- Contact Info: 
- Online Presence: 
- Writeup Link: [https://github.com/febnug/bggp6-writeup/blob/main/palindrome.md](url)


## File Info

- Target File Type: ELF
- Target File Size: 228
- SHA256 Hash: 1bdad60c5e604965bb7dceec968a51862f4fb19eb20c3535b06c66773f427fa6

### File Contents

_Please encode the file as Base64_

```
f0VMRgEBAQAAAAAAAAAAAAIAAwABAAAAVIAECDQAAAAAAAAAAAAAADQAIAABAAAAAAAAAAEAAAAAAAAAAIAECACABAjkAAAA5AAAAAUAAAAAEAAAZmg2CjHAsAQx27MBieEx0rICzYAxwLABMduzBs2AgM0Gs9sxAbDAMYDNArLSMeGJAbPbMQSwwDEKNmhmAAAQAAAAAAUAAADkAAAA5AgEgAAIBIAAAAAAAAAAAAEAAAAAAAAAAQAgADQAAAAAAAAAAAAAADQIBIBUAAAAAQADAAIAAAAAAAAAAAABAQFGTEV/
```

## Environment Info

### Target Software and Version
ELF x86
### Environment Setup

_Description of Target Software's Environment (Platform/OS, Setup Instructions, etc.)_

No dependencies here, just make it the binary as executable, <code>chmod +x febnug.bggp6</code> and run it

```
febri@ubuntu:~/project/bggp6$ ./febnug.bggp6 
6
febri@ubuntu:~/project/bggp6$ echo $?
6
febri@ubuntu:~/project/bggp6$
```

## Additional Info

_Here attach any additional information about the file, including supporting notes, screenshots, videos, console output, etc._

Hexdump output of the binary:

```
febri@ubuntu:~/project/bggp6$ hexdump -C febnug.bggp6 
00000000  7f 45 4c 46 01 01 01 00  00 00 00 00 00 00 00 00  |.ELF............|
00000010  02 00 03 00 01 00 00 00  54 80 04 08 34 00 00 00  |........T...4...|
00000020  00 00 00 00 00 00 00 00  34 00 20 00 01 00 00 00  |........4. .....|
00000030  00 00 00 00 01 00 00 00  00 00 00 00 00 80 04 08  |................|
00000040  00 80 04 08 e4 00 00 00  e4 00 00 00 05 00 00 00  |................|
00000050  00 10 00 00 66 68 36 0a  31 c0 b0 04 31 db b3 01  |....fh6.1...1...|
00000060  89 e1 31 d2 b2 02 cd 80  31 c0 b0 01 31 db b3 06  |..1.....1...1...|
00000070  cd 80 80 cd 06 b3 db 31  01 b0 c0 31 80 cd 02 b2  |.......1...1....|
00000080  d2 31 e1 89 01 b3 db 31  04 b0 c0 31 0a 36 68 66  |.1.....1...1.6hf|
00000090  00 00 10 00 00 00 00 05  00 00 00 e4 00 00 00 e4  |................|
000000a0  08 04 80 00 08 04 80 00  00 00 00 00 00 00 00 01  |................|
000000b0  00 00 00 00 00 00 00 01  00 20 00 34 00 00 00 00  |......... .4....|
000000c0  00 00 00 00 00 00 00 34  08 04 80 54 00 00 00 01  |.......4...T....|
000000d0  00 03 00 02 00 00 00 00  00 00 00 00 00 01 01 01  |................|
000000e0  46 4c 45 7f                                       |FLE.|
000000e4
febri@ubuntu:~/project/bggp6$
```

NOTE: If this is an update to an existing entry, please include a link to your entry below this text. Reminder that authors can only update an entry once during BGGP.


## Verification 

- Reviewer: netspooky
- Review Date: 2026-04-06
- SHA256: 1bdad60c5e604965bb7dceec968a51862f4fb19eb20c3535b06c66773f427fa6
- Score: 4380 [ Base: 3868 (4096 - 228) +256 (BGGP1) +256 (Writeup) ]
- Note: works as is

```
[user@test01xubuntu]-[12:57:01]-[~/bggp6/2026-04]
$ ./verify-palindrome.sh febnug.palindrome.elf
1bdad60c5e604965bb7dceec968a51862f4fb19eb20c3535b06c66773f427fa6  febnug.palindrome.elf
1bdad60c5e604965bb7dceec968a51862f4fb19eb20c3535b06c66773f427fa6  febnug.palindrome.elf.R
[user@test01xubuntu]-[12:57:12]-[~/bggp6/2026-04]
$ ./febnug.palindrome.elf
6
```
