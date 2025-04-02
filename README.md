**AWS WorkSpaces Inactive Users Report**

Overview

This script retrieves AWS WorkSpaces information across multiple regions and generates a CSV report listing all inactive users, including those who have never logged in. It merges WorkSpaces details with their connection statuses and filters out active users.

Features

Fetches AWS WorkSpaces details (username, computer name, OS, region, etc.).

Retrieves connection status to determine inactive users.

Filters users who haven't logged in for over 60 days or never logged in.

Outputs a structured CSV report (aws_vdi_full_report.csv).

Requirements

AWS CLI installed and configured with appropriate permissions.

jq installed for JSON parsing.


Customization

Modify AWS regions: Edit the AWS_REGIONS array in the script to include/exclude specific regions.

Change inactivity period: Adjust the (60 * 86400) threshold in the script to a different number of days if needed.

Output Format

The CSV report includes the following fields:

UserName,ComputerName,OperatingSystemName,Region,ConnectionState,LastKnownUserConnectionTimestamp


