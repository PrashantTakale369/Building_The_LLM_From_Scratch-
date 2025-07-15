# Building_The_LLM_From_Scratch-

## we are starting the Build an LLM ( Transform Model ) From the Scratche. 

Special thanks to *Sebastian Raschka*, author of Build a Large Language Model from Scratch, for providing a clear, hands-on guide to demystify the process of building LLMs step by step.
also the book is Natural Language Processing with Transformers by Lewis Tunstall, Leandro von Werra, Thomas Wolf (from Hugging Face) (O’Reilly, 2022)

# 1. Byte Pair Encoding ( Tokenization).
==> This section covers a more sophisticated tokenization scheme based on a concept called byte pair encoding (BPE). The BPE tokenizer covered in this section was used to train LLMs such as GPT-2, GPT-3, and the original model used in ChatGPT.

# 2. Data Loader and Input Output Pair.
==> A DataLoader is a utility that loads your dataset into memory in manageable batches, shuffles if needed, and feeds it into your model during training or inference.It is very commonly seen in     PyTorch and other frameworks

| Component              | Purpose                                      |
| ---------------------- | -------------------------------------------- |
| **DataLoader**         | Loads data in batches efficiently            |
| **Input–Output Pairs** | Teach model how to predict the next token    |
| **Why needed?**        | Efficient training of LLMs on large datasets |


# 3. Token Embedding.
==> But neural networks don’t understand text — they work with numbers.So we need to convert each token (word, subword, character) into a vector of numbers. This vector is called a token embedding.like 
Token: "cat"
Embedding: [0.21, -0.14, 0.88,…] (a vector of size, say, 768

# Positional Encoding.
==> A positional embedding is a vector that represents the position of a token in the sequence.We add (or concatenate) this vector to the token embedding.
In a transformer-based LLM, the self-attention mechanism looks at all tokens at once — it has no inherent sense of order.
But in language, word order matters!
So, we add positional information to each token’s embedding, so the model knows where each token is in the sequence.
