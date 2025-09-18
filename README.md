# AD Password Expiry Report

## Overview
A PowerShell script that generates a CSV report of all enabled Active Directory users along with their password expiry dates.  
This is useful for auditing, monitoring, and notifying users of upcoming password expirations.

## Features
- Retrieves all enabled AD users  
- Calculates password expiry date based on domain policy  
- Marks accounts with no password set as "Never Set"  
- Exports results into a CSV file  

## Usage
1. Open **PowerShell** as Administrator.  
2. Ensure the **Active Directory module** is installed.  
3. Update the `$OutputFile` variable to your desired export location.  
4. Run the script:
   ```powershell
   .\Password-Expiry-Report.ps1
