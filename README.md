# JazzyFS Sonification Audio

This repository contains the audio examples for the thesis *JazzyFS: Adaptive File Prefetching with Runtime Suppression Signals and Sonification*.

Listen online here:

<https://michelleg045.github.io/jazzyfs-audio/>

The audio files were generated from macOS/APFS JazzyFS decision logs. They are provided so readers can listen to the sonification outputs discussed in Chapter 5 and Appendix A of the thesis.

## Contents

- `Post workloads/`: 24 post-workload musical summaries, covering 8 workloads across 3 modes.
- `seek_tones/`: 8 adaptive-mode seek-tone examples, one per workload.
- `index.html`: a browser page with embedded audio players and listening-guide tables.

## Workloads

The archive includes these workloads:

- `sequential`
- `random`
- `phase_change`
- `gradual_drift`
- `seek_suppression`
- `tar_workload`
- `python_import`
- `cache_lookup_workload`

## Post-Workload Summaries

Post-workload summaries are generated after each workload finishes. They map workload phase, confidence, and prefetching mode into short musical examples.

Modes map to scale quality:

- `none`: major scale
- `baseline`: natural minor scale
- `adaptive`: harmonic minor scale

Workload phase controls tempo. Sequential phases use faster tempo, and irregular phases use slower tempo. Confidence controls whether the melody moves upward or downward. The root note can come from the natural-note set A through G.

## Seek-Tone Examples

Seek-tone files use adaptive-mode decision logs. They map seek distance to short tones:

- contiguous reads are silent
- small nonzero seeks produce lower tones
- larger offset jumps produce higher tones

These files correspond to the real-time seek sonification mapping described in the thesis.

## Listening Guide

The web page includes a `What to hear` column for every audio file. For post-workload summaries, it lists the tempo pattern, scale type, and melody direction. For seek-tone examples, it describes the expected silence, scattered tones, or frequent tones for each workload.
