Import-Module ActiveDirectory

# Get the current domain's password policy
$DomainPolicy = Get-ADDefaultDomainPasswordPolicy
$MaxPasswordAge = $DomainPolicy.MaxPasswordAge

# Get all enabled AD users
$Users = Get-ADUser -Filter {Enabled -eq $true} -Properties DisplayName, EmailAddress, PasswordLastSet

# Extract user details
$UserList = $Users | Select-Object @{Name='Username'; Expression={$_.SamAccountName}},
                                   @{Name='Display Name'; Expression={$_.DisplayName}},
                                   @{Name='Email'; Expression={$_.EmailAddress}},
                                   @{Name='Password Expiry Date'; Expression={
                                       if ($_.PasswordLastSet -ne $null) {
                                           $_.PasswordLastSet + $MaxPasswordAge
                                       } else {
                                           'Never Set'
                                       }
                                   }}

# Export the data to a CSV file
$OutputFile = "C:\Path\To\Export\PasswordExpiry.csv"
$UserList | Export-Csv -Path $OutputFile -NoTypeInformation -Encoding UTF8

Write-Host "Extraction complete. Data saved to: $OutputFile" -ForegroundColor Green
