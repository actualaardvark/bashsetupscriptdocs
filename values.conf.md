# values.conf
## Description
values.conf is the primary configuration file for the scripts contained within the repository. It defines many of the features and characteristics of the script.
## Values and Settings
### User Access
 - userid (Integer)
   - The unix user ID for the system's intended user.
   - Used to obtain the full_name variable.
 - requireduser (String)
   - The user with JAMF permissions.
   - Incorrectly setting this variable will cause unexpected behavior.
 - passwordsource (String)
   - Where the script finds the administrator password.
   - Only necessary if autopassword is enabled.
   - Legacy is best for allowing the user to set the password, but config gives the script installer more control.
   - Legacy is a set by default to avoid leaking passwords.
  - adminpasswordconf (String)
    - The admin password used when passwordsource is set to 'config'.
  - autopassword (Boolean)
    - Toggles password autofill.
    - Disabling increases work but reduces risk of password leakage.
  - prefixlength (Integer)
    - The length of the prefix. (NMS, NUS, NLS...)
    - Determines the users to demote and premote.
    - Allows for future adjustments to naming convention
  - demoteusers
    - Users to be demoted from admin to standard.
    - Based on user prefixes
  - 
