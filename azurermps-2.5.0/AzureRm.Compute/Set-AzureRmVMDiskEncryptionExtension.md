---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6BCB36BC-F5E6-4EDD-983C-8BDE7A9B004D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmdiskencryptionextension
schema: 2.0.0
ms.openlocfilehash: 76bdebc68f1fafef127863ef753c28fce7034fe0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914505"
---
# <span data-ttu-id="6f757-101">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="6f757-101">Set-AzureRmVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="6f757-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6f757-102">SYNOPSIS</span></span>
<span data-ttu-id="6f757-103">Включает шифрование на работающей виртуальной машине IaaS в Azure.</span><span class="sxs-lookup"><span data-stu-id="6f757-103">Enables encryption on a running IaaS virtual machine in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f757-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6f757-104">SYNTAX</span></span>

### <span data-ttu-id="6f757-105">AADClientSecretParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6f757-105">AADClientSecretParameterSet (Default)</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientSecret] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f757-106">AADClientCertParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f757-106">AADClientCertParameterSet</span></span>
```
Set-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [-AadClientID] <String>
 [-AadClientCertThumbprint] <String> [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String>
 [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>] [[-KeyEncryptionAlgorithm] <String>]
 [[-VolumeType] <String>] [[-SequenceVersion] <String>] [[-TypeHandlerVersion] <String>] [[-Name] <String>]
 [[-Passphrase] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-SkipVmBackup] [-ExtensionType <String>]
 [-ExtensionPublisherName <String>] [-EncryptFormatAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f757-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f757-107">DESCRIPTION</span></span>
<span data-ttu-id="6f757-108">Командлет **Set-AzureRmVMDiskEncryptionExtension** позволяет выполнять шифрование на работающей инфраструктуре в качестве виртуальной машины службы (IaaS) в Azure.</span><span class="sxs-lookup"><span data-stu-id="6f757-108">The **Set-AzureRmVMDiskEncryptionExtension** cmdlet enables encryption on a running infrastructure as a service (IaaS) virtual machine in Azure.</span></span>
<span data-ttu-id="6f757-109">Этот командлет включает шифрование, устанавливая расширение шифрования диска на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="6f757-109">This cmdlet enables encryption by installing the disk encryption extension on the virtual machine.</span></span>
<span data-ttu-id="6f757-110">Если параметр *Name* не указан, устанавливается расширение с именем по умолчанию AzureDiskEncryption для виртуальных машин, работающих под управлением операционной системы Windows или AzureDiskEncryptionForLinux для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="6f757-110">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>
<span data-ttu-id="6f757-111">Этот командлет требует подтверждения от пользователей. чтобы включить шифрование, требуется перезапуск виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6f757-111">This cmdlet requires confirmation from the users as one of the steps to enable encryption requires a restart of the virtual machine.</span></span>
<span data-ttu-id="6f757-112">Перед запуском этого командлета рекомендуется сохранить работу на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="6f757-112">It is advised that you save your work on the virtual machine before you run this cmdlet.</span></span>

## <span data-ttu-id="6f757-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6f757-113">EXAMPLES</span></span>

### <span data-ttu-id="6f757-114">Пример 1: Включение шифрования с помощью идентификатора клиента Azure AD и секрета клиента</span><span class="sxs-lookup"><span data-stu-id="6f757-114">Example 1: Enable encryption using Azure AD Client ID and Client Secret</span></span>
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

<span data-ttu-id="6f757-115">В этом примере включается шифрование с помощью идентификатора клиента Azure AD и секрета клиента.</span><span class="sxs-lookup"><span data-stu-id="6f757-115">This example enables encryption using Azure AD client ID, and client secret.</span></span>

### <span data-ttu-id="6f757-116">Пример 2: Включите шифрование с помощью идентификатора клиента Azure AD и отпечатка сертификата клиента</span><span class="sxs-lookup"><span data-stu-id="6f757-116">Example 2: Enable encryption using Azure AD client ID and client certification thumbprint</span></span>
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

<span data-ttu-id="6f757-117">В этом примере включается шифрование с помощью идентификатора клиента Azure Active Directory и отпечатков сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="6f757-117">This example enables encryption using Azure AD client ID and client certification thumbprints.</span></span>

### <span data-ttu-id="6f757-118">Пример 3: Включите шифрование с помощью идентификатора клиента Azure AD, секретного клиента и ключа шифрования диска с помощью ключа шифрования ключа.</span><span class="sxs-lookup"><span data-stu-id="6f757-118">Example 3: Enable encryption using Azure AD client ID, client secret, and wrap disk encryption key by using key encryption key</span></span>
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

<span data-ttu-id="6f757-119">В этом примере включается шифрование с помощью идентификатора клиента Azure Active Directory, секрета клиента и ключа шифрования диска с помощью ключа шифрования ключа.</span><span class="sxs-lookup"><span data-stu-id="6f757-119">This example enables encryption using Azure AD client ID, client secret, and wrap disk encryption key by using the key encryption key.</span></span>

### <span data-ttu-id="6f757-120">Пример 4: Включите шифрование с помощью идентификатора клиента Azure Active Directory, отпечатка сертификата клиента и обтекания диска EncryptionKey с помощью ключа шифрования ключей.</span><span class="sxs-lookup"><span data-stu-id="6f757-120">Example 4: Enable encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryptionkey by using key encryption key</span></span>
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

<span data-ttu-id="6f757-121">В этом примере включается шифрование с помощью идентификатора клиента Azure Active Directory, отпечатка сертификата клиента и перенос ключа шифрования диска с помощью ключа шифрования ключа.</span><span class="sxs-lookup"><span data-stu-id="6f757-121">This example enables encryption using Azure AD client ID, client cert thumbprint, and wrap disk encryption key by using key encryption key.</span></span>

## <span data-ttu-id="6f757-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6f757-122">PARAMETERS</span></span>

### <span data-ttu-id="6f757-123">-AadClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="6f757-123">-AadClientCertThumbprint</span></span>
<span data-ttu-id="6f757-124">Указывает отпечаток сертификата клиента приложения AzureActive Directory (Azure AD) с разрешениями на запись секретных данных в **KeyVault**.</span><span class="sxs-lookup"><span data-stu-id="6f757-124">Specifies the thumbprint of the AzureActive Directory (Azure AD) application client certificate that has permissions to write secrets to **KeyVault**.</span></span>
<span data-ttu-id="6f757-125">В качестве предварительной компоненты сертификат клиента Azure AD необходимо предварительно развернуть в хранилище сертификатов локального компьютера виртуальной машины `my` .</span><span class="sxs-lookup"><span data-stu-id="6f757-125">As a prerequisite, the Azure AD client certificate must be previously deployed to the virtual machine's local computer `my` certificate store.</span></span>
<span data-ttu-id="6f757-126">Для развертывания сертификата на виртуальной машине в Azure можно использовать командлет Add-AzureRmVMSecret.</span><span class="sxs-lookup"><span data-stu-id="6f757-126">The Add-AzureRmVMSecret cmdlet can be used to deploy a certificate to a virtual machine in Azure.</span></span>
<span data-ttu-id="6f757-127">Дополнительные сведения можно найти в справке по командлетам **Add-AzureRmVMSecret** .</span><span class="sxs-lookup"><span data-stu-id="6f757-127">For more details, see the **Add-AzureRmVMSecret** cmdlet help.</span></span>
<span data-ttu-id="6f757-128">Сертификат необходимо предварительно развернуть в хранилище сертификатов локального компьютера виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6f757-128">The certificate must be previously deployed to the virtual machine local computer my certificate store.</span></span>

```yaml
Type: String
Parameter Sets: AADClientCertParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f757-129">-AadClientID</span><span class="sxs-lookup"><span data-stu-id="6f757-129">-AadClientID</span></span>
<span data-ttu-id="6f757-130">Указывает идентификатор клиента приложения Azure AD, у которого есть разрешения на запись секретных данных в **KeyVault**.</span><span class="sxs-lookup"><span data-stu-id="6f757-130">Specifies the client ID of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f757-131">-AadClientSecret</span><span class="sxs-lookup"><span data-stu-id="6f757-131">-AadClientSecret</span></span>
<span data-ttu-id="6f757-132">Указывает секретный ключ клиента для приложения Azure AD, который имеет разрешения на запись секретных данных в **KeyVault**.</span><span class="sxs-lookup"><span data-stu-id="6f757-132">Specifies the client secret of the Azure AD application that has permissions to write secrets to **KeyVault**.</span></span>

```yaml
Type: String
Parameter Sets: AADClientSecretParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f757-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f757-133">-DefaultProfile</span></span>
<span data-ttu-id="6f757-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6f757-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f757-135">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="6f757-135">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="6f757-136">Указывает, что этот командлет отключает автоматическое обновление дополнительной версии расширения.</span><span class="sxs-lookup"><span data-stu-id="6f757-136">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f757-137">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="6f757-137">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="6f757-138">Указывает идентификатор ресурса **KeyVault** , на который нужно отправить ключи шифрования виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6f757-138">Specifies the resource ID of the **KeyVault** to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f757-139">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="6f757-139">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="6f757-140">Указывает URL-адрес **KeyVault** , на который нужно отправить ключи шифрования виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6f757-140">Specifies the **KeyVault** URL to which the virtual machine encryption keys should be uploaded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f757-141">-EncryptFormatAll</span><span class="sxs-lookup"><span data-stu-id="6f757-141">-EncryptFormatAll</span></span>
<span data-ttu-id="6f757-142">Encrypt-Format все диски с данными, которые еще не были зашифрованы</span><span class="sxs-lookup"><span data-stu-id="6f757-142">Encrypt-Format all data drives that are not already encrypted</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f757-143">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="6f757-143">-ExtensionPublisherName</span></span>
<span data-ttu-id="6f757-144">Имя издателя расширения.</span><span class="sxs-lookup"><span data-stu-id="6f757-144">The extension publisher name.</span></span> <span data-ttu-id="6f757-145">Указывайте этот параметр только для переопределения значения по умолчанию Microsoft. Azure. Security.</span><span class="sxs-lookup"><span data-stu-id="6f757-145">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f757-146">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="6f757-146">-ExtensionType</span></span>
<span data-ttu-id="6f757-147">Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="6f757-147">The extension type.</span></span> <span data-ttu-id="6f757-148">Укажите этот параметр для переопределения значения по умолчанию "AzureDiskEncryption" для виртуальных машин и "AzureDiskEncryptionForLinux" для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="6f757-148">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f757-149">-Force</span><span class="sxs-lookup"><span data-stu-id="6f757-149">-Force</span></span>
<span data-ttu-id="6f757-150">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="6f757-150">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f757-151">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="6f757-151">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="6f757-152">Указывает алгоритм, который используется для переноса ключа шифрования ключа виртуальной машины и его депереноса.</span><span class="sxs-lookup"><span data-stu-id="6f757-152">Specifies the algorithm that is used to wrap and unwrap the key encryption key of the virtual machine.</span></span>
<span data-ttu-id="6f757-153">Значением по умолчанию является RSA-OAEP.</span><span class="sxs-lookup"><span data-stu-id="6f757-153">The default value is RSA-OAEP.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f757-154">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="6f757-154">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="6f757-155">Задает URL-адрес ключа шифрования для ключа, который используется для переноса ключа шифрования виртуальной машины и его депереноса.</span><span class="sxs-lookup"><span data-stu-id="6f757-155">Specifies the URL of the key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="6f757-156">Это должен быть полный URL-адрес версии.</span><span class="sxs-lookup"><span data-stu-id="6f757-156">This must be the full versioned URL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f757-157">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="6f757-157">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="6f757-158">Указывает идентификатор ресурса **KeyVault** , содержащего ключ шифрования ключа, который используется для переноса ключа шифрования виртуальной машины и его декодирования.</span><span class="sxs-lookup"><span data-stu-id="6f757-158">Specifies the resource ID of the **KeyVault** that contains key encryption key that is used to wrap and unwrap the virtual machine encryption key.</span></span>
<span data-ttu-id="6f757-159">Это должен быть полный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="6f757-159">This must be a full versioned URL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f757-160">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6f757-160">-Name</span></span>
<span data-ttu-id="6f757-161">Указывает имя ресурса диспетчера ресурсов Azure, представляющего расширение.</span><span class="sxs-lookup"><span data-stu-id="6f757-161">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="6f757-162">Значение по умолчанию — AzureDiskEncryption для виртуальных машин, работающих под управлением операционной системы Windows или AzureDiskEncryptionForLinux для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="6f757-162">The default value is AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f757-163">-Парольную фразу</span><span class="sxs-lookup"><span data-stu-id="6f757-163">-Passphrase</span></span>
<span data-ttu-id="6f757-164">Указывает парольную фразу, используемую для шифрования виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="6f757-164">Specifies the passphrase used for encrypting Linux virtual machines only.</span></span>
<span data-ttu-id="6f757-165">Этот параметр не используется для виртуальных машин, работающих под управлением операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="6f757-165">This parameter is not used for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f757-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f757-166">-ResourceGroupName</span></span>
<span data-ttu-id="6f757-167">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6f757-167">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f757-168">-SequenceVersion</span><span class="sxs-lookup"><span data-stu-id="6f757-168">-SequenceVersion</span></span>
<span data-ttu-id="6f757-169">Указывает порядковый номер операций шифрования для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6f757-169">Specifies the sequence number of the encryption operations for a virtual machine.</span></span>
<span data-ttu-id="6f757-170">Это значение уникально для каждой операции шифрования, выполняемой на той же виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="6f757-170">This is unique per each encryption operation performed on the same virtual machine.</span></span>
<span data-ttu-id="6f757-171">Для получения предыдущего использованного порядкового номера можно использовать командлет Get-AzureRmVMExtension.</span><span class="sxs-lookup"><span data-stu-id="6f757-171">The Get-AzureRmVMExtension cmdlet can be used to retrieve the previous sequence number that was used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f757-172">-SkipVmBackup</span><span class="sxs-lookup"><span data-stu-id="6f757-172">-SkipVmBackup</span></span>
<span data-ttu-id="6f757-173">Пропуск создания резервной копии для виртуальных машин Linux</span><span class="sxs-lookup"><span data-stu-id="6f757-173">Skip backup creation for Linux VMs</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f757-174">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="6f757-174">-TypeHandlerVersion</span></span>
<span data-ttu-id="6f757-175">Задает версию расширения шифрования.</span><span class="sxs-lookup"><span data-stu-id="6f757-175">Specifies the version of the encryption extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f757-176">-VMName</span><span class="sxs-lookup"><span data-stu-id="6f757-176">-VMName</span></span>
<span data-ttu-id="6f757-177">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6f757-177">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f757-178">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="6f757-178">-VolumeType</span></span>
<span data-ttu-id="6f757-179">Указывает тип томов виртуальной машины для выполнения операции шифрования.</span><span class="sxs-lookup"><span data-stu-id="6f757-179">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="6f757-180">Допустимые значения виртуальных машин, работающих под управлением операционной системы Windows, описаны ниже. все, ОС и данные.</span><span class="sxs-lookup"><span data-stu-id="6f757-180">Allowed values for virtual machines that run the Windows operating system are as follows: All, OS, and Data.</span></span>
<span data-ttu-id="6f757-181">Допустимые значения для виртуальных машин Linux описаны ниже: только данные.</span><span class="sxs-lookup"><span data-stu-id="6f757-181">The allowed values for Linux virtual machines are as follows: Data only.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f757-182">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f757-182">-Confirm</span></span>
<span data-ttu-id="6f757-183">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6f757-183">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f757-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f757-184">-WhatIf</span></span>
<span data-ttu-id="6f757-185">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6f757-185">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="6f757-186">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6f757-186">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f757-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f757-187">CommonParameters</span></span>
<span data-ttu-id="6f757-188">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6f757-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f757-189">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f757-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f757-190">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6f757-190">INPUTS</span></span>

### <span data-ttu-id="6f757-191">Ничего</span><span class="sxs-lookup"><span data-stu-id="6f757-191">None</span></span>
<span data-ttu-id="6f757-192">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="6f757-192">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6f757-193">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f757-193">OUTPUTS</span></span>

### <span data-ttu-id="6f757-194">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6f757-194">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="6f757-195">Пуск</span><span class="sxs-lookup"><span data-stu-id="6f757-195">NOTES</span></span>

## <span data-ttu-id="6f757-196">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f757-196">RELATED LINKS</span></span>

[<span data-ttu-id="6f757-197">Add-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="6f757-197">Add-AzureRmVMSecret</span></span>](./Add-AzureRmVMSecret.md)

[<span data-ttu-id="6f757-198">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="6f757-198">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="6f757-199">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="6f757-199">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)


