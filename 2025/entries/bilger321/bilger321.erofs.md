## Entry Info

- Date: 10/20/2025
- BGGP Challenge: 6
- Name: bilger321
- Contact Info:
- Online Presence:
- Writeup Link: https://gist.github.com/bilger321/3359e12f1755cc7928a134115058243f

## File Info

- Target File Type: erofs
- Target File Size: 1254
- SHA256 Hash: 30e6c08d61ffa9689f867e90a6c355bdd1b72791a8965477c5ba989156a69a12

### File Contents

_Please encode the file as Base64_

```
////////////////////////////////////////////////////////////////////////////
//++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++//
//++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++//
//++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++//
//+++6+666666666o+++++++++o666666o+++++++++++o666666o+++++6+666666666o++++//
//+++6+6666+++++66++++++6666++++++66+++++++6666++++++66+++6+6666+++++66+++//
//+++6+6666++++++66+++6+6666++++++++6++++6+6666++++++++6++6+6666++++++66++//
//+++6+6666++++++66++66+6666++++++++++++66+6666+++++++++++6+6666++++++66++//
//+++6+6666+++++66+++66+6666++++++++++++66+6666+++++++++++6+6666+++++66+++//
//+++6+6666666666++++66+6666++++++++++++66+6666+++++++++++6+666666666P++++//
//+++6+6666+++++66+++66+6666+++6666666++66+6666+++6666666+6+6666++++++++++//
//+++6+6666++++++66+++6+6666++++++++6++++6+6666++++++++6++6+6666++++++++++//
//+++6+6666+++++66++++++6666++++++66+++++++6666++++++66+++6+6666++++++++++//
//+++6+666666666P+++++++++6666666P+++++++++++6666666P+++++6+6666++++++++++//
//++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++//
//++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++//
//++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++//
/////////////////////////////////////////////////////////////////////////OLh
9eCuTjE6AwAAAAkAJAACAAAAAAAAAE4bhUQAAAAAAAAAAAMAAAAAAAAAAAAAAAAAAAAAAAAAAAAA
AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA
AAAAAAAAAAAAAAAABAAAAP9BAgAoAAAAAAAAAP////8BAAAAAAAAAAAAAAAkAAAAAAAAACQAAgAk
AAAAAAAAACUAAgAnAAAAAAAAACcAAQAuLi42AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAP+B
```

## Environment Info

### Target Software and Version
erofs-utils
erofs-fuse

```
mkfs.erofs (erofs-utils) 1.8.10

erofsfuse 1.8.10
using FUSE kernel interface version 7.38
fusermount3 version: 3.16.2
```

### Environment Setup

_Description of Target Software's Environment (Platform/OS, Setup Instructions, etc.)_
* Developed on WSL: FedoraLinux42 (x86_64)
* `yum install erofs-utils erofs-fuse`

## Additional Info

_Here attach any additional information about the file, including supporting notes, screenshots, videos, console output, etc._
* The base64 above will decode into a complete erofs filesystem image.
* When mounted using `erofsfuse`, the mounted filesystem contains an empty file named "6" (created on 06/06/06), hopefully satisfying BGGP6.

`mkdir test_dir ; echo "<BASE64 GOES HERE>" | base64 -d > bggp.erofs ; erofsfuse bggp.erofs test_dir ; ls test_dir`
```
erofsfuse 1.8.10
<W> erofs: bggp.erofs mounted on test_dir with offset 0
6
```

## Verification 

- Reviewer: netspooky
- Review Date: 2025-11-22
- SHA256: 30e6c08d61ffa9689f867e90a6c355bdd1b72791a8965477c5ba989156a69a12
- Score: 3098 (base score: 2842 + 256 for writeup) 
- Note: works as is. Tested on Manjaro 25.0.10 

how I verified
```sh
yay -S erofs-utils
yay -S erofs-fuse
mkdir test
erofsfuse 6.erofs test
ls test
```
