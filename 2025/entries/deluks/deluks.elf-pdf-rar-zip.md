## Entry Info

- Date: 19.10.2025
- BGGP Challenge: 2  & 6
- Name: DeLuks
- Contact Info: `deluks.` (discord) 
- Online Presence: -
- Writeup Link: tbd


## File Info

- Target File Type: ELF + PDF + ZIP + RAR
- Target File Size: 479
- SHA256 Hash: `4f0ebfa8a0232e053a0221d2d45c73fe27160cd43b4fd43ec3d252fb15a7b4b6`

### File Contents

_Please encode the file as Base64_

```
f0VMRrA8Xw8FkJCQkJCQkAIAPgCQkJCQBAABAAAAAAAxAAAAAAAAACVQREYtMS4KJQEAAAAFOAAB
AAAAAAAAAAAAAAEAAAAAAJCQkJCQkJAAaAAAAAAAAABoAAAAAAAAAAoxIDAgb2JqPDwvS2lkc1s8
PC9SZXNvdXJjZXM8PD4+L0NvbnRlbnRzIDIgMCBSL1BhcmVudCAxIDAgUi9UeXBlL1BhZ2UvTWVk
aWFCb3hbMCAwIDYgNl0+Pl0vVHlwZS9QYWdlcy9Db3VudCAxPj5lbmRvYmoKMiAwIG9iajw8Pj5z
dHJlYW0KQlQvIDQgVGYoNiknIEVUCmVuZHN0cmVhbQplbmRvYmoKMyAwIG9iajw8L1R5cGUvQ2F0
YWxvZy9QYWdlcyAxIDAgUj4+ZW5kb2JqCgAAUmFyIRoHAQAzkrXlCgEFBgAFAQGAgABn8AhvHwID
C4AABIAApIMCAAAAAIAAAQE2CgMT8Lb0aIOGWwQdd1ZRAwUEAFBLAwQKAAAAAABZZVNbAAAAAAAA
AAAAAAAAAQAAADZQSwECHgMKAAAAAABZZVNbAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAApIEAAAAA
NlBLBQYAAAAAAQABAC8AAAAfAAAAAAA=
```

## Environment Info

### Target Software and Version

Arch: x86_64
Operating System: Linux
Distro: Arch Linux
Kernel: 6.16.8-arch3-1

### Environment Setup

#### ELF: 

On Linux x64_64, change the permissions of the file to be executable and run it with any 5 arguments and check the return value:
```sh
$ chmod +x entry.bin
$ ./entry.bin 6 6 6 6 6
$ echo $?
6
```

#### PDF:

On Linux, just open the file with zathura pdf viewer:
```sh
$ zathura entry.bin
```

#### RAR:

On Linux, run the following command to extract an empty file called "6":
```sh
$ rar e entry.bin
```

#### ZIP:

On Linux, run the following command to extract an empty file called "6":
```sh
$ unzip entry.bin
```

## Additional Info

<img width="2834" height="1658" alt="Image" src="https://github.com/user-attachments/assets/f784c10b-9d8a-4a55-a0b6-613dcbdd7603" />


## Verification 

- Reviewer: netspooky
- Review Date: 2025-10-19
- SHA256: 4f0ebfa8a0232e053a0221d2d45c73fe27160cd43b4fd43ec3d252fb15a7b4b6
- Score: 3617
- Note: tested the ELF, RAR and ZIP portions on Ubuntu 22.04 and they work. Tested the PDF portion on Manjaro 25.0.10 and installed zathura and the plugin required via `yay -S zathura zathura-pdf-mupdf`


