
#       NLP Model Grading using BLEU score


BLEU (Bilingual Evaluation Understudy) score is a commonly used metric to assess the quality of text produced by machine translation systems.
This project calculates the BLEU  score for a given candidate sentence against multiple reference sentences.
Instead of relying on external libraries like nltk,etc. for the calculation, the project implements the BLEU score algorithm from scratch, using only Python's standard libraries such as `math` and `collections` for utility functions.




## Approach

The code is a custom implementation of the BLEU score calculation, which considers both the n-gram precision and the length of the candidate sentence relative to the reference sentences.
Here's the approach,


1. **Tokenization:** Split the input text into lowercase tokens using a regular expression to handle words and punctuation.

2. **N-gram Generation:** Create n-grams (sequences of `n` words) from the tokenized text for `n = 1` to `4`.

3. **Brevity Penalty:** Calculate a penalty based on the length of the candidate sentence relative to the reference. If the candidate is shorter, the penalty reduces the BLEU score.

4. **Clipped Precision:** Count n-grams in both candidate and reference sentences. Clip the candidate's n-gram counts to avoid over-crediting repeated n-grams. Calculate precision for each n-gram size and apply equal weighting.

5. **BLEU Score Calculation:** Combine the weighted precision scores and the brevity penalty to compute the final BLEU score.

















