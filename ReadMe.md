Make Me an Admin!

This script will allow a standard user to upgrade themselves to an admin for 5 minutes and then will grab a snapshot of the logs for the past 5 minutes as well so you can track what they did.

The script will create a launch daemon to take care of demoting the user so that no matter how many times they log out or shut down, after 5 minutes of uptime, a script will be run to remove their admin privileges.

It is recommended to push this script as a policy to self service to run only once per day.

Edits: If you wish to tailor the script to your own needs, here is where to make the changes.

Time Frame for Admin Rights: Line 17  
Default time in minutes: 5

User Prompt: Line 22  
Plain text default message: You now have administrative rights for 5 minutes. DO NOT ABUSE THIS PRIVILEGE...  
Default button: "Make me an admin, please!"

Time Frame for Logs to Be Pulled:  Line 80   
String after the "--last" flag in minutes Default: 5m

Location to Save Logs: line 80    
String after "--output" flag, must be valid directory
Default: /private/var/userToRemove/${userToRemove}-${date}.logarchive
