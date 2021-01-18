---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
ms.openlocfilehash: 5a00bab81cad7b77873459ab58615a2836970b09
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507192"
---
# <span data-ttu-id="a51b7-101">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a51b7-101">Restore-AzKeyVaultSecret</span></span>

## <span data-ttu-id="a51b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a51b7-102">SYNOPSIS</span></span>
<span data-ttu-id="a51b7-103">Создает секрет в хранилище ключей из back-up secret.</span><span class="sxs-lookup"><span data-stu-id="a51b7-103">Creates a secret in a key vault from a backed-up secret.</span></span>

## <span data-ttu-id="a51b7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a51b7-104">SYNTAX</span></span>

### <span data-ttu-id="a51b7-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a51b7-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultSecret [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a51b7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a51b7-106">ByInputObject</span></span>
```
Restore-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a51b7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a51b7-107">ByResourceId</span></span>
```
Restore-AzKeyVaultSecret [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a51b7-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a51b7-108">DESCRIPTION</span></span>
<span data-ttu-id="a51b7-109">С **его нажатием** можно создать секрет в указанном хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="a51b7-109">The **Restore-AzKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="a51b7-110">Эта секретная является репликой архивной секретной части входного файла и имеет то же имя, что и у исходной секретной.</span><span class="sxs-lookup"><span data-stu-id="a51b7-110">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="a51b7-111">Если в хранилище ключей уже есть секрет с таким же именем, сбой, а не переописывание исходной секретности.</span><span class="sxs-lookup"><span data-stu-id="a51b7-111">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="a51b7-112">Если резервное копирование содержит несколько версий секрета, восстанавливаются все версии.</span><span class="sxs-lookup"><span data-stu-id="a51b7-112">If the backup contains multiple versions of a secret, all versions are restored.</span></span>
<span data-ttu-id="a51b7-113">Хранилище ключей, в которое вы восстанавливаете секрет, может быть не таким, как в хранилище ключей, в который вы его добавили.</span><span class="sxs-lookup"><span data-stu-id="a51b7-113">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="a51b7-114">Однако ключ должен использовать ту же подписку и быть в регионе Azure в той же географической области (например, в Северной Америке).</span><span class="sxs-lookup"><span data-stu-id="a51b7-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="a51b7-115">См. центр управления доверием Microsoft Azure (сопоставление регионов https://azure.microsoft.com/support/trust-center/) Azure с регионами).</span><span class="sxs-lookup"><span data-stu-id="a51b7-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="a51b7-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a51b7-116">EXAMPLES</span></span>

### <span data-ttu-id="a51b7-117">Пример 1. Восстановление back-up secret</span><span class="sxs-lookup"><span data-stu-id="a51b7-117">Example 1: Restore a backed-up secret</span></span>
```powershell
PS C:\> Restore-AzKeyVaultSecret -VaultName 'contoso' -InputFile "C:\Backup.blob"

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :
```

<span data-ttu-id="a51b7-118">Эта команда восстанавливает секрет из файла резервной копии с именем Backup.blob в хранилище ключей contoso, включая все его версии.</span><span class="sxs-lookup"><span data-stu-id="a51b7-118">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named contoso.</span></span>

## <span data-ttu-id="a51b7-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a51b7-119">PARAMETERS</span></span>

### <span data-ttu-id="a51b7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a51b7-120">-DefaultProfile</span></span>
<span data-ttu-id="a51b7-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a51b7-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a51b7-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="a51b7-122">-InputFile</span></span>
<span data-ttu-id="a51b7-123">Определяет входной файл, содержащий резервную копию секретного файла, который нужно восстановить.</span><span class="sxs-lookup"><span data-stu-id="a51b7-123">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="a51b7-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a51b7-124">-InputObject</span></span>
<span data-ttu-id="a51b7-125">Объект KeyVault</span><span class="sxs-lookup"><span data-stu-id="a51b7-125">KeyVault object</span></span>

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

### <span data-ttu-id="a51b7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a51b7-126">-ResourceId</span></span>
<span data-ttu-id="a51b7-127">KeyVault Resource Id</span><span class="sxs-lookup"><span data-stu-id="a51b7-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="a51b7-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a51b7-128">-VaultName</span></span>
<span data-ttu-id="a51b7-129">Указывает имя ключного сейфа, в который нужно восстановить секрет.</span><span class="sxs-lookup"><span data-stu-id="a51b7-129">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="a51b7-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a51b7-130">-Confirm</span></span>
<span data-ttu-id="a51b7-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a51b7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a51b7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a51b7-132">-WhatIf</span></span>
<span data-ttu-id="a51b7-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a51b7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a51b7-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a51b7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a51b7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a51b7-135">CommonParameters</span></span>
<span data-ttu-id="a51b7-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a51b7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a51b7-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a51b7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a51b7-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a51b7-138">INPUTS</span></span>

### <span data-ttu-id="a51b7-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="a51b7-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="a51b7-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a51b7-140">System.String</span></span>

## <span data-ttu-id="a51b7-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a51b7-141">OUTPUTS</span></span>

### <span data-ttu-id="a51b7-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a51b7-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="a51b7-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a51b7-143">NOTES</span></span>

## <span data-ttu-id="a51b7-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a51b7-144">RELATED LINKS</span></span>

[<span data-ttu-id="a51b7-145">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a51b7-145">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="a51b7-146">Backup-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a51b7-146">Backup-AzKeyVaultSecret</span></span>](./Backup-AzKeyVaultSecret.md)

[<span data-ttu-id="a51b7-147">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a51b7-147">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="a51b7-148">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a51b7-148">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

