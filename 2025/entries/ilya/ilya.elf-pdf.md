## Entry Info

- Date: 18 January 2026
- BGGP Challenge: bggp6
- Name: ilya
- Contact Info: `ilya:rx.haunted.computer` (matrix)
- Online Presence: none
- Writeup Link: [github gist](https://gist.github.com/ilya-lyapunov/fb2b7f66f9cfe434d664569ca6f6706c)


## File Info

- Target File Type: ELF (x86_64), PDF 
- Target File Size: 512
- SHA256 Hash: b2a9ab69ac017fcb6d568a4ba322d0352699f5648afc69f65db202ff7802a0c2

### File Contents

```
f0VMRgIBAQMAAAAAAAAAAAIAPgABAAAAsABAAAAAAABAAAAAAAAAAAAAAAAAAAAAAAAAAEAAOAAC
AEAAAAAAAAEAAAAFAAAAAAAAAAAAAAAAAEAAAAAAAAAAQAAAAAAA8AAAAAAAAADwAAAAAAAAAAAQ
AAAAAAAAAQAAAAYAAADwAAAAAAAAAPAQQAAAAAAA8BBAAAAAAAAQAQAAAAAAABABAAAAAAAAABAA
AAAAAAC+7QEAAEjHx+4AQAC4VQAAAA8FSMfCAAIAAEjHxgAAQABIice4AQAAAA8FuAMAAAAPBb8G
AAAAuDwAAAAPBTYAJVBERi0xLgoxIDAgb2JqPDwvS2lkc1s8PC9SZXNvdXJjZXM8PD4+L0NvbnRl
bnRzIDIgMCBSL1BhcmVudCAxIDAgUi9UeXBlL1BhZ2UvTWVkaWFCb3hbMCAwIDk5IDk5XT4+XS9U
eXBlL1BhZ2VzL0NvdW50IDE+PmVuZG9iagoyIDAgb2JqPDw+PnN0cmVhbQpCVC8gOSBUZig2KScg
RVQKZW5kc3RyZWFtCmVuZG9iagozIDAgb2JqPDwvVHlwZS9DYXRhbG9nL1BhZ2VzIDEgMCBSPj5l
bmRvYmoKdHJhaWxlcjw8L0luZm88PC9BdXRob3IoQkdHUCk+Pi9Sb290IDMgMCBSPj4KJUVPRgA=
```

## Environment Info

Should run on any x86_64 Linux or Unix. I used `fasm` to build the executable.

### Target Software and Version

Any x86_64 Linux or Unix.

PDF only renders in Firefox, Chrome and Adobe Reader.

### Environment Setup

From any x86_64 Linux/Unix system, just run the ELF and it should output another file called `6`.

Renaming the file to `6.pdf` and opening it in Firefox, Chrome or Adobe Reader will render the number 6.

If you run `6.pdf` as an executable, it will make another copy of itself (again called `6`).

## Additional Info

See writeup for additional info.


## Verification 

Issue: https://github.com/binarygolf/BGGP/issues/180

- Reviewer: netspooky
- Review Date: 2026-03-14
- SHA256: b2a9ab69ac017fcb6d568a4ba322d0352699f5648afc69f65db202ff7802a0c2
- Score: 4352 [ Base: 3584 (4096 - 512) +256 (BGGP2) +256 (BGGP4) +256 (Writeup) ]
- Note: works as is, PDF verified working in Firefox

Output:
```
$ base64 -d <<< f0VMRgIBAQMAAAAAAAAAAAIAPgABAAAAsABAAAAAAABAAAAAAAAAAAAAAAAAAAAAAAAAAEAAOAACAEAAAAAAAAEAAAAFAAAAAAAAAAAAAAAAAEAAAAAAAAAAQAAAAAAA8AAAAAAAAADwAAAAAAAAAAAQAAAAAAAAAQAAAAYAAADwAAAAAAAAAPAQQAAAAAAA8BBAAAAAAAAQAQAAAAAAABABAAAAAAAAABAAAAAAAAC+7QEAAEjHx+4AQAC4VQAAAA8FSMfCAAIAAEjHxgAAQABIice4AQAAAA8FuAMAAAAPBb8GAAAAuDwAAAAPBTYAJVBERi0xLgoxIDAgb2JqPDwvS2lkc1s8PC9SZXNvdXJjZXM8PD4+L0NvbnRlbnRzIDIgMCBSL1BhcmVudCAxIDAgUi9UeXBlL1BhZ2UvTWVkaWFCb3hbMCAwIDk5IDk5XT4+XS9UeXBlL1BhZ2VzL0NvdW50IDE+PmVuZG9iagoyIDAgb2JqPDw+PnN0cmVhbQpCVC8gOSBUZig2KScgRVQKZW5kc3RyZWFtCmVuZG9iagozIDAgb2JqPDwvVHlwZS9DYXRhbG9nL1BhZ2VzIDEgMCBSPj5lbmRvYmoKdHJhaWxlcjw8L0luZm88PC9BdXRob3IoQkdHUCk+Pi9Sb290IDMgMCBSPj4KJUVPRgA= > bggp
$ chmod +x bggp

$ ./bggp 

$ echo $?
6

$ sha256sum *
b2a9ab69ac017fcb6d568a4ba322d0352699f5648afc69f65db202ff7802a0c2  6
b2a9ab69ac017fcb6d568a4ba322d0352699f5648afc69f65db202ff7802a0c2  bggp
```



