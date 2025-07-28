## Challenge: ROT13  
**Category:** Cryptography  


### Thought Process

The name "ROT13" tells us what kind of cipher it is. ROT13 is a symmetric cipher where each letter is replaced with the letter 13 positions forward in the alphabet. It works only on letters (A–Z, a–z), and non-letter characters (like `{}`, `_`) are left unchanged.

---

### Tools & Techniques Used

- **ROT13 Decoder** (online or code)
- Optional Python code:
```python
import codecs
cipher = "cvpbPGS{abg_gbb_onq_bs_n_ceboyrz}"
print(codecs.decode(cipher, "rot_13"))
```

---

### Solution Steps

1. Input the ciphertext into a ROT13 decoder:
   ```
   cvpbPGS{abg_gbb_onq_bs_n_ceboyrz}
   ```

2. After decoding with ROT13, we get:
   ```
   picoCTF{not_too_bad_of_a_problem}
   ```

---

### Final Flag

```
picoCTF{not_too_bad_of_a_problem}
```


