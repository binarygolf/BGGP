## Entry Info

- Date: 2025-11-12
- BGGP Challenge: 6
- Name: dtmsecurity
- Contact Info: https://x.com/dtmsecurity
- Online Presence: https://dtm.uk/
- Writeup Link: https://rap.sh/Python_Pip_Golf


## File Info

- Target File Type: .tgz (gzipped tar archive - pip package)
- Target File Size: 150 bytes
- SHA256 Hash: 81fca99e90c6f3a3798e938bf8cddce7a88fbe3abcb039269821ed380d91a787

### File Contents

```
H4sIAAAAAAAC/6vSL04tKS3QK6hkoBkwgABctIGBuTGCDRY3MwEKKRgwjAJag7Si/FwFcBIoyc/PKVbIzC3ILyrRsgYLaRRUxufmp5TmpBbbRqsXZ5akJpcWl+TnZlalqsdqjgbeMABV+ijRSpNygGD+NzRAzf+GBkbGhqP5nx6goCgzr0TDbDQzj1AAAJMYh/oACAAA
```

## Environment Info

### Target Software and Version

- Python: 3.8 or later
- pip: Any version (tested with pip 21.0+)
- setuptools: Any version (dependency of pip)

### Environment Setup

_Description of Target Software's Environment (Platform/OS, Setup Instructions, etc.)_

**Platform:** Linux, macOS, or Windows

**Setup Instructions:**
1. Install Python 3.8 or later
2. Ensure pip is installed (usually comes with Python)
3. Run: `pip install bggp6_persistent_150b.tgz`
4. After installation, run any Python command to see "6" printed

**Expected Behavior:**
- Successfully installs a package named "sitecustomize"
- After installation, **every Python invocation** will print "6" before executing
- Effect persists until the package is uninstalled

**Warning:** This package modifies Python's site-wide startup behavior. Uninstall with:
```bash
pip uninstall sitecustomize -y
```


## Additional Info

This is the **PERSISTENT** entry - prints "6" on EVERY Python startup after installation.

**Technical Details:**
- Uses old-style pre-POSIX tar format (no ustar magic)
- Contains TWO files: `setup.py` and `sitecustomize.py`
- Directory name 'z' chosen for optimal gzip compression with 2-file archive
- File permissions set to 000
- No tar EOF marker

**Files in archive:**
1. `z/setup.py` (60 bytes): `from setuptools import*;setup(py_modules=['sitecustomize'])`
2. `z/sitecustomize.py` (9 bytes): `print(6)`

**How It Works:**
Python automatically imports `sitecustomize.py` on startup if it's installed in the site-packages directory. By installing this module via pip, we ensure that every Python invocation (scripts, interactive sessions, etc.) will execute our code first.

**Optimizations:**
1. Old-style tar format avoids ustar header overhead
2. Star import (`import*`) saves 1 byte
3. Single-char directory 'z' provides best compression for this 2-file payload
4. Mode 000 on both files
5. No EOF marker in tar archive
6. Minimal sitecustomize implementation

**Test Commands:**
```bash
# Install the package
pip install bggp6_persistent_150b.tgz

# Test 1: Run any Python command
python3 -c 'pass'
# Output: 6

# Test 2: Run a Python script
python3 -c 'print("hello")'
# Output:
# 6
# hello

# Test 3: Interactive Python
python3
# Output: 6
# Python 3.x.x ...
# >>>

# Cleanup when done
pip uninstall sitecustomize -y
```

**Expected Output Example:**
```bash
$ python3 -c "pass"
6
```

## Verification 

- Reviewer: netspooky
- Review Date: 2026-04-06
- SHA256: 81fca99e90c6f3a3798e938bf8cddce7a88fbe3abcb039269821ed380d91a787
- Score: 4202 [ Base: 3946 (4096 - 150) +256 (Writeup) ]
- Note: works as is, tested with provided docker oneliner

```
$ docker run --rm -v $(pwd):/app/ python:3.12-slim bash -c "
  pip install /app/pkg.tgz -q
  python3 -c pass"

6

$ sha256sum pkg.tgz 
81fca99e90c6f3a3798e938bf8cddce7a88fbe3abcb039269821ed380d91a787  pkg.tgz
```
