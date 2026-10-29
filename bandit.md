\# OverTheWire: Bandit Walkthrough \& Notes



\## Level 0 -> Level 1

\* \*\*Concept:\*\* Connecting via SSH on a non-standard port.

\* \*\*Commands Used:\*\*

&#x20; ```bash

&#x20; ssh bandit0@bandit.labs.overthewire.org -p 2220

&#x20; cat readme



\## Level 1 -> Level 2
\* \*\*Concept:\*\* Password Located in file called -
\* \*\* Commands Used: \*\*
```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
cat ./-


\## Level 2 => Level 3
\* \*\*Concept\*\* Password stored in a file called --spaces in this filename--
\* \*\* Commands Used: \*\*
```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
cat -- "--spaces in this filename--"

