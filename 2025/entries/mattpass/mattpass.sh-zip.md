## Entry Info

- Date: 28th Nov 2025
- BGGP Challenge: 1 + 2 + 3 + 4 + 5 + 6!
- Name: Matt Pass
- Contact Info: @mattpass
- Online Presence: x.com/mattpass
- Writeup Link: https://gist.github.com/mattpass/8b40b2e2b946f8bf7474a001b30f3a85


## File Info

- Target File Type: Zip/Shell
- Target File Size: 179 bytes
- SHA256 Hash: c4945186aafdf344d47725bde235a3e5b14b97a2

### File Contents

```
Y3AgJDAgWCYmZWNobyA0O2N1cmwgaHR0cHM6Ly9iaW5hcnkuZ29sZi81LzU7ZWNobyA2O2tpbGwg
LTExICQkICMKI1BLBQYAAAAAAAAAAAAAAAAAAAAAAQAyAAEAAAAAAAAAAAAAAAAAAAAABgVLUCMK
IyAkJCAxMS0gbGxpazs2IG9oY2U7NS81L2Zsb2cueXJhbmliLy86c3B0dGggbHJ1Yzs0IG9oY2Um
JlggMCQgcGM=
```

## Environment Info

Linux, any

### Target Software and Version

sh, unzip

### Environment Setup

Base64 decode into a 6.zip and then run:

```
└─▶ ./6.zip
4
Another #BGGP5 download!! @binarygolf https://binary.golf
6
Segmentation fault (core dumped)
```

^ Covers BGGP 4 (replicates to file named `X`), BGGP 5, BGGP 6, BGGP 3 (crashes your Shell program, eg `sh` with seg fault)

```
└─▶ unzip -zq 6.zip
2
```

^ Covers BGGP 2

The file is also a palindrome which covers BGGP 1.

## Additional Info

- None

## Verification 

Issue: https://github.com/binarygolf/BGGP/issues/165

- Reviewer: netspooky
- Review Date: 2026-03-14
- SHA256: c95322b83039915b74717b32f0b2324b73f2fec5ae050571d3bb6e5e36cd636f
- Score: 5453 [ Base: 3917 (4096 - 179) +256 (BGGP1) +256 (BGGP2) +256 (BGGP3) +256 (BGGP4) +256 (BGGP5) +256 (Writeup) ] 
- Note: works as is

Output:
```
$ base64 -d <<< Y3AgJDAgWCYmZWNobyA0O2N1cmwgaHR0cHM6Ly9iaW5hcnkuZ29sZi81LzU7ZWNobyA2O2tpbGwgLTExICQkICMKI1BLBQYAAAAAAAAAAAAAAAAAAAAAAQAyAAEAAAAAAAAAAAAAAAAAAAAABgVLUCMKIyAkJCAxMS0gbGxpazs2IG9oY2U7NS81L2Zsb2cueXJhbmliLy86c3B0dGggbHJ1Yzs0IG9oY2UmJlggMCQgcGM= > 6.zip

$ sha256sum 6.zip 
c95322b83039915b74717b32f0b2324b73f2fec5ae050571d3bb6e5e36cd636f  6.zip

$ ./verify-palindrome.sh 6.zip
c95322b83039915b74717b32f0b2324b73f2fec5ae050571d3bb6e5e36cd636f  6.zip
c95322b83039915b74717b32f0b2324b73f2fec5ae050571d3bb6e5e36cd636f  6.zip.R

[user@test01xubuntu]-[17:19:01]-[~/bggp6/2026-03]
$ ./6.zip 
4
Another #BGGP5 download!! @binarygolf https://binary.golf
6
Segmentation fault (core dumped)

[user@test01xubuntu]-[17:19:16]-[~/bggp6/2026-03]
$ unzip -zq 6.zip 
2
```
