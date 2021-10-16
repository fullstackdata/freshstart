# Pytorch
Don't index a Pandas dataframe class inside a DataSet class, it is a slow operation.
Convert dataframe to a numpy array instead to make it fast.



# Spacy
- nlp.vocab stores data shared across multiple documents
- strings -> hashes
- Hashes are irreversible, that's why the shared vocab is passed around.
- Lookup table in <b>BOTH DIRECTIONS</b>
- nlp.vocab, doc.vocab
- 
