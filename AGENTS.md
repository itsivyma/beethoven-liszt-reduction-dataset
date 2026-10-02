# AGENTS.md

## Project operating rules

### Source integrity
- Never treat a URL as equivalent to a downloaded file.
- Never mark a score as validated unless evidence is recorded.
- Never infer that a piano reduction is Liszt S.464 only from a generic Beethoven/piano-solo title.
- Preserve provenance for every imported score.
- When possible, retain upstream URL, filename, format, and validation notes.

### Dataset status semantics
Use these states distinctly:
- identified
- downloaded
- format-verified
- identity-verified
- edition-checked
- validated
- aligned
- annotated

Do not collapse them.

### Beethoven files
The files under `data/beethoven/` come from Hauptstimme/OpenScore Orchestra Corpus.
They are usable symbolic-score candidates, but still require authoritative-score validation before being treated as ground truth.

### Liszt files
Do not import a symbolic candidate into the validated Liszt dataset unless:
1. exact S.464 work/movement identity is supported,
2. the actual symbolic file is obtained,
3. provenance is documented,
4. comparison with an authoritative Liszt score has been performed.

### Alignment
Start with movement → measure → beat.
Do not attempt note-level alignment first.

### Annotation
Use the controlled vocabulary documented by this repository.
Do not invent new reduction labels silently. If a new label is needed, document and justify it first.

### Coding expectations
- Prefer small reproducible scripts over one-off manual edits.
- Write outputs to version-controlled CSV/JSON/Markdown where practical.
- Keep data-processing code deterministic.
- Add QC checks before bulk dataset mutation.
- Do not overwrite source files; write normalized derivatives to separate paths.

### Research priorities
The immediate priority is not model training.
Prioritize:
1. symbolic-score acquisition
2. structural QC
3. validation
4. measure-level alignment
5. annotation schema
6. small validated examples

### Copyright / repository hygiene
This repository is public.
Do not commit copyrighted books, papers, or scanned scores unless redistribution rights are clearly established.
Store notes, bibliographic metadata, and citations instead.
