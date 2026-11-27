# Open questions

## Name
Is the name FYNDR AI or CampusConnect AI (Figure 1 caption)?

## Implementation scope
Does InterNex implement the escalation route and the knowledge administration completely in Part II or as a simplified version? The inception document calls both a concept (Section 1.4).

## Usage
Must students log in with a university account, or is use anonymous? (Sections 2.3 and 2.7)

**Assumption in SRS draft:** all users log in with their university account (FR-AUTH-001).

## History
If anonymous, how is history linked to a person (device, session)?
If there is no history, should escalated questions get redirected to a different website with only a chat and cookies to store the chat?

**Assumption in SRS draft:** with the login, conversations are stored in the student's account and are available on every device (FR-CHAT-003, FR-HIST-002).

## Supported languages
Which languages are supported besides German and English? (NFR-QA-002)

## Language selection
Is the language chosen only manually, or detected automatically (via cookies, written text, or a selection)?
If manual, at the start with a popup menu (hello, what language?)?

**Assumption in SRS draft:** manual selection at any time; the browser language is preselected (English if it is not supported); the choice is saved in the account; answers are always in the selected language, even if the question is typed in another language (FR-LANG-001 to FR-LANG-004).

## Information conflict
How should conflicting information in different sources be handled?

**Assumption in SRS draft:** university documents take precedence over external websites (FR-ANS-011). Still open: contradictions between two university documents.

## Outside information
How should out-of-scope questions (tutoring, personal advice, other stuff than university information) be handled?

**Assumption in SRS draft:** the chatbot declines them, names the topics it can answer and does not forward them to staff (FR-ANS-010).

## Hardware & running costs
On which hardware should the model run? Cloud based bot or local DHBW hardware? Who pays the running costs? (Sections 2.4, 2.5 and 2.7)

## Model
Which model should be used as a base for the chatbot? (Sections 2.4, 2.5 and 2.7)

## Encryption
How is the chat protected against hackers? (TLS?)

## Feedback
What feedback can students give? Good/Bad or text? What information is included?

**Assumption in SRS draft:** "helpful" or "not helpful", plus an optional comment after a "not helpful" rating (FR-FB-001, FR-FB-002).

## Notifications
Should the user get notified when an escalated question got answered by staff?
Should the staff get notified when a question escalates?
What kind of notification should that be?

**Assumption in SRS draft:** the student gets an e-mail to the university address when staff replied, without the content of the reply (FR-ESC-007), and sees an indicator on the chatbot button (FR-ESC-006). Staff are not notified and check the list of escalated questions themselves.

## UI
Are the mockups for the knowledge management and escalated questions ok?

![Mockup For Managing Knowledge Base](mockup_UI_manage.png)

![Mockup For Answering Questions](mockup_UI_questions.png)

## Whe
