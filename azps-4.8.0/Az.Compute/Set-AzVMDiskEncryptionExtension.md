---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 1c69d79e148eae92307855ecfe308f5208a2f455
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94080011"
---
# <span data-ttu-id="8dbe7-101">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="8dbe7-101">Set-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="8dbe7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8dbe7-102">SYNOPSIS</span></span>
<span data-ttu-id="8dbe7-103">Включает шифрование на работающей виртуальной машине IaaS в Azure.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

## <span data-ttu-id="8dbe7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8dbe7-104">SYNTAX</span></span>

### <span data-ttu-id="8dbe7-105">SinglePassParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8dbe7-105">SinglePassParameterSet (Default)</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>] [[-VolumeType] <String>]
 [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>] [[-Passphrase] <String>]
 [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dbe7-106">AADClientSecretParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dbe7-106">AADClientSecretParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dbe7-107">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dbe7-107">AADClientCertParameterSet</span></span>
```
Set-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dbe7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dbe7-108">DESCRIPTION</span></span>
<span data-ttu-id="8dbe7-109">Командлет **Set-AzVMDiskEncryptionExtension** позволяет выполнять шифрование на работающей инфраструктуре в качестве виртуальной машины службы (IaaS) в Azure.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-109">The **Set-AzVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>  <span data-ttu-id="8dbe7-110">Это обеспечивает шифрование, устанавливая расширение шифрования диска на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-110">It enables encryption by installing the disk encryption extension on the virtual machine.</span></span> 

<span data-ttu-id="8dbe7-111">Этот командлет требует подтверждения от пользователей. чтобы включить шифрование, требуется перезапуск виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-111">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>

<span data-ttu-id="8dbe7-112">Перед запуском этого командлета рекомендуется сохранить работу на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-112">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

<span data-ttu-id="8dbe7-113">Linux: параметр **VolumeType** требуется при шифровании виртуальных машин Linux, для которого необходимо установить значение ("OS", "Data" или "ALL"), которое поддерживается дистрибутивом Linux.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-113">Linux: The **VolumeType** parameter is required when encrypting Linux virtual machines, and must be set to a value ("Os", "Data", or "All") supported by the Linux distribution.</span></span> 

<span data-ttu-id="8dbe7-114">Windows: параметр **VolumeType** можно опустить, в противном случае операция по умолчанию имеет значение ALL; Если параметр VolumeType присутствует для виртуальной машины Windows, для него должно быть задано значение ALL или OS.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-114">Windows: The **VolumeType** parameter may be omitted, in which case the operation defaults to All; if the VolumeType parameter is present for a Windows virtual machine, it must be set to either All or OS.</span></span>

## <span data-ttu-id="8dbe7-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8dbe7-115">EXAMPLES</span></span>

### <span data-ttu-id="8dbe7-116">Пример 1: Включение шифрования</span><span class="sxs-lookup"><span data-stu-id="8dbe7-116">Example 1: Enable encryption</span></span>
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

<span data-ttu-id="8dbe7-117">В этом примере включается шифрование на виртуальной машине без указания учетных данных Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-117">This example enables encryption on a VM without specifying AD credentials.</span></span>

### <span data-ttu-id="8dbe7-118">Пример 2: Включение шифрования с помощью конвейерного ввода</span><span class="sxs-lookup"><span data-stu-id="8dbe7-118">Example 2: Enable encryption with pipelined input</span></span>
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

<span data-ttu-id="8dbe7-119">Этот пример отправляет параметры с помощью конвейера ввода для включения шифрования на виртуальной машине без указания учетных данных Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-119">This example sends parameters using pipelined input to enable encryption on a VM, without specifying AD credentials.</span></span>

### <span data-ttu-id="8dbe7-120">Пример 3: Включите шифрование с помощью идентификатора клиента Azure AD и секретного клиента</span><span class="sxs-lookup"><span data-stu-id="8dbe7-120">Example 3: Enable encryption using Azure AD Client ID and Client Secret</span></span>
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

<span data-ttu-id="8dbe7-121">В этом примере идентификатор клиента Azure AD и секрет клиента используются для включения шифрования на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-121">This example uses Azure AD client ID and client secret to enable encryption on a VM.</span></span>

### <span data-ttu-id="8dbe7-122">Пример 4: Включение шифрования с помощью идентификатора клиента Azure AD и отпечатка сертификата клиента</span><span class="sxs-lookup"><span data-stu-id="8dbe7-122">Example 4: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
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

<span data-ttu-id="8dbe7-123">В этом примере для включения шифрования на виртуальной машине используется идентификатор клиента Azure AD и отпечатки сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-123">This example uses Azure AD client ID and client certification thumbprints to enable encryption on a VM.</span></span>

### <span data-ttu-id="8dbe7-124">Пример 5: Включите шифрование с помощью идентификатора клиента Azure AD, секрета клиента и ключа шифрования диска с помощью ключа шифрования ключа.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-124">Example 5: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
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

<span data-ttu-id="8dbe7-125">В этом примере идентификатор клиента Azure AD и секрет клиента используются для включения шифрования на виртуальной машине и переноса ключа шифрования диска с помощью ключа шифрования ключа.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-125">This example uses Azure AD client ID and client secret to enable encryption on a VM, and wraps the disk encryption key using a key encryption key.</span></span>

### <span data-ttu-id="8dbe7-126">Пример 6. Включите шифрование с помощью идентификатора клиента Azure Active Directory, отпечатка сертификата клиента и обтекания диска EncryptionKey с помощью ключа шифрования ключей.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-126">Example 6: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
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

<span data-ttu-id="8dbe7-127">В этом примере используется идентификатор клиента Azure AD и отпечаток сертификата клиента, чтобы включить шифрование на виртуальной машине, а также переключить ключ шифрования диска с помощью ключа шифрования ключа.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-127">This example uses Azure AD client ID and client cert thumbprint to enable encryption on a VM, and wraps the disk encryption key using a key encryption key.</span></span>

## <span data-ttu-id="8dbe7-128">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8dbe7-128">PARAMETERS</span></span>

### <span data-ttu-id="8dbe7-129">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="8dbe7-129">-AadClientCertThumbprint</span></span>
<span data-ttu-id="8dbe7-130">Указывает отпечаток сертификата клиента приложения AzureActive Directory (Azure AD) с разрешениями на запись секретных данных в **KeyVault**.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-130">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="8dbe7-131">В качестве предварительной компоненты сертификат клиента Azure AD необходимо предварительно развернуть в хранилище сертификатов локального компьютера виртуальной машины `my` .</span><span class="sxs-lookup"><span data-stu-id="8dbe7-131">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="8dbe7-132">Для развертывания сертификата на виртуальной машине в Azure можно использовать командлет Add-AzVMSecret.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-132">The Add-AzVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="8dbe7-133">Дополнительные сведения можно найти в справке по командлетам **Add-AzVMSecret** .</span><span class="sxs-lookup"><span data-stu-id="8dbe7-133">For more details, see the **Add-AzVMSecret** cmdlet help.</span></span>
<span data-ttu-id="8dbe7-134">Сертификат необходимо предварительно развернуть в хранилище сертификатов локального компьютера виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-134">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

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

### <span data-ttu-id="8dbe7-135">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="8dbe7-135">-AadClientID</span></span>
<span data-ttu-id="8dbe7-136">Указывает идентификатор клиента приложения Azure AD, у которого есть разрешения на запись секретных данных в **KeyVault**.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-136">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

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

### <span data-ttu-id="8dbe7-137">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="8dbe7-137">-AadClientSecret</span></span>
<span data-ttu-id="8dbe7-138">Указывает секретный ключ клиента для приложения Azure AD, который имеет разрешения на запись секретных данных в **KeyVault**.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-138">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

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

### <span data-ttu-id="8dbe7-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dbe7-139">-DefaultProfile</span></span>
<span data-ttu-id="8dbe7-140">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dbe7-141">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="8dbe7-141">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="8dbe7-142">Указывает, что этот командлет отключает автоматическое обновление дополнительной версии расширения.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-142">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="8dbe7-143">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="8dbe7-143">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="8dbe7-144">Указывает идентификатор ресурса **KeyVault** , на который нужно отправить ключи шифрования виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-144">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="8dbe7-145">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="8dbe7-145">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="8dbe7-146">Указывает URL-адрес **KeyVault** , на который нужно отправить ключи шифрования виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-146">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="8dbe7-147">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="8dbe7-147">-EncryptFormatAll</span></span>
<span data-ttu-id="8dbe7-148">Encrypt-Format все диски с данными, которые еще не были зашифрованы</span><span class="sxs-lookup"><span data-stu-id="8dbe7-148">Encrypt-Format all data drives that are not already encrypted</span></span>

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

### <span data-ttu-id="8dbe7-149">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="8dbe7-149">-ExtensionPublisherName</span></span>
<span data-ttu-id="8dbe7-150">Имя издателя расширения.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-150">The extension publisher name.</span></span> <span data-ttu-id="8dbe7-151">Указывайте этот параметр только для переопределения значения по умолчанию Microsoft. Azure. Security.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-151">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="8dbe7-152">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="8dbe7-152">-ExtensionType</span></span>
<span data-ttu-id="8dbe7-153">Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-153">The extension type.</span></span> <span data-ttu-id="8dbe7-154">Укажите этот параметр для переопределения значения по умолчанию "AzureDiskEncryption" для виртуальных машин и "AzureDiskEncryptionForLinux" для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-154">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="8dbe7-155">-Force</span><span class="sxs-lookup"><span data-stu-id="8dbe7-155">-Force</span></span>
<span data-ttu-id="8dbe7-156">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-156">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8dbe7-157">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="8dbe7-157">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="8dbe7-158">Указывает алгоритм, который используется для переноса ключа шифрования ключа виртуальной машины и его депереноса.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-158">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="8dbe7-159">Значением по умолчанию является RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-159">The default value is RSA-OAEP.</span></span>

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

### <span data-ttu-id="8dbe7-160">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="8dbe7-160">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="8dbe7-161">Задает URL-адрес ключа шифрования для ключа, который используется для переноса ключа шифрования виртуальной машины и его депереноса.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-161">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="8dbe7-162">Это должен быть полный URL-адрес версии.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-162">This must be the full versioned URL.</span></span>

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

### <span data-ttu-id="8dbe7-163">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="8dbe7-163">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="8dbe7-164">Указывает идентификатор ресурса **KeyVault** , содержащего ключ шифрования ключа, который используется для переноса ключа шифрования виртуальной машины и его декодирования.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-164">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="8dbe7-165">Это должен быть полный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-165">This must be a full versioned URL.</span></span>

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

### <span data-ttu-id="8dbe7-166">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8dbe7-166">-Name</span></span>
<span data-ttu-id="8dbe7-167">Указывает имя ресурса диспетчера ресурсов Azure, представляющего расширение.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-167">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span> <span data-ttu-id="8dbe7-168">Если параметр *Name* не указан, установленное расширение будет называться AzureDiskEncryption на виртуальных машинах Windows и AzureDiskEncryptionForLinux на виртуальных машинах Linux.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-168">If the *Name* parameter is omitted, the installed extension will be named AzureDiskEncryption on Windows virtual machines and AzureDiskEncryptionForLinux on Linux virtual machines.</span></span>


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

### <span data-ttu-id="8dbe7-169">-Парольную фразу</span><span class="sxs-lookup"><span data-stu-id="8dbe7-169">-Passphrase</span></span>
<span data-ttu-id="8dbe7-170">Указывает парольную фразу, используемую для шифрования виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-170">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="8dbe7-171">Этот параметр не используется для виртуальных машин, работающих под управлением операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-171">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

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

### <span data-ttu-id="8dbe7-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dbe7-172">-ResourceGroupName</span></span>
<span data-ttu-id="8dbe7-173">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-173">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="8dbe7-174">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="8dbe7-174">-SequenceVersion</span></span>
<span data-ttu-id="8dbe7-175">Указывает порядковый номер операций шифрования для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-175">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="8dbe7-176">Это значение уникально для каждой операции шифрования, выполняемой на той же виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-176">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="8dbe7-177">Для получения предыдущего использованного порядкового номера можно использовать командлет Get-AzVMExtension.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-177">The Get-AzVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

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

### <span data-ttu-id="8dbe7-178">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="8dbe7-178">-SkipVmBackup</span></span>
<span data-ttu-id="8dbe7-179">Пропуск создания резервной копии для виртуальных машин Linux</span><span class="sxs-lookup"><span data-stu-id="8dbe7-179">Skip backup creation for Linux VMs</span></span>

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

### <span data-ttu-id="8dbe7-180">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="8dbe7-180">-TypeHandlerVersion</span></span>
<span data-ttu-id="8dbe7-181">Задает версию расширения шифрования.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-181">Specifies the version of the encryption extension.</span></span>

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

### <span data-ttu-id="8dbe7-182">-VMName</span><span class="sxs-lookup"><span data-stu-id="8dbe7-182">-VMName</span></span>
<span data-ttu-id="8dbe7-183">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-183">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="8dbe7-184">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="8dbe7-184">-VolumeType</span></span>
<span data-ttu-id="8dbe7-185">Указывает тип томов виртуальных машин, для которых требуется выполнить операцию шифрования: ОС, данные или все.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-185">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="8dbe7-186">Linux: параметр **VolumeType** требуется при шифровании виртуальных машин Linux, для которого необходимо установить значение ("OS", "Data" или "ALL"), которое поддерживается дистрибутивом Linux.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-186">Linux: The **VolumeType** parameter is required when encrypting Linux virtual machines, and must be set to a value ("Os", "Data", or "All") supported by the Linux distribution.</span></span> 

<span data-ttu-id="8dbe7-187">Windows: параметр **VolumeType** можно опустить, в противном случае операция по умолчанию имеет значение ALL; Если параметр VolumeType присутствует для виртуальной машины Windows, для него должно быть задано значение ALL или OS.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-187">Windows: The **VolumeType** parameter may be omitted, in which case the operation defaults to All; if the VolumeType parameter is present for a Windows virtual machine, it must be set to either All or OS.</span></span>

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

### <span data-ttu-id="8dbe7-188">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8dbe7-188">-Confirm</span></span>
<span data-ttu-id="8dbe7-189">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-189">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dbe7-190">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dbe7-190">-WhatIf</span></span>
<span data-ttu-id="8dbe7-191">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-191">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dbe7-192">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-192">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dbe7-193">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dbe7-193">CommonParameters</span></span>
<span data-ttu-id="8dbe7-194">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8dbe7-194">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dbe7-195">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8dbe7-195">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dbe7-196">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8dbe7-196">INPUTS</span></span>

### <span data-ttu-id="8dbe7-197">System. String</span><span class="sxs-lookup"><span data-stu-id="8dbe7-197">System.String</span></span>

### <span data-ttu-id="8dbe7-198">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8dbe7-198">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8dbe7-199">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dbe7-199">OUTPUTS</span></span>

### <span data-ttu-id="8dbe7-200">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8dbe7-200">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="8dbe7-201">Пуск</span><span class="sxs-lookup"><span data-stu-id="8dbe7-201">NOTES</span></span>

## <span data-ttu-id="8dbe7-202">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8dbe7-202">RELATED LINKS</span></span>

[<span data-ttu-id="8dbe7-203">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="8dbe7-203">Add-AzVMSecret</span></span>](./Add-AzVMSecret.md)

[<span data-ttu-id="8dbe7-204">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="8dbe7-204">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="8dbe7-205">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="8dbe7-205">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)


