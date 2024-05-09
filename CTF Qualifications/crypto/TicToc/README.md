
# Solution
The file delivered contained a sequence of `Tic` and `Toc`.

```
Toc Tic Tic Toc Toc Toc Tic Tic Toc Toc Toc Tic Toc Toc Tic Tic Toc Toc Tic Tic Toc Toc Tic Tic Toc Toc Toc Tic Tic Toc Tic Tic Toc Toc Toc Tic Tic Tic Tic Tic Toc Tic Toc Tic Tic Tic Tic Tic Toc Tic Tic Tic Toc Toc Toc Tic Toc Tic Toc Tic Tic Toc Toc Tic Toc Toc Toc Toc Tic Toc Toc Tic Toc Tic Tic Tic Toc Toc Toc Tic Toc Toc Toc Tic Toc Toc Tic Tic Toc Toc Toc Toc Tic Toc Tic Tic Tic Toc Toc Tic Tic Toc Toc Tic Toc Tic Toc Toc Toc Toc Toc Tic Toc Toc Toc Tic Toc Toc Tic Tic Toc Tic Tic Tic Toc Toc Tic Tic Toc Tic Toc Toc Toc Toc Toc Tic Toc Tic Tic Tic Toc Toc Toc Tic Tic Toc Toc Tic Tic Tic Toc Tic Toc Toc Toc Tic Tic Tic Tic Tic Toc Toc Toc Toc Tic Tic Tic Tic Tic Toc Toc Tic Tic Tic Toc Tic Toc Toc Tic Tic Tic Tic Toc Tic Toc Toc Toc Tic Toc Tic Tic Tic Toc Tic Toc Toc Toc Toc Toc Tic Toc Tic Tic Tic Toc Toc Toc Tic Tic Toc Toc Tic Tic Tic Toc Tic Toc Tic Toc Tic Tic Tic Tic Tic Toc Tic Tic Tic Toc Toc Toc Tic Tic Toc Toc Tic Tic Tic Tic Tic Toc Toc Toc Tic Tic Tic Tic Tic Toc Toc Toc Toc Toc Tic Toc
```

Now this looks like some binary code. If we replace Tic with `0` and Toc with `1` we get 

```
100111001110110011001100111001001110000010100000100011101010011011110110100011101110110011110100011001101011111011101100100011001011111010001110011000101110000011110000011000101100001011101000101111101000111001100010101000001000111001100000111000001111101

```

```python
bits = "100111001110110011001100111001001110000010100000100011101010011011110110100011101110110011110100011001101011111011101100100011001011111010001110011000101110000011110000011000101100001011101000101111101000111001100010101000001000111001100000111000001111101"
text = int(bits, 2)
text.to_bytes((text.bit_length()+7)//8, 'big').decode()
```

This gives us a word which looks like some substitution cipher ([`rot13`](https://en.wikipedia.org/wiki/ROT13) for instance). And indeed, rot13 gives us the flag.

```bash
$ echo "NvfrpPGS{Gvz3_vF_G1px1at_G1PG0p}" | rot13
AisecCTF{Tim3_iS_T1ck1ng_T1CT0c}
```
