Category: Cryptography
Challenge: cryptography(rot_13)
Thought process: The challenge name and prompt both reference ROT13, which is a basic Caesar cipher where each letter is shifted 13 positions forward in the alphabet. Because the alphabet has 26 letters, applying ROT13 twice brings you back to the original message.
This cipher only affects letters (A–Z and a–z), and leaves punctuation or symbols untouched.
Tools and techniques: using python.
      import codecs
      print(codecs.decode("cvpbPGS{abg_gbb_onq_bs_n_ceboyrz}", "rot_13"))
Final flag: 
picoCTF{not_too_bad_of_a_problem}

