Tools Used
---
* bi-LSTM + CRF with character embeddings

References
---
[NER Sequence Tagging with Tensorflow](https://guillaumegenthial.github.io/sequence-tagging-with-tensorflow.html)

[Text Clustering with Named Entities](https://www.cs.utexas.edu/~ckcuong/Publications/Text%20Clustering%20with%20Named%20Entities.pdf)

Non-trivial part of the problem
---
not just tagging each word by a class from a current database; instead we may encounter words without any prior knowledge and have to tag them using contextual information, such as `EU`

Steps
---
1. for each word we need to use a dense representation $w \in R^n$
  (1) load pre-trained word embeddings $w_{GloVe} \in R^{d_1}$
  (2) extract some meanings from the characters

2. Contextual Word Representation
  for each word w, get a meaningful representation $h \in R^k$ (LSTM)
  
3. Decode from word vector representation to prediction

Word Representation
---
For each word, we need to obtain a vector $w \in R^n$

1. get word embeddings $w_{glove} \in R_{d_1}$ and concatenate word embeddings

2. obtain vector containing features extracted from character level $w_{\text{chars}} \in R^_{}$ (bi-LSTM can be used here)

each character $c_i$ is associated with a vector $c_i \in R^{d_3}$ 


End Product

1. a blog post with Toronto twitter data

2. a video presentation 

3. a MOOC

4. interviews and conferences
