# Open questions

## Name
Is the name FYNDR AI or CampusConnect AI (Figure 1 caption)?

## Usage
Must students log in with a university account, or is use anonymous?

**Assumption in SRS draft:** all users log in with their university account (FR-AUTH-001).

## History
If anonymous, how is history linked to a person (device, session)?
If there is no history, should escalated questions get redirected to a different website with only a chat and cookies to store the chat?

**Assumption in SRS draft:** with the login, conversations are stored in the student's account and are available on every device (FR-CHAT-003, FR-HIST-002).

## Language selection
Is the language chosen only manually, or detected automatically?
If manual, at the start with a popup menu (hello, what language?)?

**Assumption in SRS draft:** manual selection at any time; the browser language is preselected (English if it is not supported); the choice is saved in the account; answers are always in the selected language, even if the question is typed in another language (FR-LANG-001 to FR-LANG-004).

## Information conflict
How should conflicting information in different sources be handled?

**Assumption in SRS draft:** university documents take precedence over external websites (FR-ANS-011). Still open: contradictions between two university documents.

## Outside information
How should out-of-scope questions (tutoring, personal advice, other stuff than university information) be handled?

**Assumption in SRS draft:** the chatbot declines them, names the topics it can answer and does not forward them to staff (FR-ANS-010).

## Hardware
On which hardware should the model run? Cloud based bot or local DHBW hardware?

## Model
Which Model should be used as a base for the chatbot?

## Encryption
How is the chat protected against hackers? (TLS?)

## Feedback
What feedback can students give? Good/Bad or text?

**Assumption in SRS draft:** "helpful" or "not helpful", plus an optional comment after a "not helpful" rating (FR-FB-001, FR-FB-002).

## Notifications
Should the user get notified when a escalated question got answered by staff?
Should the staff get notified when a question escalates?
What kind of notification should that be?

**Assumption in SRS draft:** the student gets an e-mail to the university address when staff replied, without the content of the reply (FR-ESC-007), and sees an indicator on the chatbot button (FR-ESC-006). Staff are not notified and check the list of escalated questions themselves.

## UI
Are the mockups for the knowledge management and escalated questions ok?

![Mockup For Managing Knowledge Base](mockup_UI_manage.png)

![Mockup For Answering Questions](mockup_UI_questions.png)


## Where
Where should the Bot be? DHBW Homepage, Moodle?

**Assumption in SRS draft:** on all pages of the university website (FR-CHAT-001).

## Users
Who may use the chatbot: only students, or also lecturers and other employees with a university account?

**Assumption in SRS draft:** every user with a university account (FR-AUTH-003).

## Access before arrival
International and exchange students often need help before they arrive in Germany. Do they already have a university account at that time? If not, how can they use the chatbot?

**Assumption in SRS draft:** not covered yet; only users with a university account can use the chatbot (FR-AUTH-001).

## Roles
How do staff members get the roles "University Staff" and "Knowledge Administrator"?

**Assumption in SRS draft:** through their group membership in the university login system (FR-AUTH-004).

## Session timeout
After how much inactivity should a user be logged out automatically? Should this also apply to students?

**Assumption in SRS draft:** 30 minutes for all users (FR-AUTH-007).

## Conversations
Can students have several conversations, i.e. start a new one and continue an earlier one?

**Assumption in SRS draft:** yes (FR-CHAT-004, FR-HIST-004).

## Escalation trigger
Can students forward any question to staff, or only when the chatbot offers it? Can students reply to a staff reply?

**Assumption in SRS draft:** any question can be forwarded (FR-ESC-002); a staff reply cannot be answered, the student forwards a new question instead.

## Escalation routing
Should escalated questions go to specific offices (e.g. International Office, examination office), or to one shared list?

**Assumption in SRS draft:** one shared list for all staff members (Section 4.8).

## Escalation language
In which language do staff members read escalated questions and write their replies?

**Assumption in SRS draft:** staff see a German translation of questions in other languages (FR-STAFF-004); replies are delivered as written, without translation.

## Student data for staff
Which personal data of the student may staff see in an escalated question?

**Assumption in SRS draft:** name and university e-mail address; the student sees this before forwarding and has to confirm (FR-ESC-003, FR-STAFF-003).

## Data retention
NFR-SEC-003 says chats are deleted after 30 days. 30 days after the last message or after the start of the conversation? Does this also apply to escalated questions and stored feedback?

**Assumption in SRS draft:** not decided yet; the SRS only refers to NFR-SEC-003.