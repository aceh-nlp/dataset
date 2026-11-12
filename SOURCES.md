# Sources

Every source we collect from or are considering, and where it stands. Data comes in
through three channels and lands in the layer that matches how far it can be trusted.

| Channel | Lands in |
| --- | --- |
| Colleagues and community (files, scans) | `layer_1_specialist` if specialist-checked, otherwise `layer_2_everyday` |
| Internet | `layer_2_everyday` |
| AI drafts (Claude) | `layer_3_synthetic` |

## Register

| Source | Channel | Address | Licence or permission | Status | Notes |
| --- | --- | --- | --- | --- | --- |
| Acehnese Wikipedia | Internet | https://ace.wikipedia.org | CC BY-SA 4.0 (read from the site, 2026-11-12) | Sample published: `layer_2_everyday/wikipedia_ace_pages_v0`, 9 pages | About 13,000 articles but few active editors. Whole pages include headings, lists and foreign-language references. |
| NusaX | Internet (research dataset) | https://github.com/IndoNLP/nusax | To confirm on its own page | Not started | Used earlier by the project; check for overlap first. |
| FLORES-200 | Internet (research dataset) | https://github.com/facebookresearch/flores | To confirm on its own page | Not started | Translated sentences, formal style. |
| Files from colleagues | Colleagues and community | | Written permission from the owner | Waiting for the first file | |
| Community files (NGOs, schools, writers) | Colleagues and community | | Written permission from the owner | Waiting for a contact | |
| Scanned books | Colleagues and community | | Copyright to check per book | Not possible yet | One file per book, one row per page. |
| AI drafts | AI drafts | | The project's own, CC BY-SA 4.0 | `layer_3_synthetic/aceh_synthetic_v0`, 162 rows, sentence by sentence | Page-level drafts not started. |
| YouTube | Internet | | Platform terms and consent needed | Log only | Do not copy text. Only note channels, topics and rough amount. |
| Facebook | Internet | | Platform terms and consent needed | Log only | Do not copy text. Posts are personal data. |

## Rules for collecting

- Record where every page came from. No source, no page.
- Check each source's licence on its own page before collecting from it.
- No personal data: no names of private people, phone numbers, emails or private messages.
- Small samples first. No bulk downloading.
