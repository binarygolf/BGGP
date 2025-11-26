## Entry Info

- Date: 2025-11-12
- BGGP Challenge: 6
- Name: dtmsecurity
- Contact Info: https://x.com/dtmsecurity
- Online Presence: https://dtm.uk/
- Writeup Link: https://rap.sh/Python_Pip_Golf


## File Info

- Target File Type: .tgz (gzipped tar archive - pip package)
- Target File Size: 67 bytes
- SHA256 Hash: ddc6197c37e92ad21f144475507af9bb530c56c394d8b4bb05eb5035f466326b

### File Contents

```
H4sIAAAAAAAC//PQL04tKS3QK6hkoBkwgABctIGBIRIbLG5mAqQUDBhGAa1BQVFmXomGmeZoSIxMAAC5YTaHAAQAAA==
```

## Environment Info

### Target Software and Version

- Python: 3.8 or later
- pip: Any version (tested with pip 21.0+)

### Environment Setup

_Description of Target Software's Environment (Platform/OS, Setup Instructions, etc.)_

**Platform:** Linux, macOS, or Windows

**Setup Instructions:**
1. Install Python 3.8 or later
2. Ensure pip is installed (usually comes with Python)
3. Run: `pip install bggp6_minimal_67b.tgz -v`

**Expected Behavior:**
- Prints "6" during installation (visible with `-v` flag)
- Installation will error out (expected behavior for minimal entry)
- Uses old-style pre-POSIX tar format without EOF marker


## Additional Info

**Technical Details:**
- Uses pre-POSIX old-style tar format (no ustar magic bytes)
- Directory name optimized to single character 'H' for best gzip compression
- File permissions set to 000 (compresses better than standard 644)
- No tar EOF marker (saves 7 bytes)
- Payload: `print(6)` (8 bytes)

**Optimizations:**
1. Old-style tar format avoids ustar header overhead
2. Single-char directory 'H' chosen for optimal gzip compression with this specific payload
3. Mode 000 compresses better than any other permission set
4. No EOF marker - tar archives can function without the traditional 1024-byte null trailer

**Test Command:**
```bash
pip install bggp6_minimal_67b.tgz -v
```

**Expected Output:**
The package will print "6" during installation before erroring out due to missing metadata.

## Verification 

- Reviewer: netspooky
- Review Date: 2025-11-26
- SHA256: ddc6197c37e92ad21f144475507af9bb530c56c394d8b4bb05eb5035f466326b
- Score: 4285 (base 4029 + 256 for writeup)
- Note: works as is, tested on ubuntu 24.04 with python3.12

