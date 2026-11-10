# Build 2 requirements

Build 2 uses recorded smoking activity to establish a baseline and compare later spending with what the user would have been expected to spend at that rate. A Day starts and ends when the user chooses, even if it crosses midnight.

## Recording and baseline

- Choose the first 3, 5, or 7 counted, completed Days for the baseline. Divide all cigarettes recorded in those Days by their total unpaused hours. The baseline stays fixed until Reset. If it contains no unpaused time, the rate and savings are unavailable.
- After baseline completion, show the total baseline cigarettes, average cigarettes per Day, average unpaused Day length, and average cost per baseline Day. Later activity leaves these values fixed.
- At the end of a cigarette-free Day, **Yes** counts the Day, **No** saves the attempt and repeats its number at the next Start, and **Cancel** keeps the Day open. A counted cigarette-free Day contributes its unpaused time. A repeated attempt is excluded from the baseline, completed-Day averages, and savings.
- Start the time-between-cigarettes display at zero. It begins with the first saved cigarette, resets with each subsequent one, excludes paused time, and returns to zero when the Day ends.
- Preserve recorded times, captured prices, and saved history. A price change applies from its saved effective time. Build 2.9 asks for confirmation when a second cigarette is recorded within 60 seconds, including exactly 60 seconds, and records the confirmation evidence in the CSV export.

## Spending and savings

Each cigarette costs its captured pack price divided by 20. Day and program spending add those costs, including cigarettes already recorded on an active Day. The average cigarette cost is weighted by the number recorded at each price. The average pack cost uses 20 times that unrounded average. The average completed-Day cost includes counted cigarette-free Days and excludes active Days and repeat attempts. Monetary values display in US dollars to the nearest cent, with rounding applied to each final result.

For a Day after the baseline, expected spending multiplies the baseline rate by the unpaused hours at each effective price and the cost per cigarette at that price. Savings equals expected spending minus actual spending. A negative value means the user spent more than expected at the baseline rate. During a Day in Build 2.9, displayed expected spending updates when a cigarette is saved. Displayed savings stays at $0.00 until the Day ends. Ending the Day finalizes expected spending and savings.

## Worked example

In this example, the baseline rate is two cigarettes per hour. The user records one cigarette in each of two unpaused hours. A pack costs $10 in the first hour and $20 in the second.

| Measure | Calculation | Result |
| --- | --- | --- |
| Actual spending | $10 ÷ 20 + $20 ÷ 20 | $1.50 |
| Expected spending | 2 × $0.50 for the first hour + 2 × $1.00 for the second | $3.00 |
| Day savings | $3.00 − $1.50 | $1.50 |

Build 2 uses CSV for export. Charts, cessation scheduling, data import and restore, and App Store release approval were outside its scope.

This summary draws on *SM Build 2 Requirements v0.07* and the later decisions recorded in the [Build 2.9 validation record](VALIDATION.md). For what was verified and what remains open, see [Build 2 implementation and testing](BUILD_2_IMPLEMENTATION_AND_TESTING.md).
