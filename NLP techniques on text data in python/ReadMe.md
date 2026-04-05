# Experiment - 15 - NLP Techniques on Text Data in Python

Natural Language Processing (NLP) is a field of artificial intelligence that enables computers to understand, interpret, and generate human language in a way that is both meaningful and contextually relevant. 

### Aim:
To implement NLP texts on Text data in Python

### Tools Used:
Google Colab or Jupyter Notebook

### Theory:

### Natural Language Processing:

Natural Language Processing (NLP) is a branch of Artificial Intelligence that allows computers to understand, interpret, and generate human language. It serves as a bridge between human communication and machine data processing.
A list is a built-in data type in Python that can store multiple data types inside one variable. It is considered a dynamic placeholder for various data types in a specific order. 

**Types of Natural Language Processing:**

1. Natural Language Understanding (NLU):

   * It is the process of determining the meaning or the intended meaning of any human typed text
     
   * It mainly focuses on the machine reading comprehension
     
   * It is similar to encoding of a text in order for the machine to understand
  
2. Natural Language Genaration:

   * The process where the machine converts the structured data into human readable format.
     
   * It is similar to the decosing of machine text to normal text in order for our understanding

### NLTK Library:

* NLTK defined as the Natural Language Tool Kit which is the most popular open source library which is designed for working with human language.
  
* It provides a suite of text-processing libraries for classification, tokenization, stemming, tagging, and parsing

**Functions used in NLTK for Natural Language Processing:**

1. punkt:

   * This is a pre - trained model for Tokenization.
     
   * It contains the logic to breakdown paragraphs to sentences and sentences to words
     
   * It is good at understanding that the period '.' is not a delimitor always
  
2. stopwords:

   * It contains lists of "stop words" for various languages (English, French, German, etc.).
     
   * These are words like "the", "is", "at", "which", and "on"
     
   * These words are usually filtered out during text processing because they don't carry significant meaning for analysis.
  
3. punkt_tab:

   * This is a data dependancy for punkt function
     
   * It provides more details and parameters for the better boundary detection of sentences
     
   * This is used in modern versions of NLTK
  
4. wordnet:

   * This is a large lexical database of the English language.
     
   * It groups the english words into sets of synonyms called the **synsets** and provides short definitions
     
   * It can also identify if two words are related or not.
     
   * **Example: ** Words like car and automobile are related
     
   * It is used for **Lemmatization** to find the dictionary root of a word

#### Key Teachniques of NLP:

**(i)Tokenization:**

* It is the process of breaking down sentences into individual words or "tokens".
  
* The same process can be done to retreive sentences from a paragraph
  
* When it is done for words it is called as **Word Tokenization** and for sentence it is called as **Sentence Tokenization**

**(ii) Stop Word Removal:**

* High-frequency words like "is," "the," "a," and "in" often carry very little unique information for machine learning models.

* The words are identified from the stopwords corpus which is imported from the NLTK library

**(iii) Stemming and Lemmatization:**

* Stemming removes either the suffices or prefixes of the words.
* This removes only the words which even after removal the root word can be understood

* Lemmatization converts the words from normal to dictionary root words
* **Example:** was becomes be

**(iv) Part of Speech (POS) Tagging:**

* This process identifies the grammatical category of each word in a sentence, such as whether it is a noun, verb, adjective, or adverb.

* It returns a list of tuples enclosing words with their category

**(v) Word Frequency Distribution:**

* This technique counts how often each word appears in a text.

* It is done by importing the **FreqDist** library from the NLTK library and the probaility module inside it

### Learning Outcomes:

* Stemming and Lemmatization is used to convert words into their true or root form
  
* NLTK library has many modules such as **probability**, **corpus**, **stem** to perform NLP techniques
  
* Stopwords has a set of words from all the language which is used as a reference to remove it from the sentences

### Applications:

* **Healthcare and Medicine:** ASR (Automatic Speech Recognition) allows doctors to dictate clinical notes during patient interactions

* **Finance and Trading:** Real-time analysis of transaction descriptions and communication patterns helps banks identify anomalies

* **Digital Content and Communication:** Social media platforms use NLP to instantly detect and filter hate speech, spam, or offensive content before it is even visible to other users.

### Advantages of NLP

* **Efficiency and Scalability:** NLP can process millions of data in a second which humans can't do. This allows organization to identify trends and extract information easily which cannot be done manually

* **Improved Customer Experience:** NLP powers Chatbots and AI assistants which provides 24/7 support

* NLP is used in google translate which is used in **Breaking the Language Barriers**

* **Accessibility:** Speech-to-text and text-to-speech capabilities allow individuals with visual or hearing impairments to interact more easily with technology and consume digital content.


### Conclusion:

Thus, NLP techniques have been performed on textual data in Python where methods such as stemming, lemmatization, word frequency were used and the output is verified




