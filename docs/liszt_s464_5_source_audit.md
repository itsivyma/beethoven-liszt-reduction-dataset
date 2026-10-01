# Liszt S.464/5 symbolic-source audit

Date: 2026-10-01

## Target

Franz Liszt's solo-piano transcription of Beethoven, Symphony No. 5 in C minor, Op. 67, S.464/5.

## Authoritative reference

IMSLP lists a complete score of Liszt's S.464/5 and identifies Franz Liszt as arranger. A first-edition reprint is listed from Breitkopf und Härtel, 1865. This is suitable as a score-reference source, but the available file is PDF rather than MusicXML/MXL.

Reference:
https://imslp.org/wiki/Symphony_No.5%2C_S.464/5_%28Liszt%2C_Franz%29

## Symbolic candidates checked

### 1. MuseScore: Beethoven Liszt 5th Symphony
https://musescore.com/bendrums/scores/5147763

Observed metadata:
- Solo piano
- 41 pages
- 1574 measures
- uploaded 2018; updated 2024
- All rights reserved

Verdict: **candidate only**. Identity appears plausible, but the public page does not establish the source edition, nor does it independently verify a downloadable MusicXML/MXL file.

### 2. Sheet Music Library: Beethoven Liszt 5th Symphony Piano Solo arr.mscz
https://sheetmusiclibrary.website/musescore-files/

The site explicitly lists a file named:
`Beethoven Liszt 5th Symphony Piano Solo arr.mscz`

Verdict: **candidate only / not imported**. The listing establishes that an MSCZ file is claimed to exist, but access is through the library's membership/download workflow. Provenance and exact relationship to the Liszt edition are not yet established.

### 3. MuseTrainer public-domain MusicXML
https://github.com/musetrainer/library

The repository contains:
`scores/Beethoven_Symphony_No._5_1st_movement_Piano_solo.mxl`

Verdict: **rejected for the Liszt side unless further evidence emerges**. The file title identifies a Beethoven piano-solo version but does not identify Franz Liszt or S.464/5. Under the project's strict provenance standard, it must not be treated as the Liszt transcription.

## Current decision

No symbolic Liszt S.464/5 file has yet passed all of:
1. exact arranger/work identity,
2. actual symbolic-file access,
3. source-edition provenance,
4. comparison against the IMSLP Liszt reference.

Therefore the Liszt No.5 symbolic side remains **not validated**.

## Next validation action

Acquire the strongest available MSCZ/MusicXML candidate, convert to MusicXML if necessary, then compare:
- opening measures,
- movement boundaries,
- measure count / repeats,
- representative middle passages,
- ending,
against the IMSLP Liszt S.464/5 score before accepting it into `data/liszt/`.
