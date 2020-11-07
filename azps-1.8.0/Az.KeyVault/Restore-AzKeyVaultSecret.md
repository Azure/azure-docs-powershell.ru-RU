---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
ms.openlocfilehash: 9fb79628b123b5d35ae5d55ba31fd07dcbd85775
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900130"
---
# <span data-ttu-id="176f4-101">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="176f4-101">Restore-AzKeyVaultSecret</span></span>

## <span data-ttu-id="176f4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="176f4-102">SYNOPSIS</span></span>
<span data-ttu-id="176f4-103">Создает секретный ключ из резервного хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="176f4-103">Creates a secret in a key vault from a backed-up secret.</span></span>

## <span data-ttu-id="176f4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="176f4-104">SYNTAX</span></span>

### <span data-ttu-id="176f4-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="176f4-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultSecret [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="176f4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="176f4-106">ByInputObject</span></span>
```
Restore-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="176f4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="176f4-107">ByResourceId</span></span>
```
Restore-AzKeyVaultSecret [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="176f4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="176f4-108">DESCRIPTION</span></span>
<span data-ttu-id="176f4-109">Командлет **RESTORE-AzKeyVaultSecret** создает секрет в указанном хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="176f4-109">The **Restore-AzKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="176f4-110">Этот секрет — это реплика резервного файла в файле входных данных с тем же именем, что и у первоначального секрета.</span><span class="sxs-lookup"><span data-stu-id="176f4-110">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="176f4-111">Если в хранилище ключей уже есть секрет с тем же именем, этот командлет не будет работать вместо перезаписи исходного секрета.</span><span class="sxs-lookup"><span data-stu-id="176f4-111">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="176f4-112">Если резервная копия имеет несколько версий секрета, восстанавливаются все версии.</span><span class="sxs-lookup"><span data-stu-id="176f4-112">If the backup contains multiple versions of a secret, all versions are restored.</span></span>
<span data-ttu-id="176f4-113">Хранилище ключей, в которое вы восстановите секретный ключ, может отличаться от того, с помощью которого вы заархивированы из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="176f4-113">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="176f4-114">Тем не менее, в одном и том же географическом хранилище вы должны использовать одну и ту же подписку, а также находиться в регионе Azure (например, в Северной Америке).</span><span class="sxs-lookup"><span data-stu-id="176f4-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="176f4-115">Просмотрите центр управления безопасностью Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) для сопоставления областей Azure с географией).</span><span class="sxs-lookup"><span data-stu-id="176f4-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="176f4-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="176f4-116">EXAMPLES</span></span>

### <span data-ttu-id="176f4-117">Пример 1: восстановление резервной копии (секретной)</span><span class="sxs-lookup"><span data-stu-id="176f4-117">Example 1: Restore a backed-up secret</span></span>
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

<span data-ttu-id="176f4-118">Эта команда восстанавливает секрет, в том числе все его версии, из файла резервной копии с именем Backup. BLOB в хранилище ключей, именуемое contoso.</span><span class="sxs-lookup"><span data-stu-id="176f4-118">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named contoso.</span></span>

## <span data-ttu-id="176f4-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="176f4-119">PARAMETERS</span></span>

### <span data-ttu-id="176f4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="176f4-120">-DefaultProfile</span></span>
<span data-ttu-id="176f4-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="176f4-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="176f4-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="176f4-122">-InputFile</span></span>
<span data-ttu-id="176f4-123">Задает входной файл, содержащий резервную копию секрета для восстановления.</span><span class="sxs-lookup"><span data-stu-id="176f4-123">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="176f4-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="176f4-124">-InputObject</span></span>
<span data-ttu-id="176f4-125">Объект KeyVault</span><span class="sxs-lookup"><span data-stu-id="176f4-125">KeyVault object</span></span>

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

### <span data-ttu-id="176f4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="176f4-126">-ResourceId</span></span>
<span data-ttu-id="176f4-127">Идентификатор ресурса KeyVault</span><span class="sxs-lookup"><span data-stu-id="176f4-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="176f4-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="176f4-128">-VaultName</span></span>
<span data-ttu-id="176f4-129">Указывает имя хранилища ключей, в которое нужно восстановить секретный код.</span><span class="sxs-lookup"><span data-stu-id="176f4-129">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="176f4-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="176f4-130">-Confirm</span></span>
<span data-ttu-id="176f4-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="176f4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="176f4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="176f4-132">-WhatIf</span></span>
<span data-ttu-id="176f4-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="176f4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="176f4-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="176f4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="176f4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="176f4-135">CommonParameters</span></span>
<span data-ttu-id="176f4-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="176f4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="176f4-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="176f4-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="176f4-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="176f4-138">INPUTS</span></span>

### <span data-ttu-id="176f4-139">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="176f4-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="176f4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="176f4-140">System.String</span></span>

## <span data-ttu-id="176f4-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="176f4-141">OUTPUTS</span></span>

### <span data-ttu-id="176f4-142">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="176f4-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="176f4-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="176f4-143">NOTES</span></span>

## <span data-ttu-id="176f4-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="176f4-144">RELATED LINKS</span></span>

[<span data-ttu-id="176f4-145">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="176f4-145">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="176f4-146">Backup-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="176f4-146">Backup-AzKeyVaultSecret</span></span>](./Backup-AzKeyVaultSecret.md)

[<span data-ttu-id="176f4-147">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="176f4-147">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="176f4-148">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="176f4-148">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

