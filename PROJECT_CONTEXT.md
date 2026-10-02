# Project Context

## Research title

Automatic Orchestral-to-Piano Reduction with Part Importance Analysis, Musical Structure Preservation, and Playability Optimization

## Core research question

How does Liszt transform Beethoven's orchestral textures into playable piano textures, and can these reduction strategies be learned computationally for automatic orchestral-to-piano reduction?

## Dataset scope

Use only:
- Beethoven's 9 symphonies
- Franz Liszt's solo-piano transcriptions, S.464/1–9

Do not use LOP Database or METEOR as primary training data unless the scope is explicitly revisited.

Preferred representation:
- high-quality MusicXML / MXL
- Beethoven orchestral score paired with Liszt piano transcription

## Current dataset status

### Beethoven side
- 37 movements acquired as .mxl
- imported into this repository under `data/beethoven/`
- upstream source: Mark Gotham / Hauptstimme / OpenScore Orchestra Corpus
- files are imported candidates, not automatically scholarly ground truth
- authoritative-score validation is still pending

### Liszt side
- symbolic corpus is not yet fully acquired
- S.464/5 has candidate sources, but no symbolic file has yet passed strict validation
- IMSLP is used as an authoritative score reference where appropriate
- do not mark a Liszt file validated merely because a filename or webpage claims it is S.464

## Planned reduction labels

- preserve
- omit
- merge
- octave-shift
- register-transfer / redistribution
- doubling-reduction
- rhythmic simplification
- RH/LH assignment

Additional musical descriptors:
- melody
- countermelody
- bass
- harmony
- accompaniment
- doubling
- color
- texture

Playability descriptors:
- hand span
- simultaneous-note count
- note density
- leap distance

## Alignment policy

Start with:
- movement
- measure
- beat

Do not move to note-level alignment until the structural alignment is stable.

## Training plan

Later stages may include:
- ICL baseline
- SFT
- GRPO / reward optimization

Current priority is dataset construction, validation, alignment, and annotation schema—not model training.

## Project pipeline

Beethoven orchestra
→ high-quality orchestral MusicXML
→ validation
→ alignment with Liszt
→ orchestration-role annotation
→ transformation labels
→ RH/LH + playability descriptors
→ paired dataset
→ SFT
→ GRPO

## Annotation rationale

The project may store explicit annotation fields that represent:
score understanding
→ role analysis
→ importance
→ reduction decision
→ hand allocation
→ playability adjustment

These are dataset annotations, not hidden model reasoning.

## Current meeting priorities

1. Beethoven structural QC
2. Annotation schema v1
3. Small measure-level alignment prototype
4. Liszt symbolic-source blocker summary
5. Updated meeting progress document
