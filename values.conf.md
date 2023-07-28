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
 - demoteusers (Array)
   - Users to be demoted from admin to standard.
   - Based on user prefixes.
 - promoteusers (Array)
   - Users to be promoted from standard to admin.
   - Based on user prefixes.
### Networking
 - connectioncheckurl (IP Address, Web Domain)
   - The web domain or ip address used by the script to verify network connection.
 - connectioncheckenabled (Boolean)
   - Toggles the network connection check on or off.
   - It is highly recommended to leave this setting on.
### Disk Paths
 - usbdevicename (String) (Deprecated)
   - The name of the USB device the script is stored on.
### Mac Guided Enrollment Script
 - checklistge (Boolean)
   - Toggles the checklist view in the Mac Guided Enrollment Script.
 - usernamecheck (Boolean)
   - Toggles the user name check.
   - Prevents script from being run on account without JAMF admin permissions.
### App Install Inspector
 - checklistii (Boolean)
   - Toggles the checklist view in the App Install Inspector Script.
 - autorefreshenabled
   - Toggles automatic rechecking in App Install Inspector.
 - appcheckdelay (Integer)
   - The amount of time between each check if autorefreshenabled is true.
### Git Config
 - gitupdatebranch (String)
   - The Git branch the script is updated from.
### Configuration Files
 - configautoupdate (Boolean) (Deprecated)
   - Determines if the configuration file updates automatically.
   - configupdateurl (Web URL) (Deprecated)
   - The URL configautoupdate pulls the new config file from.