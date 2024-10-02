# VCL Temporal Reference Tagger

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![standard-readme compliant](https://img.shields.io/badge/readme%20style-standard-brightgreen.svg?style=flat-square)](https://github.com/RichardLitt/standard-readme)


## Background
This project is designed to classify the temporal reference (past, present, or future) of verbs and verb modifiers in English text. Using the Natural Language Toolkit (NLTK), the script processes input sentences, assigns part-of-speech (POS) tags, and analyzes the context to determine the temporal reference of each verb.

The script performs the following steps:

1) Tokenization: The input sentence is split into words.
2) POS Tagging: Each word is assigned a part-of-speech (POS) tag using NLTK.
3) Temporal Reference Assignment: Based on the POS tags, verbs are analyzed in context to determine their temporal reference (past, present, or future). Non-verbs are categorized as well.

### Temporal Categories

* PAST: Verb refers to a past action (e.g., "took").
* PRESENT: Verb refers to an ongoing or current action (e.g., "is taking").
* FUTURE: Verb refers to a future action (e.g., "will take").
* VERB_AMBIGUOUS: Verb form is ambiguous and can be interpreted in multiple ways.
* NON_VERB: Non-verbal modifiers or other non-verbal parts of the sentence.

### Functions

getTemporalReference(text)
Input:

* text: A string representing a sentence to be classified.

Output:

* tempRef: A list of tuples, where each tuple contains a word and its temporal reference.
* tags: A list of tuples containing the word and its assigned POS tag.

### Limitations
* Temporal reference assignment can be subjective, and the current implementation reflects one possible interpretation.
* This code is not optimized for performance and is written to prioritize readability.

### Requirements

- Python 3.x
- NLTK 3.4.1 or higher

## Install

### Dependencies

* Natural Language Toolkit (NLTK) for tokenization and POS tagging.
* Python standard libraries.
To install NLTK, use the following command:

```bash
pip install nltk
```

## Usage

### Example
```python
import nltk
from your_script_name import getTemporalReference
sentence = "She will be running tomorrow."
tempRef, tags = getTemporalReference(sentence)
print(tempRef)
```

## Contributing
Pull Requests are accepted, please review the [the contributing file](CONTRIBUTING.md)!

## License

[MIT license](../LICENSE)

## Citation

If you publish any work using this code or algorithm, please cite the following:

Ross, L.M., Danforth C.M., Eppstein M.J., Clarfeld, L.A., Durieux, B.N., Gramling, C.J., Hirsch, L., Rizzo, D.M., Gramling, R. (2019). Story Arcs in Serious Illness: Natural Language Processing Features of Palliative Care Conversations. Patient Education and Counseling. (in press)

The code was originally written by undergrad interns Lindsay Ross and Laurence Clarfeld (https://orcid.org/0000-0002-3927-9411) helped with code review, generalization, and prepare it for release.
