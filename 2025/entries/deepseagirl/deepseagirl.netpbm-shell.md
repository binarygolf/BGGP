## Entry Info

- Date: 2025-11-02
- BGGP Challenge: 2, 6
- Name: ackmage
- Contact Info: 
- Online Presence: [herm.it](//herm.it) 
- Writeup Link: tbd


## File Info

- Target File Type: .pbm (netpbm), .sh (shell script)
- Target File Size: 25
- SHA256 Hash: 0973848372fa87c9e05f8f3b5cd8660ef04ae4a832218fd728f78ff66dd1e6a5

### File Contents

_Please encode the file as Base64_

```
UDEgMyA1IDExMTEwMDExMTEwO2VjaG8gNg==
```

## Environment Info

### Target Software and Version

macOS file viewer (Finder)

macOS terminal (or any shell)

### Environment Setup

_Description of Target Software's Environment (Platform/OS, Setup Instructions, etc.)_

macOS Sonoma 14.5

## Additional Info

_Here attach any additional information about the file, including supporting notes, screenshots, videos, console output, etc._

this file is a polyglot consisting of a [netpbm](https://en.wikipedia.org/wiki/Netpbm) image file and a shell script

to view as a netpbm image, save file and view in Finder:

<img width="157" height="170" alt="screenshot of 6.pbm rendering as image file in Finder app" src="https://github.com/user-attachments/assets/b0bcaa74-09a5-4105-b4cc-bd25bac7d8ea" />

double-click to open it in Preview:

<img width="699" height="273" alt="screenshot of zoomed out, ultra tiny 6.pbm as image file in Preview app" src="https://github.com/user-attachments/assets/4b763667-7348-43ed-add3-80fc0e3aa3cf" />

you really gotta zoooooom in:

<img width="706" height="275" alt="screenshot of zoomed in 6.pbm as image file in Preview app" src="https://github.com/user-attachments/assets/19c43fb5-3708-4cc2-8acd-f2385538b208" />

to run as a shell script, make executable and run it:

```sh
chmod +x 6.pbm
./6.pbm
```

<img width="664" height="280" alt="screenshot of 6.pbm running in shell" src="https://github.com/user-attachments/assets/80b765b3-09ea-4e5b-a2f6-c0f1de6feeab" />

feel free to test this out on other image viewers and lmk what happens!

## Verification 

- Reviewer: netspooky
- Review Date: 2025-11-22
- SHA256: 0973848372fa87c9e05f8f3b5cd8660ef04ae4a832218fd728f78ff66dd1e6a5
- Score: 4327 (base 4071 + 256 for polyglot challenge)
- Note: Works as is on MacOS. On Ubuntu 24.04 with gnome - Image Viewer complains that the PNM loader expected to find an integer, but didn't. XnViewMP also doesn't have a loader for it. 
