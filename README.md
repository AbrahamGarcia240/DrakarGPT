# DrakarGPT

Implementation of a decoder-only model based on "Attention is all you need" to create Game of Thrones text'

This implementation follows uses an extract of Game of Thrones, creates a vocabulary based on only the lowercased characters of the document

It has around 10 M parameters, it uses a batch size of 64 and a block size of 256 (i.e the number of characters the model sees in order to produce the next one)

It has 6 layers (each layer is a block containing multihead attention, linear layers and batch norm) serially. Each layer has 6 attention heads

The embedding size used is 384 and each head of the multihead attention layer uses an internal size of 384 / 6

It takes around 50 mins to train in a T4 GPU from Google Colab
