---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificate.md
ms.openlocfilehash: dd87a5b9abf6126fee71bbc308ec3a985c9da9de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735168"
---
# <span data-ttu-id="1cdbe-101">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="1cdbe-101">Get-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="1cdbe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1cdbe-102">SYNOPSIS</span></span>
<span data-ttu-id="1cdbe-103">Получает сертификат из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="1cdbe-103">Gets a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1cdbe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1cdbe-104">SYNTAX</span></span>

### <span data-ttu-id="1cdbe-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1cdbe-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1cdbe-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="1cdbe-106">ByCertificateName</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1cdbe-107">ByCertificateVersions</span><span class="sxs-lookup"><span data-stu-id="1cdbe-107">ByCertificateVersions</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1cdbe-108">ByDeletedCertificates</span><span class="sxs-lookup"><span data-stu-id="1cdbe-108">ByDeletedCertificates</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1cdbe-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1cdbe-109">DESCRIPTION</span></span>
<span data-ttu-id="1cdbe-110">Командлет **Get-AzureKeyVaultCertificate** получает указанный сертификат или версии сертификата из хранилища ключей в хранилище ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="1cdbe-110">The **Get-AzureKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="1cdbe-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1cdbe-111">EXAMPLES</span></span>

### <span data-ttu-id="1cdbe-112">Пример 1: получение сертификата</span><span class="sxs-lookup"><span data-stu-id="1cdbe-112">Example 1: Get a certificate</span></span>
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

<span data-ttu-id="1cdbe-113">Эта команда получает сертификат с именем TestCert01 из хранилища ключей с именем ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="1cdbe-113">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="1cdbe-114">Пример 2: получение всех сертификатов, которые были удалены, но не очищены для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="1cdbe-114">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="1cdbe-115">Эта команда получает все сертификаты, которые были ранее удалены, но не очищены, в хранилище ключей contoso.</span><span class="sxs-lookup"><span data-stu-id="1cdbe-115">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="1cdbe-116">Пример 3: получение сертификата MyCert, который был удален, но не очищен для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="1cdbe-116">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="1cdbe-117">Эта команда получает сертификат с именем "MyCert", который ранее был удален, но не очищен, в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="1cdbe-117">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="1cdbe-118">Эта команда возвращает метаданные, например дату удаления, и запланированную дату очистки этого удаленного сертификата.</span><span class="sxs-lookup"><span data-stu-id="1cdbe-118">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="1cdbe-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1cdbe-119">PARAMETERS</span></span>

### <span data-ttu-id="1cdbe-120">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="1cdbe-120">-IncludeVersions</span></span>
<span data-ttu-id="1cdbe-121">Указывает на то, что эта операция получает все версии сертификата.</span><span class="sxs-lookup"><span data-stu-id="1cdbe-121">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByCertificateVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cdbe-122">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="1cdbe-122">-InRemovedState</span></span>
<span data-ttu-id="1cdbe-123">Указывает, следует ли включать в выходные данные ранее удаленные сертификаты.</span><span class="sxs-lookup"><span data-stu-id="1cdbe-123">Specifies whether to include previously deleted certificates in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedCertificates
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cdbe-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1cdbe-124">-Name</span></span>
<span data-ttu-id="1cdbe-125">Указывает имя получаемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="1cdbe-125">Specifies the name of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName, ByCertificateVersions
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedCertificates
Aliases: CertificateName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cdbe-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1cdbe-126">-VaultName</span></span>
<span data-ttu-id="1cdbe-127">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="1cdbe-127">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cdbe-128">-Version</span><span class="sxs-lookup"><span data-stu-id="1cdbe-128">-Version</span></span>
<span data-ttu-id="1cdbe-129">Определяет версию сертификата.</span><span class="sxs-lookup"><span data-stu-id="1cdbe-129">Specifies the version of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases: CertificateVersion

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cdbe-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cdbe-130">-DefaultProfile</span></span>
<span data-ttu-id="1cdbe-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1cdbe-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cdbe-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cdbe-132">CommonParameters</span></span>
<span data-ttu-id="1cdbe-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1cdbe-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cdbe-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cdbe-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cdbe-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1cdbe-135">INPUTS</span></span>

## <span data-ttu-id="1cdbe-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1cdbe-136">OUTPUTS</span></span>

### <span data-ttu-id="1cdbe-137">System. Collections. Generic. List ' 1 [Microsoft. Azure. CertificateIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="1cdbe-137">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.CertificateIdentityItem]</span></span>

### <span data-ttu-id="1cdbe-138">Microsoft. Azure. Commands. KeyVault. Models. KeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="1cdbe-138">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="1cdbe-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="1cdbe-139">NOTES</span></span>

## <span data-ttu-id="1cdbe-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1cdbe-140">RELATED LINKS</span></span>

[<span data-ttu-id="1cdbe-141">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="1cdbe-141">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="1cdbe-142">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="1cdbe-142">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="1cdbe-143">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="1cdbe-143">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)

[<span data-ttu-id="1cdbe-144">Undo-AzureKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="1cdbe-144">Undo-AzureKeyVaultSecretCertificate</span></span>](./Undo-AzureKeyVaultSecretCertificate.md)
