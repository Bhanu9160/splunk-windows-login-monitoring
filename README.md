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
Additional Security Use Case: Brute Force Detection

The dashboard was enhanced to detect potential brute force attacks by monitoring excessive failed login attempts in Windows Security Event Logs.

Brute Force Detection Query

EventCode=4625
| stats count by Account_Name
| where count > 5

This query identifies accounts that have more than 5 failed login attempts and flags them as potential brute force attack targets.

Brute Force Trend Query

EventCode=4625
| timechart count

This visualization helps track failed login activity over time and identify spikes that may indicate password guessing attacks.

Security Features Implemented

- Successful Login Monitoring (Event ID 4624)
- Failed Login Monitoring (Event ID 4625)
- User Login Activity Analysis
- Login Trend Visualization
- Top Logged-in Users Analysis
- Potential Brute Force Attack Detection
- Brute Force Trend Monitoring
- Security Alert Configuration

Skills Demonstrated

- Splunk Enterprise
- Windows Event Log Analysis
- SPL Query Development
- Security Monitoring
- Dashboard Development
- Alert Creation
- Authentication Monitoring
- Basic Threat Detection
- SOC Analyst Fundamentals
