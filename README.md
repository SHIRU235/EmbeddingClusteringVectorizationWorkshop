# EmbeddingClusteringVectorizationWorkshop

# Similarity Using Word Embeddings:
This assignment explores semantic representation of words using Word2Vec and GloVe embedding models. The focus is on applying these models over a domain-specific knowledge corpus to support tasks such as similarity search, analogical reasoning, and query matching.

# Dataset Description
This project uses a custom mini-corpus of urban AI-related sentences, manually defined to simulate a real-world, topic-specific NLP scenario.

Corpus:

1. Artificial intelligence is transforming street design.
2. Sidewalks and bike lanes are essential for inclusive mobility.
3. Smart cities leverage data to improve pedestrian safety.
4. Computer vision models detect street signs and traffic signals.
5. Urban planning needs insights from machine learning.
These sentences are used to train a custom Word2Vec model and are evaluated semantically using pretrained GloVe embeddings.

# Objective:
The goal is to analyze the strengths and trade-offs of Word2Vec and GloVe when applied to a small custom corpus. This involves:

Preprocessing text documents into tokens.

Training Word2Vec on the local context of words.

Loading GloVe embeddings based on global co-occurrence.

Comparing their effectiveness in representing semantic relationships.

# Steps Performed:
Data Collection and Preprocessing

Raw text documents were collected to form a knowledge corpus.

Tokenization was performed using nltk.word_tokenize, with punctuation and special characters cleaned using regular expressions.

Stopwords were optionally removed to focus on meaningful tokens.

Training Word2Vec

Used the gensim library to train a Word2Vec model with either Skip-Gram or CBOW.

Word embeddings were generated based on local context windows (e.g., 5 words).

Captured relationships such as usage-based similarity (e.g., buy ~ purchase).

Loading GloVe Embeddings

Pretrained GloVe vectors (50d, 100d) were downloaded using gensim.downloader.

These vectors encode global co-occurrence statistics across documents.

GloVe proved effective in analogy tasks like king - man + woman ≈ queen.

# Evaluation:

Compared word similarities and nearest neighbors using cosine distance.

Evaluated both embeddings for their ability to capture semantic meaning within the custom corpus.

Key Observations:
Word2Vec is a predictive model trained on word context windows. It performs well in capturing syntactic and usage-based similarity.

GloVe is a count-based model that encodes global co-occurrence patterns and often captures broader semantics, especially effective on small corpora.

GloVe is easier to use with pretrained vectors, while Word2Vec is better suited for fine-tuning on custom data.

For small domain-specific corpora, GloVe may generalize better due to its reliance on global co-occurrence, whereas Word2Vec requires more data for robust embeddings.

##  Team Members

## Team 9

Name – Shiranth Stephen Sahaya Anbu Anitha,  Student ID: 8961999
Name - Bhupender Sejwal, Student ID: 9044574

# Conclusion:
Both Word2Vec and GloVe are powerful tools for semantic representation. This assignment demonstrated their strengths and weaknesses when applied to a domain-specific dataset, providing practical insights into their use in real-world NLP tasks.