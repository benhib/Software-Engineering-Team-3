# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

Team 3's documentation repo for the DHBW Ravensburg Software Engineering project (TSA/TSL25, Prof. Dr. Christian Braunagel). Team: Ben Hibinger, Nikolai Schlosser, Niklas Reutter, Julien Armbruster. There is no application code yet. Part I is pure documentation in LaTeX and Markdown. The full task is in `TSATSL25_SW_Eng_Project_Part1.pdf`; read it when details matter.

All deliverables are written in **English**.

## The assignment

Theme: *Develop a software solution that improves teaching, learning, collaboration, or campus life at the Cooperative University.* The idea must be complex enough for multiple use cases, several interacting components, real business logic, persistent data, and both functional and non-functional requirements.

Part I (Q4 2026) runs in phases with a role swap:

1. **Inception**: team picks a name and an idea. Inception Document of 2 to 5 pages, deliberately high-level: project title, team name as author, problem statement, motivation, proposed solution, stakeholders, intended users, at least one use-case diagram.
2. **Project Exchange** (deadline **24.11.2026**, start of lecture): instructor assigns our idea to another team. From then on we are **customer/domain expert for our own idea** and **Requirements Engineering team for another team's idea**.
3. **Elicitation**: interviews, workshops, walkthroughs, questionnaires with the other team.
4. **Elaboration**: SRS following the IEEE template (Wiegers). Resolve ambiguities, system boundaries, FR/NFR classification, assumptions, constraints.
5. **Negotiation and Validation** with the customer team.
6. **Handover** (deadline **01.12.2026**): approved SRS goes back to the original team as the baseline.
7. **Object-Oriented Analysis** of **our own** project based on the SRS we received back: refined use-case model, analysis class diagram, class/responsibility/relationship lists.

Final submission: **06.12.2026 23:59:59**, all as PDF via Moodle. Deliverables: Inception Document, SRS (incl. history of requirement discussions), RE documentation (elicitation, meeting notes, interview notes, review and negotiation results), OOA artifacts, AI Usage Record. Grading: RE 50, OOA 30, Documentation and Professionalism 20.

Part II (Q1 2027): architecture, design, implementation, verification, demo, built on the Part I SRS.

## AI usage must be recorded

Every AI use goes into `Part_I/doc/AI_usage.md`, grouped by team member (`## <Name>`, then `### <Tool>`, then bullets). This applies to Claude Code too: when Claude does work here, add an entry under the member who ran the session.

The task (section 2.9) requires each entry to state:

- the AI tool,
- the artifact or activity it was used for,
- the purpose (brainstorming, reviewing, generating alternatives, improving docs, generating code, ...),
- **how the output was reviewed, adapted or validated by the student.**

The existing entries lack the review/validation part. New entries must include it. Full prompt transcripts are not required.

## Folder structure

```
main.tex                         SRS LaTeX template (synced from inscrive.io)
TSATSL25_SW_Eng_Project_Part1.pdf  official task description
Part_I/
  doc/                           deliverable documents (AI_usage.md, Inception.tex on the inscrive branch)
  Phase_<n>/                     working material per phase
    first_ideas/ideas_<name>.md  one brainstorming file per team member
```

Keep working material under `Part_I/Phase_<n>/` matching the phase numbering above, and final documents under `Part_I/doc/`. Part II will get its own `Part_II/` tree.

## Branches

- `main`: base, initial commit came from inscrive.io.
- `inscrive`: written by the inscrive.io sync, not by hand. `Part_I/doc/Inception.tex` currently only exists here.
- `brainstorming`: idea collection, README, task PDF, AI usage file.

Single remote (`origin`, Ben's GitHub repo), no fork.

## LaTeX

**Never edit `.tex` files locally.** All LaTeX is edited in the inscrive.io online editor and reaches the repo via inscrive's sync. Local edits would conflict with that sync. Read `.tex` files for context, and propose LaTeX changes as text for the user to paste into inscrive. If a local PDF preview is needed, build outside the repo so no aux files land in the working tree:

```
latexmk -pdf -outdir=<dir outside repo> main.tex
```

`main.tex` is an AI-generated (Gemini) LaTeX port of the IEEE SRS template. Project metadata is set once via `\projecttitle`, `\docauthor` etc. at the top. Custom macros:

- `\req{ID}{Title}{Priority}{Text}` renders a boxed requirement and registers `req:ID` as a link target. IDs use `FR-XX` / `NFR-XX`.
- `\reqref{ID}` creates a clickable reference to a requirement.
- `\guidance{...}` holds the template's placeholder hints. Replace them with real content; none should remain in a submitted PDF.

The existing FR-01, FR-02, NFR-01, NFR-02 and the "User Authentication" feature are template examples, not real requirements. `Inception.tex` reuses the same preamble and title page style.
