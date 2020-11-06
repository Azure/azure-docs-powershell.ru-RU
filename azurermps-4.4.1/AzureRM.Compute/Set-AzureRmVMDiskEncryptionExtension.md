---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMDiskEncryptionExtension.md
ms.openlocfilehash: c10b55ae0d1243320171d898058947d4781a7de1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557807"
---
# <span data-ttu-id="723ac-101">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="723ac-101">Set-AzureRmVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="723ac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="723ac-102">SYNOPSIS</span></span>
<span data-ttu-id="723ac-103">Включает шифрование на работающей виртуальной машине IaaS в Azure.</span><span class="sxs-lookup"><span data-stu-id="723ac-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="723ac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="723ac-104">SYNTAX</span></span>

### <span data-ttu-id="723ac-105">Секретные параметры клиента AAD (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="723ac-105">AAD Client Secret Parameters (Default)</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="723ac-106">Параметры сертификата клиента AAD</span><span class="sxs-lookup"><span data-stu-id="723ac-106">AAD Client Cert Parameters</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="723ac-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="723ac-107">DESCRIPTION</span></span>
<span data-ttu-id="723ac-108">Командлет **Set-AzureRmVMDiskEncryptionExtension** позволяет выполнять шифрование на работающей инфраструктуре в качестве виртуальной машины службы (IaaS) в Azure.</span><span class="sxs-lookup"><span data-stu-id="723ac-108">The **Set-AzureRmVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>
<span data-ttu-id="723ac-109">Этот командлет включает шифрование, устанавливая расширение шифрования диска на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="723ac-109">This cmdlet enables encryption by installing the disk encryption extension on the virtual machine.</span></span>
<span data-ttu-id="723ac-110">Если параметр *Name* не указан, устанавливается расширение с именем по умолчанию AzureDiskEncryption для виртуальных машин, работающих под управлением операционной системы Windows или AzureDiskEncryptionForLinux для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="723ac-110">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>
<span data-ttu-id="723ac-111">Этот командлет требует подтверждения от пользователей. чтобы включить шифрование, требуется перезапуск виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="723ac-111">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>
<span data-ttu-id="723ac-112">Перед запуском этого командлета рекомендуется сохранить работу на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="723ac-112">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

## <span data-ttu-id="723ac-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="723ac-113">EXAMPLES</span></span>

### <span data-ttu-id="723ac-114">Пример 1: Включение шифрования с помощью идентификатора клиента Azure AD и секрета клиента</span><span class="sxs-lookup"><span data-stu-id="723ac-114">Example 1: Enable encryption using Azure AD Client ID and Client Secret</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="723ac-115">В этом примере включается шифрование с помощью идентификатора клиента Azure AD и секрета клиента.</span><span class="sxs-lookup"><span data-stu-id="723ac-115">This example enables encryption using Azure AD client ID, and client secret.</span></span>

### <span data-ttu-id="723ac-116">Пример 2: Включите шифрование с помощью идентификатора клиента Azure AD и отпечатка сертификата клиента</span><span class="sxs-lookup"><span data-stu-id="723ac-116">Example 2: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$KeyValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzureRmADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -KeyValue $KeyValue -KeyType AsymmetricX509Cert 
$ServicePrincipal = New-AzureRmADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

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
Set-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName -SecretValue $Secret
Set-AzureRmKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzureRmVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzureRmVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl
Update-AzureRmVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="723ac-117">В этом примере включается шифрование с помощью идентификатора клиента Azure Active Directory и отпечатков сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="723ac-117">This example enables encryption using Azure AD client ID and client certification thumbprints.</span></span>

### <span data-ttu-id="723ac-118">Пример 3: Включите шифрование с помощью идентификатора клиента Azure AD, секретного клиента и ключа шифрования диска с помощью ключа шифрования ключа.</span><span class="sxs-lookup"><span data-stu-id="723ac-118">Example 3: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"

$AADClientID = "<clientID of your Azure AD app>"
$AADClientSecret = "<clientSecret of your Azure AD app>"

$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

$KEK = Add-AzureKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGName -VMName $VMName -AadClientID $AADClientID -AadClientSecret $AADClientSecret -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl -KeyEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="723ac-119">В этом примере включается шифрование с помощью идентификатора клиента Azure Active Directory, секрета клиента и ключа шифрования диска с помощью ключа шифрования ключа.</span><span class="sxs-lookup"><span data-stu-id="723ac-119">This example enables encryption using Azure AD client ID, client secret, and wrap disk encryption key by using the key encryption key.</span></span>

### <span data-ttu-id="723ac-120">Пример 4: Включите шифрование с помощью идентификатора клиента Azure Active Directory, отпечатка сертификата клиента и обтекания диска EncryptionKey с помощью ключа шифрования ключей.</span><span class="sxs-lookup"><span data-stu-id="723ac-120">Example 4: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
```
$RGName = "MyResourceGroup"
$VMName = "MyTestVM"
#The KeyVault must have enabledForDiskEncryption property set on it
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$KEK = Add-AzureKeyVaultKey -VaultName $VaultName -Name $KEKName -Destination "Software"
$KeyEncryptionKeyUrl = $KEK.Key.kid

# create Azure AD application and associate the certificate
$CertPath = "C:\certificates\examplecert.pfx"
$CertPassword = "Password"
$Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($CertPath, $CertPassword)
$KeyValue = [System.Convert]::ToBase64String($cert.GetRawCertData())
$AzureAdApplication = New-AzureRmADApplication -DisplayName "<Your Application Display Name>" -HomePage "<https://YourApplicationHomePage>" -IdentifierUris "<https://YouApplicationUri>" -KeyValue $KeyValue -KeyType AsymmetricX509Cert 
$ServicePrincipal = New-AzureRmADServicePrincipal -ApplicationId $AzureAdApplication.ApplicationId

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
Set-AzureKeyVaultSecret -VaultName $VaultName-Name $KeyVaultSecretName -SecretValue $Secret
Set-AzureRmKeyVaultAccessPolicy -VaultName $VaultName -ResourceGroupName $RGName -EnabledForDeployment

#deploy cert to VM
$CertUrl = (Get-AzureKeyVaultSecret -VaultName $VaultName -Name $KeyVaultSecretName).Id
$SourceVaultId = (Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName).ResourceId
$VM = Get-AzureRmVM -ResourceGroupName $RGName -Name $VMName 
$VM = Add-AzureRmVMSecret -VM $VM -SourceVaultId $SourceVaultId -CertificateStore "My" -CertificateUrl $CertUrl 
Update-AzureRmVM -VM $VM -ResourceGroupName $RGName 

#Enable encryption on the virtual machine using Azure AD client ID and client cert thumbprint
Set-AzureRmVMDiskEncryptionExtension -ResourceGroupName $RGname -VMName $VMName -AadClientID $AADClientID -AadClientCertThumbprint $AADClientCertThumbprint -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="723ac-121">В этом примере включается шифрование с помощью идентификатора клиента Azure Active Directory, отпечатка сертификата клиента и перенос ключа шифрования диска с помощью ключа шифрования ключа.</span><span class="sxs-lookup"><span data-stu-id="723ac-121">This example enables encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryption key by using key encryption key.</span></span>

## <span data-ttu-id="723ac-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="723ac-122">PARAMETERS</span></span>

### <span data-ttu-id="723ac-123">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="723ac-123">-AadClientCertThumbprint</span></span>
<span data-ttu-id="723ac-124">Указывает отпечаток сертификата клиента приложения AzureActive Directory (Azure AD) с разрешениями на запись секретных данных в **KeyVault**.</span><span class="sxs-lookup"><span data-stu-id="723ac-124">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="723ac-125">В качестве предварительной компоненты сертификат клиента Azure AD необходимо предварительно развернуть в хранилище сертификатов локального компьютера виртуальной машины `my` .</span><span class="sxs-lookup"><span data-stu-id="723ac-125">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="723ac-126">Для развертывания сертификата на виртуальной машине в Azure можно использовать командлет Add-AzureRmVMSecret.</span><span class="sxs-lookup"><span data-stu-id="723ac-126">The Add-AzureRmVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="723ac-127">Дополнительные сведения можно найти в справке по командлетам **Add-AzureRmVMSecret** .</span><span class="sxs-lookup"><span data-stu-id="723ac-127">For more details, see the **Add-AzureRmVMSecret** cmdlet help.</span></span>
<span data-ttu-id="723ac-128">Сертификат необходимо предварительно развернуть в хранилище сертификатов локального компьютера виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="723ac-128">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

```yaml
Type: System.String
Parameter Sets: AAD Client Cert Parameters
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="723ac-129">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="723ac-129">-AadClientID</span></span>
<span data-ttu-id="723ac-130">Указывает идентификатор клиента приложения Azure AD, у которого есть разрешения на запись секретных данных в **KeyVault**.</span><span class="sxs-lookup"><span data-stu-id="723ac-130">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="723ac-131">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="723ac-131">-AadClientSecret</span></span>
<span data-ttu-id="723ac-132">Указывает секретный ключ клиента для приложения Azure AD, который имеет разрешения на запись секретных данных в **KeyVault**.</span><span class="sxs-lookup"><span data-stu-id="723ac-132">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: System.String
Parameter Sets: AAD Client Secret Parameters
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="723ac-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="723ac-133">-DefaultProfile</span></span>
<span data-ttu-id="723ac-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="723ac-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="723ac-135">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="723ac-135">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="723ac-136">Указывает, что этот командлет отключает автоматическое обновление дополнительной версии расширения.</span><span class="sxs-lookup"><span data-stu-id="723ac-136">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="723ac-137">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="723ac-137">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="723ac-138">Указывает идентификатор ресурса **KeyVault** , на который нужно отправить ключи шифрования виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="723ac-138">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="723ac-139">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="723ac-139">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="723ac-140">Указывает URL-адрес **KeyVault** , на который нужно отправить ключи шифрования виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="723ac-140">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

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

### <span data-ttu-id="723ac-141">-Force</span><span class="sxs-lookup"><span data-stu-id="723ac-141">-Force</span></span>
<span data-ttu-id="723ac-142">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="723ac-142">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="723ac-143">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="723ac-143">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="723ac-144">Указывает алгоритм, который используется для переноса ключа шифрования ключа виртуальной машины и его депереноса.</span><span class="sxs-lookup"><span data-stu-id="723ac-144">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="723ac-145">Значением по умолчанию является RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="723ac-145">The default value is RSA-OAEP.</span></span>

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

### <span data-ttu-id="723ac-146">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="723ac-146">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="723ac-147">Задает URL-адрес ключа шифрования для ключа, который используется для переноса ключа шифрования виртуальной машины и его депереноса.</span><span class="sxs-lookup"><span data-stu-id="723ac-147">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="723ac-148">Это должен быть полный URL-адрес версии.</span><span class="sxs-lookup"><span data-stu-id="723ac-148">This must be the full versioned URL.</span></span>

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

### <span data-ttu-id="723ac-149">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="723ac-149">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="723ac-150">Указывает идентификатор ресурса **KeyVault** , содержащего ключ шифрования ключа, который используется для переноса ключа шифрования виртуальной машины и его декодирования.</span><span class="sxs-lookup"><span data-stu-id="723ac-150">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="723ac-151">Это должен быть полный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="723ac-151">This must be a full versioned URL.</span></span>

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

### <span data-ttu-id="723ac-152">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="723ac-152">-Name</span></span>
<span data-ttu-id="723ac-153">Указывает имя ресурса диспетчера ресурсов Azure, представляющего расширение.</span><span class="sxs-lookup"><span data-stu-id="723ac-153">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="723ac-154">Значение по умолчанию — AzureDiskEncryption для виртуальных машин, работающих под управлением операционной системы Windows или AzureDiskEncryptionForLinux для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="723ac-154">The default value is AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>

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

### <span data-ttu-id="723ac-155">-Парольную фразу</span><span class="sxs-lookup"><span data-stu-id="723ac-155">-Passphrase</span></span>
<span data-ttu-id="723ac-156">Указывает парольную фразу, используемую для шифрования виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="723ac-156">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="723ac-157">Этот параметр не используется для виртуальных машин, работающих под управлением операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="723ac-157">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

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

### <span data-ttu-id="723ac-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="723ac-158">-ResourceGroupName</span></span>
<span data-ttu-id="723ac-159">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="723ac-159">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="723ac-160">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="723ac-160">-SequenceVersion</span></span>
<span data-ttu-id="723ac-161">Указывает порядковый номер операций шифрования для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="723ac-161">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="723ac-162">Это значение уникально для каждой операции шифрования, выполняемой на той же виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="723ac-162">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="723ac-163">Для получения предыдущего использованного порядкового номера можно использовать командлет Get-AzureRmVMExtension.</span><span class="sxs-lookup"><span data-stu-id="723ac-163">The Get-AzureRmVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

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

### <span data-ttu-id="723ac-164">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="723ac-164">-SkipVmBackup</span></span>
<span data-ttu-id="723ac-165">Пропуск создания резервной копии для виртуальных машин Linux</span><span class="sxs-lookup"><span data-stu-id="723ac-165">Skip backup creation for Linux VMs</span></span>

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

### <span data-ttu-id="723ac-166">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="723ac-166">-TypeHandlerVersion</span></span>
<span data-ttu-id="723ac-167">Задает версию расширения шифрования.</span><span class="sxs-lookup"><span data-stu-id="723ac-167">Specifies the version of the encryption extension.</span></span>

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

### <span data-ttu-id="723ac-168">-VMName</span><span class="sxs-lookup"><span data-stu-id="723ac-168">-VMName</span></span>
<span data-ttu-id="723ac-169">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="723ac-169">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="723ac-170">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="723ac-170">-VolumeType</span></span>
<span data-ttu-id="723ac-171">Указывает тип томов виртуальной машины для выполнения операции шифрования.</span><span class="sxs-lookup"><span data-stu-id="723ac-171">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="723ac-172">Допустимые значения виртуальных машин, работающих под управлением операционной системы Windows, описаны ниже. все, ОС и данные.</span><span class="sxs-lookup"><span data-stu-id="723ac-172">Allowed values for virtual machines that run the Windows operating system are as follows: All, OS, and Data.</span></span>
<span data-ttu-id="723ac-173">Допустимые значения для виртуальных машин Linux описаны ниже: только данные.</span><span class="sxs-lookup"><span data-stu-id="723ac-173">The allowed values for Linux virtual machines are as follows: Data only.</span></span>

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

### <span data-ttu-id="723ac-174">-Confirm</span><span class="sxs-lookup"><span data-stu-id="723ac-174">-Confirm</span></span>
<span data-ttu-id="723ac-175">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="723ac-175">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="723ac-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="723ac-176">-WhatIf</span></span>
<span data-ttu-id="723ac-177">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="723ac-177">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="723ac-178">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="723ac-178">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="723ac-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="723ac-179">CommonParameters</span></span>
<span data-ttu-id="723ac-180">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="723ac-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="723ac-181">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="723ac-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="723ac-182">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="723ac-182">INPUTS</span></span>

## <span data-ttu-id="723ac-183">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="723ac-183">OUTPUTS</span></span>

## <span data-ttu-id="723ac-184">Пуск</span><span class="sxs-lookup"><span data-stu-id="723ac-184">NOTES</span></span>

## <span data-ttu-id="723ac-185">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="723ac-185">RELATED LINKS</span></span>

[<span data-ttu-id="723ac-186">Add-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="723ac-186">Add-AzureRmVMSecret</span></span>](./Add-AzureRmVMSecret.md)

[<span data-ttu-id="723ac-187">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="723ac-187">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="723ac-188">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="723ac-188">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)


