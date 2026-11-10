# Smoking Cessation project showcase

SM is an iPhone prototype for recording smoking activity and seeing how
spending changes over time. It uses the first few recorded days to establish a
baseline, then compares later spending with what the user would have been
expected to spend at their baseline smoking rate.

**Build 2.9 · Development on hold · Final installed-app testing and sign-off pending**

[Visit the showcase website](https://bloutzenhiser.github.io/smoking_cessation_showcase/) ·
[Read the validation record](VALIDATION.md)

## From Build 1 to Build 2

| Build | What it delivered | Status |
| --- | --- | --- |
| Build 1 | Recorded cigarettes and day history on the phone, with pause, resume, and CSV export. | Build 1.3.2 passed its final phone checklist on October 28, 2026. |
| Build 2 | Added baseline calculations and spending comparisons. Build 2.9 also recorded whether the user confirmed another cigarette within 60 seconds. | Build 2.9 is the latest tested version in this showcase. Final installed-app testing and sign-off remain open. |

The [project overview](PROJECT_OVERVIEW.md) explains the progression in plain English.

## Project experience

- Choose a baseline length and record a price per pack.
- Start and end each Day explicitly, with Pause and Resume when needed.
- Record cigarettes and review Day history.
- Keep zero-cigarette Days or repeat attempts according to the user's choice.
- Begin Program Day 1 after baseline collection is complete.
- Review spending and savings, and export records when needed.

## Demonstration screens

These earlier interface previews use invented test data.

| Setup | Day in progress |
| --- | --- |
| <img src="images/setup.png" width="320" alt="SM setup preview with pack price and baseline length options"> | <img src="images/day.png" width="320" alt="SM Day preview showing a synthetic cigarette count and recording controls"> |

## What Build 2.9 testing found

The independent CSV review covered **28 recorded events**. The report lists
**119 passing checks, one filename mismatch, 12 inconclusive checks, and five
that did not apply**. The filename mismatch came from the downloaded copy's
suffix. The CSV review leaves phone behavior and final acceptance to separate
testing.

- [Validation overview PDF](CSV_Validator/examples/build-2.9-recorded-overview.pdf) summarizes the results.
- [Detailed validation PDF](CSV_Validator/examples/build-2.9-recorded-detailed.pdf) shows the individual checks and supporting evidence.
- [Full validation record](VALIDATION.md) includes the CSV export, functional testing logs, and defect logs. The CSV uses a tester alias and replacement record IDs.

## Showcase history

### v0.03 — November 10, 2026

- Published the one-page showcase website.
- Added the Build 1 to Build 2 milestones and Build 2.9 testing summary to this README.

### v0.02 — November 10, 2026

- Added the Build 1 to Build 2 overview and Build 2.9 validation evidence.
- Recorded the development hold and outstanding acceptance work.

### v0.01 — November 5, 2026

- Established a public presentation containing an overview and synthetic screenshots.
- Kept the application implementation and development records private.
- Restricted this repository's tracked files to this overview, its screenshots,
  and the ignore rules that prevent accidental source-code additions.

Future showcase changes receive a new showcase version and an entry in this history.
