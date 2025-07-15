# BPE (Byte Pair Encoding):

Byte Pair Encoding (BPE) is a simple, effective text tokenization and compression technique.
Originally developed as a data compression algorithm (by Philip Gage in 1994), it was later adapted for subword tokenization in Natural Language Processing (NLP) tasks.

In NLP, BPE helps split words into smaller pieces (“subwords”), allowing a fixed-size vocabulary to handle rare and unknown words more effectively.

uppose the training data is:
low lower newest widest

Initial symbols:
l o w l o w e r n e w e s t w i d e s t

We count frequent pairs:

l o → lo

lo w → low

e s → es

w e → we
