## 预备
* 安装： https://github.com/PowerShell/PowerShell/releases
* docs： https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_environment_provider?view=powershell-6
## 创建/更新 环境变量
```
$env:e1="e1"
```
## 变量添加值
```
$env:path += ";c:\temp"
```
## 删除环境变量
```
del env:e1
```
## 环境变量生效
```
[environment]::SetEnvironmentvariable("Path", ";c:\powershellscript", "User")
[environment]::GetEnvironmentvariable("Path", "User")
```

# Environment provider
### Get-Location

### Set-Location
```
# 进入env drive
Set-Location Env:
# 返回到文件系统
Set-Location C:
```
### Get-Item
```
Get-Item -Path Env:
Get-ChildItem -Path Env:windir
$env:windir
```
### New_Item
```
New-Item -Path Env: -Name USERMODE -Value Non-Admin
Set-Item -Path Env:USERROLE -Value Administrator
Copy-Item -Path Env:USERROLE -Destination Env:USERROLE2
```
### Remove-Item
```
Remove-Item -Path Env:USERROLE2
```
### Clear-Item
```
Clear-Item -Path Env:USERROLE
```
### Getting help
