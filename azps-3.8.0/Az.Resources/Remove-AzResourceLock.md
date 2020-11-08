---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
ms.openlocfilehash: ba740004f22eef1f574d861c44de7e26c7f4594b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066223"
---
# <span data-ttu-id="bd9ff-101">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="bd9ff-101">Remove-AzResourceLock</span></span>

## <span data-ttu-id="bd9ff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bd9ff-102">SYNOPSIS</span></span>
<span data-ttu-id="bd9ff-103">Удаление блокировки ресурса.</span><span class="sxs-lookup"><span data-stu-id="bd9ff-103">Removes a resource lock.</span></span>

## <span data-ttu-id="bd9ff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bd9ff-104">SYNTAX</span></span>

### <span data-ttu-id="bd9ff-105">ByLockId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bd9ff-105">ByLockId (Default)</span></span>
```
Remove-AzResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd9ff-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bd9ff-106">ByResourceGroup</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd9ff-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="bd9ff-107">ByResourceGroupLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd9ff-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="bd9ff-108">BySpecifiedScope</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd9ff-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="bd9ff-109">BySubscription</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd9ff-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="bd9ff-110">BySubscriptionLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd9ff-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="bd9ff-111">ByTenantLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String> [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bd9ff-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd9ff-112">DESCRIPTION</span></span>
<span data-ttu-id="bd9ff-113">Командлет **Remove-AzResourceLock** удаляет блокировку ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="bd9ff-113">The **Remove-AzResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="bd9ff-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bd9ff-114">EXAMPLES</span></span>

### <span data-ttu-id="bd9ff-115">Пример 1: снятие блокировки</span><span class="sxs-lookup"><span data-stu-id="bd9ff-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="bd9ff-116">Эта команда удаляет блокировку с именем ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="bd9ff-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="bd9ff-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bd9ff-117">PARAMETERS</span></span>

### <span data-ttu-id="bd9ff-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bd9ff-118">-ApiVersion</span></span>
<span data-ttu-id="bd9ff-119">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bd9ff-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="bd9ff-120">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="bd9ff-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="bd9ff-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd9ff-121">-DefaultProfile</span></span>
<span data-ttu-id="bd9ff-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bd9ff-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd9ff-123">-Force</span><span class="sxs-lookup"><span data-stu-id="bd9ff-123">-Force</span></span>
<span data-ttu-id="bd9ff-124">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="bd9ff-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bd9ff-125">-LockId</span><span class="sxs-lookup"><span data-stu-id="bd9ff-125">-LockId</span></span>
<span data-ttu-id="bd9ff-126">Указывает идентификатор блокировки, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="bd9ff-126">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bd9ff-127">-LockName</span><span class="sxs-lookup"><span data-stu-id="bd9ff-127">-LockName</span></span>
<span data-ttu-id="bd9ff-128">Указывает имя блокировки, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="bd9ff-128">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9ff-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="bd9ff-129">-Pre</span></span>
<span data-ttu-id="bd9ff-130">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="bd9ff-130">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="bd9ff-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd9ff-131">-ResourceGroupName</span></span>
<span data-ttu-id="bd9ff-132">Указывает имя группы ресурсов, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="bd9ff-132">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="bd9ff-133">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="bd9ff-133">-ResourceName</span></span>
<span data-ttu-id="bd9ff-134">Указывает имя ресурса, к которому применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="bd9ff-134">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="bd9ff-135">Например, чтобы указать базу данных, используйте следующий формат: `/` база данных сервера</span><span class="sxs-lookup"><span data-stu-id="bd9ff-135">For instance, to specify a database, use the following format: Server`/`Database</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9ff-136">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="bd9ff-136">-ResourceType</span></span>
<span data-ttu-id="bd9ff-137">Указывает тип ресурса, к которому относится блокировка.</span><span class="sxs-lookup"><span data-stu-id="bd9ff-137">Specifies the resource type of the resource for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9ff-138">-Scope</span><span class="sxs-lookup"><span data-stu-id="bd9ff-138">-Scope</span></span>
<span data-ttu-id="bd9ff-139">Указывает область, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="bd9ff-139">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="bd9ff-140">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="bd9ff-140">-TenantLevel</span></span>
<span data-ttu-id="bd9ff-141">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="bd9ff-141">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd9ff-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd9ff-142">-Confirm</span></span>
<span data-ttu-id="bd9ff-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bd9ff-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd9ff-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd9ff-144">-WhatIf</span></span>
<span data-ttu-id="bd9ff-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bd9ff-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd9ff-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bd9ff-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd9ff-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd9ff-147">CommonParameters</span></span>
<span data-ttu-id="bd9ff-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bd9ff-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd9ff-149">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd9ff-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd9ff-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bd9ff-150">INPUTS</span></span>

### <span data-ttu-id="bd9ff-151">System. String</span><span class="sxs-lookup"><span data-stu-id="bd9ff-151">System.String</span></span>

## <span data-ttu-id="bd9ff-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd9ff-152">OUTPUTS</span></span>

### <span data-ttu-id="bd9ff-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="bd9ff-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="bd9ff-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="bd9ff-154">NOTES</span></span>

## <span data-ttu-id="bd9ff-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd9ff-155">RELATED LINKS</span></span>

[<span data-ttu-id="bd9ff-156">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="bd9ff-156">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="bd9ff-157">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="bd9ff-157">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="bd9ff-158">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="bd9ff-158">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


