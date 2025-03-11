# BGGP5: Download

https://binary.golf/5/

June 21 2024 to September 6 2024

## Entries

Here are the entries for this year

### 010 Editor

010 Editor is a commercial editor for text and binary files.  It has a powerful scripting language that supports running external files.

| Size | Author                                        | File Type | Writeup | Note                                |
|------|-----------------------------------------------|-----------|---------|-------------------------------------|
| 57   | [QoL15155](./entries/QoL15155/QoL15155.1sc.txt) 👑 | .1sc | | [git issue](https://github.com/binarygolf/BGGP/issues/113) |

### Adobe ExtendScript

ExtendScript is a scripting language and an associated toolkit developed by Adobe Systems, intended for use with Creative Suite and Technical Communication Suite products. It is a dialect of the ECMAScript 3 standard and therefore similar to JavaScript and ActionScript. 

| Size | Author | File Type | Writeup | Note |
|------|--------|-----------|---------|------|
| 84   | [theXappy](./entries/theXappy/theXappy.adobe-jsx.txt) 👑 | .jsx | | [git issue](https://github.com/binarygolf/BGGP/issues/115) |

### Awk

AWK is a domain-specific language designed for text processing and typically used as a data extraction and reporting tool.

#### Runs With CLI Arguments

| Size | Author                                        | File Type | Writeup | Note                                |
|------|-----------------------------------------------|-----------|---------|-------------------------------------|
| 34   | [bah](./entries/bah/bah.awk.txt) 👑 | .awk | | [git issue](https://github.com/binarygolf/BGGP/issues/50) - Runs an awk file via `-E` argument. |

#### Runs Without CLI Arguments

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 88 | [krishean](./entries/krishean/krishean.awk.txt) 👑 | .awk | | [git issue](https://github.com/binarygolf/BGGP/issues/36) |

### Burp Suite Settings JSON

Settings file for the Burp Suite web vulnerability scanner.

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 216 | [caioluders](./entries/caioluders/caioluders.burp-settings-json.txt) 👑 | .json | | [git issue](https://github.com/binarygolf/BGGP/issues/74) |

### CMake

CMake is cross-platform, free, and open-source software for build automation, testing, packaging and installation of software by using a compiler-independent method.

| Size | Author                                         | File Type | Writeup | Note |
|------|------------------------------------------------|-----------|---------|------|
| 283  | [0xca7](./entries/0xca7/0xca7.CMakeLists.txt) 👑 | .txt      | | |

### COM

COM files are a simple executable format. Found in DOS and other systems.

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 250 | [qkumba](./entries/qkumba/qkumba.com.txt) 👑 | COM | [writeup](http://pferrie.epizy.com/misc/tmp/dos.txt) | [git issue](https://github.com/binarygolf/BGGP/issues/120) - Tested on Windows 7 32 bit |

### ELF 32-bit

ELF is short for Executable and Linkable Format. It’s a format used for storing binaries, libraries, and core dumps on disks in Linux and Unix-based systems.

Moreover, the ELF format is versatile. Its design allows it to be executed on various processor types. This is a significant reason why the format is common compared to other executable file formats.

#### Runs With CLI Arguments

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 76 | [mebeim](./entries/mebeim/mebeim.elf32-cli-args.txt) 👑 | .elf | [writeup](https://github.com/mebeim/bggp) | |
| 89 | [mndz](./entries/mndz/mndz.elf.x86.32.txt) | .elf | https://github.com/0x6d6e647a/bggp-2024 | |

#### Runs Without CLI Arguments

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 81 | [VINSERTF128](./entries/VINSERTF128/VINSERTF128.elf32.txt) 👑 | .elf | [writeup](https://gist.github.com/VINSERTF128/a42d2d15abad30f4477665734f60b0d9) | [git issue](https://github.com/binarygolf/BGGP/issues/135) |
| 82 | [mebeim](./entries/mebeim/mebeim.elf32.txt) | .elf | [writeup](https://github.com/mebeim/bggp) | [git issue](https://github.com/binarygolf/BGGP/issues/118) - Needs mmap_min_addr set to 0 && uses shortened url http://7f.uk |
| 162 | [febnug](.entries/febnug/febnug.elf32.txt) | .elf | [writeup](https://catalyst.fnlqxz.my.id/misc/bggp5-entry.txt) | [git issue](https://github.com/binarygolf/BGGP/issues/133) | 
| 450 | [neuschaefer](./entries/neuschaefer/neuschaefer.elf-ARMv5-J.txt) | .elf | [writeup](https://codeberg.org/neuschaefer/bggp5-jazelle) | [git issue](https://github.com/binarygolf/BGGP/issues/101) - uses ARM Jazelle DBX and openssl, see writeup! |

### ELF 64-bit

This is the 64 bit variant of the Executable and Linkable Format with only minor differences from the 32 bit version. 

The main difference between the 32-bit and the 64-bit versions lies in the differences of struct field ordering and bit widths.

#### Runs With CLI Arguments

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 105 | [VINSERTF128](./entries/VINSERTF128/VINSERTF128.elf64-cli-args.txt) 👑 | .elf | [writeup](https://gist.github.com/VINSERTF128/a42d2d15abad30f4477665734f60b0d9) | Passes 'https://binary.golf/5/5' via argv[1] |
| 112 | [mebeim](./entries/mebeim/mebeim.elf64.txt) | .elf | [writeup](https://github.com/mebeim/bggp) | [git issue](https://github.com/binarygolf/BGGP/issues/123) - Passes 'https://binary.golf/5/5' via argv[1] |
| 3043 | [retr0id](./entries/retr0id/retr0id.elf64.txt) | .elf | [writeup](https://github.com/DavidBuchanan314/kurl) | Static aarch64 binary, uses ktls and kernel crypto apis to make a userland golf'd curl implementation |

#### Runs Without CLI Arguments

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 109 | [VINSERTF128](./entries/VINSERTF128/VINSERTF128.elf64.txt) 👑 | .elf | [writeup](https://gist.github.com/VINSERTF128/a42d2d15abad30f4477665734f60b0d9) | [git issue](https://github.com/binarygolf/BGGP/issues/136) |
| 146 | [amnesia](./entries/amnesia/amnesia.elf64.txt) | .elf | [writeup](https://amnesia.sh/bggp/2024/09/01/bggp5.html) | |
| 620 | [bah](./entries/bah/bah.elf64.txt) | .elf | [writeup](https://github.com/bahorn/bphage) | Uses a variety of cool techniques to load libssl. Check the writeup and source! |

### Elixir

Elixir is a dynamic, functional language that runs on the Erlang VM, known for creating low-latency, distributed, and fault-tolerant systems.

#### Runs With CLI Arguments
| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 105 | [riesha](./entries/riesha/riesha.exs.txt) 👑 | .exs | | Passes domain in via commandline argument |

#### Runs Without CLI Arguments

| Size | Author | File Type | Writeup | Note |
|------|--------|-----------|---------|------|
| 92 | [haxrob](./entries/haxrob/haxrob.exs.txt) 👑 | .exs | | |
| 118 | [riesha](./entries/riesha/riesha.exs.txt)  | .exs | | |

### Emacs Lisp

Emacs Lisp code is used to modify, extend and customize Emacs.

| Size | Author | File Type | Writeup | Note |
|------|--------|-----------|---------|------|
| 64 | [ZharMeny](./entries/ZharMeny/ZharMeny.emacs-lisp.txt) 👑 | .el | [writeup](https://github.com/ZharMeny/BGGP-5-submission) | [git issue](https://github.com/binarygolf/BGGP/issues/131) |

### Epub

E-book file format standard by the International Digital Publishing Forum

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 725 | [vvx7](./entries/vvx7/vvx7.epub.txt) 👑 | .epub | [Writeup](https://vvx7.io/posts/2024/06/bggp5-epub/) | |

### Erlang

Erlang is a general-purpose, concurrent, functional high-level programming language.

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 104 | [rqu](./entries/rqu/rqu.erl.txt) 👑 | .erl | [writeup](https://hacking.rip/bggp5.gmi) | [git issue](https://github.com/binarygolf/BGGP/issues/127) |
| 129 | [haxrob](./entries/haxrob/haxrob.erl.txt) 👑 | .erl | | |

### Erlang BEAM Bytecode

BEAM is part of the Erlang Run-Time System (ERTS), which compiles Erlang source code into bytecode, which is then executed on the BEAM.

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 207 | [rqu](./entries/rqu/rqu.beam.txt) 👑 | .beam | [writeup](https://hacking.rip/bggp5.gmi) | [git issue](https://github.com/binarygolf/BGGP/issues/128) |

### GDB Script

GDB scripts are used to automate actions inside of GDB, the GNU Debugger.

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 31 | [QoL15155](QoL15155/QoL15155.gdb.txt) 👑 | .gdb | | |

### Go

Go is a statically typed, compiled high-level programming language designed at Google by Robert Griesemer, Rob Pike, and Ken Thompson.

Run from source with `go run`

#### Runs Without CLI Arguments

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 138 | [airencracken](./entries/airencracken/airencracken.go.txt) 👑 | .go | | |

#### Runs With CLI Arguments

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 63 | [mebeim](./entries/mebeim/mebeim.go-cli-args.txt) 👑 | .go | [writeup](https://github.com/mebeim/bggp) | [git issue](https://github.com/binarygolf/BGGP/issues/116) |
| 121 | [Inventhrice](./entries/Inventhrice/Inventhrice.go.txt) | .go | [writeup](https://github.com/Inventhrice/bggp5-entry/blob/main/writeup.md) | [git issue](https://github.com/binarygolf/BGGP/issues/132) |


### HTML

HyperText Markup Language is the standard markup language for documents designed to be displayed in a web browser. 

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 42 | [dtmsecurity](./entries/dtmsecurity/dtmsecurity.html.txt) 👑 | .html | | [git issue](https://github.com/binarygolf/BGGP/issues/107) - uses short url |
| 62 | [mattpass](./entries/mattpass/mattpass.html.txt) | .html | [writeup](https://pastebin.com/pAcukVNK) | uses a url shortener |
| 67 | [caioluders](./entries/caioluders/caioluders.html.txt) | .html | | |
| 76 | [vvx7](./entries/vvx7/vvx7.html.txt) | .html | | |
| 80 | [mattpass](./entries/mattpass/mattpass.html.txt)  | .html | | |
| 95 | [yael333](./entries/yael333/yael333.html.txt) | .html | | |

### HTTP

HTTP (Hypertext Transfer Protocol) is an application layer protocol in the Internet protocol suite model for distributed, collaborative, hypermedia information systems.

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 37 | [continue](./entries/continue/continue.http.txt)  👑 | .html | [writeup](gemini://any-key.press/esoteric/bggp5_openssl.gmi) | Uses openssl |

### Java Class

Java is a high-level, general-purpose, memory-safe, object-oriented programming language. 

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 274 | [jbo](./entries/jbo/jbo.java-macos-only.txt) 👑 | .class | [writeup](https://github.com/yo-yo-yo-jbo/bggp5_java_editing) | [git issue](https://github.com/binarygolf/BGGP/issues/124) - works on macos only, see entry for details |
| 275 | [jbo](./entries/jbo/jbo.java.txt) | .class | [writeup](https://github.com/yo-yo-yo-jbo/bggp5_java_editing) | [git issue](https://github.com/binarygolf/BGGP/issues/97) |

### Julia

Julia is a general-purpose programming language, most commonly used for numerical analysis and computational science.

| Size | Author                                              | File Type | Writeup | Note |
|------|-----------------------------------------------------|-----------|---------|------|
| 30   | [ luskabol ](./entries/luskabol/luskabol.jl.txt) 👑 | .html | | |

### LaTeX

LaTeX is a software system for typesetting documents. LaTeX markup describes the content and layout of the documents.

#### Runs With CLI Arguments
| Size | Author                                             | File Type | Writeup | Note                               |
|------|----------------------------------------------------|-----------|---------|------------------------------------|
| 64   | [luskabol](./entries/luskabol/luskabol.tex.txt) 👑 | .tex      | | Requires `--shell-escape` argument |

### LLVM-IR

LLVM is designed around a language-independent intermediate representation (IR) that serves as a portable, high-level assembly language that can be optimized with a variety of transformations over multiple passes.

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 114 | [bah](./entries/bah/bah.ll.txt) 👑 | .ll | | [git issue](https://github.com/binarygolf/BGGP/issues/42) |

### Lua

Lua is a lightweight, high-level programming language designed primarily for embedded use in applications.

#### Runs With CLI Arguments
| Size | Author                                                                | File Type | Writeup | Note                               |
|------|-----------------------------------------------------------------------|-----------|---------|------------------------------------|
| 35   | [Rodrigo Mamedio](./entries/RodrigoMamedio/RodrigoMamedio.lua.txt) 👑 | .lua      | | Passes the command via argument, needs curl in path |

#### Runs Without CLI Arguments
| Size | Author                                                                | File Type | Writeup | Note               |
|------|-----------------------------------------------------------------------|-----------|---------|--------------------|
| 36   | [Dur4ndal](./entries/Dur4ndal/Dur4ndal.lua.txt) 👑 | .lua      | | Needs curl in path |

### Makefile

| Size | Author                                    | File Type | Writeup | Note |
|------|-------------------------------------------|-----------|---------|------|
| 10 | [Krishean](./entries/Krishean/Krishean.Makefile.txt) 👑 | Makefile | | [git issue](https://github.com/binarygolf/BGGP/issues/82) - uses cli args |

### m3u

M3U (MP3 URL or Moving Picture Experts Group Audio Layer 3 Uniform Resource Locator in full) is a computer file format for a multimedia playlist. Careless handling of M3U playlists has been the cause of vulnerabilities in many music players such as VLC media player, iTunes, Winamp, and many others.

| Size | Author                                                                | File Type | Writeup | Note                               |
|------|-----------------------------------------------------------------------|-----------|---------|------------------------------------|
| 252   | [bah](./entries/bah/bah.m3u.txt) 👑 | .m3u      | [Writeup](https://github.com/bahorn/BGGP5-m3u-vlc/tree/master) | VLC only, with CLI arguments |

### Nix

Nix package manager ensures immutable packages and reproducible builds across environments. Also, cat ears.

| Size | Author                                    | File Type | Writeup | Note |
|------|-------------------------------------------|-----------|---------|------|
| 49   | [famfo](./entries/famfo/famfo.nix.txt) 👑 | .nix      | |  |

### NodeJS

Node.js runs on the V8 JavaScript engine, and executes JavaScript code outside a web browser.

#### Runs With CLI Arguments
| Size | Author                                    | File Type | Writeup | Note |
|------|-------------------------------------------|-----------|---------|------|
| 23   | [pr3y](./entries/pr3y/pr3y.nodejs.txt) 👑 | .js       | | Uses command line arguments to pass the url and code |

#### Runs Without CLI Arguments

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 51 | [luskabol](./entries/luskabol/luskabol.js.txt) 👑 | .js | | Uses an http link shortener |
| 68 | [mattpass](./entries/mattpass/mattpass.js.txt) | .js | | |

### Nmap

The Nmap Scripting Engine (NSE) allows users to write (and share) simple scripts (using the Lua programming language ) to automate a wide variety of networking tasks.

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 98 | [eatscrayon](./entries/eatscrayon/eatscrayon.nse.txt) 👑 | .nse | | nmap 127.0.0.1 -p 69 --script=bggp5 |

### Nuclei Template

Nuclei templates are used to configure the Nuclei vulnerability scanner. 

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 134 | [caioluders](./entries/caioluders/caioluders.nuclei.txt) 👑 | .yaml | | [git issue](https://github.com/binarygolf/BGGP/issues/67) |

### NuGet Package

NuGet is a package manager for .NET. 

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 491  | [theXappy](./entries/theXappy/theXappy.nupkg.txt) 👑 | .nupkg | [writeup](https://github.com/theXappy/NupkgGolfing) | [git issue](https://github.com/binarygolf/BGGP/issues/111) | 


### ODS (OpenDocument Spreadsheet)

The Open Document Spreadsheet (ODS) is an open, XML based file format for spreadsheets. 

| Size | Author                                          | File Type | Writeup | Note |
|------|-------------------------------------------------|-----------|---------|-----|
| 720  | [koorogi](./entries/koorogi/koorogi.ods.txt) 👑 | .ods      | | |

### Perl

Perl is a high level programming language that was intended to be a general purpose scripting language for Unix systems.

#### Runs With CLI Arguments

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 8 | [mauke](./entries/mauke/mauke.pl2.txt) 👑 | .pl | | Uses command line arguments to pass the url and code |
| 18 | [vvx7](./entries/vvx7/vvx7.pl.txt) | .pl | | Uses command line arguments and environment variables |
| 41 | [airencracken](./entries/airencracken/airencracken.pl.txt) | .pl | | Uses command line arguments to pass url and load modules |

#### Runs Without CLI Arguments

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 7 | [vvx7](./entries/vvx7/vvx7.pl2.txt) 👑 | .pl | | Executes code in the filename |
| 47 | [mauke](./entries/mauke/mauke.pl.txt) | .pl | | |

### PHP

PHP (recursive acronym for PHP: Hypertext Preprocessor) is a widely-used open source general-purpose scripting language that is especially suited for web development and can be embedded into HTML.

#### Runs With CLI Arguments

| Size | Author                                               | File Type | Writeup | Note |
|------|------------------------------------------------------|-----------|---------|------|
| 8    | [Krishean](./entries/krishean/krishean.php.txt) 👑  | .php | | Uses command line arguments to pass the url and code |

#### Runs Without CLI Arguments

| Size | Author                                             | File Type | Writeup | Note |
|------|----------------------------------------------------|-----------|---------|------|
| 15   | [Digoguenes](./entries/Digoguenes/Digoguenes.php.15.txt) 👑 | .php | | [git issue](https://github.com/binarygolf/BGGP/issues/96) Uses file path to contruct the URL |
| 26   | [mebeim](./entries/mebeim/mebeim.php.txt) | .php | [writeup](https://github.com/mebeim/bggp) | [git issue](https://github.com/binarygolf/BGGP/issues/69) Requires `allow_url_include` and `short_path_on` in php.ini. File must be run from directory `/binary.golf/5/5` |
| 30   | [Digoguenes](./entries/Digoguenes/Digoguenes.php.txt) | .php | | Calls curl from php |
| 36   | [Dur4ndal](./entries/Dur4ndal/Dur4ndal.php.txt)  | .php | | Requires php.ini option `allow_url_include` and `short_open_tag` to be enabled |
| 39   | [Aleteoryx](./entries/Aleteoryx/Aleteoryx.php.txt) | .php | | Requires php.ini option `allow_url_include` to be enabled |

### Portable Executable (PE)

Portable Executables are an executable format used in Windows and other platforms. There are different types of PEs which are noted. These are treated as distinct from the UEFI App category even though PEs can run on UEFI. See UEFI App for more info.  The types are split further into 32-bit specifically, 64-bit compatible, and 64-bit specifically, since they present different challenges.

**32-bit Portable Executable on 32-bit Windows**

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 157 | [qkumba](./entries/qkumba/qkumba.pe32-winxp.txt) 👑 | PE | [writeup](http://pferrie.epizy.com/misc/tmp/winpe32.txt) | [git issue](https://github.com/binarygolf/BGGP/issues/106) - works on Windows XP and earlier |

**32-bit Portable Executable on 32- or 64-bit Windows**

| Size | Author                                                          | File Type | Writeup | Note |
|------|-----------------------------------------------------------------|-----------|---------|------|
| 268  | [qkumba](./entries/qkumba/qkumba.32pe.txt) 👑 | PE | [Writeup](http://pferrie.epizy.com/misc/tmp/winpe.txt) | |
| 385  | [kspalaiologos](./entries/kspalaiologos/kspalaiologos.pe.385.txt) | PE | | [git issue](https://github.com/binarygolf/BGGP/issues/46) |
| 399  | [kspalaiologos](./entries/kspalaiologos/kspalaiologos.pe.txt) | PE | | |
| 596  | [fliermate](./entries/fliermate/fliermate.pe.txt) | PE | [Source Code](https://github.com/flier-mate/BGGP5/blob/main/5.asm) | |

**64-bit Portable Executable on 64-bit Windows**

| Size | Author                                                          | File Type | Writeup | Note |
|------|-----------------------------------------------------------------|-----------|---------|------|
| 268  | [qkumba](./entries/qkumba/qkumba.64pe.txt) 👑                   | PE | [Writeup](http://pferrie.epizy.com/misc/tmp/winpe64.txt) | Calls curl from executable |
| 345  | [frank2](./entries/frank2/frank2.exe.txt)                    | PE | | |

### PowerShell Script

PowerShell scripts can be invoked in numerous ways, so we have categories for both types of entries.

#### Runs With CLI Arguments

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 6 | [Zach](./entries/Zach/Zach.Powershell.txt) 👑 | .ps1 | | Requires setting an environment variable to hold the actual code |

#### Runs Without CLI Arguments

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 14 | [gremlinbeet](./entries/gremlinbeet/gremlinbeet.ps1.txt) 👑 | .ps | [Writeup](https://github.com/gremlinbeet/binarygolf/blob/main/bggp5/powershell14.adoc) |  |
| 22 | [nephryte](./entries/nephryte/nephryte.ps.txt)   | .ps | |  |
| 35 | [remy](./entries/remy/remy.ps1.txt) | .ps1 | |  |
| 88 | [theXappy](./entries/theXappy/theXappy.ps1.txt) | .ps1 | |  |

### Python

Python is a high-level, general-purpose programming language. Its design philosophy emphasizes code readability with the use of significant indentation. 

#### Runs With CLI Arguments

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 12 | [Luidiblu](./entries/Luidiblu/Luidiblu.py.txt) 👑 | .py | | Passes entire command via arguments |
| 266 | [hyp](./entries/hyp/hyp.py-ebpf.txt) | .py | [writeup](https://scratchadams.github.io/posts/bggp5/) | [git issue](https://github.com/binarygolf/BGGP/issues/83) - Uses an ebpf filter to set all requests to https://binary.golf/5/5 | 

#### Runs Without CLI Arguments

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 22 | [continue](./entries/continue/continue.py.txt) 👑 | .py | [writeup](gemini://any-key.press/esoteric/bggp5_pyc.gmi) | Executes the filename as a script |
| 35 | [Aaron DeVera](./entries/Aaron%20DeVera/Aaron%20DeVera.py.txt) | .py | | Passes entire command in the file name and executes |
| 41 | [dtmsecurity](./entries/dtmsecurity/dtmsecurity.py.txt)   | .py | | Uses a URL shortener |
| 46 | [jbo](./entries/jbo/jbo.py.txt)   | .py | | |
| 64 | [caioluders](./entries/caioluders/caioluders.py.txt) | .py | | Needs requests module installed |
| 77 | [matteyeux](./entries/matteyeux/matteyeux.py.txt) | .py | | |
| 86 | [Aleteoryx](./entries/Aleteoryx/Aleteoryx.py.txt) | .py | | Uses standard library only |


### Python .pyc

In Python, .pyc files are compiled bytecode files that are generated by the Python interpreter when a Python script is imported or executed. They can also be executed as standalone programs.

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 120 | [continue](./entries/continue/continue.pyc.txt) 👑 | .py | [writeup](gemini://any-key.press/esoteric/bggp5_pyc.gmi) | Executes the filename with python bytecode. |

### QR Code

A QR code, quick-response code, is a type of two-dimensional matrix barcode invented in 1994 by Masahiro Hara of Japanese company Denso Wave for labelling automobile parts.

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 157 | [mattpass](./entries/mattpass/mattpass.qr-code-gif.txt) 👑 | .gif | [writeup](https://pastebin.com/pAcukVNK) | [git issue](https://github.com/binarygolf/BGGP/issues/141) - uses a url shortener | 

### Radare2
Radare2 is a featureful low-level command-line tool that provides a set of libraries and plugins to ease reverse engineering tasks.

#### Runs With CLI Arguments

| Size | Author                                                  | File Type | Writeup | Note                    |
|------|---------------------------------------------------------|-----------|---------|-------------------------|
| 46   | [caioluders](./entries/caioluders/caioluders.r2.txt) 👑 | .r2       | | Evaluates a config file |

### Ruby

Ruby is a high level programming language with an emphasis on programming productivity and simplicity.

#### Runs With CLI Arguments

| Size | Author                                    | File Type | Writeup | Note |
|------|-------------------------------------------|-----------|---------|------|
| 7    | [thedeadbyte](./entries/thedeadbyte/thedeadbyte.rb.txt) 👑 | .rb | | Uses command line args and curl |
| 12   | [luskabol](./entries/luskabol/luskabol.rb.txt)  | .rb | | Passes the entire command via arguments, needs curl in path |
| 27   | [vvx7](./entries/vvx7/vvx7.rb.txt)        | .rb | | Entry loads open-uri via the -r argument, URL passed on command line |

#### Runs Without CLI Arguments

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 51 | [demon-i386](./entries/demon-i386/demon-i386.rb.txt) 👑 | .rb | | Entry loads the 'net/http' library via the -r argument |

### Shellcode

Shellcode is machine code for a given CPU architecture, often used in exploits.

| Size | Author | File Type | Writeup | Note |
|------|--------|-----------|---------|------|
| 46 | [jbo](./entries/jbo/jbo.shellcode.txt) 👑 | .bin | [writeup](https://github.com/yo-yo-yo-jbo/bggp5_linux_shellcode) | [git issue](https://github.com/binarygolf/BGGP/issues/52) |

### Shell Script

Shell scripts can be invoked in numerous ways, so we have categories for both types of entries.

#### Runs With CLI Arguments

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 2 | [jbo](./entries/jbo/jbo.sh.txt) 👑 | .sh | | Passes the entire command via arguments, needs curl in path |
| 5 | [oriel](./entries/oriel/oriel.sh.txt) | .sh | | Passes part of the command in the file name, with arguments |
| 7 | [mattpass](./entries/mattpass/mattpass.sh.txt) | .sh | | Passes the url via command line argument |
| 97 | [mattpass](./entries/mattpass/mattpass.sh.97.txt) | .sh | [writeup](https://pastebin.com/pAcukVNK) | Uses the PS1 to download the file every time the shell starts up. Could technically be 0 bytes but we are counting based on the total size of the oneliner. It could also be counted as 38 bytes due to the addition to the .bashrc. |

#### Runs Without CLI Arguments

| Size | Author                                                    | File Type | Writeup | Note                                               |
|------|-----------------------------------------------------------|-----------|---------|----------------------------------------------------|
|  2   | [Luna Hart](./entries/Luna%20Hart/Luna%20Hart.sh.txt) 👑  | .sh | | Passes entire command in the file name and executes |
| 11   | [oriel](./entries/oriel/oriel.sh2.txt)                   | .sh | | Passes entire command in the file name and executes |
| 13   | [dtmsecurity](./entries/dtmsecurity/dtmsecurity.sh.txt) | .sh | | Uses a redirect to shorten the URL                 |
| 19   | [mauke](./entries/mauke/mauke.sh.txt)                     | .sh | | Uses the perl LWP tools with SSL support           |

### SQL 

Structured Query Language (SQL) is a domain-specific language used to manage data, especially in a relational database management system (RDBMS).

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 48 | [mattpass](./entries/mattpass/mattpass.sql.txt) 👑 | .sql | [writeup](https://pastebin.com/pAcukVNK) | [git issue](https://github.com/binarygolf/BGGP/issues/140) - Uses link shortener and sqlite-http | 

### SVG

Scalable Vector Graphics is an XML-based vector image format for defining two-dimensional graphics, having support for interactivity and animation. The SVG specification is an open standard developed by the World Wide Web Consortium since 1999.

| Size | Author | File Type | Writeup | Note |
|------|--------|-----------|---------|------|
| 108  | [caioluders](./entries/caioluders/caioluders.svg.txt) 👑 | .svg | | [git issue](https://github.com/binarygolf/BGGP/issues/84) |
| 111  | [avlidienbrunn](./entries/avlidienbrunn/avlidienbrunn.svg.txt) | .svg | | Needs to be served and viewed in Firefox. |
| 125  | [Kasumivero](./entries/Kasumivero/Kasumivero.svg.txt) | .svg | | Needs to be served and viewed in Firefox. |
| 248  | [vvx7](./entries/vvx7/vvx7.svg.txt) | .svg | | Needs to be served and viewed in Firefox. |

### UEFI App

UEFI Apps are executables that run on UEFI firmware. They are responsible for low level setup and hardware configuration before your main Operating System boots. There are two executable types that can run on UEFI, the PE (Portable Executable) or the TE (Terse Executable). There is also limited scripting capabilities depending on the platform.

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 316 | [mebeim](./entries/mebeim/mebeim.pe-uefi.txt) 👑 | .efi (PE) | [writeup](https://github.com/mebeim/bggp/blob/master/uefi/README.md) | [git issue](https://github.com/binarygolf/BGGP/issues/130) |

### Uiua

Uiua (pronounced "wee-wuh") is a stack-based array programming language. Documentation, examples, and an online interpreter can be found at uiua.org.

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 146 | [pr3y](./entries/pr3y/pr3y.ua.txt) 👑 | .ua | | [git issue](https://github.com/binarygolf/BGGP/issues/103) |

### URL

URL files are links to websites, that can be stored in the filesystem.

| Size | Author | File Type | Writeup | Note |
|------|------|-----------|---------|------|
|  31  | [dtmsecurity](./entries/dtmsecurity/dtmsecurity.url.txt) 👑 | .bat |  | Uses a link shortener |

### VBScript

VBScript is a scripting language that grew out of Visual Basic.

| Size | Author | File Type | Writeup | Note |
|------|------|-----------|---------|------|
| 129  | [sdb](./entries/sdb/sdb.vbs.txt) 👑 | .vbs | https://vacantmotel.neocities.org/stuff/golf/vbs2024 |  |


### VSCode Workspace

A [VSCode Workspace](https://code.visualstudio.com/docs/editor/workspaces) is a collection of folders and configurations that set up a working environment in VSCode.

| Size | Author | File Type | Writeup | Note |
|------|------|-----------|---------|------|
| 134 | [theXappy](./entries/theXappy/theXappy.vscode-workspace.txt) 👑 | .code-workspace | | [git issue](https://github.com/binarygolf/BGGP/issues/119) |


### Windows Batch

Windows Batch files are a scripting language inherited from DOS.

| Size | Author | File Type | Writeup | Note |
|------|------|-----------|---------|------|
|   3  | [gremlinbeet](./entries/gremlinbeet/gremlinbeet.bat.txt) 👑 | .bat | [writeup](https://github.com/gremlinbeet/binarygolf/blob/main/bggp5.batch3.adoc) | Passes entire command in file name and executes, requires Powershell |
|   5  | [Krishean](./entries/Krishean/Krishean.bat.txt)   | .bat |  | Passes entire command in file name and executes |

## Polyglots

### Shell Script / Linux x64 Shellcode 

These entries can be run as a shell script or as shell code.

| Size | Author | File Type | Writeup | Note |
|------|------|-----------|---------|------|
| 69 | [jbo](./entries/jbo/jbo.sh.shellcode.txt) 👑 | .sh | [writeup](https://github.com/yo-yo-yo-jbo/bggp5_linux_shellcode) | [git issue](https://github.com/binarygolf/BGGP/issues/85) - no cli args! |

### Windows Batch / PHP

| Size | Author | File Type | Writeup | Note |
|------|--------|-----------|---------|------|
| 63   | [Krishean](./entries/Krishean/Krishean.bat-php.txt) 👑 | .bat / .php | | [git issue](https://github.com/binarygolf/BGGP/issues/63) |

## 0 Byte Files 

0 byte files have historically not been allowed, but that caveat wasn't included in this years challenge page. 0 byte entries are listed here just because the tricks are interesting.

| Size | Author | File Type | Writeup | Note |
|--------|------|-----------|---------|------|
| 0 | [mattpass](https://github.com/binarygolf/BGGP/blob/main/2024/entries/mattpass/mattpass.txt.0.txt) | .txt | [writeup](https://pastebin.com/pAcukVNK) | [git issue](https://github.com/binarygolf/BGGP/issues/65) |
| 0 | [mattpass](https://github.com/binarygolf/BGGP/blob/main/2024/entries/mattpass/mattpass.sh.0.txt) | .sh | [writeup](https://pastebin.com/pAcukVNK) | [git issue](https://github.com/binarygolf/BGGP/issues/75) |
| 0 | [jbo](https://github.com/binarygolf/BGGP/blob/main/2024/entries/jbo/jbo.py.0.txt) | .py | | [git issue](https://github.com/binarygolf/BGGP/issues/122) |
| 0 | [jbo](./entries/jbo/jbo.pl.txt)  | .pl | | Uses environment variable to pass the url and code |
