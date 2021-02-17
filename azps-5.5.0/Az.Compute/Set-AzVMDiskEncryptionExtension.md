---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 1c69d79e148eae92307855ecfe308f5208a2f455
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238663"
---
# <span data-ttu-id="e10f1-101">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="e10f1-101">Set-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="e10f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e10f1-102">SYNOPSIS</span></span>
<span data-ttu-id="e10f1-103">Включает шифрование на запущенной виртуальной машине IaaS в Azure.</span><span class="sxs-lookup"><span data-stu-id="e10f1-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

## <span data-ttu-id="e10f1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e10f1-104">SYNTAX</span></span>

### <span data-ttu-id="e10f1-105">SinglePassParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e10f1-105">SinglePassParameterSet (Default)</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>] [[-VolumeType] <String>]
 [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>] [[-Passphrase] <String>]
 [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e10f1-106">AADClientSecretParameterSet</span><span class="sxs-lookup"><span data-stu-id="e10f1-106">AADClientSecretParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e10f1-107">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="e10f1-107">AADClientCertParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e10f1-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e10f1-108">DESCRIPTION</span></span>
<span data-ttu-id="e10f1-109">С **помощью cmdlet Set-AzVMDiskEncryptionExtension** можно шифровать запущенную инфраструктуру как виртуальную машину (IaaS) в Azure.</span><span class="sxs-lookup"><span data-stu-id="e10f1-109">The **Set-AzVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>  <span data-ttu-id="e10f1-110">Оно включает шифрование, устанавливая расширение шифрования диска на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="e10f1-110">It enables encryption by installing the disk encryption extension on the virtual machine.</span></span> 

<span data-ttu-id="e10f1-111">Для этого cmdlet требуется подтверждение от пользователей, так как для того чтобы включить шифрование, необходимо перезапустить виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="e10f1-111">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>

<span data-ttu-id="e10f1-112">Рекомендуется сохранить работу на виртуальной машине перед запуском этого cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e10f1-112">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

<span data-ttu-id="e10f1-113">Linux: параметр **VolumeType** является обязательным при шифровании виртуальных машин Linux и должен иметь значение ("Ос", "Данные" или "Все"), поддерживаемые дистрибутивом Linux.</span><span class="sxs-lookup"><span data-stu-id="e10f1-113">Linux: The **VolumeType** parameter is required when encrypting Linux virtual machines, and must be set to a value ("Os", "Data", or "All") supported by the Linux distribution.</span></span> 

<span data-ttu-id="e10f1-114">Windows: параметр **VolumeType** может быть опущен, в этом случае операция по умолчанию — all; если параметр VolumeType присутствует для виртуальной машины Windows, необходимо установить для него параметр All или OS.</span><span class="sxs-lookup"><span data-stu-id="e10f1-114">Windows: The **VolumeType** parameter may be omitted, in which case the operation defaults to All; if the VolumeType parameter is present for a Windows virtual machine, it must be set to either All or OS.</span></span>

## <span data-ttu-id="e10f1-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e10f1-115">EXAMPLES</span></span>

### <span data-ttu-id="e10f1-116">Пример 1. Включить шифрование</span><span class="sxs-lookup"><span data-stu-id="e10f1-116">Example 1: Enable encryption</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="e10f1-117">В этом примере включается шифрование в VM-технологию без указания учетных данных AD.</span><span class="sxs-lookup"><span data-stu-id="e10f1-117">This example enables encryption on a VM without specifying AD credentials.</span></span>

### <span data-ttu-id="e10f1-118">Пример 2. Включить шифрование с конвейерными входными данными</span><span class="sxs-lookup"><span data-stu-id="e10f1-118">Example 2: Enable encryption with pipelined input</span></span>
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

<span data-ttu-id="e10f1-119">В этом примере параметры отправляются с использованием конвейерной входной информации для шифрования в VM без указания учетных данных AD.</span><span class="sxs-lookup"><span data-stu-id="e10f1-119">This example sends parameters using pipelined input to enable encryption on a VM, without specifying AD credentials.</span></span>

### <span data-ttu-id="e10f1-120">Пример 3. Включить шифрование с помощью службы "Код клиента Azure AD" и "Секрет клиента"</span><span class="sxs-lookup"><span data-stu-id="e10f1-120">Example 3: Enable encryption using Azure AD Client ID and Client Secret</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="e10f1-121">В этом примере используются код клиента Azure AD и секрет клиента для шифрования в VM-клиенте.</span><span class="sxs-lookup"><span data-stu-id="e10f1-121">This example uses Azure AD client ID and client secret to enable encryption on a VM.</span></span>

### <span data-ttu-id="e10f1-122">Пример 4. Включить шифрование с помощью удостоверения клиента Azure AD и thumbprint сертификации клиента</span><span class="sxs-lookup"><span data-stu-id="e10f1-122">Example 4: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"

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
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="e10f1-123">В этом примере используются эскизы azure AD и сертификации клиента, чтобы включить шифрование на VM-накопителе.</span><span class="sxs-lookup"><span data-stu-id="e10f1-123">This example uses Azure AD client ID and client certification thumbprints to enable encryption on a VM.</span></span>

### <span data-ttu-id="e10f1-124">Пример 5. Включить шифрование с использованием ИД клиента Azure AD, секрета клиента и ключа шифрования диска с помощью ключа шифрования ключа</span><span class="sxs-lookup"><span data-stu-id="e10f1-124">Example 5: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"

$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"

$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "All"

$KEKName = "MyKeyEncryptionKey"
$KEK = Add-AzKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="e10f1-125">В этом примере используются код клиента Azure AD и секрет клиента, чтобы включить шифрование на VM-модели, и перенос ключа шифрования диска с помощью ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="e10f1-125">This example uses Azure AD client ID and client secret to enable encryption on a VM, and wraps the disk encryption key using a key encryption key.</span></span>

### <span data-ttu-id="e10f1-126">Пример 6. Включить шифрование с помощью ключа шифрования Azure AD, печати эскиза клиента cert и ключа шифрования диска</span><span class="sxs-lookup"><span data-stu-id="e10f1-126">Example 6: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
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
$VolumeType = "All"

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
Set-AzVMDiskEncryptionExtension -ResourceGroupName $RGname -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId -VolumeType $VolumeType
```

<span data-ttu-id="e10f1-127">В этом примере используются эскизы azure AD и cert для шифрования на VM-модели, а ключ шифрования диска переносим с помощью ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="e10f1-127">This example uses Azure AD client ID and client cert thumbprint to enable encryption on a VM, and wraps the disk encryption key using a key encryption key.</span></span>

## <span data-ttu-id="e10f1-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e10f1-128">PARAMETERS</span></span>

### <span data-ttu-id="e10f1-129">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="e10f1-129">-AadClientCertThumbprint</span></span>
<span data-ttu-id="e10f1-130">Определяет эскиз сертификата клиента приложения AzureActive Directory (Azure AD), который имеет разрешения на запись секретов **KeyVault.**</span><span class="sxs-lookup"><span data-stu-id="e10f1-130">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="e10f1-131">Для этого необходимо предварительно развернуть сертификат клиента Azure AD в локальном хранилище `my` сертификатов на локальном компьютере виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e10f1-131">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="e10f1-132">С Add-AzVMSecret можно использовать для развертывания сертификата на виртуальной машине в Azure.</span><span class="sxs-lookup"><span data-stu-id="e10f1-132">The Add-AzVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="e10f1-133">Дополнительные сведения см. в справке по **add-AzVMSecret.**</span><span class="sxs-lookup"><span data-stu-id="e10f1-133">For more details, see the **Add-AzVMSecret** cmdlet help.</span></span>
<span data-ttu-id="e10f1-134">Сертификат должен быть ранее развернут на локальном компьютере виртуальной машины, где хранится мой сертификат.</span><span class="sxs-lookup"><span data-stu-id="e10f1-134">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

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

### <span data-ttu-id="e10f1-135">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="e10f1-135">-AadClientID</span></span>
<span data-ttu-id="e10f1-136">Определяет ИД клиента приложения Azure AD, который имеет разрешения на запись секретов **keyVault.**</span><span class="sxs-lookup"><span data-stu-id="e10f1-136">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

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

### <span data-ttu-id="e10f1-137">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="e10f1-137">-AadClientSecret</span></span>
<span data-ttu-id="e10f1-138">Определяет секрет клиента приложения Azure AD, которое имеет разрешения на запись секретов **в KeyVault.**</span><span class="sxs-lookup"><span data-stu-id="e10f1-138">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

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

### <span data-ttu-id="e10f1-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e10f1-139">-DefaultProfile</span></span>
<span data-ttu-id="e10f1-140">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e10f1-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e10f1-141">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="e10f1-141">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="e10f1-142">Указывает на то, что этот cmdlet отключает автоматическое обновление незначительных версий расширения.</span><span class="sxs-lookup"><span data-stu-id="e10f1-142">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="e10f1-143">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="e10f1-143">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="e10f1-144">Определяет код ресурса **KeyVault,** на который должны быть загружены ключи шифрования виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e10f1-144">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="e10f1-145">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="e10f1-145">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="e10f1-146">Url-адрес **keyVault,** на который должны быть загружены ключи шифрования виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e10f1-146">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="e10f1-147">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="e10f1-147">-EncryptFormatAll</span></span>
<span data-ttu-id="e10f1-148">Encrypt-Format всех еще не зашифрованных дисков данных</span><span class="sxs-lookup"><span data-stu-id="e10f1-148">Encrypt-Format all data drives that are not already encrypted</span></span>

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

### <span data-ttu-id="e10f1-149">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="e10f1-149">-ExtensionPublisherName</span></span>
<span data-ttu-id="e10f1-150">Имя издателя расширения.</span><span class="sxs-lookup"><span data-stu-id="e10f1-150">The extension publisher name.</span></span> <span data-ttu-id="e10f1-151">Укажите этот параметр только для переопределения значения по умолчанию microsoft.Azure.Security.</span><span class="sxs-lookup"><span data-stu-id="e10f1-151">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="e10f1-152">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="e10f1-152">-ExtensionType</span></span>
<span data-ttu-id="e10f1-153">Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="e10f1-153">The extension type.</span></span> <span data-ttu-id="e10f1-154">Укажите этот параметр, чтобы переопречить стандартное значение AzureDiskEncryption для VMs Windows и AzureDiskEncryptionForLinux для VMs для Linux.</span><span class="sxs-lookup"><span data-stu-id="e10f1-154">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="e10f1-155">-Force</span><span class="sxs-lookup"><span data-stu-id="e10f1-155">-Force</span></span>
<span data-ttu-id="e10f1-156">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="e10f1-156">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e10f1-157">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="e10f1-157">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="e10f1-158">Алгоритм, используемый для переноса и размывания ключа шифрования ключа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e10f1-158">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="e10f1-159">Значение по умолчанию — RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="e10f1-159">The default value is RSA-OAEP.</span></span>

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

### <span data-ttu-id="e10f1-160">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="e10f1-160">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="e10f1-161">Указывает URL-адрес ключа шифрования ключа, который используется для переноса и размывания ключа шифрования виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e10f1-161">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="e10f1-162">Это должен быть полный URL-адрес с версией.</span><span class="sxs-lookup"><span data-stu-id="e10f1-162">This must be the full versioned URL.</span></span>

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

### <span data-ttu-id="e10f1-163">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="e10f1-163">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="e10f1-164">Определяет код ресурса **keyVault,** который содержит ключ шифрования ключа, который используется для переноса и разверки ключа шифрования виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e10f1-164">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="e10f1-165">Это должен быть полный URL-адрес с версией.</span><span class="sxs-lookup"><span data-stu-id="e10f1-165">This must be a full versioned URL.</span></span>

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

### <span data-ttu-id="e10f1-166">-Name</span><span class="sxs-lookup"><span data-stu-id="e10f1-166">-Name</span></span>
<span data-ttu-id="e10f1-167">Имя ресурса Диспетчера ресурсов Azure, представляюца расширение.</span><span class="sxs-lookup"><span data-stu-id="e10f1-167">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span> <span data-ttu-id="e10f1-168">Если  этот параметр опущен, установленное расширение будет называться AzureDiskEncryption на виртуальных машинах Windows и AzureDiskEncryptionForLinux на виртуальных машинах Linux.</span><span class="sxs-lookup"><span data-stu-id="e10f1-168">If the *Name* parameter is omitted, the installed extension will be named AzureDiskEncryption on Windows virtual machines and AzureDiskEncryptionForLinux on Linux virtual machines.</span></span>


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

### <span data-ttu-id="e10f1-169">-Passphrase</span><span class="sxs-lookup"><span data-stu-id="e10f1-169">-Passphrase</span></span>
<span data-ttu-id="e10f1-170">Указывает passphrase, используемый только для шифрования виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="e10f1-170">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="e10f1-171">Этот параметр не используется для виртуальных машин, работающих в операционной системе Windows.</span><span class="sxs-lookup"><span data-stu-id="e10f1-171">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

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

### <span data-ttu-id="e10f1-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e10f1-172">-ResourceGroupName</span></span>
<span data-ttu-id="e10f1-173">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e10f1-173">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="e10f1-174">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="e10f1-174">-SequenceVersion</span></span>
<span data-ttu-id="e10f1-175">Определяет последовательность операций шифрования для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e10f1-175">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="e10f1-176">Это уникально для каждой операции шифрования, выполняемой на одной виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="e10f1-176">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="e10f1-177">Этот Get-AzVMExtension можно использовать для получения номера предыдущей последовательности.</span><span class="sxs-lookup"><span data-stu-id="e10f1-177">The Get-AzVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

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

### <span data-ttu-id="e10f1-178">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="e10f1-178">-SkipVmBackup</span></span>
<span data-ttu-id="e10f1-179">Пропустить создание резервных копий для VMs для Linux</span><span class="sxs-lookup"><span data-stu-id="e10f1-179">Skip backup creation for Linux VMs</span></span>

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

### <span data-ttu-id="e10f1-180">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="e10f1-180">-TypeHandlerVersion</span></span>
<span data-ttu-id="e10f1-181">Указывает версию расширения шифрования.</span><span class="sxs-lookup"><span data-stu-id="e10f1-181">Specifies the version of the encryption extension.</span></span>

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

### <span data-ttu-id="e10f1-182">-VMName</span><span class="sxs-lookup"><span data-stu-id="e10f1-182">-VMName</span></span>
<span data-ttu-id="e10f1-183">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e10f1-183">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="e10f1-184">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="e10f1-184">-VolumeType</span></span>
<span data-ttu-id="e10f1-185">Определяет тип томов виртуальной машины, с которыми выполняется операция шифрования: ОС, Data или All.</span><span class="sxs-lookup"><span data-stu-id="e10f1-185">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="e10f1-186">Linux: параметр **VolumeType** является обязательным при шифровании виртуальных машин Linux и должен иметь значение ("Ос", "Данные" или "Все"), поддерживаемые дистрибутивом Linux.</span><span class="sxs-lookup"><span data-stu-id="e10f1-186">Linux: The **VolumeType** parameter is required when encrypting Linux virtual machines, and must be set to a value ("Os", "Data", or "All") supported by the Linux distribution.</span></span> 

<span data-ttu-id="e10f1-187">Windows: параметр **VolumeType** может быть опущен, в этом случае операция по умолчанию — all; если параметр VolumeType присутствует для виртуальной машины Windows, необходимо установить для него параметр All или OS.</span><span class="sxs-lookup"><span data-stu-id="e10f1-187">Windows: The **VolumeType** parameter may be omitted, in which case the operation defaults to All; if the VolumeType parameter is present for a Windows virtual machine, it must be set to either All or OS.</span></span>

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

### <span data-ttu-id="e10f1-188">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e10f1-188">-Confirm</span></span>
<span data-ttu-id="e10f1-189">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e10f1-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e10f1-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e10f1-190">-WhatIf</span></span>
<span data-ttu-id="e10f1-191">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e10f1-191">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e10f1-192">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e10f1-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e10f1-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e10f1-193">CommonParameters</span></span>
<span data-ttu-id="e10f1-194">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e10f1-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e10f1-195">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e10f1-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e10f1-196">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e10f1-196">INPUTS</span></span>

### <span data-ttu-id="e10f1-197">System.String</span><span class="sxs-lookup"><span data-stu-id="e10f1-197">System.String</span></span>

### <span data-ttu-id="e10f1-198">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e10f1-198">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e10f1-199">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e10f1-199">OUTPUTS</span></span>

### <span data-ttu-id="e10f1-200">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e10f1-200">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e10f1-201">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e10f1-201">NOTES</span></span>

## <span data-ttu-id="e10f1-202">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e10f1-202">RELATED LINKS</span></span>

[<span data-ttu-id="e10f1-203">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="e10f1-203">Add-AzVMSecret</span></span>](./Add-AzVMSecret.md)

[<span data-ttu-id="e10f1-204">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="e10f1-204">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="e10f1-205">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="e10f1-205">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)


