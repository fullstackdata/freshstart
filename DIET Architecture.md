# Universal Sentence Encoder
Instead of individual token or word embeddings and averaging all the tokens in a sentence for similarity or any other downstream general task, USE provide embeddings
for the entire sentence.

In USE, we send a sequence of tokens through the layers and do pooling so as to get an uniform shape irrespective of the sentence length.
If you want something to be general, you want more tasks than training on just one specific task.

Might still be a little overkill.
