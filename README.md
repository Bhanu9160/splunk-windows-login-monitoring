# Windows Login Monitoring Dashboard using Splunk

## Project Overview
Developed a Splunk dashboard to monitor Windows login activities using Windows Security Event Logs.

## Features
- Successful Login Monitoring (Event ID 4624)
- Failed Login Monitoring (Event ID 4625)
- Login Trends Analysis
- Top Logged-in Users
- Dashboard Visualizations

## Tools Used
- Splunk Enterprise
- Windows Event Logs
- SPL (Search Processing Language)

## Dashboard Panels
1. Successful Logins
2. Failed Logins
3. Successful Logins by User
4. Failed Logins by User
5. Login Trend Over Time
6. Top Logged-in Users

## SPL Queries

### Successful Logins
```spl
EventCode=4624
