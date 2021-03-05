---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
ms.openlocfilehash: 391c156fea6e8d29bdf5794d1921a790cbefcc06
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004051"
---
# <span data-ttu-id="47981-101">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="47981-101">Get-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="47981-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47981-102">SYNOPSIS</span></span>
<span data-ttu-id="47981-103">Получает сертификат из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="47981-103">Gets a certificate from a key vault.</span></span>

## <span data-ttu-id="47981-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="47981-104">SYNTAX</span></span>

### <span data-ttu-id="47981-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="47981-105">ByName (Default)</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47981-106">ByCertificateNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="47981-106">ByCertificateNameAndVersion</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47981-107">ByCertificateAllVersions</span><span class="sxs-lookup"><span data-stu-id="47981-107">ByCertificateAllVersions</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47981-108">ByNameInputObject</span><span class="sxs-lookup"><span data-stu-id="47981-108">ByNameInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47981-109">ByCertificateNameAndVersionInputObject</span><span class="sxs-lookup"><span data-stu-id="47981-109">ByCertificateNameAndVersionInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47981-110">ByCertificateAllVersionsInputObject</span><span class="sxs-lookup"><span data-stu-id="47981-110">ByCertificateAllVersionsInputObject</span></span>
```
Get-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47981-111">ByNameResourceId</span><span class="sxs-lookup"><span data-stu-id="47981-111">ByNameResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-IncludePending]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47981-112">ByCertificateNameAndVersionResourceId</span><span class="sxs-lookup"><span data-stu-id="47981-112">ByCertificateNameAndVersionResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47981-113">ByCertificateAllVersionsResourceId</span><span class="sxs-lookup"><span data-stu-id="47981-113">ByCertificateAllVersionsResourceId</span></span>
```
Get-AzKeyVaultCertificate [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47981-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47981-114">DESCRIPTION</span></span>
<span data-ttu-id="47981-115">Cmdlet **Get-AzKeyVaultCertificate** получает указанный сертификат или его версии из хранилища ключей в хранилище ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="47981-115">The **Get-AzKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="47981-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="47981-116">EXAMPLES</span></span>

### <span data-ttu-id="47981-117">Пример 1. Получить сертификат</span><span class="sxs-lookup"><span data-stu-id="47981-117">Example 1: Get a certificate</span></span>
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

### <span data-ttu-id="47981-118">Пример 2. Получить сертификат и сохранить его в качестве pfx</span><span class="sxs-lookup"><span data-stu-id="47981-118">Example 2: Get cert and save it as pfx</span></span>
<span data-ttu-id="47981-119">Эта команда получает сертификат TestCert01 из хранилища ключей ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="47981-119">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span> <span data-ttu-id="47981-120">Чтобы скачать сертификат как pfx-файл, запустите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="47981-120">To download the certificate as pfx file, run following command.</span></span> <span data-ttu-id="47981-121">Эти команды доступа к SecretId, а затем сохранить содержимое в файле PFX.</span><span class="sxs-lookup"><span data-stu-id="47981-121">These commands access SecretId and then save the content as a pfx file.</span></span>

```powershell
$cert = Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
$secret = Get-AzKeyVaultSecret -VaultName $vaultName -Name $cert.Name -AsPlainText
$secretByte = [Convert]::FromBase64String($secret)
$x509Cert = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2($secretByte, "", "Exportable,PersistKeySet")
$type = [System.Security.Cryptography.X509Certificates.X509ContentType]::Pfx
$pfxFileByte = $x509Cert.Export($type, $password)

# Write to a file
[System.IO.File]::WriteAllBytes("KeyVault.pfx", $pfxFileByte)
```

### <span data-ttu-id="47981-122">Пример 3. Получите все сертификаты, которые были удалены, но не удалены из этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="47981-122">Example 3: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="47981-123">Эта команда получает все сертификаты, которые были ранее удалены, но не удалены, в хранилище ключей Contoso.</span><span class="sxs-lookup"><span data-stu-id="47981-123">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="47981-124">Пример 4. Возвращает сертификат MyCert, который был удален, но не был удален из этого сейфа ключа.</span><span class="sxs-lookup"><span data-stu-id="47981-124">Example 4: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="47981-125">Эта команда получает сертификат MyCert, который ранее был удален, но не был удален, в хранилище ключей Contoso.</span><span class="sxs-lookup"><span data-stu-id="47981-125">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="47981-126">Эта команда возвращает метаданные, такие как дата удаления и запланированная дата удаления этого удаленного сертификата.</span><span class="sxs-lookup"><span data-stu-id="47981-126">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

### <span data-ttu-id="47981-127">Пример 5. Сертификаты списков с использованием фильтрации</span><span class="sxs-lookup"><span data-stu-id="47981-127">Example 5: List certificates using filtering</span></span>
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

## <span data-ttu-id="47981-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47981-128">PARAMETERS</span></span>

### <span data-ttu-id="47981-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47981-129">-DefaultProfile</span></span>
<span data-ttu-id="47981-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="47981-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47981-131">-IncludePending</span><span class="sxs-lookup"><span data-stu-id="47981-131">-IncludePending</span></span>
<span data-ttu-id="47981-132">Указывает, следует ли включать сертификаты, ожидающих проверки, в выходные данные.</span><span class="sxs-lookup"><span data-stu-id="47981-132">Specifies whether to include pending certificates in the output</span></span>

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

### <span data-ttu-id="47981-133">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="47981-133">-IncludeVersions</span></span>
<span data-ttu-id="47981-134">Указывает на то, что эта операция возвращает все версии сертификата.</span><span class="sxs-lookup"><span data-stu-id="47981-134">Indicates that this operation gets all versions of the certificate.</span></span>

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

### <span data-ttu-id="47981-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47981-135">-InputObject</span></span>
<span data-ttu-id="47981-136">Объект KeyVault.</span><span class="sxs-lookup"><span data-stu-id="47981-136">KeyVault object.</span></span>

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

### <span data-ttu-id="47981-137">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="47981-137">-InRemovedState</span></span>
<span data-ttu-id="47981-138">Указывает, следует ли включать ранее удаленные сертификаты в выходные данные.</span><span class="sxs-lookup"><span data-stu-id="47981-138">Specifies whether to include previously deleted certificates in the output</span></span>

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

### <span data-ttu-id="47981-139">-Name</span><span class="sxs-lookup"><span data-stu-id="47981-139">-Name</span></span>
<span data-ttu-id="47981-140">Указывает имя сертификата, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="47981-140">Specifies the name of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByNameInputObject, ByNameResourceId
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateAllVersions, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject, ByCertificateNameAndVersionResourceId, ByCertificateAllVersionsResourceId
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="47981-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47981-141">-ResourceId</span></span>
<span data-ttu-id="47981-142">ИД ресурса KeyVault.</span><span class="sxs-lookup"><span data-stu-id="47981-142">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="47981-143">-VaultName</span><span class="sxs-lookup"><span data-stu-id="47981-143">-VaultName</span></span>
<span data-ttu-id="47981-144">Указывает имя сейфа ключа.</span><span class="sxs-lookup"><span data-stu-id="47981-144">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="47981-145">-Version</span><span class="sxs-lookup"><span data-stu-id="47981-145">-Version</span></span>
<span data-ttu-id="47981-146">Определяет версию сертификата.</span><span class="sxs-lookup"><span data-stu-id="47981-146">Specifies the version of a certificate.</span></span>

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

### <span data-ttu-id="47981-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47981-147">CommonParameters</span></span>
<span data-ttu-id="47981-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47981-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47981-149">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47981-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47981-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47981-150">INPUTS</span></span>

### <span data-ttu-id="47981-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="47981-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="47981-152">System.String</span><span class="sxs-lookup"><span data-stu-id="47981-152">System.String</span></span>

## <span data-ttu-id="47981-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="47981-153">OUTPUTS</span></span>

### <span data-ttu-id="47981-154">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="47981-154">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

### <span data-ttu-id="47981-155">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="47981-155">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

### <span data-ttu-id="47981-156">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="47981-156">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

### <span data-ttu-id="47981-157">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="47981-157">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="47981-158">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="47981-158">NOTES</span></span>

## <span data-ttu-id="47981-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47981-159">RELATED LINKS</span></span>

[<span data-ttu-id="47981-160">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="47981-160">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="47981-161">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="47981-161">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="47981-162">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="47981-162">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="47981-163">Undo-AzKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="47981-163">Undo-AzKeyVaultSecretCertificate</span></span>](./Undo-AzKeyVaultSecretCertificate.md)
