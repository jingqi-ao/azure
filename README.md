# azure

# Install Azure module

https://docs.microsoft.com/en-us/powershell/azure/install-azurerm-ps?view=azurermps-3.7.0

If exception "Import-Module : File C:\Program Files\WindowsPowerShell\Modules\AzureRM\3.8.0\AzureRM.psm1 cannot be loaded because running scripts is disabled on this system. " happens:

```
PS > Set-ExecutionPolicy RemoteSigned
```

# Create a security principal
Follow: https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions

# Login using security principal
```
PS >  Login-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid

```