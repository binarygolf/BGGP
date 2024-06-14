![](https://binary.golf/4/art/BGGP4_logo_trans_x4.png)

# Binary Golf Grand Prix 4: Replicate

Welcome golfers, to another exciting year of the Binary Golf Grand Prix! Scoring this year took us a bit longer than usual, which may be due to the whopping 80+ entries we got! This is more than double the amount we got last year, and over 20 times more entries than [BGGP1](https://github.com/binarygolf/BGGP/tree/main/2020) back in 2020...

This year, we challenged you to create the smallest file which could replicate itself, AND print, return, or otherwise display the number "4". While this type of challenge can lead to some disastrous results, we established some ground rules to limit potential harm. These rules enabled us to quickly verify that the file works as intended with consistent behavior from all entries, and prevented uncontrolled spread.

To be a valid entry, the file:
- Must return or print 4
- Must create a file called 4
- Must not execute the file it created

The targets were diverse this year, with a variety of tricks, hacks, and system quirks being used to achieve the goal. Some were quite popular, with Python, Shell, COM, and ELF each having 5 or more distinct entries. Some new file types, such as self-replicating VSCode Workspaces, UEFI Applications, and rizin debugger scripts, have left us feeling hopeful about future BGGP entries.

The Binary Golf Association would like to thank everyone who participated in BGGP4! We appreciate your patience as we scale this so we can keep it a fun, free, community event. Special shoutouts go to tmp.0ut, the Haunted Computer Club, PoC||GTFO, Phrack, and everyone else up doing weird stuff to their files.

Links:
- The official BGGP repo now lives here: https://github.com/binarygolf/bggp
- BGGP4 Website: https://binary.golf/4/
- Website: https://binary.golf/
- Mastodon: https://haunted.computer/@binarygolf
- Twitter: https://twitter.com/binarygolf

## Scoring

There were no score modifiers this year, so the lowest byte count wins.

Each file type has it's own scoreboard. Combinations of files (polyglots) are in their own category, sorted by specific combination.

## Single File Entries

These are files that are just one file. Polyglot files are in the next section.
### AHK

AutoHotkey (AHK) files are plain text files written in the AutoHotkey scripting language for Windows.

|Author|Date|Size|Notes|
|---|---|---|---|
|mirusu400|2023-08-16|25|Doesn't return or print 4, but copies the file in a more compact way|
|13x1 👑|2023-09-08|38||

### APK

Android Package Kit (APK) files are used by the Android operating system. They are ZIP archives containing files necessary to run code.

|Author|Date|Size|Notes|
|---|---|---|---|
|caioluders 👑|2023-09-08|6403|
|h0wdy|2023-08-25|333434|

### AppleScript
AppleScript is a scripting language used on macOS.

|Author|Date|Size|Notes|
|---|---|---|---|
|latortuga71 👑|2023-06-24|350||

### autoit3
AutoIt3 (AU3) files are used to automate GUI programs in Windows as well as general scripting.

|Author|Date|Size|Notes|
|---|---|---|---|
|gilda 👑|2023-07-03|56|

### bat
Batch (BAT) files are scripts for DOS, OS/2 and Microsoft Windows.

|Author|Date|Size|Notes|
|---|---|---|---|
|jpstewart 👑|2023-06-23|19|

### C
C files are source code that get compiled into program code. In some cases they can act almost like a script, and instruct the compiler to do additional things. 

This behavior can be entirely compiler dependent. For an extensive exploration of pre-processor wizardry, check out https://www.ioccc.org/

|Author|Date|Size|Notes|
|---|---|---|---|
|R3tr074 👑|2023-07-08|125|

### COM
COM files are a simple executable format. These files were validated within DOS Box.

|Author|Date|Size|Notes|
|---|---|---|---|
|bitrake 👑|2023-06-30|18|
|koorogi|2023-09-01|20|
|aburka|2023-09-11|21|
|Author 01|2023-07-24|21|
|JBO|2023-06-28|22|
|hed0x|2023-08-01|54|

### ELF
ELF files are the main executable format for Linux.

#### ELF32
|Author|Date|Size|Notes|
|---|---|---|---|
|CianLR 👑|2023-06-27|110|

#### ELF64

|Author|Date|Size|Notes|
|---|---|---|---|
|endofunky 👑|2023-08-31|112|Works on kernel 6.4, might need CONFIG_IA32_EMULATION|
|tecknicaltom|2023-07-23|129|
|R3tr074|2023-07-08|158|
|FlierMate|2023-06-27|290|

### Forth
Forth is a programming language. It is used in surprising places.

| Author    | Date       | Size | Notes |
| --------- | ---------- | ---- | ----- |
| MaeMiller 👑| 2023-08-31 | 349  |       |
### HTML

|Author|Date|Size|Notes|
|---|---|---|---|
|13x1 👑|2023-09-08|50|Needs to be served to work|
|13x1|2023-09-08|81||
|13x1|2023-09-08|82|As a Data URL|
|xfavatax |2023-07-17|83|
|Aleteoryx|2023-09-08|137|
|DeltaF1|2023-09-08|151|
|bob|2023-07-02|161|
|remy|2023-07-11|185|

### Javascript

#### Self-XSS
While this is technically not a "file" in the traditional sense, it's useful to demonstrate

| Author | Date | Size | Notes |
| ------ | ---- | ---- | ----- |
|13x1 👑|2023-09-08|102|

#### NodeJS

| Author | Date | Size | Notes |
| ------ | ---- | ---- | ----- |
|13x1 👑|2023-09-08|42|Node.js REPL with underscore variable|
|13x1|2023-09-08|43|Node.js REPL without underscore variable|
|13x1|2023-09-08|44|Node.js Script|
|13x1|2023-09-08|135|Node.js Server|

### Lua
Lua is a programming language. It's used in many scripting engines.

|Author|Date|Size|Notes|
|---|---|---|---|
|Flash ANG 👑|2023-07-31|36|
|bitrake|2023-06-26|65|

### Makefile
Makefiles are used to build applications in languages such as C. 

|Author|Date|Size|Notes|
|---|---|---|---|
|bitrake 👑|2023-06-25|25|
|dtm|2023-07-27|26|
|tecknicaltom|2023-06-25|34|

### Neovim Script
Neovim is a text editor based on vim. 

|Author|Date|Size|Notes|
|---|---|---|---|
|santaclz 👑|2023-06-24|19|

### NimScript
NimScript is a scripting language that can be used for a variety of tasks centered around the Nim programming language. It's used in configuration files, build tools, and other metaprogramming tasks.

|Author|Date|Size|Notes|
|---|---|---|---|
|T0k1To 👑|2023-07-11|48|

### PDF
PDF is a document format. 

|Author|Date|Size|Notes|
|---|---|---|---|
|gaycomputers 👑|2023-09-10|160|

### Perl
Perl is a high level programming language that was intended to be a general purpose scripting language for Unix systems.

|Author|Date|Size|Notes|
|---|---|---|---|
|isra 👑|2023-08-31|4|
|kpm|2023-08-25|16|
|tecknicaltom|2023-06-24|47|
|timpoiko|2023-06-24|60|

### PHP
PHP is a general purpose scripting language geared towards web development.

|Author|Date|Size|Notes|
|---|---|---|---|
|Aleteoryx 👑|2023-09-07|25|
|Flash ANG|2023-06-25|34|

### Portable Executable (PE)
Portable Executables are an exectuable format used in Windows and other platforms. There are different types of PEs which are noted. These are treated as distinct from the UEFI App category even though PEs can run on UEFI. See UEFI App for more info.

|Author|Date|Size|Notes|
|---|---|---|---|
|FlierMate 👑|2023-06-23|1024|PE|
|FuzzySec|2023-06-26|1548|.NET PE|
|FlierMate|2023-07-02|3072|DLL|
|eatscrayon|2023-07-13|19456|DLL Hijack|

### Python

Python is a high level programming language.

|Author|Date|Size|Notes|
|---|---|---|---|
|nopcorn 👑|2023-09-01|42|
|Flash ANG|2023-07-31|45|py2 only|
|retr0id|2023-09-07|46|
|bitrake|2023-09-12|49|
|caioluders|2023-07-01|50|
|CyberChords|2023-06-23|51|
|int0x80|2023-06-24|58|py3
|astreuzz|2023-07-09|66|py3

### pyc file

These are binary files containing bytecode used by the Python interpreter as a faster way to import library code. They are generated when you run `import somelibrary` and cached until there is a change to the underlying code.

There is no cross-compatibility guaranteed between different python versions due to changes in both the pyc file format and supported opcodes. This makes each entry tied to a specific Python version, which is specified in the table.

We used the [deadsnakes](https://launchpad.net/%7Edeadsnakes/+archive/ubuntu/ppa) PPA on Ubuntu to grab old versions of Python for testing. For Python 2.0 we built it from source.

```
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt update
sudo apt install python3.10
```


|Author|Date|Size|Notes|
|---|---|---|---|
|kaze 👑|2023-08-14|113|python3.6|
|Ajabep|2023-09-05|131|python2.0|
|int0x80|2023-06-24|195|python3.10|
|acron1ks|2023-07-07|204|python2.7|

### QEMU BIOS

This is a BIOS application that runs in QEMU.

|Author|Date|Size|Notes|
|---|---|---|---|
|endofunky 👑|2023-08-30|65536|

### Rizin Script

These are scripts you can run in the rizin debugger.

|Author|Date|Size|Notes|
|---|---|---|---|
|ert 👑|2023-09-08|252|Also a quine!|
### Ruby
Ruby is a high level programming language with an emphasis on programming productivity and simplicity.

|Author|Date|Size|Notes|
|---|---|---|---|
|jbrowning 👑|2023-08-22|16|
|astreuzz|2023-07-09|28|

### Shell Script

Shell scripts can be invoked in numerous ways, so we have categories for both types of entries. 

#### Invoked Without Arguments
These entries execute as is.

|Author|Date|Size|Notes|
|---|---|---|---|
| nopcorn 👑 | 2023-09-01 | 10   |
| caioluders | 2023-07-01 | 11   |
| dtm        | 2023-06-30 | 12   |
| mattpass   | 2023-06-23 | 12   |
| JBO        | 2023-06-38 | 16   |

#### Invoked With Arguments
These entries rely on command line arguments.

|Author|Date|Size|Notes|
|---|---|---|---|
| mauke 👑   | 2023-09-03 | 2    |

#### Interpreter Arguments (#! Only)

These entries do it with just the shebang "#!" and arguments to an interpreter.

##### /bin/env (With subshell)
|Author|Date|Size|Notes|
|---|---|---|---|
|13x1 👑|2023-09-08|33|

##### /bin/env (No subshell)
|Author|Date|Size|Notes|
|---|---|---|---|
|13x1 👑|2023-09-08|45|

### UEFI App

UEFI Apps are executables that run on UEFI firmware. They are responsible for low level setup and hardware configuration before your main Operating System boots. There are two executable types that can run on UEFI, the PE (Portable Executable) or the TE (Terse Executable). There is also limited scripting capabilities depending on the platform.

#### PE

|Author|Date|Size|Notes|
|---|---|---|---|
| netspooky | 2024-03-01|420| Submitted after the challenge ended |
|ic3qu33n 👑|2023-09-10|1480|Uses qemu |
|ytvwld|2023-07-10|7680|Uses uefi-run |

### VBScript
VBScript is a scripting language developed by Microsoft that is modeled on Visual Basic.

|Author|Date|Size|Notes|
|---|---|---|---|
|bitrake 👑|2023-06-25|71|

### VSCode Workspace

A [VSCode Workspace](https://code.visualstudio.com/docs/editor/workspaces) is a collection of folders and configurations that set up a working environment in VSCode. 

|Author|Date|Size|Notes|
|---|---|---|---|
|seeinglogic 👑|2023-08-24|136|

### Zip

Zip is an archive format.

|Author|Date|Size|Notes|
|---|---|---|---|
|retr0id 👑|2023-09-10|973|


## Polyglot File Entries

Polyglot files are two or more files at the same time. Here is a quick video from [LiveOverflow](https://www.youtube.com/watch?v=VVdmmN0su6E) about file formats and polyglots with links to other resources. For more Polyglot file fun, check out [BGGP2](https://github.com/binarygolf/BGGP/tree/main/2021), which was a challenge to find the smallest polyglot file of a given arrangement of files. Also check out the work of [Ange Albertini](https://github.com/corkami/pocs) and the polyglot fun in the pages of [PoC||GTFO](https://www.alchemistowl.org/pocorgtfo/).

Each file combination used by a given polyglot entry is treated as a distinct file type!

### Polyglot: BAT/PHP

|Author|Date|Size|
|---|---|---|
|Krishean 👑|2023-09-07|99|

### Polyglot: C, Haskell, Shell, Perl, Python, Make

|Author|Date|Size|
|---|---|---|
|mauke 👑|2023-09-03|376|

### Polyglot: COM, SH

|Author|Date|Size|
|---|---|---|
|JBO 👑|2023-06-29|41|

### Polyglot: Gameboy ROM, Bash

|Author|Date|Size|
|---|---|---|
|CaptnBanana 👑|2023-08-05|397|

### Polyglot: GIF, PHP

|Author|Date|Size|
|---|---|---|
|maki 👑|2023-07-06|82|

### Polyglot: PYC, PHP, SH

|Author|Date|Size|
|---|---|---|
|Ajabep 👑|2023-09-08|167|

### Polyglot: SH, Perl, Haskell

|Author|Date|Size|
|---|---|---|
|barubary 👑|2023-08-31|209|

## Community 

This year resulted in a significant amount more entries than previous years. To make sure that things go quicker in the future, we are standardizing our BGGP entry form and verification process to allow golfers to submit entries even after the challenge is over.

### BGGPx Entries

If you want to add your own entry to BGGP4 or past challenges, create a pull request to this repo with your entry file. 
```
---BEGIN BGGPx---
Submit Date: 
BGGP Challenge Number: 
Author: 
Contact Info (Optional): 
Online Presence (Website/Social Media): 
Target File Type: 
File Size: 
SHA256 Hash: 
Target Environment (How do we run the file?): 
Any additional info?: 
Link to PoC video, screenshot, or console output, if any: 
Link to writeup, if any: 
File contents (base64 encoded please): 
---END BGGPx---
```

**Make sure you** name the file with your github username, the file type, and end with `.txt` 
- Example `netspooky.py.txt`

In the case of polyglots, add underscores between each file extension. 
- Example `netspooky.exe_js_pdf.txt`

Once the PR is approved, your entry can be verified by Binary Golf Association staff, or by community members watching this repo.

### Community Verifications

If you want to verify any entries, you can use this simple text format. 

This is our verification format. You can fill it out with your information. Please use your github username for the reviewer name, or include it next to your name.
```
---BEGIN VERIFICATION---
Reviewer: 
Review Date: 
Score: 
Note: 
---END VERIFICATION---
```

If it works as is, you can say "works as is" in the Note, otherwise, document any additional information that was required to test the file.

Example
```
---BEGIN VERIFICATION---
Reviewer: netspooky
Review Date: 2023-09-11
Score: 42
Note: Works as is
---END VERIFICATION---
```

If you can't verify the entry or have a question about it, you can open a git issue and link the entry along with your comments.

Once you've verified that an entry works, append your verification text to the end of an existing entry file. Make sure to include the BEGIN VERIFICATION and END VERIFICATION lines too. Create a pull request to this repo with your changes.

## .fini

Thank you so much for checking out this year's BGGP! We hope it inspired you to play with your favorite files, and learn about new ones. See you next year! 

~ netspooky/BGA
