# AutoNessus
This script communicates with the Nessus API in an attempt to help with automating scans. Depending on the flag issued with the script, you can list all scans, list all policies, start, stop, pause, and resume a scan. It may be helpful to create a cron job/scheduled task for automating the start or pause of scans if the client has a desired testing window.

Please feel free to use and modify this code; it works for our purposes but may not work perfectly for yours. Any suggestions or improvements are highly encouraged.


# Dependencies
Requires python version 2.x and "requests" module to be installed.
Installation can be found here: http://docs.python-requests.org/en/latest/user/install/

# Start & Help
> python autoNessus.py

> python autoNessus.py -h

Both will run the help menu and display a list of options.


# Credentials
This script authenticates to the Nessus server when supplying any other flag than -h. Correct URL and credentials must be placed on lines 52-56 of the script.


# Examples
List all scans and scan IDs (scan IDs to be used with other flags)

> python autoNessus.py -l

Start scan 42
 
> python autoNessus.py -sS 42

Pause scan 42

> python autoNessus --pause 42


# Notes
If you would like to start an already completed scan (one with a "completed" status) you must add 'completed' to the list on line 272. This was done to ensure that scans would not re-run once completed.

# Credits
Thank you to Stephen Haywood for writing the example script that some of the functionality for this tool used. The example script can be found here: https://github.com/averagesecurityguy/Nessus6/blob/master/nessus6_scan_demo.py

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.
