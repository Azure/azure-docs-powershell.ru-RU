---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 363FA51E-D075-4800-A4BE-BFF63FD25C90
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificate.md
ms.openlocfilehash: 40514bdd6ed8d37679d3002f80146e622a0614e9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910307"
---
# <span data-ttu-id="c54a3-101">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="c54a3-101">Get-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="c54a3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c54a3-102">SYNOPSIS</span></span>
<span data-ttu-id="c54a3-103">Получает сертификат из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="c54a3-103">Gets a certificate from a key vault.</span></span>

## <span data-ttu-id="c54a3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c54a3-104">SYNTAX</span></span>

### <span data-ttu-id="c54a3-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c54a3-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c54a3-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="c54a3-106">ByCertificateName</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c54a3-107">ByCertificateVersions</span><span class="sxs-lookup"><span data-stu-id="c54a3-107">ByCertificateVersions</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c54a3-108">ByDeletedCertificates</span><span class="sxs-lookup"><span data-stu-id="c54a3-108">ByDeletedCertificates</span></span>
```
Get-AzKeyVaultCertificate [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c54a3-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c54a3-109">DESCRIPTION</span></span>
<span data-ttu-id="c54a3-110">Командлет **Get-AzKeyVaultCertificate** получает указанный сертификат или версии сертификата из хранилища ключей в хранилище ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="c54a3-110">The **Get-AzKeyVaultCertificate** cmdlet gets the specified certificate or the versions of a certificate from a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="c54a3-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c54a3-111">EXAMPLES</span></span>

### <span data-ttu-id="c54a3-112">Пример 1: получение сертификата</span><span class="sxs-lookup"><span data-stu-id="c54a3-112">Example 1: Get a certificate</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
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

<span data-ttu-id="c54a3-113">Эта команда получает сертификат с именем TestCert01 из хранилища ключей с именем ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="c54a3-113">This command gets the certificate named TestCert01 from the key vault named ContosoKV01.</span></span>

### <span data-ttu-id="c54a3-114">Пример 2: получение всех сертификатов, которые были удалены, но не очищены для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="c54a3-114">Example 2: Get all the certificates that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="c54a3-115">Эта команда получает все сертификаты, которые были ранее удалены, но не очищены, в хранилище ключей contoso.</span><span class="sxs-lookup"><span data-stu-id="c54a3-115">This command gets all the certificates that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="c54a3-116">Пример 3: получение сертификата MyCert, который был удален, но не очищен для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="c54a3-116">Example 3: Gets the certificate MyCert that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="c54a3-117">Эта команда получает сертификат с именем "MyCert", который ранее был удален, но не очищен, в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="c54a3-117">This command gets the certificate named 'MyCert' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="c54a3-118">Эта команда возвращает метаданные, например дату удаления, и запланированную дату очистки этого удаленного сертификата.</span><span class="sxs-lookup"><span data-stu-id="c54a3-118">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted certificate.</span></span>

## <span data-ttu-id="c54a3-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c54a3-119">PARAMETERS</span></span>

### <span data-ttu-id="c54a3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c54a3-120">-DefaultProfile</span></span>
<span data-ttu-id="c54a3-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c54a3-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c54a3-122">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="c54a3-122">-IncludeVersions</span></span>
<span data-ttu-id="c54a3-123">Указывает на то, что эта операция получает все версии сертификата.</span><span class="sxs-lookup"><span data-stu-id="c54a3-123">Indicates that this operation gets all versions of the certificate.</span></span>

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

### <span data-ttu-id="c54a3-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="c54a3-124">-InRemovedState</span></span>
<span data-ttu-id="c54a3-125">Указывает, следует ли включать ранее удаленные сертификаты в выходной файл.</span><span class="sxs-lookup"><span data-stu-id="c54a3-125">Specifies whether to include previously deleted certificates in the output</span></span>

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

### <span data-ttu-id="c54a3-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c54a3-126">-Name</span></span>
<span data-ttu-id="c54a3-127">Указывает имя получаемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="c54a3-127">Specifies the name of the certificate to get.</span></span>

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

### <span data-ttu-id="c54a3-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c54a3-128">-VaultName</span></span>
<span data-ttu-id="c54a3-129">Указывает имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="c54a3-129">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="c54a3-130">-Version</span><span class="sxs-lookup"><span data-stu-id="c54a3-130">-Version</span></span>
<span data-ttu-id="c54a3-131">Определяет версию сертификата.</span><span class="sxs-lookup"><span data-stu-id="c54a3-131">Specifies the version of a certificate.</span></span>

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

### <span data-ttu-id="c54a3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c54a3-132">CommonParameters</span></span>
<span data-ttu-id="c54a3-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c54a3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c54a3-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c54a3-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c54a3-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c54a3-135">INPUTS</span></span>

### <span data-ttu-id="c54a3-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="c54a3-136">None</span></span>
<span data-ttu-id="c54a3-137">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="c54a3-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c54a3-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c54a3-138">OUTPUTS</span></span>

### <span data-ttu-id="c54a3-139">System. Collections. Generic. List ' 1 [Microsoft. Azure. CertificateIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="c54a3-139">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.CertificateIdentityItem]</span></span>

### <span data-ttu-id="c54a3-140">Microsoft. Azure. Commands. KeyVault. Models. KeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="c54a3-140">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="c54a3-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="c54a3-141">NOTES</span></span>

## <span data-ttu-id="c54a3-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c54a3-142">RELATED LINKS</span></span>

[<span data-ttu-id="c54a3-143">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="c54a3-143">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="c54a3-144">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="c54a3-144">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="c54a3-145">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="c54a3-145">Remove-AzKeyVaultCertificate</span></span>](./Remove-AzKeyVaultCertificate.md)

[<span data-ttu-id="c54a3-146">Undo-AzKeyVaultSecretCertificate</span><span class="sxs-lookup"><span data-stu-id="c54a3-146">Undo-AzKeyVaultSecretCertificate</span></span>](./Undo-AzKeyVaultSecretCertificate.md)
