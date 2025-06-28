# **Tokens (Unigrams)**
* The smallest meaningful units you split text into
* Example: ["The", "quick", "brown", "fox", "jumps", "over", "the", "lazy", "dog", "."]

# **N-Grams**
* An n-gram is a sequence of n consecutive tokens.

``Unigram (n=1): Single tokens:``
* Example: ["The"], ["quick"], ["brown"], …

``Bigram (n=2): Pairs of adjacent tokens``
* Example: ["The quick"], ["quick brown"], ["brown fox"], …

  
``Trigram (n=3): Triplets of adjacent tokens``
* Example: ["The quick brown"], ["quick brown fox"], …

**Why use them?**
* Unigrams capture individual words.
* Bigrams/trigrams capture short phrases and local context (e.g., “brown fox” vs. “fox jumps”).
* Example: ["The", "quick", "brown", "fox", "jumps", "over", "the", "lazy", "dog", "."]


# **Bag-of-Words (BoW)**
*  A representation that counts how many times each unique token (or n-gram) appears in a document, ignoring order.

![image](https://github.com/user-attachments/assets/32d62f84-1e2f-4188-bdbb-7bb1f839deae)
![image](https://github.com/user-attachments/assets/656d45bd-0099-4942-865a-4a50c80edc7f)


# **Term Frequency (TF)**
* Convert raw counts to normalized frequency (divide by total words in that document).
![image](https://github.com/user-attachments/assets/88983305-1bd6-48bb-8366-f93d18e9d69a)

# **Inverse Document Frequency (IDF)**
* Measure how “rare” each word is across all documents.
![image](https://github.com/user-attachments/assets/f5e9295f-0100-41b9-8116-8081d842c0ca)

# **TF-IDF**
* Multiply TF by IDF
* TF Alone: Too Local. Limitation: Common words in that document (e.g. “the”, “and”, or document-specific words) get high TF, even if they aren’t meaningful across the corpus.
* IDF Alone: Too Global. Limitation: Rare words get high IDF even if they appear only once (perhaps by mistake), and very common words get low IDF—even if they’re important in a particular document.
* TF × IDF: The Sweet Spot.

![image](https://github.com/user-attachments/assets/8765b4bb-0493-4a53-89ac-d7bef1d3ac3e)
