---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
ms.openlocfilehash: 5047ce0ebeb4f93d1d73473edbec50eaf65c6875
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249828"
---
# <span data-ttu-id="53fb2-101">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="53fb2-101">Remove-AzResourceLock</span></span>

## <span data-ttu-id="53fb2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="53fb2-102">SYNOPSIS</span></span>
<span data-ttu-id="53fb2-103">Удаление блокировки ресурса.</span><span class="sxs-lookup"><span data-stu-id="53fb2-103">Removes a resource lock.</span></span>

## <span data-ttu-id="53fb2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="53fb2-104">SYNTAX</span></span>

### <span data-ttu-id="53fb2-105">ByLockId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="53fb2-105">ByLockId (Default)</span></span>
```
Remove-AzResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53fb2-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="53fb2-106">ByResourceGroup</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53fb2-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="53fb2-107">ByResourceGroupLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53fb2-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="53fb2-108">BySpecifiedScope</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53fb2-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="53fb2-109">BySubscription</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53fb2-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="53fb2-110">BySubscriptionLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="53fb2-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="53fb2-111">DESCRIPTION</span></span>
<span data-ttu-id="53fb2-112">Командлет **Remove-AzResourceLock** удаляет блокировку ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="53fb2-112">The **Remove-AzResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="53fb2-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="53fb2-113">EXAMPLES</span></span>

### <span data-ttu-id="53fb2-114">Пример 1: снятие блокировки</span><span class="sxs-lookup"><span data-stu-id="53fb2-114">Example 1: Remove a lock</span></span>
```powershell
PS C:\>Remove-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="53fb2-115">Эта команда удаляет блокировку с именем ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="53fb2-115">This command removes the lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="53fb2-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="53fb2-116">Example 2</span></span>

<span data-ttu-id="53fb2-117">Удаление блокировки ресурса.</span><span class="sxs-lookup"><span data-stu-id="53fb2-117">Removes a resource lock.</span></span> <span data-ttu-id="53fb2-118">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="53fb2-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
Remove-AzResourceLock -LockName 'ContosoSiteLock' -ResourceGroupName myresourcegroup -ResourceName '/subscriptions/00000000-0000-0000-0000-00000000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test' -ResourceType 'Microsoft.ClassicCompute/storageAccounts'
```

## <span data-ttu-id="53fb2-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="53fb2-119">PARAMETERS</span></span>

### <span data-ttu-id="53fb2-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="53fb2-120">-ApiVersion</span></span>
<span data-ttu-id="53fb2-121">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="53fb2-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="53fb2-122">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="53fb2-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53fb2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53fb2-123">-DefaultProfile</span></span>
<span data-ttu-id="53fb2-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="53fb2-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53fb2-125">-Force</span><span class="sxs-lookup"><span data-stu-id="53fb2-125">-Force</span></span>
<span data-ttu-id="53fb2-126">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="53fb2-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="53fb2-127">-LockId</span><span class="sxs-lookup"><span data-stu-id="53fb2-127">-LockId</span></span>
<span data-ttu-id="53fb2-128">Указывает идентификатор блокировки, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="53fb2-128">Specifies the ID of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53fb2-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="53fb2-129">-LockName</span></span>
<span data-ttu-id="53fb2-130">Указывает имя блокировки, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="53fb2-130">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53fb2-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="53fb2-131">-Pre</span></span>
<span data-ttu-id="53fb2-132">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="53fb2-132">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="53fb2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53fb2-133">-ResourceGroupName</span></span>
<span data-ttu-id="53fb2-134">Указывает имя группы ресурсов, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="53fb2-134">Specifies the name of the resource group for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53fb2-135">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="53fb2-135">-ResourceName</span></span>
<span data-ttu-id="53fb2-136">Указывает имя ресурса, к которому применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="53fb2-136">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="53fb2-137">Например, чтобы указать базу данных, используйте следующий формат: `/` база данных сервера</span><span class="sxs-lookup"><span data-stu-id="53fb2-137">For instance, to specify a database, use the following format: Server`/`Database</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53fb2-138">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="53fb2-138">-ResourceType</span></span>
<span data-ttu-id="53fb2-139">Указывает тип ресурса, к которому относится блокировка.</span><span class="sxs-lookup"><span data-stu-id="53fb2-139">Specifies the resource type of the resource for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53fb2-140">-Scope</span><span class="sxs-lookup"><span data-stu-id="53fb2-140">-Scope</span></span>
<span data-ttu-id="53fb2-141">Указывает область, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="53fb2-141">Specifies the scope to which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53fb2-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53fb2-142">-Confirm</span></span>
<span data-ttu-id="53fb2-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="53fb2-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53fb2-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53fb2-144">-WhatIf</span></span>
<span data-ttu-id="53fb2-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="53fb2-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53fb2-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="53fb2-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53fb2-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53fb2-147">CommonParameters</span></span>
<span data-ttu-id="53fb2-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="53fb2-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53fb2-149">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53fb2-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53fb2-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="53fb2-150">INPUTS</span></span>

### <span data-ttu-id="53fb2-151">System. String</span><span class="sxs-lookup"><span data-stu-id="53fb2-151">System.String</span></span>

## <span data-ttu-id="53fb2-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="53fb2-152">OUTPUTS</span></span>

### <span data-ttu-id="53fb2-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="53fb2-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="53fb2-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="53fb2-154">NOTES</span></span>

## <span data-ttu-id="53fb2-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="53fb2-155">RELATED LINKS</span></span>

[<span data-ttu-id="53fb2-156">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="53fb2-156">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="53fb2-157">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="53fb2-157">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="53fb2-158">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="53fb2-158">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


