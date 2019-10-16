#  CREATE CREDENTIALS
PowerShell Command Doc : Link



## REQUIRED
1. Windows PowerShell
2. Username
3. Password
4. Local Drive/Remote Drive (Save Location)

## WINDOWS – EXPLORER
- Create a blank .xml file named “prodcred.xml” in Windows Explorer – This will hold your encrypted credentials

- Locate the xml’s file location e.g.: 

> C:\Users\<user_Name>\<folder>\prodcred.xml – Example Location

## POWERSHELL COMMANDS
- Input the following into PowerShell.

`[string]$credpath = "C:\Users\<user_Name>\<folder>\prodcred.xml"`
`$export = Get-Credential`
`$export | Export-Clixml -Path $credpath`

[^] This generates a .xml document to be used in future functions stored in a .xml file