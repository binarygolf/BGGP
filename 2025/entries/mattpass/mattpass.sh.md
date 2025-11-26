## Entry Info

- Date: 21st Oct 2025
- BGGP Challenge:  1 + 2 + 6
- Name: Matt Pass
- Contact Info:  @mattpass
- Online Presence:  x.com/mattpass
- Writeup Link: https://pastebin.com/YBcdvF57

## File Info

- Target File Type: Shell, with args
- Target File Size: 5 bytes
- SHA256 Hash: 0f17827fba2d13b2fca4eb1ada39903f7fdced92e7cfa6a7dcea3cc3be4b0a58

### File Contents

```
JEAjQCQ=
```

## Environment Info

Linux with Chrome installed.

### Target Software and Version

Google Chrome, any

### Environment Setup

Write the file contents to a file, eg `6.sh` and run `chmod +x 6.sh` to make it executable. Then run `./6.sh google-chrome "data:text/html,6<script>setTimeout(window.location='https://t.ly/3jGrK',5000)</script>"`. You'll find it will open a browser tab firstly showing a number 6 and then after 5 seconds, download the content for challenge 5 using W3C's HTML to text service and output in the browser.

I think this covers the following past BGGPs:

1 - Palindrome - as Shell file content is `$@#@$`
5 - Download - it downloads the BGGP 5 content

## Additional Info

- None

## Verification 

- Reviewer: XfavataX
- Review Date: 2025-11-26
- SHA256: 0f17827fba2d13b2fca4eb1ada=25639903f7fdced92e7cfa6a7dcea3cc3be4b0a58
- Score: 4859 (4096 - 5) base + (256 + 256) challenges 1 and 5 + 256 writeup
- Note: Works as expected. Tested on Debian 13 with Chromium. Can adjust the timeout time to make the 6 last longer if it's going too fast. Displays "6" in the browser and then downloads the challenge five payload. Script is also a palindrome.
