# BERT Classification

## Dataset Overview

**Token level classification datasets (POS, Chunk and NER)**, (`CoNLL` dataset):

Dataset | Language | Classes | Training tokens | Dev tokens | Test tokens
:---: | :---: | :---: | :---: | :---: | :---:
CoNLL-2000 Chunk | English (en) | 23 | 211727 | - | 47377
CoNLL-2002 NER | Spanish (es) | 9 | 207484 (18797) | 51645 (4351) | 52098 (3558)
CoNLL-2002 NER | Dutch (nl) | 9 | 202931 (13344) | 37761 (2616) | 68994 (3941)
CoNLL-2003 NER | English (en) | 9 | 204567 (23499) | 51578 (5942) | 46666 (5648)

> `CoNLL-2000 Chunking` and `CoNLL-2002 NER` datasets are obtained from [[teropa/nlp/resources/corpora]](
https://github.com/teropa/nlp/tree/master/resources/corpora), `CoNLL-2003 NER` dataset is obtained from 
[[synalp/NER/corpus/CoNLL-2003]](https://github.com/synalp/NER/tree/master/corpus/CoNLL-2003). All the lines in those 
datasets are convert to `(word, label)` pairs with `\t` as separator and drop all the `-DOCSTART-` lines.

**Sentence level classification datasets**, (`CR`, `MR`, `SST`, `SUBJ` and `TREC` datasets):

Dataset | Classes | Average sentence length | Train size | Dev size | Test size
:---: | :---: | :---: | :---: | :---: | :---:
CR | 2 | 19 | 3395 | - | 377
MR | 2 | 20 | 9595 | - | 1066
SST2 | 2 | 19 | 67349 | 872 | 1821
SST5 | 5 | 18 | 8544 | 1101 | 2210
SUBJ | 2 | 23 | 9000 | - | 1000
TREC | 6 | 10 | 5452 | - | 500

> All the datasets are converted to `utf-8` format. For the `SUBJ`, `MR` and `CR` datasets, `90%` for train, `10%` 
for test, while the dev dataset is the duplicate of test dataset. For `TREC` dataset, the dev dataset is the duplicate 
of test dataset. Those datasets are obtained from [[facebookresearch/SentEval]](
https://github.com/facebookresearch/SentEval).

**Natural language inference (sentence pair classification) datasets**, (`MRPC`, `SICK` and `SNLI` datasets):

Dataset | Classes | Train size | Dev size | Test size
:---: | :---: | :---: | :---: | :---:
MRPC | 2 | 4077 | 1726 | 1726
SICK | 3 | 4501 | 501 | 4928
SNLI | 3 | 549367 | 9842 | 9824

> Those datasets are obtained from [[facebookresearch/SentEval]](https://github.com/facebookresearch/SentEval). Note 
that [MNLI](https://www.nyu.edu/projects/bowman/multinli/) and [XNLI](https://www.nyu.edu/projects/bowman/xnli/) 
datasets are implemented by the official BERT already, see `run_classifier.py` in [[google-research/bert]](
https://github.com/google-research/bert).

## Experiment Results

**Token level classification datasets**

Dataset | CoNLL-2000 en Chunk | CoNLL-2002 es NER | CoNLL-2002 nl NER | CoNLL-2003 en NER
:---: | :---: | :---: | :---: | :---:
Precision (%) | - | - | - | -
Recall (%) | - | - | - | -
F1 (%) | - | - | - | -


**Sentence level classification datasets**

Dataset | CR | MR | SST2 | SST5 | SUBJ | TREC
:---: | :---: | :---: | :---: | :---: | :---: | :---:
Dev Accuracy (%) | - | - | 91.3 | 50.1 | - | -
Test Accuracy (%) | 89.2 | 85.4 | 93.5 | 53.3 | 97.3 | 96.6

**Natural language inference datasets**

Dataset | MRPC | SICK | SNLI
:---: | :---: | :---: | :---:
Dev Accuracy (%) | - | - | -
Test Accuracy (%) | - | - | -

## Reference
- [[google-research/bert]](https://github.com/google-research/bert).
- [[macanv/BERT-BiLSTM-CRF-NER]](https://github.com/macanv/BERT-BiLSTM-CRF-NER).
- [[Kyubyong/bert_ner]](https://github.com/Kyubyong/bert_ner).
- [[kyzhouhzau/BERT-NER]](https://github.com/kyzhouhzau/BERT-NER).
