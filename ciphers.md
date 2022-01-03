# XOR Cipher
**Definition**: Message encoded with a "key" using XOR logic.

**Example 1**: 
```text
01110011 01101001 01110011 -> message (SIS)
10101010 10101010 10101010 -> key (random binary)
--------
11011001 11000011 11011001 -> encrypted text (gibberish)


--------
11011001 11000011 11011001 -> encrypted text (gibberish)
10101010 10101010 10101010 -> key (random binary)
--------
01110011 01101001 01110011 -> message (SIS)
```

**Example 2**
```text
01000010 01010010 01001111 -> message (BRO)
11011011 11011011 11011011 -> key (random binary)
--------
10011001 10001001 10010100 -> encrypted text (gibberish)

--------
10011001 10001001 10010100 -> encrypted text (gibberish)
11011011 11011011 11011011 -> key (random binary)
--------
01000010 01010010 01001111 -> message (BRO)
```

# Caesar Cipher
**Definition**: Message encoded with each letter that corresponds with a "shifted" alphabet character.

A B C

B C D
```text
SIS -> message
    -> key (Shifted by one as shown above)
--------
TJT -> encrypted text (gibberish)


--------
TJT -> encrypted text (gibberish)
    -> key (Shifted by one as shown above)
--------
SIS -> text
```

**Example 2**
```text
BRO -> message
    -> key (Shifted by one as shown above)
--------
CSC -> encrypted text (gibberish)


--------
CSC -> encrypted text (gibberish)
    -> key (Shifted by one as shown above)
--------
BRO -> text
```