---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
ms.openlocfilehash: 32a3dbb458c4848a5578309593b205b4ced5be03
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903973"
---
# <span data-ttu-id="e565a-101">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="e565a-101">Remove-AzResourceLock</span></span>

## <span data-ttu-id="e565a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e565a-102">SYNOPSIS</span></span>
<span data-ttu-id="e565a-103">Удаление блокировки ресурса.</span><span class="sxs-lookup"><span data-stu-id="e565a-103">Removes a resource lock.</span></span>

## <span data-ttu-id="e565a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e565a-104">SYNTAX</span></span>

### <span data-ttu-id="e565a-105">ByLockId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e565a-105">ByLockId (Default)</span></span>
```
Remove-AzResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e565a-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e565a-106">ByResourceGroup</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e565a-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="e565a-107">ByResourceGroupLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e565a-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="e565a-108">BySpecifiedScope</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e565a-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="e565a-109">BySubscription</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e565a-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="e565a-110">BySubscriptionLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e565a-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="e565a-111">ByTenantLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String> [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e565a-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e565a-112">DESCRIPTION</span></span>
<span data-ttu-id="e565a-113">Командлет **Remove-AzResourceLock** удаляет блокировку ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="e565a-113">The **Remove-AzResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="e565a-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e565a-114">EXAMPLES</span></span>

### <span data-ttu-id="e565a-115">Пример 1: снятие блокировки</span><span class="sxs-lookup"><span data-stu-id="e565a-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="e565a-116">Эта команда удаляет блокировку с именем ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="e565a-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="e565a-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e565a-117">PARAMETERS</span></span>

### <span data-ttu-id="e565a-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e565a-118">-ApiVersion</span></span>
<span data-ttu-id="e565a-119">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e565a-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e565a-120">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="e565a-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="e565a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e565a-121">-DefaultProfile</span></span>
<span data-ttu-id="e565a-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e565a-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e565a-123">-Force</span><span class="sxs-lookup"><span data-stu-id="e565a-123">-Force</span></span>
<span data-ttu-id="e565a-124">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="e565a-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e565a-125">-LockId</span><span class="sxs-lookup"><span data-stu-id="e565a-125">-LockId</span></span>
<span data-ttu-id="e565a-126">Указывает идентификатор блокировки, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e565a-126">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e565a-127">-LockName</span><span class="sxs-lookup"><span data-stu-id="e565a-127">-LockName</span></span>
<span data-ttu-id="e565a-128">Указывает имя блокировки, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e565a-128">Specifies the name of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e565a-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="e565a-129">-Pre</span></span>
<span data-ttu-id="e565a-130">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="e565a-130">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e565a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e565a-131">-ResourceGroupName</span></span>
<span data-ttu-id="e565a-132">Указывает имя группы ресурсов, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="e565a-132">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="e565a-133">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e565a-133">-ResourceName</span></span>
<span data-ttu-id="e565a-134">Указывает имя ресурса, к которому применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="e565a-134">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="e565a-135">Например, чтобы указать базу данных, используйте следующий формат: `/` база данных сервера</span><span class="sxs-lookup"><span data-stu-id="e565a-135">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="e565a-136">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e565a-136">-ResourceType</span></span>
<span data-ttu-id="e565a-137">Указывает тип ресурса, к которому относится блокировка.</span><span class="sxs-lookup"><span data-stu-id="e565a-137">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="e565a-138">-Scope</span><span class="sxs-lookup"><span data-stu-id="e565a-138">-Scope</span></span>
<span data-ttu-id="e565a-139">Указывает область, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="e565a-139">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="e565a-140">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="e565a-140">-TenantLevel</span></span>
<span data-ttu-id="e565a-141">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="e565a-141">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="e565a-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e565a-142">-Confirm</span></span>
<span data-ttu-id="e565a-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e565a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e565a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e565a-144">-WhatIf</span></span>
<span data-ttu-id="e565a-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e565a-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e565a-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e565a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e565a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e565a-147">CommonParameters</span></span>
<span data-ttu-id="e565a-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e565a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e565a-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e565a-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e565a-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e565a-150">INPUTS</span></span>

### <span data-ttu-id="e565a-151">System. String</span><span class="sxs-lookup"><span data-stu-id="e565a-151">System.String</span></span>

## <span data-ttu-id="e565a-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e565a-152">OUTPUTS</span></span>

### <span data-ttu-id="e565a-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="e565a-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e565a-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="e565a-154">NOTES</span></span>

## <span data-ttu-id="e565a-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e565a-155">RELATED LINKS</span></span>

[<span data-ttu-id="e565a-156">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="e565a-156">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="e565a-157">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="e565a-157">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="e565a-158">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="e565a-158">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


