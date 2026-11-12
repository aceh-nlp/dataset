---
language:
  - ace
license: cc-by-sa-4.0
pretty_name: Acehnese Wikipedia pages v0 (unverified)
size_categories:
  - n<1K
tags:
  - acehnese
  - low-resource
  - indonesia
  - wikipedia
---

# Acehnese Wikipedia pages v0 (unverified)

**A small test sample, not a finished dataset.** Nine whole pages copied from the
Acehnese Wikipedia to find out how good that source is. One row is one page; the text is
not cut into sentences. No speaker review is recorded yet, so every row is
`verified: false`. Do not use it as a reference for correct Acehnese.

This replaces the earlier sentence-level sample `wikipedia_ace_pilot_v0` (44 sentences
from the same articles), which is still in the repository history.

## Versions

| Version | File | Rows | Contents | Verified | sha256 |
| --- | --- | --- | --- | --- | --- |
| `wikipedia_ace_pages_v0` | `./wikipedia_ace_pages_v0.jsonl` | 9 | 9 pages, 87,321 characters, 13,308 words | 0% | `589ae75fef89093acd7fa126ee6ad2a097c58be27ea7ddc42186172d4f4fcc88` |

## Source and licence

Text is from [ace.wikipedia.org](https://ace.wikipedia.org), written by Wikipedia
contributors and licensed CC BY-SA 4.0, collected on 2026-11-12. Each row's `source_url`
is a permanent link to the exact page version it was taken from:

| Page | Version | Characters | Words |
| --- | --- | --- | --- |
| Dayah | [158750](https://ace.wikipedia.org/wiki/Special:Permalink/158750) | 18476 | 2840 |
| Idul Fitri | [107975](https://ace.wikipedia.org/wiki/Special:Permalink/107975) | 4089 | 617 |
| Jagong | [160434](https://ace.wikipedia.org/wiki/Special:Permalink/160434) | 10647 | 1633 |
| Lamri | [159055](https://ace.wikipedia.org/wiki/Special:Permalink/159055) | 6372 | 971 |
| Harah Jawoe | [158494](https://ace.wikipedia.org/wiki/Special:Permalink/158494) | 5105 | 776 |
| Hasan di Tiro | [150607](https://ace.wikipedia.org/wiki/Special:Permalink/150607) | 5011 | 783 |
| Madinah | [158497](https://ace.wikipedia.org/wiki/Special:Permalink/158497) | 11019 | 1734 |
| Keuseutani Rayek | [157872](https://ace.wikipedia.org/wiki/Special:Permalink/157872) | 5437 | 749 |
| Kuala Lumpur | [158818](https://ace.wikipedia.org/wiki/Special:Permalink/158818) | 21165 | 3205 |

## Data

Fields: `type` (always `page`), `id` (`acewiki_` plus Wikipedia's page number), `title`,
`ace` (the whole page as plain text, with line breaks), `source`, `source_url`,
`licence`, `collected`, `verified` (always `false`).

`raw/annotation_sheet.jsonl` has one row per page for the collector's judgement
(`rating_1_5`, `dialect`, `notes`). All of it is still empty.

## How it was made

Ten pages were picked by hand and their plain text taken through Wikipedia's own
interface. Changes from the Wikipedia text, all mechanical:

- Leftover page code was removed: page-error messages, broken template links and stray
  wiki brackets.
- Spaces at line ends and runs of empty lines were trimmed.
- No words were changed. Spelling is as found.

One of the ten pages (Ali Hasjmy) is held back: its family section names the person's
wife and children, and about a third of it is a list of Indonesian book titles.

## Limitations

- Unverified, and the pages were picked by hand, so this says little about the whole
  Acehnese Wikipedia.
- A whole page carries more than Acehnese sentences: headings, lists, tables turned into
  lines, and reference lists with Indonesian, English and French titles.
- Encyclopaedia style, not everyday speech; some pages are translated world topics.
- Spelling is inconsistent, even within one page (for example `uroe` and `uroë`).
- No dialect labels and no translations.

## Citation

```
@misc{wikipedia_ace_pages_v0_2026,
  title  = {Acehnese Wikipedia pages v0 (unverified)},
  author = {Aceh NLP},
  year   = {2026},
  url    = {https://github.com/aceh-nlp/dataset},
  note   = {Text by Acehnese Wikipedia contributors, CC BY-SA 4.0}
}
```
