---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
ms.openlocfilehash: 87b030229eb2a1f4bb91122aaec8a119134d27fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561767"
---
# <span data-ttu-id="1b273-101">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="1b273-101">Get-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="1b273-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1b273-102">SYNOPSIS</span></span>
<span data-ttu-id="1b273-103">Получает сертификат из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="1b273-103">Gets a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b273-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1b273-104">SYNTAX</span></span>

### <span data-ttu-id="1b273-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1b273-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b273-106">ByCertificateNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="1b273-106">ByCertificateNameAndVersion</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b273-107">ByCertificateAllVersions</span><span class="sxs-lookup"><span data-stu-id="1b273-107">ByCertificateAllVersions</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b273-108">ByNameInputObject</span><span class="sxs-lookup"><span data-stu-id="1b273-108">ByNameInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b273-109">ByCertificateNameAndVersionInputObject</span><span class="sxs-lookup"><span data-stu-id="1b273-109">ByCertificateNameAndVersionInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b273-110">ByCertificateAllVersionsInputObject</span><span class="sxs-lookup"><span data-stu-id="1b273-110">ByCertificateAllVersionsInputObject</span></span>
```
Get-AzureKeyVaultCertificate [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b273-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b273-111">DESCRIPTION</span></span>
<span data-ttu-id="1b273-112">Командлет **Get-AzureKeyVaultCertificate** получает указанный сертификат или версии сертификата из хранилища ключей в хранилище ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="1b273-112">The **Get-AzureKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="1b273-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1b273-113">EXAMPLES</span></span>

### <span data-ttu-id="1b273-114">Пример 1: получение сертификата</span><span class="sxs-lookup"><span data-stu-id="1b273-114">Example 1: Get a certificate</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : testCert01
Certificate : [Subject] 
                CN=contoso.com

              [Issuer] 
                CN=contoso.com

              [Serial Number] 
                05979C5A2F0741D5A3B6F97673E8A118

              [Not Before] 
                2/8/2016 3:11:45 PM

              [Not After] 
                8/8/2016 4:21:45 PM

              [Thumbprint] 
                3E9B6848AD1834284157D68B060F748037F663C8

Thumbprint  : 3E9B6848AD1834284157D68B060F748037F663C8
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:21:45 PM
Updated     : 2/8/2016 11:21:45 PM
```

<span data-ttu-id="1b273-115">Эта команда получает сертификат с именем TestCert01 из хранилища ключей с именем ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="1b273-115">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="1b273-116">Пример 2: получение всех сертификатов, которые были удалены, но не очищены для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="1b273-116">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="1b273-117">Эта команда получает все сертификаты, которые были ранее удалены, но не очищены, в хранилище ключей contoso.</span><span class="sxs-lookup"><span data-stu-id="1b273-117">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="1b273-118">Пример 3: получение сертификата MyCert, который был удален, но не очищен для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="1b273-118">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="1b273-119">Эта команда получает сертификат с именем "MyCert", который ранее был удален, но не очищен, в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="1b273-119">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="1b273-120">Эта команда возвращает метаданные, например дату удаления, и запланированную дату очистки этого удаленного сертификата.</span><span class="sxs-lookup"><span data-stu-id="1b273-120">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="1b273-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1b273-121">PARAMETERS</span></span>

### <span data-ttu-id="1b273-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b273-122">-DefaultProfile</span></span>
<span data-ttu-id="1b273-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1b273-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1b273-124">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="1b273-124">-IncludeVersions</span></span>
<span data-ttu-id="1b273-125">Указывает на то, что эта операция получает все версии сертификата.</span><span class="sxs-lookup"><span data-stu-id="1b273-125">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByCertificateAllVersions, ByCertificateAllVersionsInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b273-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b273-126">-InputObject</span></span>
<span data-ttu-id="1b273-127">Объект KeyVault.</span><span class="sxs-lookup"><span data-stu-id="1b273-127">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByNameInputObject, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b273-128">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="1b273-128">-InRemovedState</span></span>
<span data-ttu-id="1b273-129">Указывает, следует ли включать ранее удаленные сертификаты в выходной файл.</span><span class="sxs-lookup"><span data-stu-id="1b273-129">Specifies whether to include previously deleted certificates in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByName, ByNameInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b273-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1b273-130">-Name</span></span>
<span data-ttu-id="1b273-131">Указывает имя получаемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="1b273-131">Specifies the name of the certificate to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByNameInputObject
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateAllVersions, ByCertificateNameAndVersionInputObject, ByCertificateAllVersionsInputObject
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b273-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1b273-132">-VaultName</span></span>
<span data-ttu-id="1b273-133">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="1b273-133">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByCertificateNameAndVersion, ByCertificateAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b273-134">-Version</span><span class="sxs-lookup"><span data-stu-id="1b273-134">-Version</span></span>
<span data-ttu-id="1b273-135">Определяет версию сертификата.</span><span class="sxs-lookup"><span data-stu-id="1b273-135">Specifies the version of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateNameAndVersion, ByCertificateNameAndVersionInputObject
Aliases: CertificateVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b273-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b273-136">CommonParameters</span></span>
<span data-ttu-id="1b273-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1b273-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b273-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b273-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b273-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1b273-139">INPUTS</span></span>

### <span data-ttu-id="1b273-140">Ничего</span><span class="sxs-lookup"><span data-stu-id="1b273-140">None</span></span>
<span data-ttu-id="1b273-141">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="1b273-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1b273-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b273-142">OUTPUTS</span></span>

### <span data-ttu-id="1b273-143">System. Collections. Generic. List ' 1 [Microsoft. Azure. PSKeyVaultCertificateIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="1b273-143">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem]</span></span>

### <span data-ttu-id="1b273-144">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="1b273-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="1b273-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="1b273-145">NOTES</span></span>

## <span data-ttu-id="1b273-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1b273-146">RELATED LINKS</span></span>

[<span data-ttu-id="1b273-147">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="1b273-147">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="1b273-148">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="1b273-148">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="1b273-149">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="1b273-149">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="1b273-150">Undo-AzureKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="1b273-150">Undo-AzureKeyVaultSecretCertificate</span></span>](./Undo-AzureKeyVaultSecretCertificate.md)
