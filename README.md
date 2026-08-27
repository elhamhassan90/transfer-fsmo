# transfer-fsmo

##on PDC
```
Get-ADDomainController -Filter * | Select-Object Name,HostName,Site,IPv4Address
```

```
Move-ADDirectoryServerOperationMasterRole -Identity "ADC" -OperationMasterRole 0,1,2,3,4

netdom query fsmo
```
<img width="1456" height="915" alt="image" src="https://github.com/user-attachments/assets/bc19f379-7af6-4b18-98ed-3632decb6a63" />
<img width="1458" height="921" alt="image" src="https://github.com/user-attachments/assets/7456b103-a22f-45d2-a8e4-ca3458726809" />



##on PDC demotion
```
repadmin /replsummary
Uninstall-ADDSDomainController
```

<img width="1377" height="925" alt="image" src="https://github.com/user-attachments/assets/c593663e-ce87-4c9c-978a-59080b7a9c8c" />
