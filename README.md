A simple chatterbot demo with some features allow integrate to any Web application.

For Vietnamese installation: 
https://docs.google.com/document/d/1-h9evQzBLzFUX3JlT2mradFkAWYy8y9zJM5KylsM2WU/edit?usp=sharing

Edit file: your-env\Lib\site-packages\chatterbot\tagging.py

```python
if self.language.ISO_639_1.lower() == 'en':
    self.nlp = spacy.load('en_core_web_sm')
else:
    self.nlp = spacy.load(self.language.ISO_639_1.lower())
```