# EncPNG

A steganographic library to encrypt files and text in PNG images using CSPRNG random generated pixel colors, shuffled charset for pybase64, and AES-256 with tag (anti-tamper support, and with Intel-NI support on Intel processors) to encrypt or decrypt data (full UTF-8 support).

Available for Linux, MacOS, Raspberry Pi, Windows.

<br>If you get memory error from Python, increase Windows paging or Linux swap.<br>

## INSTALLATION
```
pip3 install encpng
```

## USING LIBRARY ENCPNG

```python
from encpng import EncPNG
enc = EncPNG("Ko n ni chi ka!", "Password ][!")
# Image passed as bytes
img = enc.encrypt()
result = enc.decrypt(img)
```

```python
from encpng import EncPNG
enc = EncPNG("Ko n ni chi ka!", "Password ][!", "/path/to/out")
enc.encrypt()
enc.decrypt("08a30930-ecdf-4f6a-9978-c274093d63e1.png", "Password ][!", "/path/to/file")
```
