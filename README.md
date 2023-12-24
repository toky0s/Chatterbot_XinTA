A simple chatterbot demo with some features allow integrate to any Web application.

For Vietnamese installation: 
https://docs.google.com/document/d/1-h9evQzBLzFUX3JlT2mradFkAWYy8y9zJM5KylsM2WU/edit?usp=sharing

Installation:
error: Microsoft Visual C++ 14.0 is required. Get it with "Microsoft Visual C++ Build Tools"
Refer to https://www.scivision.dev/python-windows-visual-c-14-required/

1. Download Visual Studio Installer 2019 or 2022, ...
2. Tab Workloads -> Desktop development with C++.
3. In Installation details on your right hand side, select two options:
- MSVC v142 - VS 2019 C++ x64/x86 build tools
- Windows 10 SDK

4. Install Python 3.6 (python-3.6.8rc1-amd64)
5. ```pip install virtualenv```
6. ```virtualenv [your_env_name]```
7. On Windows - CMD, ```[your_env_name]\Scripts\activate.bat```. To deactive, ```[your_env_name]\Scripts\deactivate.bat```
8. ```pip install spacy```
9. ```python -m spacy download en```
10. ```pip install chatterbot```

Edit file: ```your-env\Lib\site-packages\chatterbot\tagging.py```

```python
if self.language.ISO_639_1.lower() == 'en':
    self.nlp = spacy.load('en_core_web_sm')
else:
    self.nlp = spacy.load(self.language.ISO_639_1.lower())
```