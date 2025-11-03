# English-Amharic-parallel-corpus
This repository provides a high-quality English–Amharic parallel corpus developed using a systematic combination of web crawling, document collection, data cleaning, and sentence-level alignment techniques. The corpus is intended to support research in machine translation, cross-lingual NLP, and under-resourced language technologies.


## Corpus Description
To construct this dataset, we employed both automated crawling tools and manual collection methods:
  * **HTTrack** and **Heritrix** were used to crawl and archive a diverse range of websites, including news portals, blogs, and public information resources.
  * A substantial number of legal and administrative documents were gathered from various online repositories to enrich the linguistic and domain coverage.
  * From the collected raw text, we performed:
      - Content extraction
      - Text normalization and cleaning
      - Sentence segmentation
      - Parallel sentence alignment
The final aligned texts are stored as UTF-8 encoded files, one for English and one for Amharic.

## Dataset Statistics

| Language | Number of Sentences | Encoding |
| -------- | ------------------: | -------- |
| English  |             225,304 | UTF-8    |
| Amharic  |             225,304 | UTF-8    |


Both files are aligned at the sentence level, ensuring that each line in the English file corresponds directly to the same line in the Amharic file.

## Repository Structure
├── data/
│   ├── amharic.txt        # UTF-8 encoded Amharic sentences
│   ├── english.txt        # UTF-8 encoded English sentences
│   └── README.md
├── scripts/
│   └── alignment_tools/   # Optional scripts for processing and alignment
└── LICENSE

## Usage
You may load and use the corpus directly in tools or frameworks such as:

with open("data/english.txt", "r", encoding="utf-8") as en, \
     open("data/amharic.txt", "r", encoding="utf-8") as am:
    english_sentences = en.readlines()
    amharic_sentences = am.readlines()

Suitable applications include:
  * Training machine translation (MT) models
  * Cross-lingual representation learning
  * Data augmentation for under-resourced language tasks
  * Evaluation of alignment and sentence-level similarity models

## Citation
  If you use this corpus in your research, please cite the following work:

** BibTex**

```bibtex
@inproceedings{biadgligne2021parallel,
    title       = {Parallel corpora preparation for English-Amharic machine translation},
    author      = {Biadgligne, Yohanens and Sma{\"i}li, Kamel},
    booktitle   = {International Work-Conference on Artificial Neural Networks},
    pages       = {443--455},
    year        = {2021},
    organization= {Springer}
} ```



**APA Style**
Biadgligne, Y., & Smaïli, K. (2021). Parallel corpora preparation for English–Amharic machine translation. In International Work-Conference on Artificial Neural Networks (pp. 443–455). Springer.


