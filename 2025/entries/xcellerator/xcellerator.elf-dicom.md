## Entry Info

- Date: 1/1/2026
- BGGP Challenge: Palindrome and Polyglot
- Name: xcel
- Contact Info: 
- Online Presence: 
- Writeup Link: https://github.com/xcellerator/polydrome


## File Info

- Target File Type: RV32 ELF and DICOM image
- Target File Size: 472 bytes
- SHA256 Hash: 0dda851905962bc0083233cefe66922a723e51b59564c6b77289083eb138da2c

### File Contents

_Please encode the file as Base64_

```
f0VMRgEBAf///////////wIA8wD/////wgABADQAAAD/////AAAAADQAIAABAP///////wEAAAAA
AAAAAAABAP////9cAAAAXAAAAAUAAAD////////////////D+8PDw9v729vbw8PLy+P72/v728PD
w8PD//////////////9ESUNNKAAQAAIAAAAoACgAEQACAAAAKAAoAAABAgAAAAEAKAABAQIAAAAB
ACgAAwECAAAAAADgfxAAGgEAAAAAAHMFBQUFBQUFBQUFBQX9Bf0F/QX9Bf0F/QX9Bf0F/QX9Bf0F
4QWNCZPIBRMTBciTCY0F4QX9Bf0F/QX9Bf0F/QX9Bf0F/QX9Bf0FBQUFBQUFBQUFBQVzAAAAAAAB
GgAQf+AAAAAAAAIBAwAoAAEAAAACAQEAKAABAAAAAgEAACgAKAAAAAIAEQAoACgAAAACABAAKE1D
SUT//////////////8PDw8PD2/v72/vjy8vDw9vb2/vbw8PD+8P///////////////8AAAAFAAAA
XAAAAFz/////AAEAAAAAAAAAAAAB////////AAEAIAA0AAAAAP////8AAAA0AAEAwv////8A8wAC
////////////AQEBRkxFfw==
```

## Environment Info

Tested on Debian 13 Trixie.

### Target Software and Version

N/A

### Environment Setup

Should just need `sudo apt install build-essential nasm dcmtk qemu-user feh python3 xxd`.

## Additional Info

See repo [polydrome](https://github.com/xcellerator/polydrome) for screenshot.

NOTE: If this is an update to an existing entry, please include a link to your entry below this text. Reminder that authors can only update an entry once during BGGP.


## Verification 

- Reviewer: netspooky
- Review Date: 2026-04-06
- SHA256: 0dda851905962bc0083233cefe66922a723e51b59564c6b77289083eb138da2c
- Score: 4392 [ Base: 3624 (4096 - 472) +256 (BGGP1) +256 (BGGP2) +256 (Writeup) ]
- Note: works as is. Tested on Ubuntu 22.04. I compiled dcmtk from here: https://github.com/DCMTK/dcmtk

```
$ qemu-riscv32 -strace xcel.elf
79827 exit(6)

$ sha256sum xcel.elf
0dda851905962bc0083233cefe66922a723e51b59564c6b77289083eb138da2c  xcel.elf

$ ./verify-palindrome.sh xcel.elf
0dda851905962bc0083233cefe66922a723e51b59564c6b77289083eb138da2c  xcel.elf
0dda851905962bc0083233cefe66922a723e51b59564c6b77289083eb138da2c  xcel.elf.R

### ... built dcmtk ... running from home directory

### make sure to export the DCMDICTPATH or it won't work !
$ export DCMDICTPATH=/home/user/dcmtk/bin-install/usr/local/share/dcmtk-3.7.0-DEV/dicom.dic

$ ~/dcmtk/bin-install/usr/local/bin/dcm2img --accept-acr-nema xcel.elf xcel.png
W: DcmMetaInfo: Found Preamble but no File Meta Information Header
W: DcmFileFormat: Could not determine Transfer Syntax from File Meta Information Header
W: DcmPixelData: Mandatory element PhotometricInterpretation (0028,0004) is missing
W: can't determine 'PhotometricInterpretation' of decompressed image ... assuming MONOCHROME2 (ACR-NEMA compatibility)
W: missing value for 'HighBit' ... assuming 0
W: missing value for 'SamplesPerPixel' ... assuming 1

$ dcm2img --accept-acr-nema xcel.elf xcel.png

$ feh -Z --zoom 600 xcel.png
```
