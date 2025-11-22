## Entry Info

- Date: 2025-10-21
- BGGP Challenge: 4, 5, 6
- Name: bah
- Contact Info: bahorn in the BGGP discord
- Online Presence: https://b.horn.uk/
- Writeup Link: https://gist.github.com/bahorn/4a0d8505d84e7acab21358c39fdab4a7


## File Info

- Target File Type: `.curlrc`
- Target File Size: 62
- SHA256 Hash: e664df8af2ac8d6bcef04ad9d7654012ab8e2d97

### File Contents

_Please encode the file as Base64_

```
LUxvNgp1cmw9ZmlsZTovcHJvYy9zZWxmL2N3ZC8uY3VybHJjCnVybD1iaW5hcnkuZ29sZi81LzUKdXJsPWE=
```

## Environment Info

### Target Software and Version

Any modern curl version should work, I tested on curl 8.5.0, on a default Ubuntu 24.04 install.

### Environment Setup

_Description of Target Software's Environment (Platform/OS, Setup Instructions, etc.)_


On any recent Ubuntu install:
```
$ apt-get install curl
``` 

Then run the entry by writing it `$HOME/.curlrc` and just invoking `curl` from the same directory.

Run curl like `HOME=$PWD curl` if you don't want to overwrite your users `.curlrc`.

## Additional Info

_Here attach any additional information about the file, including supporting notes, screenshots, videos, console output, etc._

NOTE: If this is an update to an existing entry, please include a link to your entry below this text. Reminder that authors can only update an entry once during BGGP.

This implements both BGGP 4 and 5. Copying the file by going to `/proc/self/cwd/.curlrc` and writing it to `6` with the `-o` option.
Returns 6 by passing curl a domain that doesn't resolve.
Downloading the BGGP5 file is as expected.

Expect the following output:
```
$ HOME=`pwd` curl
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100    62  100    62    0     0   672k      0 --:--:-- --:--:-- --:--:--  672k
Another #BGGP5 download!! @binarygolf https://binary.golf
curl: (6) Could not resolve host: a
$ echo $?
6
$ shasum .curlrc 6
e664df8af2ac8d6bcef04ad9d7654012ab8e2d97  .curlrc
e664df8af2ac8d6bcef04ad9d7654012ab8e2d97  6
```

## Verification 

- Reviewer: netspooky
- Review Date: 2025-11-22
- SHA256: b07e2671c7ca491f1c62a93935707ab954d85f27a779c946beef92774c071a4a 
- Score: 4802 (base score 4034 + 256 for 4 5 and a writeup)
- Note: works as is. Creates a file called 6 containing the .curlrc contents, as well as downloads the 5 file, and returns 6.

