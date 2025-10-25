# EX.6 Implementation of Semantic ANalysis
### ENTER YOUR NAME : EASWAR R
### ENTER YOUR REGISTER NO : 212223230053
### DATE: 25/10/2025

## Aim: 
To perform Parts of speech identification and Synonym using Natural Language Processing (NLP) techniques.
## Algorithm:
Step 1: Import the nltk library.

Step 2: Download the 'punkt', 'wordnet', and 'averaged_perceptron_tagger' resources.

Step 3:Accept user input for the text.

Step 4:Tokenize the input text into words using the word_tokenize function.

Step 5:Iterate through each word in the tokenized text.

•	Perform part-of-speech tagging on the tokenized words using nltk.pos_tag.

•	Print each word along with its corresponding part-of-speech tag.

•	For each verb , iterate through its synsets (sets of synonyms) using wordnet.synsets(word).

•	Extract synonyms and antonyms using lemma.name() and lemma.antonyms()[0].name() respectively.

•	Print the unique sets of synonyms and antonyms.
## Program:
```
!pip install nltk
import nltk
#import wordnet
nltk.download( 'punkt_tab' )
nltk.download('wordnet')
from nltk.tokenize import word_tokenize
nltk.download( 'averaged_perceptron_tagger_eng' )
sentence=input ()
# Tokenize the sentence into words
words = word_tokenize(sentence)
# Identify the parts of speech for each word
pos_tags= nltk.pos_tag(words)
# Print the parts of speech
for word, tag in pos_tags:
    print(word, tag)
# Tokenize the sentence into words
words = word_tokenize(sentence)
# Identify the parts of speech for each word
pos_tags= nltk.pos_tag(words)
from nltk.corpus import wordnet

# Identify synonyms and antonyms for each word
synonyms =[]
antonyms =[]
for word in words:
	for syn in wordnet.synsets(word) :
		for lemma in syn.lemmas():
			synonyms . append (lemma . name( ) )
			if lemma . antonyms():
				antonyms . append ( lemma. antonyms ( ) [0] . name ( ) )
# Print the synonyms and antonyms
print ( "Synonyms : " ,set (synonyms) )
print ( "Antonyms : " ,set(antonyms) )
```

## Output
<img width="417" height="38" alt="image" src="https://github.com/user-attachments/assets/933cdd52-75cf-47ad-94de-dbba53815242" />

<img width="198" height="171" alt="image" src="https://github.com/user-attachments/assets/4ba551dd-ce8e-4ffb-b030-30d4f1fd1cdf" />

<img width="1772" height="22" alt="image" src="https://github.com/user-attachments/assets/c3ddba41-9947-449a-bb16-1400d95a1e1d" />

<img width="1612" height="26" alt="image" src="https://github.com/user-attachments/assets/0bee1117-d0e6-4f03-8436-34e451c741ce" />

<img width="358" height="25" alt="image" src="https://github.com/user-attachments/assets/569d69f0-aaaa-46f5-aceb-cbe900c6a734" />

## Result:
Thus ,the program to perform the Parts of Speech identification and Synonymis executed sucessfully.
