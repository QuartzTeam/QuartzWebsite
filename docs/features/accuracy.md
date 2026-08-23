# Too Much Accuracy

Scores how close every single hit was, not just which judgement it landed in. Each tile is measured against its exact perfect timing, turned into two accuracy percentages, and kept as a per-tile record you can read after the run or export as a file.

## Where to find it

Open the Quartz menu in-game and pick **Overlay → Too Much Accuracy** from the sidebar. Turn on **Too Much Accuracy** to start recording.

## The two scores

Both are tracked at once, and each has its own switch:

- **JEA Accuracy** — *Just Enough Accuracy*. Scores the angular error of each hit, normalized to a reference tempo, so the same physical precision scores the same on a slow map and a fast one.
- **NEA Accuracy** — *Not Enough Accuracy*. Scores the plain millisecond deviation of each hit, so being 8 ms early always costs the same regardless of tempo.

Turn one off and it stops being shown; the other keeps going on its own.

## Seeing it while you play

- **Show Score In Hit Text** — adds the tile's score to the game's own hit text as it pops up, so you get per-hit feedback without looking anywhere else.
- Both percentages are published as stats, so you can put **JEA Accuracy** and **NEA Accuracy** on a [Panels](panels.md) overlay and watch them update live during a run.

## Death markers

- **Show Death Markers** — leaves a red ring on the tile where you died, so a run's problem spots stay visible while you retry them. The last twenty are kept.
- **Clear Death Markers** wipes them all at once.

## Last run

The **Last Run** section under the settings shows the finished run's totals — each score with the number of tiles it covered — followed by one row per tile: the tile number, its judgement, how many milliseconds early or late you were, and both scores. Long runs list the most recent 300 tiles and say how many there were in total.

**Export Last Run (JSON)** writes the whole run — totals plus every tile, with no 300-tile cut-off — to a timestamped file in the `AccuracyExports` folder inside Quartz's data folder, and the page tells you the exact path it wrote.

!!! note
    Midspins are skipped rather than scored, so a spin tile never counts for or against your accuracy.
