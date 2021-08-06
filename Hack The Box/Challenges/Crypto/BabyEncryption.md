Flag is encrypted by shifting, we must find inverse of 123 and 256

Python code
```python
from Crypto.Util.number import inverse
def decryption(msg):
    pt = []
    inv = inverse(123, 256)
    for c in msg:
        pt.append(inv * (c - 18) % 256)
        print(pt[len(pt)-1])
    return bytes(pt)

with open('msg.enc') as f:
    ct = bytes.fromhex(f.read())
print(decryption(ct))
```
**Flag: HTB{l00k_47_y0u_r3v3rs1ng_3qu4710n5_c0ngr475}**
