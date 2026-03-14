## Entry Info

- Date: 25th Nov 2025
- BGGP Challenge: 2 + 5 + 6
- Name: Matt Pass
- Contact Info: @mattpass
- Online Presence: x.com/mattpass
- Writeup Link: https://pastebin.com/13tPuZaB


## File Info

- Target File Type: Zip/Shell/SQL
- Target File Size: 159 bytes
- SHA256 Hash: 80ebd6592bbc62b3cfa91a1370c7a7136d8a7a0d

### File Contents

```
Lyo6IDI+L2Rldi9udWxsO2N1cmwgaHR0cHM6Ly9iaW5hcnkuZ29sZi81LzUgIyovU0VMRUNUIDY7
LS1QSwMEFAAAAAAAHU95WwAAAAAAAAAAAAAAAAEAAAAyUEsBAhQDFAAAAAAAHU95WwAAAAAAAAAA
AAAAAAEAAAAAAAAAAAAAAIABAAAAADJQSwUGAAAAAAEAAQAvAAAAHwAAAAAA
```

## Environment Info

Linux, any

### Target Software and Version

sh, sqlite3, unzip

### Environment Setup

Base64 decode into a 6.zip and then run:

```
└─▶ unzip -Z1 6.zip 2>/dev/null
2
```

```
└─▶ sh 6.zip
Another #BGGP5 download!! @binarygolf https://binary.golf
```

```
└─▶ sqlite3 :memory: < 6.zip
6
```

## Additional Info

- None


## Verification 

Issue: https://github.com/binarygolf/BGGP/issues/164

- Reviewer: netspooky
- Review Date: 2026-03-14
- SHA256: 6ca01adccb2aaeb3878a524d7221e6a83b457c05737ba62c3d8c8a077619a1f9
- Score: 4705 [ Base: 3937 (4096 - 159) +256 (BGGP2) +256 (BGGP5) +256 (Writeup) ]
- Note: works as is


```
$ base64 -d <<< Lyo6IDI+L2Rldi9udWxsO2N1cmwgaHR0cHM6Ly9iaW5hcnkuZ29sZi81LzUgIyovU0VMRUNUIDY7LS1QSwMEFAAAAAAAHU95WwAAAAAAAAAAAAAAAAEAAAAyUEsBAhQDFAAAAAAAHU95WwAAAAAAAAAAAAAAAAEAAAAAAAAAAAAAAIABAAAAADJQSwUGAAAAAAEAAQAvAAAAHwAAAAAA > 6.zip

$ sha256sum 6.zip 
6ca01adccb2aaeb3878a524d7221e6a83b457c05737ba62c3d8c8a077619a1f9  6.zip

$ sh 6.zip
Another #BGGP5 download!! @binarygolf https://binary.golf

$ sqlite3 :memory: < 6.zip
6

$ unzip -Z1 6.zip 2>/dev/null
2
```
