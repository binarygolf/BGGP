## Entry Info

- Date: 17.1.2026
- BGGP Challenge: 3+4+5+6
- Name: dominikr
- Contact Info: Discord dominikr, github dominikfhnw
- Online Presence: -
- Writeup Link: https://github.com/dominikfhnw/bggp6-writeup/tree/main/deb (WiP)


## File Info

- Target File Type: Debian Package and shell script
- Target File Size: 182 bytes
- SHA256 Hash: ab8040e9fab2ca6e6c39045d66bb3290dec2f375bb9b4e14ec750e20b8651c29

### File Contents

_Please encode the file as Base64_

```
MC45MzY2NgoxNzAKH4sICApjdXJsIC1MIDZsLmFsCgDt0wEHwlAUBeAL4P2KizGCbVUPCSIIGAiE
zX1XPb3e5u6mv98CoAA25n0HzvkBh7qo0gWYw66En9bV1kIyiaPQ3SuTvoT32IZg6pYe7W0c1lxY
Bt/Fb4VFSnphHweFOVj77/+2gkkk5LBYFVldn09mYMVGBfNrmeOYAz1d8JEbQw7p7Qz1mG3QmgYW
IvkAJjMRewAIAAA=
```

## Environment Info

### Target Software and Version

Debian GNU/Linux or any derivative like Ubuntu

Does *not* work with `dpkg` from busybox

### Environment Setup

Most commands must be run as root. Use a VM and not your regular distro...

## Additional Info

Try to install the deb/output for BGGP6:
```
root@VM:/tmp/bggp6/writeup/deb# dpkg -i bggp456.deb
dpkg: warning: parsing file '/var/lib/dpkg/tmp.ci/control' near line 4 package '6':
 missing 'Description' field
dpkg: warning: parsing file '/var/lib/dpkg/tmp.ci/control' near line 4 package '6':
 missing 'Maintainer' field
(Reading database ... 138190 files and directories currently installed.)
Preparing to unpack bggp456.deb ...
/var/lib/dpkg/tmp.ci/preinst: 5: Syntax error: EOF in backquote substitution
dpkg: error processing archive bggp456.deb (--install):
 new 6 package pre-installation script subprocess returned error exit status 2
Errors were encountered while processing:
 bggp456.deb
```

Check BGGP4:
```
root@VM:/tmp/bggp6/writeup/deb# ls -l bggp456.deb 6
-rw-r--r-- 1 root  root  182 Jan 17 01:26 6
-rw-r--r-- 1 root root 182 Jan  8 14:30 bggp456.deb
```

BGGP6 is implemented as a shellscript polyglot (embedded in the header of the gzip file which is part of the deb):
```
# bash 6
6: line 1: 0.93666: command not found
6: line 2: 170: command not found
6: line 3: $'\037\213\b\b': command not found
Another #BGGP6 download!!!!!! Hi @binarygolf https://binary.golf/6
6: line 5: $'\352\226\036\355m\034\326X\006\337\305o\205EJza\037\a\2059X\373\357\377\266\202I$\344\260X\025Y]\237Of': command not found
6: line 5: $'3\021{\b': command not found
6: line 5: $'\355\323\001\a\302P\024\005\340\v\340\375\212\2131\202mU\017': command not found
```

Edit: It also does BGGP3 by crashing dpkg with an error message, as seen above


## Verification 

Issue: https://github.com/binarygolf/BGGP/issues/175

- Reviewer: netspooky
- Review Date: 2026-03-14
- SHA256: ab8040e9fab2ca6e6c39045d66bb3290dec2f375bb9b4e14ec750e20b8651c29
- Score: 4938 [ Base: 3914 (4096 - 182) +256 (BGGP2) +256 (BGGP4) +256 (BGGP5) +256 (Writeup) ]
- Note: works as is, note that dpkg doesn't crash (tested on ubuntu 22.04), but points were added for the polyglot aspect

```
$ base64 -d <<< MC45MzY2NgoxNzAKH4sICApjdXJsIC1MIDZsLmFsCgDt0wEHwlAUBeAL4P2KizGCbVUPCSIIGAiEzX1XPb3e5u6mv98CoAA25n0HzvkBh7qo0gWYw66En9bV1kIyiaPQ3SuTvoT32IZg6pYe7W0c1lxYBt/Fb4VFSnphHweFOVj77/+2gkkk5LBYFVldn09mYMVGBfNrmeOYAz1d8JEbQw7p7Qz1mG3QmgYWIvkAJjMRewAIAAA= > bggp456.deb

$ sha256sum bggp456.deb 
ab8040e9fab2ca6e6c39045d66bb3290dec2f375bb9b4e14ec750e20b8651c29  bggp456.deb

$ sh bggp456.deb
bggp456.deb: 1: 0.93666: not found
bggp456.deb: 2: 170: not found
bggp456.deb: 3:: not found
Another #BGGP6 download!!!!!! Hi @binarygolf https://binary.golf/6
bggp456.deb: 5: 3: not found
bggp456.deb: 1: ��m�X��o�EJza�9X�����I$�XY]�Of: not found
bggp456.deb: 5: ���P�
                     ����1�mU: not found

$ sudo dpkg -i bggp456.deb 
dpkg: warning: parsing file '/var/lib/dpkg/tmp.ci/control' near line 4 package '6':
 missing 'Description' field
dpkg: warning: parsing file '/var/lib/dpkg/tmp.ci/control' near line 4 package '6':
 missing 'Maintainer' field
Selecting previously unselected package 6.
(Reading database ... 186769 files and directories currently installed.)
Preparing to unpack bggp456.deb ...
/var/lib/dpkg/tmp.ci/preinst: 5: Syntax error: EOF in backquote substitution
dpkg: error processing archive bggp456.deb (--install):
 new 6 package pre-installation script subprocess returned error exit status 2
Errors were encountered while processing:
 bggp456.deb

$ sha256sum *
ab8040e9fab2ca6e6c39045d66bb3290dec2f375bb9b4e14ec750e20b8651c29  6
ab8040e9fab2ca6e6c39045d66bb3290dec2f375bb9b4e14ec750e20b8651c29  bggp456.deb
```

