---
language:
  - ace
  - id
  - en
license: cc-by-sa-4.0
task_categories:
  - translation
  - automatic-speech-recognition
  - text-to-speech
pretty_name: Aceh Everyday Speech and Text
size_categories:
  - n<1K
tags:
  - acehnese
  - low-resource
  - indonesia
  - community-collected
---

# Aceh Everyday Speech and Text

<!-- Replace every TODO before publishing. -->

## Versions

| Version | File | Rows | Contents | Verified | sha256 |
| --- | --- | --- | --- | --- | --- |
| `aceh_synthetic_data_v0` | `./aceh_synthetic_data_v0.jsonl` | 162 | 128 sentences + 32 dialogue turns + 2 long paragraphs | 0% (100% AI-drafted, Claude Fable 5.1, low effort, Nov 2026) | `50268047c0c94413864cf2b9a64688208a5d175d432003f360aa9940798f5d9e` |

v0 is synthetic and unverified: every row is an AI draft awaiting native-speaker correction. v1 will be the speaker-corrected release built from the filled correction sheet.

## Dataset summary

Everyday Acehnese (ISO 639-3 `ace`) sentences and short dialogues, each verified by
native speakers and aligned with Indonesian and English, plus recordings of speakers
reading them. Collected in Banda Aceh and surrounding regencies starting November 2026
by TODO (group name). Domain: daily life — home, transport, work, market, food, village,
prayer, family.

## Why

Acehnese has ~3.4 million speakers but almost no open transcribed speech; existing
models (Meta MMS, NLLB) were trained mostly on Bible text and perform poorly on
conversation. This set is a first step toward conversational coverage across dialects.

## Data

| Split | Rows | Clips | Hours | Speakers |
| --- | --- | --- | --- | --- |
| train | TODO | TODO | TODO | TODO |

Fields (text): `id`, `ace` (EBAYD spelling), `ace_plain` (diacritics stripped), `ind`,
`eng`, `dialect`, `speaker_id`, `rating` (1–5 naturalness by the verifying speaker),
`section`, `ace_draft` (the original AI draft the speaker corrected, kept for research
on AI errors in Acehnese).

Fields (audio): `file_name`, `transcription` (= `ace`), `ind`, `eng`, `speaker_id`, `dialect`.
Audio is 16 kHz mono WAV.

## Collection process

1. 128 sentences and 4 dialogues were drafted by an AI model (Claude Fable 5.1, low effort, Nov 2026) as prompts.
2. Native speakers rated each draft 1–5 and rewrote it as they would say it.
3. Speakers recorded their corrected sentences on a phone in a quiet room.
4. `scripts/build_dataset.py` validated and packaged the result.

## Speakers

TODO: number, age range, gender balance, dialect areas (banda_aceh, pidie, aceh_utara,
barat, ...). All speakers gave recorded verbal consent to CC BY-SA 4.0 release.
No names or identifying metadata are included.

## Limitations

- Read speech, not spontaneous conversation.
- Sentences were drafted by a non-speaker AI and then corrected, so topic choice
  reflects a visitor's view of daily life.
- Small size; dialect coverage uneven (see table).
- Spelling follows EBAYD but Acehnese orthography is not fully standardised.

## Citation

```
@misc{aceh_everyday_2026,
  title  = {Aceh Everyday Speech and Text},
  author = {TODO},
  year   = {2026},
  url    = {https://huggingface.co/datasets/TODO}
}
```

## Acknowledgements

Balai Bahasa Provinsi Aceh (KBDA Daring), IndoNLP (NusaX), the speakers of Banda Aceh.
