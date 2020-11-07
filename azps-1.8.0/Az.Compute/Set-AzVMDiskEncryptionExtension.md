---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: da50845ff5012d466eed0c68103cdbd0baea4e7f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901118"
---
# <span data-ttu-id="93327-101">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="93327-101">Set-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="93327-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="93327-102">SYNOPSIS</span></span>
<span data-ttu-id="93327-103">Включает шифрование на работающей виртуальной машине IaaS в Azure.</span><span class="sxs-lookup"><span data-stu-id="93327-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

## <span data-ttu-id="93327-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="93327-104">SYNTAX</span></span>

### <span data-ttu-id="93327-105">SinglePassParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="93327-105">SinglePassParameterSet (Default)</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>] [[-VolumeType] <String>]
 [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>] [[-Passphrase] <String>]
 [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93327-106">AADClientSecretParameterSet</span><span class="sxs-lookup"><span data-stu-id="93327-106">AADClientSecretParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93327-107">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="93327-107">AADClientCertParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93327-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="93327-108">DESCRIPTION</span></span>
<span data-ttu-id="93327-109">Командлет **Set-AzVMDiskEncryptionExtension** позволяет выполнять шифрование на работающей инфраструктуре в качестве виртуальной машины службы (IaaS) в Azure.</span><span class="sxs-lookup"><span data-stu-id="93327-109">The **Set-AzVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>
<span data-ttu-id="93327-110">Этот командлет включает шифрование, устанавливая расширение шифрования диска на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="93327-110">This cmdlet enables encryption by installing the disk encryption extension on the virtual machine.</span></span>
<span data-ttu-id="93327-111">Если параметр *Name* не указан, устанавливается расширение с именем по умолчанию AzureDiskEncryption для виртуальных машин, работающих под управлением операционной системы Windows или AzureDiskEncryptionForLinux для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="93327-111">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>
<span data-ttu-id="93327-112">Этот командлет требует подтверждения от пользователей. чтобы включить шифрование, требуется перезапуск виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="93327-112">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>
<span data-ttu-id="93327-113">Перед запуском этого командлета рекомендуется сохранить работу на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="93327-113">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

## <span data-ttu-id="93327-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="93327-114">EXAMPLES</span></span>

### <span data-ttu-id="93327-115">Пример 1: Включение шифрования</span><span class="sxs-lookup"><span data-stu-id="93327-115">Example 1: Enable encryption</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="93327-116">В этом примере показано, как включить шифрование без указания учетных данных рекламы.</span><span class="sxs-lookup"><span data-stu-id="93327-116">This example demonstrates enabling encryption without specifying AD credentials.</span></span>   

### <span data-ttu-id="93327-117">Пример 2: Включение шифрования с помощью конвейерного ввода</span><span class="sxs-lookup"><span data-stu-id="93327-117">Example 2: Enable encryption with pipelined input</span></span>
```
$params = New-Object PSObject -Property @{
    ResourceGroupName = "[resource-group-name]"
    VMName = "[vm-name]"
    DiskEncryptionKeyVaultId = "/subscriptions/[subscription-id-guid]/resourceGroups/[resource-group-name]/providers/Microsoft.KeyVault/vaults/[keyvault-name]"
    DiskEncryptionKeyVaultUrl = "https://[keyvault-name].vault.azure.net"
    KeyEncryptionKeyVaultId = "/subscriptions/[subscription-id-guid]/resourceGroups/[resource-group-name]/providers/Microsoft.KeyVault/vaults/[keyvault-name]"
    KeyEncryptionKeyUrl = "https://[keyvault-name].vault.azure.net/keys/[kekname]/[kek-unique-id]"
    VolumeType = "All"
}

$params | Set-AzVmDiskEncryptionExtension
```

<span data-ttu-id="93327-118">В этом примере показано, как отправить параметры с помощью конвейера ввода, чтобы включить шифрование без указания учетных данных Active Directory.</span><span class="sxs-lookup"><span data-stu-id="93327-118">This example demonstrates sending parameters using pipelined input to enable encryption without specifying AD credentials.</span></span>  

### <span data-ttu-id="93327-119">Пример 3: Включите шифрование с помощью идентификатора клиента Azure AD и секретного клиента</span><span class="sxs-lookup"><span data-stu-id="93327-119">Example 3: Enable encryption using Azure AD Client ID and Client Secret</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="93327-120">В этом примере включается шифрование с помощью идентификатора клиента Azure AD и секрета клиента.</span><span class="sxs-lookup"><span data-stu-id="93327-120">This example enables encryption using Azure AD client ID, and client secret.</span></span>

### <span data-ttu-id="93327-121">Пример 4: Включение шифрования с помощью идентификатора клиента Azure AD и отпечатка сертификата клиента</span><span class="sxs-lookup"><span data-stu-id="93327-121">Example 4: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$CertValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -CertValue $CertValue 
$ServicePrincipal = New-AzADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

$AADClientID = $AzureAdApplication.ApplicationId
$aadClientCertThumbprint= $cert.Thumbprint

#Upload pfx to KeyVault 
$KeyVaultSecretName = "MyAADCert"
$FileContentBytes = get-content $CertPath -Encoding Byte
$FileContentEncoded = [System.Convert]::ToBase64String($fileContentBytes)
$JSONObject = @"
    { 
        "data" : "$filecontentencoded", 
        "dataType" : "pfx", 
        "password" : "$CertPassword" 
    } 
"@
$JSONObjectBytes = [System.Text.Encoding]::UTF8.GetBytes($jsonObject)
$JSONEncoded = [System.Convert]::ToBase64String($jsonObjectBytes)

$Secret = ConvertTo-SecureString -String $JSONEncoded -AsPlainText -Force
Set-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName -SecretValue $Secret
Set-AzKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl
Update-AzVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="93327-122">В этом примере включается шифрование с помощью идентификатора клиента Azure Active Directory и отпечатков сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="93327-122">This example enables encryption using Azure AD client ID and client certification thumbprints.</span></span>

### <span data-ttu-id="93327-123">Пример 5: Включите шифрование с помощью идентификатора клиента Azure AD, секрета клиента и ключа шифрования диска с помощью ключа шифрования ключа.</span><span class="sxs-lookup"><span data-stu-id="93327-123">Example 5: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"

$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"

$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="93327-124">В этом примере включается шифрование с помощью идентификатора клиента Azure Active Directory, секрета клиента и ключа шифрования диска с помощью ключа шифрования ключа.</span><span class="sxs-lookup"><span data-stu-id="93327-124">This example enables encryption using Azure AD client ID, client secret, and wrap disk encryption key by using the key encryption key.</span></span>

### <span data-ttu-id="93327-125">Пример 6. Включите шифрование с помощью идентификатора клиента Azure Active Directory, отпечатка сертификата клиента и обтекания диска EncryptionKey с помощью ключа шифрования ключей.</span><span class="sxs-lookup"><span data-stu-id="93327-125">Example 6: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$CertValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -CertValue $CertValue
$ServicePrincipal = New-AzADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

$AADClientID = $AzureAdApplication.ApplicationId
$AADClientCertThumbprint= $Cert.Thumbprint

#Upload pfx to KeyVault 
$KeyVaultSecretName = "MyAADCert"
$FileContentBytes = get-content $CertPath -Encoding Byte
$FileContentEncoded = [System.Convert]::ToBase64String($FileContentBytes)
$JSONObject = @"
    { 
        "data" : "$filecontentencoded", 
        "dataType" : "pfx", 
        "password" : "$CertPassword" 
    } 
"@
$JSONObjectBytes = [System.Text.Encoding]::UTF8.GetBytes($JSONObject)
$JsonEncoded = [System.Convert]::ToBase64String($JSONObjectBytes)
$Secret = ConvertTo-SecureString -String $JSONEncoded -AsPlainText -Force
Set-AzKeyVaultSecret -VaultName $VaultName-Name $KeyVaultSecretName -SecretValue $Secret
Set-AzKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl 
Update-AzVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGname -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="93327-126">В этом примере включается шифрование с помощью идентификатора клиента Azure Active Directory, отпечатка сертификата клиента и перенос ключа шифрования диска с помощью ключа шифрования ключа.</span><span class="sxs-lookup"><span data-stu-id="93327-126">This example enables encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryption key by using key encryption key.</span></span>

## <span data-ttu-id="93327-127">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="93327-127">PARAMETERS</span></span>

### <span data-ttu-id="93327-128">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="93327-128">-AadClientCertThumbprint</span></span>
<span data-ttu-id="93327-129">Указывает отпечаток сертификата клиента приложения AzureActive Directory (Azure AD) с разрешениями на запись секретных данных в **KeyVault**.</span><span class="sxs-lookup"><span data-stu-id="93327-129">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="93327-130">В качестве предварительной компоненты сертификат клиента Azure AD необходимо предварительно развернуть в хранилище сертификатов локального компьютера виртуальной машины `my` .</span><span class="sxs-lookup"><span data-stu-id="93327-130">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="93327-131">Для развертывания сертификата на виртуальной машине в Azure можно использовать командлет Add-AzVMSecret.</span><span class="sxs-lookup"><span data-stu-id="93327-131">The Add-AzVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="93327-132">Дополнительные сведения можно найти в справке по командлетам **Add-AzVMSecret** .</span><span class="sxs-lookup"><span data-stu-id="93327-132">For more details, see the **Add-AzVMSecret** cmdlet help.</span></span>
<span data-ttu-id="93327-133">Сертификат необходимо предварительно развернуть в хранилище сертификатов локального компьютера виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="93327-133">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientCertParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93327-134">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="93327-134">-AadClientID</span></span>
<span data-ttu-id="93327-135">Указывает идентификатор клиента приложения Azure AD, у которого есть разрешения на запись секретных данных в **KeyVault**.</span><span class="sxs-lookup"><span data-stu-id="93327-135">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientSecretParameterSet, AADClientCertParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93327-136">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="93327-136">-AadClientSecret</span></span>
<span data-ttu-id="93327-137">Указывает секретный ключ клиента для приложения Azure AD, который имеет разрешения на запись секретных данных в **KeyVault**.</span><span class="sxs-lookup"><span data-stu-id="93327-137">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: System.String
Parameter Sets: AADClientSecretParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93327-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93327-138">-DefaultProfile</span></span>
<span data-ttu-id="93327-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="93327-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93327-140">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="93327-140">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="93327-141">Указывает, что этот командлет отключает автоматическое обновление дополнительной версии расширения.</span><span class="sxs-lookup"><span data-stu-id="93327-141">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93327-142">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="93327-142">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="93327-143">Указывает идентификатор ресурса **KeyVault** , на который нужно отправить ключи шифрования виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="93327-143">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93327-144">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="93327-144">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="93327-145">Указывает URL-адрес **KeyVault** , на который нужно отправить ключи шифрования виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="93327-145">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93327-146">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="93327-146">-EncryptFormatAll</span></span>
<span data-ttu-id="93327-147">Encrypt-Format все диски с данными, которые еще не были зашифрованы</span><span class="sxs-lookup"><span data-stu-id="93327-147">Encrypt-Format all data drives that are not already encrypted</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93327-148">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="93327-148">-ExtensionPublisherName</span></span>
<span data-ttu-id="93327-149">Имя издателя расширения.</span><span class="sxs-lookup"><span data-stu-id="93327-149">The extension publisher name.</span></span> <span data-ttu-id="93327-150">Указывайте этот параметр только для переопределения значения по умолчанию Microsoft. Azure. Security.</span><span class="sxs-lookup"><span data-stu-id="93327-150">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93327-151">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="93327-151">-ExtensionType</span></span>
<span data-ttu-id="93327-152">Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="93327-152">The extension type.</span></span> <span data-ttu-id="93327-153">Укажите этот параметр для переопределения значения по умолчанию "AzureDiskEncryption" для виртуальных машин и "AzureDiskEncryptionForLinux" для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="93327-153">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93327-154">-Force</span><span class="sxs-lookup"><span data-stu-id="93327-154">-Force</span></span>
<span data-ttu-id="93327-155">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="93327-155">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93327-156">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="93327-156">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="93327-157">Указывает алгоритм, который используется для переноса ключа шифрования ключа виртуальной машины и его депереноса.</span><span class="sxs-lookup"><span data-stu-id="93327-157">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="93327-158">Значением по умолчанию является RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="93327-158">The default value is RSA-OAEP.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93327-159">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="93327-159">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="93327-160">Задает URL-адрес ключа шифрования для ключа, который используется для переноса ключа шифрования виртуальной машины и его депереноса.</span><span class="sxs-lookup"><span data-stu-id="93327-160">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="93327-161">Это должен быть полный URL-адрес версии.</span><span class="sxs-lookup"><span data-stu-id="93327-161">This must be the full versioned URL.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93327-162">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="93327-162">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="93327-163">Указывает идентификатор ресурса **KeyVault** , содержащего ключ шифрования ключа, который используется для переноса ключа шифрования виртуальной машины и его декодирования.</span><span class="sxs-lookup"><span data-stu-id="93327-163">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="93327-164">Это должен быть полный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="93327-164">This must be a full versioned URL.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93327-165">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="93327-165">-Name</span></span>
<span data-ttu-id="93327-166">Указывает имя ресурса диспетчера ресурсов Azure, представляющего расширение.</span><span class="sxs-lookup"><span data-stu-id="93327-166">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="93327-167">Значение по умолчанию — AzureDiskEncryption для виртуальных машин, работающих под управлением операционной системы Windows или AzureDiskEncryptionForLinux для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="93327-167">The default value is AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93327-168">-Парольную фразу</span><span class="sxs-lookup"><span data-stu-id="93327-168">-Passphrase</span></span>
<span data-ttu-id="93327-169">Указывает парольную фразу, используемую для шифрования виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="93327-169">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="93327-170">Этот параметр не используется для виртуальных машин, работающих под управлением операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="93327-170">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93327-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93327-171">-ResourceGroupName</span></span>
<span data-ttu-id="93327-172">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="93327-172">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93327-173">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="93327-173">-SequenceVersion</span></span>
<span data-ttu-id="93327-174">Указывает порядковый номер операций шифрования для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="93327-174">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="93327-175">Это значение уникально для каждой операции шифрования, выполняемой на той же виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="93327-175">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="93327-176">Для получения предыдущего использованного порядкового номера можно использовать командлет Get-AzVMExtension.</span><span class="sxs-lookup"><span data-stu-id="93327-176">The Get-AzVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93327-177">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="93327-177">-SkipVmBackup</span></span>
<span data-ttu-id="93327-178">Пропуск создания резервной копии для виртуальных машин Linux</span><span class="sxs-lookup"><span data-stu-id="93327-178">Skip backup creation for Linux VMs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93327-179">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="93327-179">-TypeHandlerVersion</span></span>
<span data-ttu-id="93327-180">Задает версию расширения шифрования.</span><span class="sxs-lookup"><span data-stu-id="93327-180">Specifies the version of the encryption extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93327-181">-VMName</span><span class="sxs-lookup"><span data-stu-id="93327-181">-VMName</span></span>
<span data-ttu-id="93327-182">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="93327-182">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93327-183">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="93327-183">-VolumeType</span></span>
<span data-ttu-id="93327-184">Указывает тип томов виртуальной машины для выполнения операции шифрования.</span><span class="sxs-lookup"><span data-stu-id="93327-184">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="93327-185">Допустимые значения виртуальных машин, работающих под управлением операционной системы Windows, описаны ниже. все, ОС и данные.</span><span class="sxs-lookup"><span data-stu-id="93327-185">Allowed values for virtual machines that run the Windows operating system are as follows: All, OS, and Data.</span></span>
<span data-ttu-id="93327-186">Допустимые значения для виртуальных машин Linux описаны ниже: только данные.</span><span class="sxs-lookup"><span data-stu-id="93327-186">The allowed values for Linux virtual machines are as follows: Data only.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93327-187">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93327-187">-Confirm</span></span>
<span data-ttu-id="93327-188">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="93327-188">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93327-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93327-189">-WhatIf</span></span>
<span data-ttu-id="93327-190">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="93327-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93327-191">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="93327-191">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93327-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93327-192">CommonParameters</span></span>
<span data-ttu-id="93327-193">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="93327-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93327-194">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93327-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93327-195">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="93327-195">INPUTS</span></span>

### <span data-ttu-id="93327-196">System. String</span><span class="sxs-lookup"><span data-stu-id="93327-196">System.String</span></span>

### <span data-ttu-id="93327-197">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="93327-197">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="93327-198">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="93327-198">OUTPUTS</span></span>

### <span data-ttu-id="93327-199">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="93327-199">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="93327-200">Пуск</span><span class="sxs-lookup"><span data-stu-id="93327-200">NOTES</span></span>

## <span data-ttu-id="93327-201">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="93327-201">RELATED LINKS</span></span>

[<span data-ttu-id="93327-202">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="93327-202">Add-AzVMSecret</span></span>](./Add-AzVMSecret.md)

[<span data-ttu-id="93327-203">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="93327-203">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="93327-204">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="93327-204">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)


