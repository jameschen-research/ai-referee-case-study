# Can a Model Referee a Materials Paper?

An expert-oversight case study. I asked a frontier model (Claude Opus 5.5) to referee one published experimental paper in my field, three times, and scored its review against my own frozen issue list and against the journal's published referee reports.

**Read the case study:** https://jameschen-research.github.io/ai-referee-case-study/

**Paper reviewed:** Cao, N., Zhang, Y., Gu, X. & Wu, M. Efficient recycling of spent Li-ion battery cathodes by laser-induced high-temperature thermal shock. *Nature Communications* 16, 7169 (2025). https://doi.org/10.1038/s41467-025-62434-1

## Key results

| Measure | Result |
|---|---|
| Critical key issues found over 3 runs (of 16) | AI 11 fully or partly, 7 fully · referees 6 |
| Key issues found over 3 runs (of 19) | 13 fully or partly, 9 fully |
| Recall, single run (partial = 0.5) | 42–53% |
| Key issues missed in all 3 runs | 6, all requiring process-physics or scale-up reasoning |
| Precision of scored AI comments | 93.0% (9 false alarms) |
| AI comments left unscored (costly to verify) | 52 of 180 (29%) |
| Distinct issues across all three sources | 66 (expert 19 · AI 47 · referees 26) |

## Method

- **Answer key:** 19 issues (16 critical), written and frozen before any model run, each with a severity and an error category.
- **Model:** Claude Opus 5.5. Prompt, verbatim: "Please review this paper as a referee for Nature Communications." Main text and supplementary information attached. Three runs, each in a new session with no prior context. A pilot run in a session that held study context was excluded.
- **Referees:** the journal's published peer-review file (three referees, two rounds).
- **Ratings per AI comment:** hit, partial, new valid, false alarm, unscored.
- **Recall** (issue level, per run) = (fully found + 0.5 × partly found) ÷ 19. Union counts are reported both for full matches and for full-or-partial matches.
- **Precision** (comment level) = (hit + partial + new valid) ÷ (comments − unscored).
- **Issue counts** across sources describe coverage and are not a like-for-like score: AI new issues were merged by topic, and most referee-only issues are minor.
- **AI-assisted scoring:** merging duplicates, mapping referee comments and aligning ratings across runs were drafted with Claude and checked by the author item by item. One of 67 proposed changes was wrong and was reverted.

## Disclosure

The author has a Matters Arising on this paper under editorial consideration at *Nature Communications*. Until that process ends, the case study describes the 19 answer-key issues by topic and error category only and does not reproduce the manuscript's arguments.

## Limitations

One paper, one model, one rater. The rater wrote the answer key and is not blind to the source of each comment. Unscored comments are excluded from precision. The numbers describe this case and should not be read as general rates.

## Materials

Available to reviewers on request: the frozen answer key, the raw model outputs and the scoring workbook.

---

James Chen, Ph.D., P.Eng., FCAE · November 2026. Claude assisted with organizing the scoring and drafting this page; all ratings, numbers and conclusions were checked by the author.
