

## Overview
This script demonstrates how Lua can be used to automate basic SOC workflows.  
It loops through a table of suspicious IP addresses and flags each one, simulating how analysts triage Indicators of Compromise (IOCs) during incident response.


## How It Works
- Stores suspicious IPs in a Lua table.  
- Uses a loop (`ipairs`) to iterate through each IP.  
- Calls a function (`flag_ip`) to print flagged IOCs.  
- Output is printed to the console.


