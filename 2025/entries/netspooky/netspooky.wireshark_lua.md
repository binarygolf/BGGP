## Entry Info

- Date: 2025-11-02
- BGGP Challenge: 6
- Name: netspooky
- Contact Info: 
- Online Presence: https://n0.lol
- Writeup Link: https://n0.lol/bggp6-wireshark/


## File Info

- Target File Type: .lua (Wireshark Dissector)
- Target File Size: 17
- SHA256 Hash: ef75f59a6c00175070e7820d4546688c5aaa53ab1b91e1417813e1d76c24e051

### File Contents

_Please encode the file as Base64_

```
VGV4dFdpbmRvdy5uZXcoNik=
```

## Environment Info

### Target Software and Version

Wireshark 4.2.2 (Should work on any version with Lua support)

### Environment Setup

_Description of Target Software's Environment (Platform/OS, Setup Instructions, etc.)_

Tested on Ubuntu 24.04

Wireshark was installed through the package manager

I placed my dissector in `~/.local/lib/wireshark/plugins` named `6.lua`

I opened a pcap ( telnet-cooked.pcap from here: https://wiki.wireshark.org/samplecaptures#telnet )

The window should pop up with a 6 as the title. See writeup for more info!

## Additional Info

_Here attach any additional information about the file, including supporting notes, screenshots, videos, console output, etc._

<img width="1577" height="692" alt="Image" src="https://github.com/user-attachments/assets/44f70617-d0c4-41b9-a8ed-3ca1f5d6d36f" />



## Verification
Issue: [158](https://github.com/binarygolf/BGGP/issues/158)

- Reviewer: rqu
- Review Date: 2026-03-16
- SHA256: ef75f59a6c00175070e7820d4546688c5aaa53ab1b91e1417813e1d76c24e051
- Score: 4335 (4079 + 256)
- Note: Works as is
