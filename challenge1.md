# Challenge Name: ROT13 Challenge

**Category:** Cryptography   
## My Thought Process:

Since the challenge specifically mentions ROT13, I immediately recognized that it was using the **ROT13 cipher**. This is commonly used in beginner CTFs to introduce basic cryptography.

ROT13 replaces each letter with the one 13 letters after it. It is symmetric — applying ROT13 again brings you back to the original.

## Tools/Techniques Used:
I used a simple Python script to decode the ROT13 cipher:

```python
import codecs

cipher = "cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_GYpXOHqX}"
decoded = codecs.decode(cipher, 'rot_13')
print(decoded)
```
## Final flag:

Running the above Python script gave me the flag:
```
picoCTF{next_time_I'll_try_2_rounds_of_rot13_TLcKBUdK}
```
