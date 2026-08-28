# Too Much Accuracy

Scores how close every single hit was, not just which judgement it landed in. Each tile is measured against its exact perfect timing, scored on a curve you shape yourself, and kept as a per-tile record you can read after the run or export as a file.

## Where to find it

Open the Quartz menu in-game and pick **Overlay → Too Much Accuracy** from the sidebar. Turn on **Too Much Accuracy** to start recording.

## The score

Every hit earns 0–100 points from its millisecond deviation, and the run's accuracy is the average across its tiles. The **Scoring Curve** section shapes it:

- **Perfect Window** — deviations up to this many milliseconds score the full 100.
- **Max Deviation** — at this deviation and beyond, a hit scores 0.
- **Curve Exponent** — how the score falls between the two: higher values stay forgiving near the window and drop harder toward the edge.

## Combo

A combo counts hits in a row that scored well, under the **Combo** section:

- **Combo Threshold** — the score a hit needs to keep the combo going; anything below resets it.
- **Empty Press Tolerance** — how many stray presses in a row are let through before they start costing you. Within the tolerance an empty press scores 0 and the combo survives; past it, each one breaks the combo and takes the **Empty Press Penalty**.

## Penalties

The **Penalties** section sets what mistakes cost: **Miss Penalty**, **Overload Penalty**, and **Empty Press Penalty** are each their own (negative) score.

## Seeing it while you play

- **Show Score In Hit Text** — adds the hit's score to the game's own hit text as it pops up, so you get per-hit feedback without looking anywhere else.
- The running accuracy and combo are published as stats, so you can put **TMA Accuracy** and **TMA Combo** on a [Panels](panels.md) overlay and watch them update live during a run.

## Death markers

- **Show Death Markers** — leaves a red ring on the tile where you died, so a run's problem spots stay visible while you retry them. The last twenty are kept.
- **Clear Death Markers** wipes them all at once.

## Last run

The **Last Run** section under the settings shows the finished run's totals, followed by one row per tile: the tile number, its judgement, how many milliseconds early or late you were, and its score. Long runs list the most recent 300 tiles and say how many there were in total.

**Export Last Run (JSON)** writes the whole run — totals plus every tile, with no 300-tile cut-off — to a timestamped file in the `AccuracyExports` folder inside Quartz's data folder, and the page tells you the exact path it wrote.

!!! note
    Midspins are skipped rather than scored, so a spin tile never counts for or against your accuracy.
