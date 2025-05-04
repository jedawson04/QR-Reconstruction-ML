# README Documentation for `gen_qr.py` and `gen_set.py` and `gen_set_big.py` 
## (for generating individual QR codes, and groups of QR codes respectively)

## `gen_qr.py` - 
This file generates invididual instances of qr codes using the qrcodegen library.

the generate qr method allow for specification on the message to be encoded, the error correction level (low through high), the type of masking (0-7), and the size to generate and return a QR code object.

the file output method takes in a QR code object, 