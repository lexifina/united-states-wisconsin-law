# United States (Wisconsin): law history in git

The law of Wisconsin as a git history: one file per provision, with `git blame` and `git log` working line by line. It follows the shared design of [lexifina/global-law](https://github.com/lexifina/global-law).

**What is in it now (a first build, not complete)**

| Folder | Act | Versions | History |
| --- | --- | ---: | --- |
| `chapter-NNNN/` | Wisconsin Statutes: 243 of the 470 chapters in the table of contents, one folder per chapter | 1 | 11801 sections; each chapter dated by the "Published and certified under s. 35.18" date on its PDF (2026-10-01: 146, 2026-09-04: 4, 2026-08-05: 2, 2026-07-01: 7, 2026-06-19: 1, 2026-05-22: 10, 2026-05-13: 2, 2026-04-03: 7, 2026-03-01: 10, 2026-01-30: 14, 2025-12-19: 12, 2025-11-21: 8, 2025-11-01: 3, 2025-10-15: 2, 2025-09-17: 2, 2025-08-28: 1, 2025-07-29: 1, 2025-07-08: 7, 2025-06-25: 3, 2025-03-07: 1) |

Only the statute text, the section headings and each section's "History:" note are taken; the court annotations, editorial NOTEs and cross-references printed with the statutes are left out.

## Dates

The source carries the current text only. Each chapter is therefore one version, "oldest version available", dated by the date printed on its PDF after "Published and certified under s. 35.18." (the edition the chapter was taken from). The newest Internet Archive capture of each chapter PDF was read, so most chapters carry the 1 October 2026 edition and some an earlier one. Later builds will add later versions on top.

## How it is checked

Every version is read back from git on the day it took effect and on the day before (`tools/check_repo.py`) and must match `corpus.json`; the results are in `REPRODUCE.md`.

## What "author" means

The author of a commit is the law that made the change, with an e-mail address that cannot exist (`<law key>@docs-legis-wisconsin-gov.invalid`). In this first build no dated history is available, so every commit is credited to the publisher as "oldest version available". The committer is always Lexifina.

## Limits

243 of the 470 chapters listed in the statutes' table of contents (capture of 30 October 2026) are included. Not included (227): chapters 349, 350, 351, 401, 402, 403, 404, 405, 407, 408, 409, 410, 411, 421, 422, 423, 424, 425, 426, 427, 428, 429, 440, 441, 442, 443, 444, 445, 446, 447, 448, 449, 450, 451, 452, 454, 455, 456, 457, 458, 459, 460, 462, 463, 466, 470, 480, 551, 552, 553, 562, 563, 565, 569, 600, 601, 604, 605, 607, 609, 610, 611, 612, 613, 614, 616, 617, 618, 619, 620, 622, 623, 625, 626, 627, 628, 629, 630, 631, 632, 633, 635, 644, 645, 646, 647, 648, 655, 700, 701, 702, 703, 704, 705, 706, 707, 708, 709, 710, 711, 750, 751, 752, 753, 755, 756, 757, 758, 765, 766, 767, 768, 769, 770, 775, 778, 779, 780, 781, 782, 783, 784, 785, 786, 788, 799, 800, 801, 802, 803, 804, 805, 806, 807, 808, 809, 810, 811, 812, 813, 814, 815, 816, 818, 820, 821, 822, 823, 840, 841, 842, 843, 844, 846, 847, 851, 852, 853, 854, 856, 857, 858, 859, 860, 861, 862, 863, 865, 867, 868, 877, 878, 879, 881, 882, 885, 887, 889, 891, 893, 895, 898, 901, 902, 903, 904, 905, 906, 907, 908, 909, 910, 911, 938, 939, 940, 941, 942, 943, 944, 945, 946, 947, 948, 949, 950, 951, 961, 967, 968, 969, 970, 971, 972, 973, 974, 975, 976, 977, 978, 979, 980, 985, 990, 991, 992, 995. Reasons: no capture (227). The Wisconsin Constitution, the session laws (Wisconsin Acts) and administrative rules are not included. There is no history before the dates above.
