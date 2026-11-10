# Build 2 implementation and testing

**Latest candidate** · Build 2.9 / app version 2.9.0

**Status** · Development on hold. Final testing of the installed iPhone app and Build 2 sign-off remain open.

## What Build 2 added

Build 2 builds on the recording and export behavior accepted in Build 1. It adds a fixed baseline, Day and program spending, cost averages, and savings calculated against expected spending. It preserves the price and time captured with each cigarette, accounts for price changes at the time they take effect, and excludes paused time from the baseline rate and expected spending.

Later Build 2 revisions added the choice to count or repeat cigarette-free Days, changed when expected spending and savings appear on screen, and recorded close-cigarette confirmations in the Build 2.9 CSV export. The [Build 2 requirements](BUILD_2_REQUIREMENTS.md) explain the rules and include a worked spending example.

## What the testing establishes

| Evidence | Finding |
| --- | --- |
| Early Build 2.0 testing | The November 4 implementation record lists 14 of 15 Expo Go cases as confirmed. These results apply to Build 2.0. |
| Build 2.9 CSV review | The independent report covers 28 recorded events. It lists 119 passing checks, one filename mismatch caused by the download suffix, 12 inconclusive checks, and five that did not apply. Three close-cigarette pairs had saved confirmation evidence. |
| Build 2.9 phone testing | The functional log records the cases checked in Expo Go and their remaining limits. The exact 60-second phone check was deferred. Automated boundary checks passed, and the published CSV has no exactly 60-second pair. |

The CSV review verifies evidence present in the export. Checks such as on-screen spending, response to Cancel, and save recovery require separate app tests.

## What remains open

- Compare the full Day's actual spending, expected spending, and savings with an independent calculation in Build 2.9.
- Verify that the installed Build 2 app preserves existing history, including earlier counted cigarette-free Days, and confirm that reopening and exporting work as expected.
- Complete installed-app regression testing and record final Build 2 sign-off.

The [validation record](VALIDATION.md) links to the overview and detailed PDF reports, the functional testing and defect logs, and the CSV used for the independent review. This summary draws on the historical *SM Build 2 Implementation and Acceptance v0.02* and the newer Build 2.9 functional testing and validation records.
