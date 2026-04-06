## Entry Info

- Date: 22.10.2025
- BGGP Challenge: 6
- Name: dominikr
- Contact Info: Discord dominikr, github dominikfhnw
- Online Presence: -
- Writeup Link: https://gist.github.com/dominikfhnw/5cf86ce2c7b539a910f6c26307d0a5ab


## File Info

- Target File Type: ELF/Linux x86 32bit
- Target File Size: 45 bytes
- SHA256 Hash: 2d5acb305a11b6d3d88c9f3e1523e3d10ef90a1e3790aed3962ebd488d415b04

### File Contents
```
f0VMRgEAAAA2CgAANroEaAIAAwAZsARoGbAEaAQAAAC5CLAEaFrNgOv+IAAB
```

## Environment Info

### Target Software and Version
Linux x86 32bit (or 64bit w/32bit support enabled)

### Environment Setup

No external dependencies needed. Should work with any x86/x64 Linux kernel that supports the ELF executable format.
 
Put content in a file and make it executable (i.e. `chmod +x ./e`). Filename does not matter. Execute it in the terminal with `./e`. 

## Additional Info

Expected output:
```
$ ./e
6

```
Program does not automatically exit after printing. Press Ctrl+C to exit.

STDIN *must* be a TTY for the program to work. This should be the case if the program is started in a terminal session as described above. More about this weird requirement will follow in the writeup.

## Verification 

- Reviewer: netspooky
- Review Date: 2026-04-06
- SHA256: 2d5acb305a11b6d3d88c9f3e1523e3d10ef90a1e3790aed3962ebd488d415b04
- Score: 4307 [ Base: 4051 (4096 - 45) +256 (Writeup) ]
- Note: works as is

```
$ sha256sum dominikr.6.elf32
2d5acb305a11b6d3d88c9f3e1523e3d10ef90a1e3790aed3962ebd488d415b04  dominikr.6.elf32

$ ./dominikr.6.elf32
6
^C
```
