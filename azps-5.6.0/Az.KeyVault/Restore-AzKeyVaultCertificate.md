---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/restore-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultCertificate.md
ms.openlocfilehash: 4af261f10a4d5f3d7228f31b511a092600cb93bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952483"
---
# <span data-ttu-id="5493e-101">Restore-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="5493e-101">Restore-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="5493e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5493e-102">SYNOPSIS</span></span>
<span data-ttu-id="5493e-103">Восстановление сертификата в хранилище ключа из файла резервной копии.</span><span class="sxs-lookup"><span data-stu-id="5493e-103">Restores a certificate in a key vault from a backup file.</span></span>

## <span data-ttu-id="5493e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5493e-104">SYNTAX</span></span>

### <span data-ttu-id="5493e-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5493e-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultCertificate [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5493e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5493e-106">ByInputObject</span></span>
```
Restore-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5493e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5493e-107">ByResourceId</span></span>
```
Restore-AzKeyVaultCertificate [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5493e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5493e-108">DESCRIPTION</span></span>
<span data-ttu-id="5493e-109">При нажатии на **AzKeyVaultCertificate** в указанном хранилище ключа создается сертификат из файла резервной копии.</span><span class="sxs-lookup"><span data-stu-id="5493e-109">The **Restore-AzKeyVaultCertificate** cmdlet creates a certificate in the specified key vault from a backup file.</span></span>
<span data-ttu-id="5493e-110">Этот сертификат является копией архивного сертификата в входной файле с тем же именем, что и у исходного сертификата.</span><span class="sxs-lookup"><span data-stu-id="5493e-110">This certificate is a replica of the backed-up certificate in the input file and has the same name as the original certificate.</span></span>
<span data-ttu-id="5493e-111">Если хранилище ключей уже содержит сертификат с таким же именем, этот cmdlet не может переописать исходный сертификат.</span><span class="sxs-lookup"><span data-stu-id="5493e-111">If the key vault already contains a certificate by the same name, this cmdlet fails instead of overwriting the original certificate.</span></span>
<span data-ttu-id="5493e-112">Если резервная копия содержит несколько версий сертификата, восстанавливаются все версии.</span><span class="sxs-lookup"><span data-stu-id="5493e-112">If the backup contains multiple versions of a certificate, all versions are restored.</span></span>
<span data-ttu-id="5493e-113">Хранилище ключей, в которое вы восстанавливаете сертификат, может быть не таким, как в хранилище ключей, из хранилища, из который был был восстановлен.</span><span class="sxs-lookup"><span data-stu-id="5493e-113">The key vault that you restore the certificate into can be different from the key vault that you backed up the certificate from.</span></span>
<span data-ttu-id="5493e-114">Однако ключ должен использовать ту же подписку и быть в регионе Azure в той же географической области (например, в Северной Америке).</span><span class="sxs-lookup"><span data-stu-id="5493e-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="5493e-115">См. центр управления доверием Microsoft Azure (сопоставление регионов https://azure.microsoft.com/support/trust-center/) Azure с регионами).</span><span class="sxs-lookup"><span data-stu-id="5493e-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="5493e-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5493e-116">EXAMPLES</span></span>

### <span data-ttu-id="5493e-117">Пример 1. Восстановление back-up certificate</span><span class="sxs-lookup"><span data-stu-id="5493e-117">Example 1: Restore a backed-up certificate</span></span>
```powershell
PS C:\> Restore-AzKeyVaultCertificate -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Certificate   : [Subject]
                  CN=contoso.com

                [Issuer]
                  CN=contoso.com

                [Serial Number]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                [Not Before]
                  5/25/2018 3:47:41 AM

                [Not After]
                  11/25/2018 2:57:41 AM

                [Thumbprint]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId         : https://mykeyvault.vault.azure.net:443/keys/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
SecretId      : https://mykeyvault.vault.azure.net:443/secrets/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
Thumbprint    : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel : Purgeable
Enabled       : True
Expires       : 11/25/2018 10:57:41 AM
NotBefore     : 5/25/2018 10:47:41 AM
Created       : 5/25/2018 10:57:41 AM
Updated       : 5/25/2018 10:57:41 AM
Tags          : 
VaultName     : MyKeyVault
Name          : cert1
Version       : bd406f6d6b3a41a1a1c633494d8c3c3a
Id            : https://mykeyvault.vault.azure.net:443/certificates/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
```

<span data-ttu-id="5493e-118">Эта команда восстанавливает сертификат, включая все его версии, из файла резервной копии Backup.blob в хранилище ключа MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="5493e-118">This command restores a certificate, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="5493e-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5493e-119">PARAMETERS</span></span>

### <span data-ttu-id="5493e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5493e-120">-DefaultProfile</span></span>
<span data-ttu-id="5493e-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5493e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5493e-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="5493e-122">-InputFile</span></span>
<span data-ttu-id="5493e-123">Входной файл.</span><span class="sxs-lookup"><span data-stu-id="5493e-123">Input file.</span></span>
<span data-ttu-id="5493e-124">Входной файл, содержащий исходный BLOB-файл</span><span class="sxs-lookup"><span data-stu-id="5493e-124">The input file containing the backed-up blob</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5493e-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5493e-125">-InputObject</span></span>
<span data-ttu-id="5493e-126">Объект KeyVault</span><span class="sxs-lookup"><span data-stu-id="5493e-126">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5493e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5493e-127">-ResourceId</span></span>
<span data-ttu-id="5493e-128">KeyVault Resource Id</span><span class="sxs-lookup"><span data-stu-id="5493e-128">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5493e-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5493e-129">-VaultName</span></span>
<span data-ttu-id="5493e-130">Имя сейфа.</span><span class="sxs-lookup"><span data-stu-id="5493e-130">Vault name.</span></span>
<span data-ttu-id="5493e-131">С его учетом именем и выбранной средой строится FQDN хранилища.</span><span class="sxs-lookup"><span data-stu-id="5493e-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5493e-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5493e-132">-Confirm</span></span>
<span data-ttu-id="5493e-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5493e-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5493e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5493e-134">-WhatIf</span></span>
<span data-ttu-id="5493e-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5493e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5493e-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5493e-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5493e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5493e-137">CommonParameters</span></span>
<span data-ttu-id="5493e-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5493e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5493e-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5493e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5493e-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5493e-140">INPUTS</span></span>

### <span data-ttu-id="5493e-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="5493e-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="5493e-142">System.String</span><span class="sxs-lookup"><span data-stu-id="5493e-142">System.String</span></span>

## <span data-ttu-id="5493e-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5493e-143">OUTPUTS</span></span>

### <span data-ttu-id="5493e-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="5493e-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="5493e-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5493e-145">NOTES</span></span>

## <span data-ttu-id="5493e-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5493e-146">RELATED LINKS</span></span>
