## Entry Info

- Date: 21/10/2025
- BGGP Challenge: 2 & 6
- Name: febnug
- Contact Info: 
- Online Presence: 
- Writeup Link: [https://github.com/febnug/bggp6-writeup/blob/main/polyglot.md](url)


## File Info

- Target File Type: ELF/PDF/JS
- Target File Size: 725
- SHA256 Hash: 0d9a623731beb61e436040a6b35d448aa50d512ea396e65fe1c7aa1aca075ea1

### File Contents

_Please encode the file as Base64_

```
f0VMRgEBAQAAAAAAAAAAAAIAAwABAAAAt4IECDQAAAAAAAAAAAAAADQAIAABAAAAAAAAAAEAAAAAAAAAAIAECACABAjVAgAA1QIAAAUAAAAAEAAAJVBERi0xLjEKJf////8KMSAwIG9iago8PCAvVHlwZSAvQ2F0YWxvZyAvUGFnZXMgMiAwIFIgPj4KZW5kb2JqCjIgMCBvYmoKPDwgL1R5cGUgL1BhZ2VzIC9LaWRzIFszIDAgUl0gL0NvdW50IDEgPj4KZW5kb2JqCjMgMCBvYmoKPDwgL1R5cGUgL1BhZ2UgL1BhcmVudCAyIDAgUiAvUmVzb3VyY2VzIDw8IC9Gb250IDw8IC9GMSA0IDAgUiA+PiA+PiAvTWVkaWFCb3ggWzAgMCAyMDAgMjAwXSAvQ29udGVudHMgNSAwIFIgPj4KZW5kb2JqCjQgMCBvYmoKPDwgL1R5cGUgL0ZvbnQgL1N1YnR5cGUgL1R5cGUxIC9CYXNlRm9udCAvSGVsdmV0aWNhID4+CmVuZG9iago1IDAgb2JqCjw8IC9MZW5ndGggMzMgPj4Kc3RyZWFtCkJUIC9GMSA0OCBUZiA1MCAxMDAgVGQgKDYpIFRqIEVUCmVuZHN0cmVhbQplbmRvYmoKeHJlZgowIDYKMDAwMDAwMDAwMCA2NTUzNSBmIAowMDAwMDAwMDk5IDAwMDAwIG4gCjAwMDAwMDAxNDggMDAwMDAgbiAKMDAwMDAwMDIwNSAwMDAwMCBuIAowMDAwMDAwMzMxIDAwMDAwIG4gCjAwMDAwMDA0MDEgMDAwMDAgbiAKdHJhaWxlcgo8PCAvU2l6ZSA2IC9Sb290IDEgMCBSID4+CnN0YXJ0eHJlZgo0ODMKJSVFT0YKPHNjcmlwdD5hbGVydCgiNiIpOzwvc2NyaXB0PgpmaDYKMcCwBDHbswGJ4THSsgLNgDHAsAEx27MGzYA=
```

## Environment Info

### Target Software and Version
ELF x86
### Environment Setup

_Description of Target Software's Environment (Platform/OS, Setup Instructions, etc.)_

Arch: x86_64
Operating System: Linux
Distro: Ubuntu 25.04
Kernel: 6.14.0-33-generic

<b>ELF:</b>

On Linux x64_64, change the permissions of the file to be executable and run it:
```
$ chmod +x febnug.bggp6
$ ./febnug.bggp6
6
$ echo $?
6
```

<b>PDF:</b>

Extract the PDF file with this command:
```
$ dd if=febnug.bggp6 bs=1 skip=84 count=582 of=febnug.bggp6.pdf status=none
```
It will do generate PDF file

<b>JS:</b>

Extract the JS file with this command:
```
$ dd if=febnug.bggp6 bs=1 skip=666 of=febnug.bggp6.html status=none
```
It will do generate HTML file

## Additional Info

_Here attach any additional information about the file, including supporting notes, screenshots, videos, console output, etc._

<b>Here, demonstrate an HTML file opened in the browser</b>

<img src="https://raw.githubusercontent.com/febnug/bggp6-writeup/refs/heads/main/js.png"/>

<b>Here, demonstrate an PDF file opened in the browser</b>

<img src="https://raw.githubusercontent.com/febnug/bggp6-writeup/refs/heads/main/pdf.png"/>

It should also be normal and can be opened using another PDF viewer.


## Verification 

- Reviewer: netspooky
- Review Date: 2026-04-06
- SHA256: 0d9a623731beb61e436040a6b35d448aa50d512ea396e65fe1c7aa1aca075ea1
- Score: 3883 [ Base: 3371 (4096 - 725) +256 (BGGP2) +256 (Writeup) ]
- Note: works as is, ELF tested Ubuntu 22.04 x86_64, PDF and HTML tested in Firefox

```
[user@test01xubuntu]-[12:47:30]-[~/bggp6/2026-04]
$ ./febnug.poly.elf
6
[user@test01xubuntu]-[12:47:34]-[~/bggp6/2026-04]
$ sha256sum febnug.poly.elf
0d9a623731beb61e436040a6b35d448aa50d512ea396e65fe1c7aa1aca075ea1  febnug.poly.elf
```

