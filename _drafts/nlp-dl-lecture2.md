## Lecture 2: Word Vector Representations
==========================================
Word vectors represent meaning

Traditional way:
* Look at WordNet which is a dataset in ntlk, it's a taxonomy of words
* Contains hypernyms (is-a) relations and synonym sets
* Sort of like a dataset based on the webster's dictionary

Issues:
* misses nuances
* misses new words being added very quickly
* hard to compute word similarity

Statistical NLP considers words as atomic symbols
hotel: [0 0 0 0 0 0 1 0 0 0 0 ]
long vectors
this is called one-hot representation
No inherent relationsip between words

"dell notebook battery size" should match "dell laptop battery capacity"
one hot vector dot products are 0 so no natural similarity between them

Solutions:
Distributional Similarity based representations: semantics of word obtained by the context they appear in
"You shall know a word by the company it keeps"

Dot product between dense vectors for words will show similarity and context so they can be predicted together

### Word2Vec
-------------
Define a model to predict between center word and surrounding context words
p(context | W(t))
loss function: J = 1 - p( W(-t) | W(t))

Two Algos:
1. Skip gram
2. CBOW (continuous bag of words)

Training algos:
1. Hierarchical softmax
2. Negative sampling

### Skip Gram Model
--------------------
radius of window size 'm'
center word at t
p(w t-2 | wt), p(w t+2 | wt)
