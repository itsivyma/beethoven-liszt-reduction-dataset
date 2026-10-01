# Beethoven–Liszt Reduction Dataset

Research repository for a paired symbolic dataset of Ludwig van Beethoven's nine symphonies and Franz Liszt's solo-piano transcriptions (S.464), for studying automatic orchestral-to-piano reduction.

## Current status

- **Beethoven orchestral side:** 37 movements available as compressed MusicXML (`.mxl`) from the Hauptstimme / OpenScore Orchestra Corpus.
- **Liszt piano side:** symbolic corpus still under validation. IMSLP S.464 is used as an authoritative score reference, but its available materials are primarily PDF scans.
- **Alignment / annotation:** not started yet.

## Validation policy

A source URL is not treated as a validated dataset file. Each score should pass:

1. source identified
2. file obtained
3. format verified
4. work/movement identity verified
5. authoritative-score comparison
6. MusicXML/MXL normalization
7. measure-level alignment
8. reduction annotation

## Planned structure

```
data/
  beethoven/
  liszt/
metadata/
alignment/
annotations/
docs/
scripts/
```

## Beethoven source provenance

Beethoven orchestral symbolic files are imported from the **Hauptstimme / OpenScore Orchestra Corpus**:

https://github.com/MarkGotham/Hauptstimme

The upstream corpus contains Beethoven's complete nine symphonies (37 movements) and provides `.mxl` files converted from annotated MuseScore scores.

Imported symbolic files are candidates, not automatically scholarly ground truth. They must still be checked against authoritative editions.

## Liszt reference

Franz Liszt, *Beethoven Symphonies*, S.464:

https://imslp.org/wiki/Beethoven_Symphonies%2C_S.464_%28Liszt%2C_Franz%29

## Research goal

To study orchestral-to-piano reduction decisions including preservation, omission, merging, octave/register transfer, doubling reduction, rhythmic simplification, hand allocation, orchestral-role preservation, texture, and playability.
