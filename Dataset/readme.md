This project uses the BoroPOS Tag Corpus, an annotated dataset for the Bodo language stored in
CSV format. Each sentence consists of a sequence of word–POS tag pairs, where every token is
represented in the format word\tag. The corpus is written in the Devanagari script, which is the
official writing system of the Bodo language.
The dataset was preprocessed by extracting each word\tag pair into separate word and POS tag
sequences. Empty or invalid entries were removed, and only valid sentences with matching
numbers of words and POS tags were retained. The processed dataset was then analyzed to obtain
statistics such as the total number of sentences, total number of words, vocabulary size, average
sentence length, number of unique POS tags, and tag frequency distribution.

The dataset was analyzed to understand its characteristics before model training. Basic statistics
such as the number of sentences, vocabulary size, number of POS tags, data split, and preprocessing
operations were examined to ensure the quality of the corpus and prepare it for training.
The corpus contains approximately 6,000 annotated sentences with a vocabulary of 21,202 unique
words. The final dataset consists of 35 unique POS tags, representing different grammatical
categories used in the Bodo language. Since the corpus is manually annotated, no missing POS
labels were observed after preprocessing.
The dataset was divided into training, validation, and testing subsets to facilitate model
development and evaluation. The same data split was used for both the BiLSTM-CRF and
IndicBERT v2 models to ensure a fair comparison of their performance.
