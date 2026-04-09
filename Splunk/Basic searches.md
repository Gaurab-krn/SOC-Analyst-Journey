
* Search everything (last 24 hours by default)
index=*	

* Search a specific index
index=windows

* Search by keyword
index=* "failed password"

* Search with time range
index=* earliest=-7d latest=now

* Search by source type
index=* sourcetype=syslog

* Combine conditions (AND is default)
index=* sourcetype=WinEventLog EventCode=4625

* Use OR
index=* (EventCode=4625 OR EventCode=4624)

* Exclude keyword
index=* NOT sourcetype=metrics
* View all available source types
| metadata type=sourcetypes index=*

* Windows Event Logs
index=* sourcetype=WinEventLog

* Linux Syslog
index=* sourcetype=syslog

* Firewall Logs
index=* sourcetype=cisco:asa

* DNS Logs
index=* sourcetype=stream:dns

* Web Access Logs
index=* sourcetype=access_combined

* Count events by source type
index=* | stats count by sourcetype | sort -count
