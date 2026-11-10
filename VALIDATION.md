# SM Build 2 validation record

SM is an iPhone prototype for recording smoking activity, establishing a
baseline, and comparing later spending with that baseline.

**Validation snapshot v0.03 · Build 2.9 (app v2.9.0) · November 10, 2026**

Snapshot v0.03 identifies this evidence package. The
[showcase README](README.md) tracks the public presentation version separately.

Development is on hold. Installed-app regression and final Build 2 acceptance
remain open.

[Return to the showcase](README.md) or [read the project overview](PROJECT_OVERVIEW.md).

For the calculation rules and testing status, see the
[Build 2 requirements](BUILD_2_REQUIREMENTS.md) and
[Build 2 implementation and testing](BUILD_2_IMPLEMENTATION_AND_TESTING.md).

## Build 2.9 validation evidence

[CSV export](CSV_Validator/examples/SM_Build2.9_v2.9.0_Device-A_20261107T205513245Z_87095b6b-1053-4c55-977e-d1312783a336%20%281%29.csv) · [Overview PDF](CSV_Validator/examples/build-2.9-recorded-overview.pdf) · [Detailed PDF](CSV_Validator/examples/build-2.9-recorded-detailed.pdf) · [Functional validation log](CSV_Validator/examples/14_Build_2.9_v2.9.0_Functional_Testing_Validation_Log_v0.14.xlsx) · [Plain-English validation log](CSV_Validator/examples/14_Build_2.9_Plain_English_Validation_Log_v0.08.xlsx) · [Defect log](CSV_Validator/examples/15_Build_2_Defect_Log_v0.06.xlsx) · [Plain-English defect log](CSV_Validator/examples/15_Build_2.9_Plain_English_Defect_Log_v0.05.xlsx)

**The CSV contains recorded test evidence.** The showcase screenshots use
invented demo data. The export preserves 28 recorded events, their
timestamps and values. Device-A
replaces the tester label, and record UUIDs were regenerated consistently. The
public workbooks omit local paths and personal author metadata. Both PDFs use
the public CSV hash. The original download suffix was kept to preserve the
filename validation finding.


## Reviewing the results

The CSV is the input to the published Python validation run. The PDFs report
the outcomes and supporting evidence, and the Excel logs track functional
tests and defects, including pending and inconclusive cases. Re-running the
original checks requires the separately maintained Python validator. Readers
can check the spending math independently using the
[worked example](BUILD_2_REQUIREMENTS.md#worked-example).
