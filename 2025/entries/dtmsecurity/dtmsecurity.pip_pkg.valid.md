## Entry Info

- Date: 2025-11-12
- BGGP Challenge: 6
- Name: dtmsecurity
- Contact Info: https://x.com/dtmsecurity
- Online Presence: https://dtm.uk/
- Writeup Link: https://rap.sh/Python_Pip_Golf


## File Info

- Target File Type: .tgz (gzipped tar archive - pip package)
- Target File Size: 127 bytes
- SHA256 Hash: 2464b6c487b994afc28b5e712004e433140c572fd21499c111c4aa72b9724258

### File Contents

```
H4sIAAAAAAAC/+3SsQ5AMBDG8T5KRzXQBYOnMZBI0KY9g7cntViMROL/W77Ld8MtV5Wxl9UXflOPsae7tLa6zKlv6iO0VS9Yo3ThOKn+aQhu1ukFxLkp6nH2Lkje+jAuktWmTbvMKAAAAAAAAAAAAAAAAADAp+yZEA7KACgAAA==
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
3. Run: `pip install bggp6_best_127b.tgz -v`

**Expected Behavior:**
- Prints "6" three times during installation
- Successfully installs as a Python package named "UNKNOWN"
- Package can be uninstalled with: `pip uninstall UNKNOWN -y`


## Additional Info

This is the **BEST WORKING** entry - a fully functional pip package at only 127 bytes.

**Technical Details:**
- Uses POSIX ustar tar format for full pip compatibility
- Directory name '5' chosen for optimal gzip compression
- File permissions set to 000 (pip overwrites them anyway)
- Payload: `from setuptools import*;print(6);setup()` (42 bytes)

**Optimizations:**
1. Star import (`import*`) saves 1 byte vs `import *`
2. Single-char directory '5' provides best compression with this payload
3. Mode 000 compresses better than standard permissions
4. Minimal setup() call with no arguments (creates installable package)
5. All timestamps and ownership info set to 0/empty for better compression

**Why This Works:**
The setup.py file is executed during pip installation. The star import from setuptools provides the `setup()` function, `print(6)` outputs our target, and `setup()` with no arguments creates a valid (though minimal) package that pip accepts.

**Test Commands:**
```bash
# Install and observe "6" printed three times
pip install bggp6_best_127b.tgz -v

# Verify installation
pip list | grep UNKNOWN

# Cleanup
pip uninstall UNKNOWN -y
```

**Expected Output:**
```
Processing ./bggp6_best_127b.tgz
6
  Preparing metadata (setup.py) ... 6
done
Building wheels for collected packages: UNKNOWN
  Building wheel for UNKNOWN (setup.py) ... 6
done
Successfully installed UNKNOWN-0.0.0
```

## Verification 

- Reviewer: netspooky
- Review Date: 2025-11-26
- SHA256: 2464b6c487b994afc28b5e712004e433140c572fd21499c111c4aa72b9724258
- Score: 4225 (base 3969 + 256 for writeup)
- Note: works as is, tested on ubuntu 24.04 with python3.12

