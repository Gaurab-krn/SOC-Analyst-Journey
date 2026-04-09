 # Splunk Basic Searches & Notes

## What is Splunk?
Splunk is a SIEM (Security Information and Event Management) tool
used by SOC analysts to search, monitor, and analyze log data
from various sources in real time.

## Basic Search Commands
### Search all events
index=*
### Search within a specific index
 index=main
 ### Search by keyword
 index=* "failed login"
 
### Search by source IP address
 index=* src_ip="192.168.1.1"
 ### Search by destination IP
 ### Search by destination IP
index=* dest_ip="10.0.0.1"
### Search failed login attempts
index=* "failed login" OR "authentication failed"
### Search by time range (last 24 hours)
index=* earliest=-24h latest=now 
### Count events by source
index=* | stats count by src_ip
### Find top 10 source IPs
index=* | top limit=10 src_ip
### Search for specific user activity
index=* user="admin"
### Search for error 
index=* log_level="ERROR"



