# United States (Wisconsin): law history in git

The law of Wisconsin as a git history: one file per provision, with `git blame` and `git log` working line by line. It follows the shared design of [lexifina/global-law](https://github.com/lexifina/global-law).

**What is in it now (a first build, not complete)**

| Folder | Act | Versions | History |
| --- | --- | ---: | --- |
| `constitution-*/` | Constitution of the State of Wisconsin: the preamble and 14 articles | 1 | 175 provisions, dated 2026-08-05, the publication date of the Annotated Wisconsin Constitution read (last amended at the April 2025 election) |
| `chapter-NNNN/` | Wisconsin Statutes: 416 of the 470 chapters in the table of contents, one folder per chapter | 1 | 16653 sections; each chapter dated by the "Published and certified under s. 35.18" date on its PDF (2026-10-01: 256, 2026-09-04: 6, 2026-08-05: 4, 2026-07-01: 7, 2026-06-19: 3, 2026-05-22: 16, 2026-05-13: 4, 2026-04-03: 11, 2026-03-01: 17, 2026-01-30: 24, 2025-12-19: 22, 2025-11-21: 13, 2025-11-01: 10, 2025-10-15: 3, 2025-09-17: 2, 2025-08-28: 1, 2025-07-29: 2, 2025-07-08: 8, 2025-06-25: 3, 2025-05-30: 1, 2025-03-07: 3) |

Only the statute text, the section headings and each section's "History:" note are taken; the court annotations, editorial NOTEs and cross-references printed with the statutes are left out. The Constitution is read the same way from the Annotated Wisconsin Constitution PDF (docs.legis.wisconsin.gov/constitution/wi.pdf): its court annotations are left out, and the bracketed amendment notes printed in the text are kept.

## Dates

The source carries the current text only. Each chapter is therefore one version, "oldest version available", dated by the date printed on its PDF after "Published and certified under s. 35.18." (the edition the chapter was taken from). The newest Internet Archive capture of each chapter PDF was read, so most chapters carry the 1 October 2026 edition and some an earlier one. Later builds will add later versions on top.

## How it is checked

Every version is read back from git on the day it took effect and on the day before (`tools/check_repo.py`) and must match `corpus.json`; the results are in `REPRODUCE.md`.

## What "author" means

The author of a commit is the law that made the change, with an e-mail address that cannot exist (`<law key>@docs-legis-wisconsin-gov.invalid`). In this first build no dated history is available, so every commit is credited to the publisher as "oldest version available". The committer is always Lexifina.

## Limits

416 of the 470 chapters listed in the statutes' table of contents (capture of 30 October 2026) are included. Not included (54): chapters 881, 882, 885, 887, 889, 891, 893, 895, 898, 901, 902, 903, 904, 905, 906, 907, 908, 909, 910, 911, 938, 939, 940, 941, 942, 943, 944, 945, 946, 947, 948, 949, 950, 951, 961, 967, 968, 969, 970, 971, 972, 973, 974, 975, 976, 977, 978, 979, 980, 985, 990, 991, 992, 995. Reasons: no capture (54). The session laws (Wisconsin Acts) and administrative rules are not included. There is no history before the dates above.
