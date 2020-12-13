---
layout: post
title: Make Romanizer Work for Morphemes
excerpt_separator:  <!--more-->
categories:
  - Python
tags:
  - Python
  - NLP
---

### Summary
- There is a korean_romanizer module.  [link](https://github.com/osori/korean-romanizer)
- However, the korean_romanizer module's `Romanizer()` cannot romanize a morpheme(형태소) that starts with a Jongseong(종성) - ex) ㅂ니다, ㄴ다, ㄹ것이다 등
- The below code allows you to Romanize such morphemes.
<!--more-->
- `romanize_word()` receives a morpheme in Korean and returns its equivalent Roman spelling
- `romanize_()` receives a list of morphemes in Korean and returns a list of equivalent Roman spellings

```python
# !pip install korean_romanizer
from korean_romanizer.romanizer import Romanizer

def romanize_word(x):
    """
    change Korean word to an equivalent Roman spelling
    """
    s = ''
    for c in [char for char in x]:
        try:
            s = s + Romanizer(c).romanize()
        except:
            if c == 'ㄱ':
                s = s + '-g'
            elif c == 'ㄴ':
                s = s + '-n'
            elif c == 'ㄷ':
                s = s + '-d'
            elif c == 'ㄹ':
                s = s + '-l'
            elif c == 'ㅁ':
                s = s + '-m'
            elif c == 'ㅂ':
                s = s + '-b'
            elif c == 'ㅅ':
                s = s + '-s'
            elif c == 'ㅇ':
                s = s + '-ng'
            elif c == 'ㅈ':
                s = s + '-j'
            elif c == 'ㅊ':
                s = s + '-ch'
            elif c == 'ㅋ':
                s = s + '-k'
            elif c == 'ㅌ':
                s = s + '-t'
            elif c == 'ㅍ':
                s = s + '-p'
            elif c == 'ㅎ':
                s = s + '-h'
    return s

def romanize(src):
    """
    change entire sentence
    """
    return [romanize_word(x) for x in src]
```
