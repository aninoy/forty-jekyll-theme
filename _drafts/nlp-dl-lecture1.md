## Lecture 1: Introduction
===========================
### What is NLP?
	intersection of ai, computer science and linguistics
	understand natural language to perform useful tasks, for e.g personal voice assistant
	fully understand and represent the meaning of language

### Applications:
	- search, text/speech
	- ad matching
	- automated machine translation
	- chatbots
	- speech recognition

Lanugage is a discrete signal system using symbols, which is communicated on continuou substrate

DL is subfield of ML
Traditional ML works using human designed representations and input features. For e.g. for NER, we use these features:
	- cur word
	- prev word
	- next word
	- POS tag
	- surrounding POS tags
	- etc
Machine is only a way to optimize weights on features to make predictions
DL is Representation learning
machine invents features and from the raw inputs and learn an optimized representation of the data

DL is getting better at amazing speed, month after month
huge industry excited in the last 5 years
most techniques were invented in the 80s and 90s
The difference today is huge compute power and vast amounts of data, and gpu marriage with dl

First breakthroughs were in speech recognition (studetns on Geoff Hinton)
	- 32% decrease in Word Error Rate
Second in Coputer Vision imagenet competition
	- students of geoff hinton
	- image classification
	- 37% error reduction

### Why is NLP difficult?
	- News headline: The pope's baby steps on gays (its idiomatic, grammar structure)
	- scientists study whales from space

DL provides the same toolbox for solving many many problems, in vision, language, signal analysis, knowledge representation

Starts off with word meaning, represented as a vector, 300 dimensional vector, 1000 dims for state of the art
multi dimensional vector space serves as a great space for semantic understanding
all countries cluster together
all verbs (say, think)
2d projection is done via dim reduction like pca

### DL for NLP applications
	1. Morpohology:
	use small word representations to form bigger word vectors, like un-fortunate-ly
	first combine: un-fortunate
	then combine: unfortunate-ly
	arrive at final vector for unfortuntely
