# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Build

Compile the resume with LuaLaTeX:

```bash
lualatex mark-cerqueira-resume.tex
```

This produces `mark-cerqueira-resume.pdf`. Requires MacTeX (`brew install mactex`).

## Structure

- `mark-cerqueira-resume.tex` — main entry point; sets personal info, layout, and imports sections
- `sections/` — one `.tex` file per resume section (`professional.tex`, `education.tex`, `projects.tex`, `snowflake.tex`, `skills.tex`)
- `awesome-cv.cls` — the AwesomeCV document class defining all custom commands (`\cventry`, `\cvsection`, `\cvparagraph`, etc.)
- `fonts/` — Roboto + FontAwesome fonts required by AwesomeCV

## Key LaTeX commands

- `\cventry{title}{org}{location}{dates}{items}` — a job entry with bullet points inside `\begin{cvitems}`
- `\cvsection{Name}` — section header
- `\begin{cvparagraph}` — free-form paragraph section (used for Projects and Fun Facts)
- Commented-out lines (`%`) throughout sections are content that was removed but kept for reference

To toggle a section on/off, comment/uncomment its `\input{sections/...}` line in the main `.tex` file.
