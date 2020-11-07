---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificate
schema: 2.0.0
ms.openlocfilehash: ed52e229f114666782cb24388db585fd08fa685b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914874"
---
# <span data-ttu-id="a4950-101">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a4950-101">Get-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="a4950-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4950-102">SYNOPSIS</span></span>
<span data-ttu-id="a4950-103">Получает сертификат из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="a4950-103">Gets a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4950-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4950-104">SYNTAX</span></span>

### <span data-ttu-id="a4950-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a4950-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a4950-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="a4950-106">ByCertificateName</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4950-107">ByCertificateVersions</span><span class="sxs-lookup"><span data-stu-id="a4950-107">ByCertificateVersions</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4950-108">ByDeletedCertificates</span><span class="sxs-lookup"><span data-stu-id="a4950-108">ByDeletedCertificates</span></span>
```
Get-AzureKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4950-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4950-109">DESCRIPTION</span></span>
<span data-ttu-id="a4950-110">Командлет **Get-AzureKeyVaultCertificate** получает указанный сертификат или версии сертификата из хранилища ключей в хранилище ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="a4950-110">The **Get-AzureKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="a4950-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4950-111">EXAMPLES</span></span>

### <span data-ttu-id="a4950-112">Пример 1: получение сертификата</span><span class="sxs-lookup"><span data-stu-id="a4950-112">Example 1: Get a certificate</span></span>
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

<span data-ttu-id="a4950-113">Эта команда получает сертификат с именем TestCert01 из хранилища ключей с именем ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="a4950-113">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="a4950-114">Пример 2: получение всех сертификатов, которые были удалены, но не очищены для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="a4950-114">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="a4950-115">Эта команда получает все сертификаты, которые были ранее удалены, но не очищены, в хранилище ключей contoso.</span><span class="sxs-lookup"><span data-stu-id="a4950-115">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="a4950-116">Пример 3: получение сертификата MyCert, который был удален, но не очищен для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="a4950-116">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="a4950-117">Эта команда получает сертификат с именем "MyCert", который ранее был удален, но не очищен, в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="a4950-117">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="a4950-118">Эта команда возвращает метаданные, например дату удаления, и запланированную дату очистки этого удаленного сертификата.</span><span class="sxs-lookup"><span data-stu-id="a4950-118">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="a4950-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4950-119">PARAMETERS</span></span>

### <span data-ttu-id="a4950-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4950-120">-DefaultProfile</span></span>
<span data-ttu-id="a4950-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a4950-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4950-122">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="a4950-122">-IncludeVersions</span></span>
<span data-ttu-id="a4950-123">Указывает на то, что эта операция получает все версии сертификата.</span><span class="sxs-lookup"><span data-stu-id="a4950-123">Indicates that this operation gets all versions of the certificate.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByCertificateVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4950-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="a4950-124">-InRemovedState</span></span>
<span data-ttu-id="a4950-125">Указывает, следует ли включать ранее удаленные сертификаты в выходной файл.</span><span class="sxs-lookup"><span data-stu-id="a4950-125">Specifies whether to include previously deleted certificates in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedCertificates
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4950-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a4950-126">-Name</span></span>
<span data-ttu-id="a4950-127">Указывает имя получаемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="a4950-127">Specifies the name of the certificate to get.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName, ByCertificateVersions
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedCertificates
Aliases: CertificateName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4950-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a4950-128">-VaultName</span></span>
<span data-ttu-id="a4950-129">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="a4950-129">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="a4950-130">-Version</span><span class="sxs-lookup"><span data-stu-id="a4950-130">-Version</span></span>
<span data-ttu-id="a4950-131">Определяет версию сертификата.</span><span class="sxs-lookup"><span data-stu-id="a4950-131">Specifies the version of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName
Aliases: CertificateVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4950-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4950-132">CommonParameters</span></span>
<span data-ttu-id="a4950-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4950-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4950-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4950-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4950-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4950-135">INPUTS</span></span>

## <span data-ttu-id="a4950-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4950-136">OUTPUTS</span></span>

### <span data-ttu-id="a4950-137">System. Collections. Generic. List ' 1 [Microsoft. Azure. CertificateIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="a4950-137">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.CertificateIdentityItem]</span></span>

### <span data-ttu-id="a4950-138">Microsoft. Azure. Commands. KeyVault. Models. KeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a4950-138">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="a4950-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4950-139">NOTES</span></span>

## <span data-ttu-id="a4950-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4950-140">RELATED LINKS</span></span>

[<span data-ttu-id="a4950-141">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a4950-141">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="a4950-142">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a4950-142">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="a4950-143">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="a4950-143">Remove-AzureKeyVaultCertificate</span></span>](./Remove-AzureKeyVaultCertificate.md)


