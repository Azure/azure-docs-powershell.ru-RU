---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
ms.openlocfilehash: f41e15a01a667576ee8f045d94bcb6b6dfee1e7b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078223"
---
# <span data-ttu-id="98796-101">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="98796-101">Get-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="98796-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="98796-102">SYNOPSIS</span></span>
<span data-ttu-id="98796-103">Получает сертификат из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="98796-103">Gets a certificate from a key vault.</span></span>

## <span data-ttu-id="98796-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="98796-104">SYNTAX</span></span>

### <span data-ttu-id="98796-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="98796-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98796-106">ByCertificateNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="98796-106">ByCertificateNameAndVersion</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98796-107">ByCertificateAllVersions</span><span class="sxs-lookup"><span data-stu-id="98796-107">ByCertificateAllVersions</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98796-108">ByNameInputObject</span><span class="sxs-lookup"><span data-stu-id="98796-108">ByNameInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98796-109">ByCertificateNameAndVersionInputObject</span><span class="sxs-lookup"><span data-stu-id="98796-109">ByCertificateNameAndVersionInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98796-110">ByCertificateAllVersionsInputObject</span><span class="sxs-lookup"><span data-stu-id="98796-110">ByCertificateAllVersionsInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98796-111">ByNameResourceId</span><span class="sxs-lookup"><span data-stu-id="98796-111">ByNameResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98796-112">ByCertificateNameAndVersionResourceId</span><span class="sxs-lookup"><span data-stu-id="98796-112">ByCertificateNameAndVersionResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98796-113">ByCertificateAllVersionsResourceId</span><span class="sxs-lookup"><span data-stu-id="98796-113">ByCertificateAllVersionsResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98796-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98796-114">DESCRIPTION</span></span>
<span data-ttu-id="98796-115">Командлет **Get-AzKeyVaultCertificate** получает указанный сертификат или версии сертификата из хранилища ключей в хранилище ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="98796-115">The **Get-AzKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="98796-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="98796-116">EXAMPLES</span></span>

### <span data-ttu-id="98796-117">Пример 1: получение сертификата</span><span class="sxs-lookup"><span data-stu-id="98796-117">Example 1: Get a certificate</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : testCert01
Certificate : [Subject] 
                CN=contoso.com

              [Issuer] 
                CN=contoso.com

              [Serial Number] 
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

              [Not Before] 
                2/8/2016 3:11:45 PM

              [Not After] 
                8/8/2016 4:21:45 PM

              [Thumbprint] 
                XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId       : https://contoso.vault.azure.net:443/keys/TestCert01/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
SecretId    : https://contoso.vault.azure.net:443/secrets/TestCert01/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Thumbprint  : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

### <span data-ttu-id="98796-118">Пример 2: получение сертификата и сохранение его в качестве PFX</span><span class="sxs-lookup"><span data-stu-id="98796-118">Example 2: Get cert and save it as pfx</span></span>
<span data-ttu-id="98796-119">Эта команда получает сертификат с именем TestCert01 из хранилища ключей с именем ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="98796-119">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span> <span data-ttu-id="98796-120">Чтобы скачать сертификат как PFX-файл, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="98796-120">To download the certificate as pfx file, run following command.</span></span> <span data-ttu-id="98796-121">Эти команды обращаются к SecretId, а затем сохраняют содержимое в виде PFX-файла.</span><span class="sxs-lookup"><span data-stu-id="98796-121">These commands access SecretId and then save the content as a pfx file.</span></span>

```powershell
$cert = Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
$secret = Get-AzKeyVaultSecret -VaultName $vaultName -Name $cert.Name

$secretByte = [Convert]::FromBase64String($secret.SecretValueText)
$x509Cert = new-object System.Security.Cryptography.X509Certificates.X509Certificate2
$x509Cert.Import($secretByte, "", "Exportable,PersistKeySet")
$type = [System.Security.Cryptography.X509Certificates.X509ContentType]::Pfx
$pfxFileByte = $x509Cert.Export($type, $password)

# Write to a file
[System.IO.File]::WriteAllBytes("KeyVault.pfx", $pfxFileByte)
```

### <span data-ttu-id="98796-122">Пример 3: получение всех сертификатов, которые были удалены, но не очищены для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="98796-122">Example 3: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName 'contoso' -InRemovedState

DeletedDate        : 5/24/2018 6:08:32 PM
Enabled            : True
Expires            : 11/24/2018 6:08:13 PM
NotBefore          : 5/24/2018 5:58:13 PM
Created            : 5/24/2018 6:08:13 PM
Updated            : 5/24/2018 6:08:13 PM
Tags               :
VaultName          : contoso
Name               : test1
Version            :
Id                 : https://contoso.vault.azure.net:443/certificates/test1

ScheduledPurgeDate : 8/22/2018 6:10:47 PM
DeletedDate        : 5/24/2018 6:10:47 PM
Enabled            : True
Expires            : 11/24/2018 6:09:44 PM
NotBefore          : 5/24/2018 5:59:44 PM
Created            : 5/24/2018 6:09:44 PM
Updated            : 5/24/2018 6:09:44 PM
Tags               :
VaultName          : contoso
Name               : test2
Version            :
Id                 : https://contoso.vault.azure.net:443/certificates/test2
```

<span data-ttu-id="98796-123">Эта команда получает все сертификаты, которые были ранее удалены, но не очищены, в хранилище ключей contoso.</span><span class="sxs-lookup"><span data-stu-id="98796-123">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="98796-124">Пример 4: получение сертификата MyCert, который был удален, но не очищен для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="98796-124">Example 4: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName 'contoso' -Name 'test1' -InRemovedState

Certificate        : [Subject]
                       CN=contoso.com

                     [Issuer]
                       CN=contoso.com

                     [Serial Number]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                     [Not Before]
                       5/24/2018 10:58:13 AM

                     [Not After]
                       11/24/2018 10:08:13 AM

                     [Thumbprint]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId              : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
SecretId           : https://contoso.vault.azure.net:443/secrets/test1/7fe415d5518240c1a6fce89986b8d334
Thumbprint         : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel      : Recoverable+Purgeable
ScheduledPurgeDate : 8/22/2018 6:08:32 PM
DeletedDate        : 5/24/2018 6:08:32 PM
Enabled            : True
Expires            : 11/24/2018 6:08:13 PM
NotBefore          : 5/24/2018 5:58:13 PM
Created            : 5/24/2018 6:08:13 PM
Updated            : 5/24/2018 6:08:13 PM
Tags               :
VaultName          : contoso
Name               : test1
Version            : 7fe415d5518240c1a6fce89986b8d334
Id                 : https://contoso.vault.azure.net:443/certificates/test1/7fe415d5518240c1a6fce89986b8d334
```

<span data-ttu-id="98796-125">Эта команда получает сертификат с именем "MyCert", который ранее был удален, но не очищен, в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="98796-125">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="98796-126">Эта команда возвращает метаданные, например дату удаления, и запланированную дату очистки этого удаленного сертификата.</span><span class="sxs-lookup"><span data-stu-id="98796-126">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

### <span data-ttu-id="98796-127">Пример 5: перечисление сертификатов с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="98796-127">Example 5: List certificates using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "test*"

Enabled   : True
Expires   : 8/5/2019 2:39:25 AM
NotBefore : 2/5/2019 2:29:25 AM
Created   : 2/5/2019 2:39:25 AM
Updated   : 2/5/2019 2:39:25 AM
Tags      :
VaultName : ContosoKV01
Name      : test1
Version   :
Id        : https://ContosoKV01.vault.azure.net:443/certificates/test1

Enabled   : True
Expires   : 8/5/2019 2:39:25 AM
NotBefore : 2/5/2019 2:29:25 AM
Created   : 2/5/2019 2:39:25 AM
Updated   : 2/5/2019 2:39:25 AM
Tags      :
VaultName : ContosoKV01
Name      : test2
Version   :
Id        : https://ContosoKV01.vault.azure.net:443/certificates/test2

This command gets all certificates starting with "test" from the key vault named ContosoKV01.
```

## <span data-ttu-id="98796-128">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="98796-128">PARAMETERS</span></span>

### <span data-ttu-id="98796-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98796-129">-DefaultProfile</span></span>
<span data-ttu-id="98796-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="98796-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98796-131">-IncludePending</span><span class="sxs-lookup"><span data-stu-id="98796-131">-IncludePending</span></span>
<span data-ttu-id="98796-132">Указывает, нужно ли включать в вывод ожидающие сертификаты.</span><span class="sxs-lookup"><span data-stu-id="98796-132">Specifies whether to include pending certificates in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98796-133">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="98796-133">-IncludeVersions</span></span>
<span data-ttu-id="98796-134">Указывает на то, что эта операция получает все версии сертификата.</span><span class="sxs-lookup"><span data-stu-id="98796-134">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByCertificateAllVersions, ByCertificateAllVersionsInputObject, ByCertificateAllVersionsResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98796-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98796-135">-InputObject</span></span>
<span data-ttu-id="98796-136">Объект KeyVault.</span><span class="sxs-lookup"><span data-stu-id="98796-136">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByNameInputObject, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98796-137">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="98796-137">-InRemovedState</span></span>
<span data-ttu-id="98796-138">Указывает, следует ли включать ранее удаленные сертификаты в выходной файл.</span><span class="sxs-lookup"><span data-stu-id="98796-138">Specifies whether to include previously deleted certificates in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98796-139">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="98796-139">-Name</span></span>
<span data-ttu-id="98796-140">Указывает имя получаемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="98796-140">Specifies the name of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateAllVersions, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject, ByCertificateNameAndVersionResourceId, ByCertificateAllVersionsResourceId
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98796-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98796-141">-ResourceId</span></span>
<span data-ttu-id="98796-142">Идентификатор ресурса KeyVault.</span><span class="sxs-lookup"><span data-stu-id="98796-142">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameResourceId, ByCertificateNameAndVersionResourceId, ByCertificateAllVersionsResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98796-143">-VaultName</span><span class="sxs-lookup"><span data-stu-id="98796-143">-VaultName</span></span>
<span data-ttu-id="98796-144">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="98796-144">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByCertificateNameAndVersion, ByCertificateAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98796-145">-Version</span><span class="sxs-lookup"><span data-stu-id="98796-145">-Version</span></span>
<span data-ttu-id="98796-146">Определяет версию сертификата.</span><span class="sxs-lookup"><span data-stu-id="98796-146">Specifies the version of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateNameAndVersionInputObject, ByCertificateNameAndVersionResourceId
Aliases: CertificateVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98796-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98796-147">CommonParameters</span></span>
<span data-ttu-id="98796-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="98796-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98796-149">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98796-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98796-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="98796-150">INPUTS</span></span>

### <span data-ttu-id="98796-151">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="98796-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="98796-152">System. String</span><span class="sxs-lookup"><span data-stu-id="98796-152">System.String</span></span>

## <span data-ttu-id="98796-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="98796-153">OUTPUTS</span></span>

### <span data-ttu-id="98796-154">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="98796-154">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

### <span data-ttu-id="98796-155">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="98796-155">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

### <span data-ttu-id="98796-156">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="98796-156">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

### <span data-ttu-id="98796-157">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="98796-157">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="98796-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="98796-158">NOTES</span></span>

## <span data-ttu-id="98796-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98796-159">RELATED LINKS</span></span>

[<span data-ttu-id="98796-160">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="98796-160">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="98796-161">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="98796-161">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="98796-162">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="98796-162">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="98796-163">Undo-AzKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="98796-163">Undo-AzKeyVaultSecretCertificate</span></span>](./Undo-AzKeyVaultSecretCertificate.md)
