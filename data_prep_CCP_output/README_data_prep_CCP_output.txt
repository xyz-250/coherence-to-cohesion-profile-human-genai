data_prep_CCP_output

This folder contains the frozen prepared data for the CCP generation pipeline.

The earlier part of the R project functions as data preparation.
From MODUL 5b onward, CCP_generation_pipeL reads only from this folder.

Included core files:

- l1_corpus_clean.rds: cleaned L1-Corpus reference space
- human_baseline_clean.rds: frozen human baseline text
- basic_texts_clean.rds: frozen LLM reconstruction texts
- current_paragraph_layer.rds: paragraph-preserving layer for y4
- current_texts_parsed.rds: token-level parsed layer from MODUL 5a
- parsed_S_layer.rds: sentence-level parsed layer from MODUL 5a
- ims_psychometric_lexicon_clean.rds: cleaned IMS psychometric lexicon for y1
- ims_dictionary_concreteness.rds: lemma-level concreteness dictionary
- ims_dictionary_imageability.rds: lemma-level imageability dictionary
- ims_dictionary_abstractness_proxy.rds: lemma-level abstractness proxy dictionary

IMS note:
The IMS psychometric resource was prepared before export and is only copied here.
The actual y1 measurement is not computed in this file.
MODUL 5b joins the parsed token lemmas with the IMS psychometric lexicon by lemma.

Pipeline rule:
Every new module reads existing outputs.
No previous module is regenerated unless explicitly needed.

Frozen on: 2026-07-09
