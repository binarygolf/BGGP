## Entry Info

- Date: 2025-10-20
- BGGP Challenge: 6
- Name:  Aleksey R. (`@continue`)
- Contact Info: 
- Online Presence: https://honk.any-key.press/u/continue
- Writeup Link: gemini://any-key.press/esoteric/bggp6_4th.gmi (in Russian)


## File Info

- Target File Type: `.forth`
- Target File Size: 3
- SHA256 Hash: 13f992229298f371bce44256fa7c726a2e738c5229f7f1b31bfec8d330ccda03

### File Contents

```
NiAu
```

## Environment Info

Any Forth system.

### Target Software and Version

For example: [Portable Forth Environment](https://pfe.sourceforge.net/) 0.33.71 (Sep 26 2024 14:14:11)

### Environment Setup

Any operating system with Forth.

## Additional Info

Drop file `/tmp/bggp6.forth`:
```
$ echo "NiAu" | python3 -m base64 -d > /tmp/bggp6.forth
```

Run as Forth:
```
$ pfe -y -q /tmp/bggp6.forth
6 
```

## Verification

- Reviewer: rqu
- Review Date: 2025-11-22
- SHA256: 13f992229298f371bce44256fa7c726a2e738c5229f7f1b31bfec8d330ccda03
- Score: 4349 (4093 base + 256 for writeup)
- Note: works as is, tested on the first online forth interpreter I found (https://www.jdoodle.com/execute-forth-online)
