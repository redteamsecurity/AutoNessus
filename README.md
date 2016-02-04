# PyNessusScript
This script communicates with the Nessus API in an attempt to help with automating scans. Depending on flag issued with the script, you can list all scans, list all policies, start, stop, pause, and resume a scan.


# Dependencies
Requires python version 2.x and "requests" module to be installed.
Installation can be found here: http://docs.python-requests.org/en/latest/user/install/

# Start & Help
> python pyNessusScript.py

> python pyNessusScript.py -h

Both will run the help menu and display a list of options.


# Credentials
This script authenticates to the Nessus server when supplying any other flag than -h. Correct URL and credentials must be placed on lines 52-56 of the script.


# Example
List all scans and scan IDs (scan IDs to be used with other flags)

> python pyNessusScript.py -l

Start scan 42
 
> python pyNessusScript.py -sS 42

Pause scan 42

> python pyNessusScript.py --pause 42


# Note
If you would like to start an already completed scan (one with a "completed" status) you must add 'completed' to the list on line 272. This was done to ensure that scans would not re-run once completed.


This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.
