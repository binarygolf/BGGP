# BGGP6: RECYCLE

![](assets/BGGP6-Flyer.jpg)

See the BGGP6 challenge info [here](6.md)!

## Entries

![](assets/directory_open_cool-3.png) ![](assets/directory_open_cool-3.png) ![](assets/directory_open_cool-3.png) ![](assets/directory_open_cool-3.png) ![](assets/directory_open_cool-3.png) ![](assets/directory_open_cool-3.png) 

Single file entries

### .curlrc

The .curlrc file is a configuration file used by curl. It allows users to define default options and arguments that curl will use every time it's invoked, without needing to specify them on the command line. You can also specify a config file using the `-K` or `--config` arguments.

| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 62 | [bah](./entries/bah/bah.curlrc.md) | .curlrc | 4, 5, 6 | 4802 | [154](https://github.com/binarygolf/BGGP/issues/154) | [writeup](https://gist.github.com/bahorn/4a0d8505d84e7acab21358c39fdab4a7) | | 

### C 

| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 1368 | [OwOday](./entries/OwOday/OwOday.C.md) | C | 6 | 2984 | [176](https://github.com/binarygolf/BGGP/issues/176) | [writeup](https://github.com/OwOday/bggp6) | |

### ELF32

| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 45   | [dominikr](./entries/dominikr/dominikr.elf32.download-with-args.md) | ELF | 4 5 6 | 4819 | [174](https://github.com/binarygolf/BGGP/issues/174) | [writeup](https://github.com/dominikfhnw/bggp6-writeup/tree/main/download) | uses cli args |
| 71   | [dominikr](./entries/dominikr/dominikr.elf32.download-no-args.md) | ELF | 5 6 | 4537 | [173](https://github.com/binarygolf/BGGP/issues/173) | [writeup](https://github.com/dominikfhnw/bggp6-writeup/tree/main/download) | no cli args |
| 228  | [febnug](./entries/febnug/febnug.elf.palindrome.md) | ELF | 1, 6 | 4380 | [157](https://github.com/binarygolf/BGGP/issues/157) | [writeup](https://github.com/febnug/bggp6-writeup) | Palindrome |

### ELF64
| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 1696 | [febnug](./entries/febnug/febnug.elf-aarch64.download.md) | ELF | 5, 6 | 2912 | [160](https://github.com/binarygolf/BGGP/issues/160) | [writeup](https://github.com/febnug/bggp6-writeup) | |

### EROFS

EROFS stands for Enhanced Read-Only File System. It aims to form a generic read-only filesystem solution for various read-only use cases instead of just focusing on storage space saving without considering any side effects of runtime performance.

| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 1254 | [bilger321](./entries/bilger321/bilger321.erofs.md) 👑 | .erofs | 6 | 3098 | [149](https://github.com/binarygolf/BGGP/issues/149) | [writeup](https://gist.github.com/bilger321/3359e12f1755cc7928a134115058243f) | don't install fuse on ubuntu 22.04+ because it apparently breaks your system. |


### Forth

Forth is a stack-oriented programming language and interactive integrated development environment designed by Charles H. "Chuck" Moore and first used by other programmers in 1970. Forth has a niche in astronomical and space applications as well as a history in embedded systems. The Open Firmware boot ROMs used by Apple, IBM, Sun, and OLPC XO-1 contain a Forth environment. 

| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 3 | [continue](./entries/continue/continue.forth.md) 👑 | .forth | 6 | 4349 | [150](https://github.com/binarygolf/BGGP/issues/150) | [writeup](gemini://any-key.press/esoteric/bggp6_4th.gmi) | |

### .inputrc

| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 126 | [bah](./entries/bah/bah.inputrc.md) | .inputrc | 3 4 5 6 | 3970 | [166](https://github.com/binarygolf/BGGP/issues/166) | [writeup](https://github.com/bahorn/inputrc-bd/tree/main/bggp) | |

### Perl

Perl is a high-level, interpreted, dynamic programming language renowned for powerful text processing, system administration, and web backend development.

| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 29 | [dominikr](./entries/dominikr/dominikr.perl.crash.md) 👑 | .pl | 3 6 | 4579 | [168](https://github.com/binarygolf/BGGP/issues/168) | [writeup](https://github.com/dominikfhnw/bggp6-writeup/tree/main#perl-crasher) | crashes perl |

### Python Pip Package

| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 67 | [dtmsecurity](./entries/dtmsecurity/dtmsecurity.pip_pkg.minimal.md) 👑 | .tgz | 6 | 4285 | [161](https://github.com/binarygolf/BGGP/issues/161) | [writeup](https://rap.sh/Python_Pip_Golf) | Doesn't install, but prints "6" in the output. |
| 127 | [dtmsecurity](./entries/dtmsecurity/dtmsecurity.pip_pkg.valid.md) | .tgz | 6 | 4225 | [162](https://github.com/binarygolf/BGGP/issues/162) | [writeup](https://rap.sh/Python_Pip_Golf) | This one actually installs as a package called UNKNOWN |

### Shell Script with Args

| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 5 | [mattpass](./entries/mattpass/mattpass.sh.md) 👑 | .sh | 1 5 6 | 4859 | [151](https://github.com/binarygolf/BGGP/issues/151) | [writeup](https://pastebin.com/YBcdvF57) | Tested on debian 13 with chromium. Works as expected. |

### Shell Script no Args

| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 24 | [q3w3e3](./entries/q3w3e3/q3w3e3.bash.md) 👑 | .sh | 3 4 5 6 | 5096 | [169](https://github.com/binarygolf/BGGP/issues/169) | [writeup](https://www.gaiaonline.com/journal/?mode=view&post_id=48177153&u=44309835) [backup](https://gist.github.com/q3w3e3/2c7809fa92c75c9cac9ca37ef5696ad7) | Works as is |

### TAR

| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 148 | [dominikr](./entries/dominikr/dominikr.tar.md) 👑 | .tgz | 5 | 4204 | [178](https://github.com/binarygolf/BGGP/issues/178) | | uses a git hook to download |

### TXT

| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 1    | [int0x80](entries/int0x80/int0x80.txt.md) 👑 | TXT | 6 | 4095 | [145](https://github.com/binarygolf/BGGP/issues/145) | | |

### Lua Wireshark Plugin

| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 1    | [netspooky](entries/netspooky/netspooky.wireshark_lua.md) 👑 | Lua wireshark | 6 | 4335 | [158](https://github.com/binarygolf/BGGP/issues/158) | | |

## Polyglots

![](assets/directory_open_file_mydocs-4.png) ![](assets/directory_open_file_mydocs-4.png) ![](assets/directory_open_file_mydocs-4.png) ![](assets/directory_open_file_mydocs-4.png) ![](assets/directory_open_file_mydocs-4.png) ![](assets/directory_open_file_mydocs-4.png) 

[Polyglot](https://en.wikipedia.org/wiki/Polyglot_(computing)) entries. Each set of files used in the polyglot is treated as their own category.

### COM, Perl, Shell, Make

| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 55   | [mauke](entries/mauke/mauke.com-perl-shell-make.md) 👑 | COM, Perl, Shell, Make | 1, 2 | 4553 | [146](https://github.com/binarygolf/BGGP/issues/146) | [writeup](https://blogs.perl.org/users/mauke/2025/10/a-palindromic-polyglot-program-in-x86-machine-code-perl-shell-and-make.html) | |

### DEB, Shellscript 

| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 182 | [dominikr](./entries/dominikr/dominikr.deb-sh.md) 👑 | .deb, .sh | 2 4 5 6 | 4938 | [175](https://github.com/binarygolf/BGGP/issues/175) | [writeup](https://github.com/dominikfhnw/bggp6-writeup/tree/main/deb) | |

### ELF, PDF

| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 512 | [ilya](./entries/ilya/ilya.elf-pdf.md) 👑 | elf pdf | 2 4 6 | 3584 | [180](https://github.com/binarygolf/BGGP/issues/180) | [writeup](https://gist.github.com/ilya-lyapunov/fb2b7f66f9cfe434d664569ca6f6706c) | |
| 2571 | [EmmaStrck](./entries/EmmaStrck/EmmaStrck.elf-pdf.md) | elf pdf | 2 6 | 1781 | [179](https://github.com/binarygolf/BGGP/issues/179) | | |

### ELF, PDF, JS

| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 725 | [febnug](./entries/febnug/febnug.elf-pdf-js.md) | elf pdf js | 2 6 | 3883 | [152](https://github.com/binarygolf/BGGP/issues/152) | [writeup](https://github.com/febnug/bggp6-writeup) | |

### ELF, PDF, RAR, ZIP

| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 479  | [deluks](entries/deluks/deluks.elf-pdf-rar-zip.md) 👑 | ELF, PDF, RAR, ZIP | 2, 6 | 3873 | [147](https://github.com/binarygolf/BGGP/issues/147) | tbd | pdf requires zathura 0.5.12 at least |

### ELF, Shellscript

| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 64   | [dominikr](entries/dominikr/dominikr.elf-sh.md) 👑 | ELF, .sh | 2 | 4032 | [144](https://github.com/binarygolf/BGGP/issues/144) | | Works on bash 5.1 or lower due to ELF header checks in 5.2+ (see entry) |

### NetPBM, shellscript

| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 25 | [deepseagirl](./entries/deepseagirl/deepseagirl.netpbm-shell.md) 👑 | .pbm, .sh | 2, 6 | 4327 | [159](https://github.com/binarygolf/BGGP/issues/159) | | Seems to work only on MacOS |

### Powershell, TXT

| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 1    | [squiblydoo](./entries/squiblydoo/squiblydoo.ps1-txt.md) 👑 | .ps1, .txt | 2, 6 | 4351 | [153](https://github.com/binarygolf/BGGP/issues/153) | | |

### Shell, Perl

| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 26 | [q3w3e3](./entries/q3w3e3/q3w3e3.bash-perl.crash.md) 👑 | .sh, .pl | 2 3 4 5 6 | 5350 | [171](https://github.com/binarygolf/BGGP/issues/171) | [writeup](https://www.gaiaonline.com/journal/?mode=view&post_id=48177153&u=44309835) [backup](https://gist.github.com/q3w3e3/2c7809fa92c75c9cac9ca37ef5696ad7) | Needs curl 8.10.1 or higher, args in file name |
| 44 | [q3w3e3](./entries/q3w3e3/q3w3e3.bash-perl.no-args.md) 👑 | .sh, .pl | 2 3 4 5 6 | 5332 | [172](https://github.com/binarygolf/BGGP/issues/172) | [writeup](https://www.gaiaonline.com/journal/?mode=view&post_id=48177153&u=44309835) [backup](https://gist.github.com/q3w3e3/2c7809fa92c75c9cac9ca37ef5696ad7) | Works as is, no args in file name |

### Shell, ZIP

| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 179 | [mattpass](./entries/mattpass/mattpass.sh-zip.md) 👑 | .sh, .sql, .zip | 1 2 3 4 5 6 | 5453 | [165](https://github.com/binarygolf/BGGP/issues/165) | [writeup](https://gist.github.com/mattpass/8b40b2e2b946f8bf7474a001b30f3a85) | 🔥 Satisfies all 6 BGGPs! |

### SQL, Shellscript, ZIP

| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 159 | [mattpass](./entries/mattpass/mattpass.sh-sql-zip.md) 👑 | .sh, .sql, .zip | 2 5 6 | 4705 | [164](https://github.com/binarygolf/BGGP/issues/164) | [writeup](https://pastebin.com/13tPuZaB) | |
