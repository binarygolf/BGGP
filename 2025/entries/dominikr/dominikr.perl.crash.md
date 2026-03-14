## Entry Info

- Date: 8.1.2026
- BGGP Challenge: 3&6
- Name: dominikr
- Contact Info: Discord dominikr, github dominikfhnw
- Online Presence: -
- Writeup Link: https://github.com/dominikfhnw/bggp6-writeup/tree/main#perl-crasher


## File Info

- Target File Type: perl script
- Target File Size: 29 bytes
- SHA256 Hash: 6e7ed92f3176bcb8c36a361bc9234b7b504bd35f9f45054d6ff19182cd2971f2

### File Contents

```
REVTVFJPWXtibGVzc1tdfWRpZSQ9LGJsZXNzW10=
```

## Environment Info

### Target Software and Version

Perl version 5.6 - 5.42

### Environment Setup

Tested on Perl for Linux. Perl for Windows, VMS, OS/2 etc not tested, but should work there too.

Either set executable flag and run with `./crash.pl`, or with `perl crash.pl`

Alternatively, run it online: https://perlbanjo.com/d3909c6491

## Additional Info
Expected output:
```
$ perl perl/crash.pl
60main=ARRAY(0x5555558ff4b8) at perl/crash.pl line 1.
Segmentation fault (core dumped)
```

Smaller 23-byte version (but without printing 6) is available under https://github.com/dominikfhnw/bggp6-writeup/blob/main/perl/crash2.pl

See writeup for more info


## Verification 

Issue: https://github.com/binarygolf/BGGP/issues/168

- Reviewer: netspooky
- Review Date: 2026-03-14
- SHA256: 6e7ed92f3176bcb8c36a361bc9234b7b504bd35f9f45054d6ff19182cd2971f2
- Score: 4579 [ Base: 4067 (4096 - 29) +256 (BGGP3) +256 (Writeup) ]
- Note: works as is

```
$ base64 -d <<< REVTVFJPWXtibGVzc1tdfWRpZSQ9LGJsZXNzW10= > bggp6.pl

$ sha256sum bggp6.pl 
6e7ed92f3176bcb8c36a361bc9234b7b504bd35f9f45054d6ff19182cd2971f2  bggp6.pl

$ perl bggp6.pl 
60main=ARRAY(0x59f7017564b8) at bggp6.pl line 1.
Segmentation fault (core dumped)
```
