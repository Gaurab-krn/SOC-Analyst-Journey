# Basic Splunk Searches

## Search all events
index=*

## Search by source IP
index=* src_ip="192.168.1.1"

## Search failed logins
index=* "failed login"
