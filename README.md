# Processed data

These are processed data sets for feeding into my seq2seq model each is based on a different subset of ~2.5 lines of twitter feed data with different preprocessing NLP filters applied. 

The preprocessing pipeline is:

  - Strip non-alphanumeric characters (except question mark and periods)
  - Lower case
  - Stem using Porter stemmer
  - Count word frequencies and sequence lengths
  - Confine all sequences, *x*, to be between *seq<sub>min</sub><x<seq<sub>max</sub>*
  - Remove all sequences containing rare tokens that occur less then *n<sub>min</sub>*
  - Assign <UNK> token to all rare tokens occuring *n<sub>min</sub>< word < n_<sub>threshold</sub>*, where n_<sub>threshold</sub> is determined heuristically.
