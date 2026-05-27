# JazzyFS Sonification Audio

This repository contains the audio examples for the thesis *JazzyFS: Adaptive File Prefetching with Runtime Suppression Signals and Sonification*.

The files are generated from macOS/APFS JazzyFS decision logs and are provided so readers can listen to the sonification outputs discussed in Chapter 5 and Appendix A of the thesis.

## Contents

- `Post workloads/`: post-workload musical summaries for each workload and mode.
- `seek_tones/`: adaptive-mode seek-tone examples for each workload.
- `index.html`: a browser page with embedded audio players for all examples.

## Post-Workload Summaries

Post-workload summaries are generated after each workload finishes. They map workload phase, confidence, and prefetching mode into short musical examples.

Modes map to scale quality:

- `none`: major scale
- `baseline`: natural minor scale
- `adaptive`: harmonic minor scale

The workload phase controls tempo. Sequential phases use faster tempo, and irregular phases use slower tempo. Confidence controls whether the melody moves upward or downward.

## Seek-Tone Examples

Seek-tone files use adaptive-mode decision logs. They map seek distance to short tones:

- contiguous reads are silent
- small nonzero seeks produce lower tones
- larger offset jumps produce higher tones

These files correspond to the real-time seek sonification mapping described in the thesis.

## Listening

Open the GitHub Pages site for this repository, or open `index.html` locally in a browser.
