---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 8932402fb9e4e6b27f284313bfddc764192c5e93
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912239"
---
# <span data-ttu-id="b5efc-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="b5efc-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="b5efc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b5efc-102">SYNOPSIS</span></span>
<span data-ttu-id="b5efc-103">Обновите состояние хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="b5efc-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="b5efc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b5efc-104">SYNTAX</span></span>

### <span data-ttu-id="b5efc-105">UpdateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b5efc-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5efc-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5efc-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5efc-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5efc-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5efc-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5efc-108">DESCRIPTION</span></span>
<span data-ttu-id="b5efc-109">Этот командлет обновляет состояние хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="b5efc-109">This cmdlet updates the state of an Azure key vault.</span></span>
<span data-ttu-id="b5efc-110">Обратите внимание на то, что обновление некоторых свойств является необратимым действием, например, если вы включили функцию обратимого удаления, больше нельзя будет отключить.</span><span class="sxs-lookup"><span data-stu-id="b5efc-110">Please note updating some of the properties is an irreversible action, for example once soft delete has been enabled, it cannot be disabled anymore.</span></span>

## <span data-ttu-id="b5efc-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b5efc-111">EXAMPLES</span></span>

### <span data-ttu-id="b5efc-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b5efc-112">Example 1</span></span>
```powershell
PS C:\> Update-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName -EnableSoftDelete
```

<span data-ttu-id="b5efc-113">Включает обратимое удаление в хранилище ключей, которое называется " `$keyVaultName` Группа ресурсов" `$resourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="b5efc-113">Enables soft delete on the key vault named `$keyVaultName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="b5efc-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b5efc-114">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="b5efc-115">Включает защиту от очистки с помощью синтаксиса трубопроводов.</span><span class="sxs-lookup"><span data-stu-id="b5efc-115">Enables purge protection using piping syntax.</span></span>

## <span data-ttu-id="b5efc-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b5efc-116">PARAMETERS</span></span>

### <span data-ttu-id="b5efc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5efc-117">-DefaultProfile</span></span>
<span data-ttu-id="b5efc-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b5efc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5efc-119">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="b5efc-119">-EnablePurgeProtection</span></span>
<span data-ttu-id="b5efc-120">Включите функцию защиты от очистки для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="b5efc-120">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="b5efc-121">После включения оно не может быть отключено.</span><span class="sxs-lookup"><span data-stu-id="b5efc-121">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="b5efc-122">Для включения требуется мягкое удаление.</span><span class="sxs-lookup"><span data-stu-id="b5efc-122">It requires soft-delete to be turned on.</span></span>

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

### <span data-ttu-id="b5efc-123">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="b5efc-123">-EnableSoftDelete</span></span>
<span data-ttu-id="b5efc-124">Включите функцию мягкого удаления для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="b5efc-124">Enable the soft-delete functionality for this key vault.</span></span>
<span data-ttu-id="b5efc-125">После включения оно не может быть отключено.</span><span class="sxs-lookup"><span data-stu-id="b5efc-125">Once enabled it cannot be disabled.</span></span>

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

### <span data-ttu-id="b5efc-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5efc-126">-InputObject</span></span>
<span data-ttu-id="b5efc-127">Объект хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="b5efc-127">Key vault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5efc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5efc-128">-ResourceGroupName</span></span>
<span data-ttu-id="b5efc-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b5efc-129">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5efc-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5efc-130">-ResourceId</span></span>
<span data-ttu-id="b5efc-131">Идентификатор ресурса для хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="b5efc-131">Resource ID of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5efc-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b5efc-132">-VaultName</span></span>
<span data-ttu-id="b5efc-133">Имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="b5efc-133">Name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: UpdateByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5efc-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5efc-134">-Confirm</span></span>
<span data-ttu-id="b5efc-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b5efc-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5efc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5efc-136">-WhatIf</span></span>
<span data-ttu-id="b5efc-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b5efc-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5efc-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b5efc-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5efc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5efc-139">CommonParameters</span></span>
<span data-ttu-id="b5efc-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b5efc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5efc-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5efc-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5efc-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b5efc-142">INPUTS</span></span>

### <span data-ttu-id="b5efc-143">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="b5efc-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="b5efc-144">System. String</span><span class="sxs-lookup"><span data-stu-id="b5efc-144">System.String</span></span>

## <span data-ttu-id="b5efc-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5efc-145">OUTPUTS</span></span>

### <span data-ttu-id="b5efc-146">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="b5efc-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="b5efc-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="b5efc-147">NOTES</span></span>

## <span data-ttu-id="b5efc-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5efc-148">RELATED LINKS</span></span>
