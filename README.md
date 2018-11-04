# PowerShell Commands
**Set Profile**</br>
```Initialize-AWSDefaultConfiguration -ProfileName dev -Region us-east-1```</br>
**List Name of EC2 Instances**</br>
```foreach($i in (Get-EC2Instance).Instances) { ($i.Tag | ? {$_.Key -eq "Name"} | select -expand Value) }```</br>
**List Name and Type of EC2 Instance**</br>
```foreach($i in (Get-EC2Instance).Instances) { ($i.Tag | ? {$_.Key -eq "Name"} | select -expand Value), $i.InstanceType }```</br>
**List Hosts Defined in Putty**</br>
```Get-Content 'C:\Users\ekendall\Desktop\Registry Files\regbackup.reg' | Select-String -Pattern HKEY```</br>
**LIst Auto Scaling Groups**</br>
```Get-ASAutoScalingGroup | Select-Object AutoScalingGroupName | Sort-Object -CaseSensitive```</br>
**List Certificates**</br>
```Get-ACMCertificateList | Select-Object DomainName | Sort-Object -CaseSensitive```</br>
**List Cloudformation Templates**</br>
```Get-CFNStack | Select-Object StackName | Sort-Object -Property StackName```</br>
**List Domains**</br>
```Get-R53HostedZoneList | Select-Object Name | Sort-Object -CaseSensitive```</br>
**List DynamoDB Tables**</br>
```Get-DDBTableList | Sort-Object -CaseSensitive```</br>
**List EFS Filesystems**</br>
```Get-EFSFileSystem | Select-Object Name | Sort-Object -CaseSensitive```</br>	
**List IAM Users**</br>
```Get-IAMUserList | Select-Object UserName | Sort-Object -CaseSensitive```</br>	
**List Lambda Functions**</br>
```Get-LMFunctionList | Select-Object FunctionName,Runtime | Sort-Object Runtime```</br>
**LIst Database Instances**</br>
```Get-RDSDBInstance | Select-Object DBInstanceArn,DBInstanceClass,Engine,EngineVersion```</br>
**List S3 Buckets**</br>
```Get-S3Bucket | Select-Object BucketName | Sort-Object -CaseSensitive```</br>
**List SNS Topics**</br>
```Get-SNSTopic | Sort-Object -CaseSensitive```</br>
**List VPC**</br>
```Get-EC2Vpc | Select-Object -Property VpcId | Sort-Object -CaseSensitive```</br>