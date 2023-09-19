```markdown
# Poly Playfair Cipher

Poly Playfair Cipher(Polyalphabetic Playfair cipher) is a Python library that provides tools for encrypting and decrypting text using the Playfair Cipher with a customizable key matrix.

## Installation

You can install Poly Playfair Cipher using pip:

```bash
pip install poly-playfair-cipher
```

## Example
```python
from PlayfairCipher import PlayfairCipher
# Define a PlainText for the Playfair Cipher
pt="Fluffy"
# Define a key for the Playfair Cipher
key="keyword"
# Generate KeyMatrix 
def genM(m):
  for i in range(5):
    for j in range(5):
      print(m[i][j],end= " ")
    print()
# Creating a KeyMatrix :
km=PlayfairCipher.matrix(key)
# splitting plaintext into a pairs of two letters ie.(digraphs)
p=PlayfairCipher.pairs(pt)
# printing keymatrix :
print("key matrix :")
genM(km)
### Encrypting Text
ct=PlayfairCipher.encryption(p,km)
print("Cipher Txt :",ct)
### Decrypting Text
pct=PlayfairCipher.decryption(ct,km)
print("Plain Txt :",pct)

```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
```
