# Smoking Cessation project overview

Smoking Cessation is an iPhone prototype that helps people track when they
smoke, establish a baseline, and compare later spending with that baseline.

This repository is a public record of testing through Build 2.9. The
[validation record](VALIDATION.md) links to the PDF reports, the test and defect spreadsheets,
and an export of 28 recorded events. The export uses a tester alias and
replacement record IDs. The reports and spreadsheets show which checks passed,
which issues were found, and what still needs testing.

## From Build 1 to Build 2

**Build 1 established reliable recording.** It recorded smoking activity on
the phone, supported pausing and resuming, and exported records for review.
Build 1.3.2 passed its final phone checklist on October 28, 2026.

**Build 2 added a way to measure progress.** It used the recorded activity to
establish a baseline and compare later spending with what the person would
have been expected to spend at their baseline smoking rate. Build 2.9 also
recorded whether the user confirmed another cigarette within 60 seconds.

## Why the measurement changed

The first outputs made it possible to count cigarettes for a recorded Day.
Reviewing those counts showed that the length of the Day could change the
apparent result. Six cigarettes over three unpaused hours is two per hour.
Six over six unpaused hours is one per hour. That comparison led to using
cigarettes per unpaused hour for the baseline. Build 2 then used that rate
and the effective prices to calculate what a later Day would cost at the
baseline rate. The [requirements](BUILD_2_REQUIREMENTS.md#worked-example)
show how to check the calculation.

## How the work was reviewed

- **AI assistance.** ChatGPT Work mode helped implement changes, prepare
  documentation and test materials, and calculate and review outputs.
- **Human decisions.** The project owner set and approved requirements,
  reviewed outputs with AI assistance, confirmed phone-test outcomes where
  evidence was available, and retained final acceptance authority.
- **Verification.** The Python validator checked recorded CSV data separately
  from the app. The published CSV and reports show what was checked and what
  those checks established. A separate calculation checks a result
  independently of the app. External reproduction would require someone to
  repeat the checks. Phone behavior and installed-app acceptance require
  their own evidence.

Development is on hold. Final testing of the installed app and sign-off are
still pending.
