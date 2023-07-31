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
### Flawed Config File Implementation
```bash
source values.conf
```
 - Using source to import values.conf is not ideal, since it executes the config file rather than reads it.
 ### Lacking Error Handling
 - Improved error handling would make debugging significantly easier.