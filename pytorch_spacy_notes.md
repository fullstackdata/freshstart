# Pytorch
Don't index a Pandas dataframe class inside a DataSet class, it is a slow operation.
Convert dataframe to a numpy array instead to make it fast.



# Spacy
Ines Montani's wonderful tutorial - https://www.youtube.com/watch?v=THduWAnG97k

- nlp.vocab stores data shared across multiple documents
- strings -> hashes
- Hashes are irreversible, that's why the shared vocab is passed around.
- Lookup table in <b>BOTH DIRECTIONS</b>
- nlp.vocab, doc.vocab
- Lexemes are <b>context independent</b>.


- ![Lexemes are context independent](https://user-images.githubusercontent.com/3958917/137585620-9e6cd310-ad20-479f-af5f-e7669588774b.png)
- doc.ents are writable.
- doc and span objects are optimized, <b>convert them to strings as late as possible.</b>
- Don't forget to pass around the shared vocab.
- ??PhraseMatcher
  - REVISIT

### Pipeline
- Tagger, Parser, NER - is this order needed?
- Text categories are always very specific, so they are not included in any pretrained models by default.
- nlp.add_pipe
- Tokenizer is detached from other components, adding a component as the <b>first</b> makes it available right after the tokenizer.
- Custom attributes <code>._</code> property.
- Need to be registered on the global Doc, Span and Token classes.
- Using <code>set_extension</code>, defaults can also be set using <code>default</code> attribute.

### Scaling & performance
- nlp.pipe is different from Pipeline
- ![Screenshot from 2021-10-16 08-58-25](https://user-images.githubusercontent.com/3958917/137588447-7c9b4c13-b424-4e25-a9ee-f799fe2655a7.png)

