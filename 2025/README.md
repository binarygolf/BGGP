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


### EROFS

EROFS stands for Enhanced Read-Only File System. It aims to form a generic read-only filesystem solution for various read-only use cases instead of just focusing on storage space saving without considering any side effects of runtime performance.

| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 1254 | [bilger321](./entries/bilger321/bilger321.erofs.md) 👑 | .erofs | 6 | 3098 | [149](https://github.com/binarygolf/BGGP/issues/149) | [writeup](https://gist.github.com/bilger321/3359e12f1755cc7928a134115058243f) | don't install fuse on ubuntu 22.04+ because it apparently breaks your system. |


## Forth

Forth is a stack-oriented programming language and interactive integrated development environment designed by Charles H. "Chuck" Moore and first used by other programmers in 1970. Forth has a niche in astronomical and space applications as well as a history in embedded systems. The Open Firmware boot ROMs used by Apple, IBM, Sun, and OLPC XO-1 contain a Forth environment. 

| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 3 | [continue](./entries/continue/continue.forth.md) 👑 | .forth | 6 | 4349 | [150](https://github.com/binarygolf/BGGP/issues/150) | [writeup](gemini://any-key.press/esoteric/bggp6_4th.gmi) | |

### TXT

| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 1    | [int0x80](entries/int0x80/int0x80.txt.md) 👑 | TXT | 6 | 4095 | [145](https://github.com/binarygolf/BGGP/issues/145) | | |


## Polyglots

![](assets/directory_open_file_mydocs-4.png) ![](assets/directory_open_file_mydocs-4.png) ![](assets/directory_open_file_mydocs-4.png) ![](assets/directory_open_file_mydocs-4.png) ![](assets/directory_open_file_mydocs-4.png) ![](assets/directory_open_file_mydocs-4.png) 

[Polyglot](https://en.wikipedia.org/wiki/Polyglot_(computing)) entries. Each set of files used in the polyglot is treated as their own category.

### COM, Perl, Shell, Make

| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 55   | [mauke](entries/mauke/mauke.com-perl-shell-make.md) 👑 | COM, Perl, Shell, Make | 1, 2 | 4553 | [146](https://github.com/binarygolf/BGGP/issues/146) | [writeup](https://blogs.perl.org/users/mauke/2025/10/a-palindromic-polyglot-program-in-x86-machine-code-perl-shell-and-make.html) | |

## ELF, PDF, RAR, ZIP

| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 479  | [deluks](entries/deluks/deluks.elf-pdf-rar-zip.md) 👑 | ELF, PDF, RAR, ZIP | 2 | 3617 | [147](https://github.com/binarygolf/BGGP/issues/147) | tbd | pdf requires zathura 0.5.12 at least |

### ELF, Shellscript

| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 64   | [dominikr](entries/dominikr/dominikr.elf-sh.md) 👑 | ELF, .sh | 2 | 4032 | [144](https://github.com/binarygolf/BGGP/issues/144) | | Works on bash 5.1 or lower due to ELF header checks in 5.2+ (see entry) |

### NetPBM, shellscript

| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 25 | [deepseagirl](./entries/deepseagirl/deepseagirl.netpbm-shell.md) 👑 | .pbm, .sh | 2, 6 | 4327 | [159](https://github.com/binarygolf/BGGP/issues/159) | | Seems to work only on MacOS |

## Powershell, TXT

| Size | Author | Type | BGGP | Score | Issue | Writeup | Note |
|------|--------|------|------|-------|-------|---------|------|
| 1    | [squiblydoo](./entries/squiblydoo/squiblydoo.ps1-txt.md) 👑 | .ps1, .txt | 2, 6 | 4351 | [153](https://github.com/binarygolf/BGGP/issues/153) | | |
