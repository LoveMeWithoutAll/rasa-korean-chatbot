# rasa korean chatbot starter pack

## It uses

1. [Rasa2](https://github.com/RasaHQ/rasa)
1. [HuggingFace](https://github.com/huggingface)
1. [bert-base-multilingual-cased](https://huggingface.co/bert-base-multilingual-cased)
1. [kr-bert](https://huggingface.co/snunlp/KR-BERT-char16424)
1. [kobert](https://huggingface.co/monologg/kobert#)

## For using other bert model

1. open `config.yml`
1. edit line #17 `model_weights` from `bert-base-multilingual-cased` to other one like `snunlp/KR-BERT-char16424` and `monologg/kobert`
1. open `path/lib/python3.x/site-packages/transformers/modeling_utils.py`
1. edit line #640 from `from_pt = kwargs.pop("from_pt", False)` to `from_pt = kwargs.pop("from_pt", True)`

Rasa v2.1.2 does not yet support train from pytorch models. So some editing code is needed.
