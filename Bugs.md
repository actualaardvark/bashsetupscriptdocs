# Bug Tracker
## Description
A list of existing script bugs and potential points of failure.
## Bugs
### Potentially Unreliable 'cd' Command
```bash
cd "$(dirname "${BASH_SOURCE[0]}")"
```
 - Users online seem to have some issue with using the 'BASH_SOURCE[0]' code.
 - Needs exit condition for improved reliability.