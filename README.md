# PyNessusScript
This script communicates with the Nessus API in an attempt to help with automating scans. Depending on flag issued with the script, you can list all scans, list all policies, start, stop, pause, and resume a scan.


# Start & Help
> python pyNessusScript.py

> python pyNessusScript.py -h

Both will run the help menu and display a list of options.


# Credentials
This script authenticates to the Nessus server when supplying any other flag than -h. Correct URL and credentials must be placed on lines 52-56 of the script.


# Example
> python pyNessusScript.py -l
List all scans and scan IDs (scan IDs to be used with other flags)
  
> python pyNessusScript.py -sS 42
Starts scan 42

> python pyNessusScript.py --pause 42
Pauses scan 42


# Note
If you would like to start an already completed scan (one with a "completed" status) you must add 'completed' to the list on line 272. This was done to ensure that scans would not re-run once completed.
