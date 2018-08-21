Readme

foreach($i in (Get-EC2Instance).Instances) { ($i.Tag | ? {$_.Key -eq "Name"} | select -expand Value) }

 Initialize-AWSDefaultConfiguration -ProfileName dev -Region us-east-1
 
  Get-Content 'C:\Users\ekendall\Desktop\Registry Files\regbackup.reg' | Select-String -Pattern HKEY
