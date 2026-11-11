# Educational companion: Adaptive decision support under frozen rules

Choose the depth you need:

- **Concise study guide:** [PDF](STUDY_GUIDE.pdf) or [Markdown](STUDY_GUIDE.md), four pages on the question, the main results, and what the study does not show.
- **Complete companion:** [PDF](COMPANION.pdf) or [Markdown](COMPANION.md), with ten guided lessons (P01 to P10), twelve section readings (R01 to R12), seven supplement modules (S01 to S07), six worked examples (W01 to W06), and a twelve-question self-test (T01 to T12) with explained answers.
- **Coverage and checks:** [coverage map](COMPLETE_COVERAGE.md), [check results](VALIDATION.json), and [file hashes](ARTIFACTS.json).

## Basis

Both editions explain *Adaptive decision support under frozen rules: guarantees, failure modes, and component admission*, as submitted to *PLOS ONE* on 11 November 2026 (manuscript SHA-256 `5c984ac151e9751486bc5fcce03a5b8333524a2dcffd10b02b9a4fe1fc613130`). The manuscript is under review. The raw simulation histories are public at Zenodo (https://doi.org/10.5281/zenodo.24117501).

## What was checked

A script checked both editions against the manuscript and its seven appendices:

- every number in the text appears in those sources, apart from labeled illustrative inputs and arithmetic on reported values;
- every cited line range starts and ends at a section boundary;
- each guided lesson has its six parts, and the self-test has four core, four boundary, and four transfer questions;
- the five global nonclaims are quoted word for word;
- readability is at grade 7.7 for the study guide and 7.8 for the companion, with no sentence longer than 30 words.

The script was itself tested by planting seven faults in copies of the text, such as a changed result and a deleted nonclaim. It caught all seven.

## What was not done

No reader from the intended audience has reviewed these editions, no person has reviewed them for claims they might add to the paper, and the self-test has not been given to readers.

## Scope

All evidence in the paper was computational; no physical system was tested. These editions restate the paper and add no results.
