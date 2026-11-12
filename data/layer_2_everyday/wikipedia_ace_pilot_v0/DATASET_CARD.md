---
language:
  - ace
license: cc-by-sa-4.0
pretty_name: Acehnese Wikipedia pilot v0 (unverified)
size_categories:
  - n<1K
tags:
  - acehnese
  - low-resource
  - indonesia
  - wikipedia
---

# Acehnese Wikipedia pilot v0 (unverified)

**A small test sample, not a finished dataset.** 44 sentences copied from ten articles of
the Acehnese Wikipedia to find out how good that source is. No speaker review is recorded
in this repository, so every row is `verified: false`. Do not use it as a reference for
correct Acehnese.

## Versions

| Version | File | Rows | Contents | Verified | sha256 |
| --- | --- | --- | --- | --- | --- |
| `wikipedia_ace_pilot_v0` | `./wikipedia_ace_pilot_v0.jsonl` | 44 | sentences from 10 articles | 0% | `b3b5d9fe99d4b565604f4c8578e7a7b2ee563d090a2870f179e8167e981cefa0` |

## Source and licence

Text is from [ace.wikipedia.org](https://ace.wikipedia.org), written by Wikipedia
contributors and licensed CC BY-SA 4.0, collected on 2026-11-12. Each row's `source_url`
is a permanent link to the exact article version it was taken from:

| Article | Version | Rows |
| --- | --- | --- |
| Dayah | [158750](https://ace.wikipedia.org/wiki/Special:Permalink/158750) | 5 |
| Idul Fitri | [107975](https://ace.wikipedia.org/wiki/Special:Permalink/107975) | 5 |
| Jagong | [160434](https://ace.wikipedia.org/wiki/Special:Permalink/160434) | 4 |
| Lamri | [159055](https://ace.wikipedia.org/wiki/Special:Permalink/159055) | 5 |
| Harah Jawoe | [158494](https://ace.wikipedia.org/wiki/Special:Permalink/158494) | 5 |
| Hasan di Tiro | [150607](https://ace.wikipedia.org/wiki/Special:Permalink/150607) | 5 |
| Ali Hasjmy | [150746](https://ace.wikipedia.org/wiki/Special:Permalink/150746) | 1 |
| Madinah | [158497](https://ace.wikipedia.org/wiki/Special:Permalink/158497) | 5 |
| Keuseutani Rayek | [157872](https://ace.wikipedia.org/wiki/Special:Permalink/157872) | 4 |
| Kuala Lumpur | [158818](https://ace.wikipedia.org/wiki/Special:Permalink/158818) | 5 |

## Data

Fields: `type` (always `sentence`), `id`, `ace` (the Acehnese text), `ind` and `eng`
(empty: no translations yet), `source`, `source_url`, `licence`, `collected`,
`verified` (always `false`).

## How it was made

The first five sentences of 40 to 220 characters were taken from each of ten articles
(50 rows). Changes from the Wikipedia text:

- Six rows were dropped: two sentence fragments, three list items and one list of a
  person's family members. That is why the ids `wiki_0001` to `wiki_0050` have gaps.
- A page-rendering error message was removed from `wiki_0006`.
- Nothing else was edited. Spelling is as found.

## Limitations

- Unverified, and the articles were picked by hand, so this says little about the
  whole Acehnese Wikipedia.
- Encyclopaedia style, not everyday speech; some articles are translated world topics.
- Spelling is inconsistent, even within one article (for example `uroe` and `uroë`).
- Very small, with no dialect labels and no translations.

## Citation

```
@misc{wikipedia_ace_pilot_v0_2026,
  title  = {Acehnese Wikipedia pilot v0 (unverified)},
  author = {Aceh NLP},
  year   = {2026},
  url    = {https://github.com/aceh-nlp/dataset},
  note   = {Text by Acehnese Wikipedia contributors, CC BY-SA 4.0}
}
```
