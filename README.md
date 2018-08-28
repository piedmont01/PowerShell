Readme

foreach($i in (Get-EC2Instance).Instances) { ($i.Tag | ? {$_.Key -eq "Name"} | select -expand Value) }

 Initialize-AWSDefaultConfiguration -ProfileName dev -Region us-east-1
 
  Get-Content 'C:\Users\ekendall\Desktop\Registry Files\regbackup.reg' | Select-String -Pattern HKEY
Get-ASAutoScalingGroup | Select-Object AutoScalingGroupName | Sort-Object -CaseSensitive	
Get-ACMCertificateList | Select-Object DomainName | Sort-Object -CaseSensitive	
Get-CFNStack | Select-Object StackName | Sort-Object -Property StackName	
Get-R53HostedZoneList | Select-Object Name | Sort-Object -CaseSensitive	
Get-DDBTableList | Sort-Object -CaseSensitive	
foreach($i in (Get-EC2Instance).Instances) { ($i.Tag | ? {$_.Key -eq "Name"} | select -expand Value), $i.InstanceType }	
Get-EFSFileSystem | Select-Object Name | Sort-Object -CaseSensitive	
Get-IAMUserList | Select-Object UserName | Sort-Object -CaseSensitive	
Get-LMFunctionList | Select-Object FunctionName,Runtime | Sort-Object Runtime	
Get-RDSDBInstance | Select-Object DBInstanceArn,DBInstanceClass,Engine,EngineVersion			
Get-S3Bucket | Select-Object BucketName | Sort-Object -CaseSensitive	
Get-SNSTopic | Sort-Object -CaseSensitive	
Get-EC2Vpc | Select-Object -Property VpcId | Sort-Object -CaseSensitive	
