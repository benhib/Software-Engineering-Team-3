# AI Usage Table

## Ben
### Gemini
| General Usage  | Artifact | Purpose of use | Review |
| :------------- | -------- | -------------- | ------ |
| Searching tools for online collaborative requirements making | Use of `inscrive.io` | Easier collaboration work and cleaner output files | - |
| Create **LaTeX** template for requirements making | `main.tex` | Template to base requirements on | When doing requirements Engineering the entire template will get a workover |
| Fix LaTeX formatting | syntax in `Inception.tex` | Cleaner output file | Peer reviewed |

## Julien
### Claude Code
| General Usage  | Artifact | Purpose of use | Review |
| :------------- | -------- | -------------- | ------ |
| Translate own ideas (campus room plan with navigation, parking spot reporting) into English and format them like `ideas_ben.md` | `ideas_julien.md` | Brainstorming | Ideas are Julien's own, Claude only translated and formatted them. Julien checked the file against the original ideas before committing |
| Check use case diagram for errors | `Use-Case-Diagram.png` | Correctness and UML conformity of the diagram | Peer reviewed |

## Nikolai
### Claude Code
| General Usage  | Artifact | Purpose of use | Review |
| :------------- | -------- | -------------- | ------ |
| Create a context file for the AI assistant (task summary, deadlines, folder structure, AI usage rules) | `CLAUDE.md` | Improving documentation | Nikolai checked it against the task PDF and the repo, and corrected the LaTeX workflow (LaTeX is only edited in inscrive, never locally) |
| Create an ignore file for macOS system files and LaTeX build artifacts | .gitignore | Repository setup | Verified with `git check-ignore` that the junk files are ignored and the task PDF is still tracked |

## Niklas
### Claude Code
| General Usage | Artifact | Purpose of use | Review |
| :--------------|----------|----------------|--------|
| Explain the project task in German | – | Understanding the task | Niklas compared the explanation with the original PDF |
| Suggest project ideas around the theme and the timetable, then simplify them and translate them into simple English | `ideas_Niklas.md` | Brainstorming | Claude suggested many ideas, Niklas chose the final three and rejected several others. Niklas checked the file before committing |
