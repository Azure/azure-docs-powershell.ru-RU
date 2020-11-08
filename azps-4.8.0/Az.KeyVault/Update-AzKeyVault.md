---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 4302f2f9c4c2d6b2c7afa879fc28e2ff4edbb592
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236171"
---
# <span data-ttu-id="888ca-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="888ca-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="888ca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="888ca-102">SYNOPSIS</span></span>
<span data-ttu-id="888ca-103">Обновите состояние хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="888ca-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="888ca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="888ca-104">SYNTAX</span></span>

### <span data-ttu-id="888ca-105">UpdateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="888ca-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-SoftDeleteRetentionInDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="888ca-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="888ca-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-SoftDeleteRetentionInDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="888ca-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="888ca-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-SoftDeleteRetentionInDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="888ca-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="888ca-108">DESCRIPTION</span></span>
<span data-ttu-id="888ca-109">Этот командлет обновляет состояние хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="888ca-109">This cmdlet updates the state of an Azure key vault.</span></span>
<span data-ttu-id="888ca-110">Обратите внимание на то, что обновление некоторых свойств является необратимым действием, например, если вы включили функцию обратимого удаления, больше нельзя будет отключить.</span><span class="sxs-lookup"><span data-stu-id="888ca-110">Please note updating some of the properties is an irreversible action, for example once soft delete has been enabled, it cannot be disabled anymore.</span></span>

## <span data-ttu-id="888ca-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="888ca-111">EXAMPLES</span></span>

### <span data-ttu-id="888ca-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="888ca-112">Example 1</span></span>
```powershell
PS C:\> Update-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName -EnableSoftDelete
```

<span data-ttu-id="888ca-113">Включает обратимое удаление в хранилище ключей, которое называется " `$keyVaultName` Группа ресурсов" `$resourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="888ca-113">Enables soft delete on the key vault named `$keyVaultName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="888ca-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="888ca-114">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="888ca-115">Включает защиту от очистки с помощью синтаксиса трубопроводов.</span><span class="sxs-lookup"><span data-stu-id="888ca-115">Enables purge protection using piping syntax.</span></span>

## <span data-ttu-id="888ca-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="888ca-116">PARAMETERS</span></span>

### <span data-ttu-id="888ca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="888ca-117">-DefaultProfile</span></span>
<span data-ttu-id="888ca-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="888ca-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="888ca-119">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="888ca-119">-EnablePurgeProtection</span></span>
<span data-ttu-id="888ca-120">Включите функцию защиты от очистки для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="888ca-120">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="888ca-121">После включения оно не может быть отключено.</span><span class="sxs-lookup"><span data-stu-id="888ca-121">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="888ca-122">Для включения требуется мягкое удаление.</span><span class="sxs-lookup"><span data-stu-id="888ca-122">It requires soft-delete to be turned on.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="888ca-123">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="888ca-123">-EnableRbacAuthorization</span></span>
<span data-ttu-id="888ca-124">Включение и отключение этого хранилища ключей для авторизации действий с данными с помощью управления доступом на основе ролей (RBAC).</span><span class="sxs-lookup"><span data-stu-id="888ca-124">Enable or disable this key vault to authorize data actions by Role Based Access Control (RBAC).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="888ca-125">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="888ca-125">-EnableSoftDelete</span></span>
<span data-ttu-id="888ca-126">Включите функцию мягкого удаления для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="888ca-126">Enable the soft-delete functionality for this key vault.</span></span>
<span data-ttu-id="888ca-127">После включения оно не может быть отключено.</span><span class="sxs-lookup"><span data-stu-id="888ca-127">Once enabled it cannot be disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="888ca-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="888ca-128">-InputObject</span></span>
<span data-ttu-id="888ca-129">Объект хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="888ca-129">Key vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="888ca-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="888ca-130">-ResourceGroupName</span></span>
<span data-ttu-id="888ca-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="888ca-131">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="888ca-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="888ca-132">-ResourceId</span></span>
<span data-ttu-id="888ca-133">Идентификатор ресурса для хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="888ca-133">Resource ID of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="888ca-134">-SoftDeleteRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="888ca-134">-SoftDeleteRetentionInDays</span></span>
<span data-ttu-id="888ca-135">Указывает, как долго будут храниться удаленные ресурсы, а также как долго, пока не будет очищено хранилище или объект в удаленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="888ca-135">Specifies how long deleted resources are retained, and how long until a vault or an object in the deleted state can be purged.</span></span> <span data-ttu-id="888ca-136">Значение по умолчанию — 90 дней.</span><span class="sxs-lookup"><span data-stu-id="888ca-136">The default is 90 days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="888ca-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="888ca-137">-VaultName</span></span>
<span data-ttu-id="888ca-138">Имя хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="888ca-138">Name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="888ca-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="888ca-139">-Confirm</span></span>
<span data-ttu-id="888ca-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="888ca-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="888ca-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="888ca-141">-WhatIf</span></span>
<span data-ttu-id="888ca-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="888ca-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="888ca-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="888ca-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="888ca-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="888ca-144">CommonParameters</span></span>
<span data-ttu-id="888ca-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="888ca-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="888ca-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="888ca-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="888ca-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="888ca-147">INPUTS</span></span>

### <span data-ttu-id="888ca-148">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="888ca-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="888ca-149">System. String</span><span class="sxs-lookup"><span data-stu-id="888ca-149">System.String</span></span>

## <span data-ttu-id="888ca-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="888ca-150">OUTPUTS</span></span>

### <span data-ttu-id="888ca-151">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="888ca-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="888ca-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="888ca-152">NOTES</span></span>

## <span data-ttu-id="888ca-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="888ca-153">RELATED LINKS</span></span>
