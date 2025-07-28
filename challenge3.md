# Challenge: Disk Image Forensics
**Category:** Forensics  


##  Thought Process

We are given a compressed disk image file (`.dd.gz`). These are raw dumps of disk partitions and may contain file system structures, deleted files, or embedded strings.

---

## Tools Used

- `gzip` (to decompress `.gz`)
- Python `re` module to extract readable strings
- `strings` command (optional CLI alternative)


---

## Steps to Solve

1. **Decompress the image**:
   ```bash
   gzip -d disko-1.dd.gz
   ```

2. **Search for flag patterns**:
    used Python to extract all printable strings longer than 10 characters and filter any containing `picoCTF{`.

   ```python
   import re
   with open("disko-1.dd", "rb") as f:
       content = f.read()
   strings = re.findall(rb'[ -~]{10,}', content)
   flags = [s.decode() for s in strings if b'picoCTF{' in s]
   ```

---

## Final Flag

```
picoCTF{1t5_ju5t_4_5tr1n9_e3408eef}
```

This flag was found embedded directly in the disk image as plaintext.

---
