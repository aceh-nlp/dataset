# aceh-nlp/dataset

**Data only.** This repository holds every dataset for the
Aceh NLP project — and no code. The other three
repositories consume it:

| Repository | Owns |
|---|---|
| [aceh-nlp/frontend](https://github.com/aceh-nlp/frontend) | Static interface (sign-in, review, upload) |
| [aceh-nlp/dataset](https://github.com/aceh-nlp/dataset) | Data: datasets |
| [aceh-nlp/backend](https://github.com/aceh-nlp/backend) | API: serves this data, stores ratings, proxies the GPU |
| [aceh-nlp/gpu](https://github.com/aceh-nlp/gpu) | Model hosting: inference server |

## Layout

```
SOURCES.md                 every source we collect from, and where it stands
data/
  layer_1_specialist/      checked by educated native speakers from NGOs and institutions
  layer_2_everyday/        daily speakers, recordings, internet text
    wikipedia_ace_pages_v0/  9 whole pages from the Acehnese Wikipedia, a source test,
                           0% speaker-verified; see its DATASET_CARD.md (sha256 inside)
  layer_3_synthetic/       AI-drafted or rule-generated
    aceh_synthetic_v0/     162 AI-drafted rows (sentences, dialogue turns, paragraphs),
                           0% speaker-verified; see its DATASET_CARD.md (sha256 inside)
```

## Rules

- Every new data file is **JSONL** (UTF-8, one object per line). No TSV/CSV for
  new data.
- Collected text is kept whole: one row per page (a web page, an article, one page of
  a book), not cut into sentences. A book is one file, one row per page.
- Annotation of collected text is per page or per book, not per sentence. It goes in
  the dataset's `raw/annotation_sheet.jsonl` (`rating_1_5`, `dialect`, `notes`) and
  carries no personal information.
- Synthetic / AI-drafted content stays explicitly marked (`verified: false`,
  `source` field) and separate from human-verified data.
- Earlier material (NusaX, grammar pairs, evaluator prompts, model-screening
  results, provenance and research notes) and the pre-November history live in
  the original repository, `gee842/aceh-nlp-dataset`, at tag `evidence-20261103`.
- No code, no tests, no CI here. Validation lives in the backend repository.
- Runtime data (ratings, uploads, anything with personal information) never
  enters this repository.
