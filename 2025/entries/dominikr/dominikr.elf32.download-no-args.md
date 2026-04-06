## Entry Info

- Date: 17.1.2026
- BGGP Challenge: 5+6 
- Name: dominikr
- Contact Info: Discord dominikr, github dominikfhnw
- Online Presence: -
- Writeup Link: https://github.com/dominikfhnw/bggp6-writeup/tree/main/download

## File Info

- Target File Type: ELF/Linux x86 32bit
- Target File Size: 71 bytes
- SHA256 Hash: 4ba432d30c3c86e2ead229850aabfea03ef68bf57d228b54190eee1e52b307cd

### File Contents

```
f0VMRgEAAAAAAAAAALALPQIAAwAZsAs9GbALPQQAAABTuzawCz1Ts0WpIAABAFOzO1OJ4c2ANmwu
YWwvYmluL2N1cmwALUw=
```

## Environment Info

### Target Software and Version

Linux x86 32bit (or 64bit w/32bit support enabled).

### Environment Setup

* Should work on any recent-ish Linux version. 
* Requires curl in /bin/curl. 
* Mainly tested on Ubuntu 22.04

## Additional Info

Copy the file over to any modern-ish x86/x64 Linux distribution, and make it executable with `chmod +x`.

```
$ ./dload
Another #BGGP6 download!!!!!! Hi @binarygolf https://binary.golf/6
```

See the writeup for more info


## Verification 

- Reviewer: netspooky
- Review Date: 2026-04-06
- SHA256: 4ba432d30c3c86e2ead229850aabfea03ef68bf57d228b54190eee1e52b307cd
- Score: 4537 [ Base: 4025 (4096 - 71) +256 (BGGP5) +256 (Writeup) ]
- Note: works as is, downloads from 6l.al

```
[user@test01xubuntu]-[13:06:15]-[~/bggp6/2026-04]
$ ./dominikr.dl.noargs.elf32
Another #BGGP6 download!!!!!! Hi @binarygolf https://binary.golf/6
[user@test01xubuntu]-[13:06:17]-[~/bggp6/2026-04]
$ sha256sum dominikr.dl.noargs.elf32
4ba432d30c3c86e2ead229850aabfea03ef68bf57d228b54190eee1e52b307cd  dominikr.dl.noargs.elf32
```
