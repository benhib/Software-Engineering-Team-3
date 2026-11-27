# AI Usage Table

## Ben
### Gemini
| General Usage  | Artifact | Purpose of use | Review |
| :------------- | -------- | -------------- | ------ |
| Finding wording, phrases and restructuring sentences, kepping their meaning but in cleaner englisch | Written text | A cleaner document with better and more precice english | Reworked sentences that are too complex |
| Phrasing the title of the External Requirements | Titles of the External Requirements | More professional sounding Requirement titles | Self reviewed, overworked to complex or non logical Titles |
| Fixing ugly formatting in the pdf output of LaTeX | `requirements_engineering.tex` | A cleaner looking output file | Tested if everything was formatted correctly. | 

## Julien
### Claude Code
| General Usage  | Artifact | Purpose of use | Review |
| Generate a first draft of SRS Section 4 (System Features) with requirements, stimulus/response sequences and priorities, based on InterNex's inception document, our interview notes, the lecture rules for good requirements and the current Sections 3 and 5 | `requirements_engineering.tex`, Section 4 | Generating a baseline draft, improving wording | Julien reviewed every requirement, decided on open points (e.g. login) and on which requirements to keep. Afterwards the team reworked Section 4 together (e.g. optional login, simplified escalation) |
| Collect open questions that came up while writing Section 4 and update them after the SRS was revised | `open_questions.md` | Finding gaps and inconsistencies | Julien reviewed the questions and added them to the file himself |

## Nikolai
### Claude (via Hermes agent)
| General Usage  | Artifact | Purpose of use | Review |
| :------------- | -------- | -------------- | ------ |
| Generate a first draft of SRS Sections 1 (Introduction) and 2 (Overall Description), the context diagram (TikZ) and new entries for Appendix A (Glossary) and Appendix C (TBD List), based on InterNex's inception document, our interview notes, our open questions and the current Sections 3 and 5 | `requirements_engineering.tex`, Sections 1 and 2, Appendix A and C | Generating a baseline draft | The AI draft is only used as a baseline. The team reworked and reviewed every section manually in meeting 2. |

### Raycast AI
| General Usage  | Artifact | Purpose of use | Review |
| :------------- | -------- | -------------- | ------ |
| Merged the SRS TBD items into `Openquestions.md`, deduplicating overlapping points and removing TBD references | `Openquestions.md` | Keeping all open questions consolidated in one document | Cross-checked with the document. |
| Grammar and phrasing improvements for individual sections | `requirements_engineering.tex` (individual sections) | Improving language correctness only | Reviewed via diff against the previous version before inserting |



## Niklas
### Claude Code
| General Usage | Artifact | Purpose of use | Review |
| :--------------|----------|----------------|--------|

