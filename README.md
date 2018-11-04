# PowerShell Commands
**Set Profile**
```Initialize-AWSDefaultConfiguration -ProfileName dev -Region us-east-1```
**List Name of EC2 Instances**
```foreach($i in (Get-EC2Instance).Instances) { ($i.Tag | ? {$_.Key -eq "Name"} | select -expand Value) }```
**List Name and Type of EC2 Instance**
```foreach($i in (Get-EC2Instance).Instances) { ($i.Tag | ? {$_.Key -eq "Name"} | select -expand Value), $i.InstanceType }```	
**List Hosts Defined in Putty**
```Get-Content 'C:\Users\ekendall\Desktop\Registry Files\regbackup.reg' | Select-String -Pattern HKEY```
**LIst Auto Scaling Groups**
```Get-ASAutoScalingGroup | Select-Object AutoScalingGroupName | Sort-Object -CaseSensitive```
**List Certificates**	
```Get-ACMCertificateList | Select-Object DomainName | Sort-Object -CaseSensitive```
**List Cloudformation Templates**	
```Get-CFNStack | Select-Object StackName | Sort-Object -Property StackName```
**List Domains**
```Get-R53HostedZoneList | Select-Object Name | Sort-Object -CaseSensitive```	
**List DynamoDB Tables**
```Get-DDBTableList | Sort-Object -CaseSensitive```	
**List EFS Filesystems**
```Get-EFSFileSystem | Select-Object Name | Sort-Object -CaseSensitive```	
**List IAM Users**
```Get-IAMUserList | Select-Object UserName | Sort-Object -CaseSensitive```	
**List Lambda Functions**
```Get-LMFunctionList | Select-Object FunctionName,Runtime | Sort-Object Runtime```	
**LIst Database Instances**
```Get-RDSDBInstance | Select-Object DBInstanceArn,DBInstanceClass,Engine,EngineVersion```		
**List S3 Buckets**	
```Get-S3Bucket | Select-Object BucketName | Sort-Object -CaseSensitive```
**List SNS Topics**	
```Get-SNSTopic | Sort-Object -CaseSensitive```	
**List VPC**
```Get-EC2Vpc | Select-Object -Property VpcId | Sort-Object -CaseSensitive```	