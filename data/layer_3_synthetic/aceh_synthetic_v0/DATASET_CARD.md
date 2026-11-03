---
language:
  - ace
  - id
  - en
license: cc-by-sa-4.0
task_categories:
  - translation
pretty_name: Aceh Synthetic v0 (unverified AI drafts)
size_categories:
  - n<1K
tags:
  - acehnese
  - low-resource
  - indonesia
  - synthetic
---

# Aceh Synthetic v0 (unverified AI drafts)

**Every row here is an AI draft. No native speaker has checked, corrected or
recorded any of it, and no speakers have taken part yet.** Do not use it as a
reference for correct Acehnese, or to test how well a model handles Acehnese.

## Versions

| Version | File | Rows | Contents | Verified | sha256 |
| --- | --- | --- | --- | --- | --- |
| `aceh_synthetic_data_v0` | `./aceh_synthetic_data_v0.jsonl` | 162 | 128 sentences + 32 dialogue turns + 2 long paragraphs | 0% (100% AI-drafted, Claude Fable 5.1, low effort, Nov 2026) | `50268047c0c94413864cf2b9a64688208a5d175d432003f360aa9940798f5d9e` |

## Dataset summary

Everyday Acehnese (ISO 639-3 `ace`) sentences, short dialogues and paragraphs, drafted by an
AI model in November 2026. Domain: daily life, such as home, transport, work, market, food,
village, prayer and family. There is no audio.

## Why

Acehnese has millions of speakers but little open text or speech. These drafts are prompts
for native speakers to correct, not finished data.

## Data

| Type | Rows |
| --- | --- |
| Sentences | 128 |
| Dialogue turns (4 dialogues) | 32 |
| Paragraphs | 2 |

Fields in `aceh_synthetic_data_v0.jsonl`:

- All rows: `type`, `id`, `ace_draft` (the AI's Acehnese), `source`, `verified` (always `false`).
- Sentences: `section`, `ind`, `eng`.
- Dialogue turns: `dialogue`, `setting`, `turn`, `speaker`, `ind`, `eng`. `speaker` is a role
  in the drafted dialogue, not a real person.
- Paragraphs: `title`, `eng_summary`.

`raw/` holds the seed files and `correction_sheet.jsonl`, whose 160 rows cover the sentences and
dialogue turns. Its fields for speakers to fill in (`rating_1_5`, `ace_corrected`, `dialect`,
`speaker_id`, `notes`) are all still empty.

## How it was made

128 sentences, 4 dialogues and 2 paragraphs were drafted by an AI model (Claude Fable 5.1, low
effort, Nov 2026). The Indonesian and English in these files come from the same drafting and have
not been checked by a person either. Nothing else has happened to this data yet.

## Plans (none of this has happened)

Native speakers would rate and correct the drafts, producing a speaker-corrected v1. Any recording
would come later, and only after a consent process is in place.

## Limitations

- Unverified: expect spelling mistakes, Indonesian words left in and unnatural phrasing.
- Written by an AI that is not a speaker, so topic choice reflects a visitor's view of daily life.
- Very small, with no dialect labels.
- Spelling aims to follow EBAYD, but Acehnese orthography is not fully standardised.

## Citation

```
@misc{aceh_synthetic_v0_2026,
  title  = {Aceh Synthetic v0 (unverified AI drafts)},
  author = {Aceh NLP},
  year   = {2026},
  url    = {https://github.com/aceh-nlp/dataset}
}
```
