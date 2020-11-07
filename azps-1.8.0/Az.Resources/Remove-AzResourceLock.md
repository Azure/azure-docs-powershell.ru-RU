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
ms.locfileid: "93729331"
---
# <span data-ttu-id="89baa-101">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="89baa-101">Remove-AzResourceLock</span></span>

## <span data-ttu-id="89baa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="89baa-102">SYNOPSIS</span></span>
<span data-ttu-id="89baa-103">Удаление блокировки ресурса.</span><span class="sxs-lookup"><span data-stu-id="89baa-103">Removes a resource lock.</span></span>

## <span data-ttu-id="89baa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="89baa-104">SYNTAX</span></span>

### <span data-ttu-id="89baa-105">ByLockId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="89baa-105">ByLockId (Default)</span></span>
```
Remove-AzResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89baa-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="89baa-106">ByResourceGroup</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89baa-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="89baa-107">ByResourceGroupLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89baa-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="89baa-108">BySpecifiedScope</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89baa-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="89baa-109">BySubscription</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89baa-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="89baa-110">BySubscriptionLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="89baa-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="89baa-111">ByTenantLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String> [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89baa-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89baa-112">DESCRIPTION</span></span>
<span data-ttu-id="89baa-113">Командлет **Remove-AzResourceLock** удаляет блокировку ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="89baa-113">The **Remove-AzResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="89baa-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="89baa-114">EXAMPLES</span></span>

### <span data-ttu-id="89baa-115">Пример 1: снятие блокировки</span><span class="sxs-lookup"><span data-stu-id="89baa-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="89baa-116">Эта команда удаляет блокировку с именем ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="89baa-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="89baa-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="89baa-117">PARAMETERS</span></span>

### <span data-ttu-id="89baa-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="89baa-118">-ApiVersion</span></span>
<span data-ttu-id="89baa-119">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="89baa-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="89baa-120">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="89baa-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="89baa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89baa-121">-DefaultProfile</span></span>
<span data-ttu-id="89baa-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="89baa-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="89baa-123">-Force</span><span class="sxs-lookup"><span data-stu-id="89baa-123">-Force</span></span>
<span data-ttu-id="89baa-124">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="89baa-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="89baa-125">-LockId</span><span class="sxs-lookup"><span data-stu-id="89baa-125">-LockId</span></span>
<span data-ttu-id="89baa-126">Указывает идентификатор блокировки, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="89baa-126">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="89baa-127">-LockName</span><span class="sxs-lookup"><span data-stu-id="89baa-127">-LockName</span></span>
<span data-ttu-id="89baa-128">Указывает имя блокировки, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="89baa-128">Specifies the name of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="89baa-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="89baa-129">-Pre</span></span>
<span data-ttu-id="89baa-130">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="89baa-130">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="89baa-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89baa-131">-ResourceGroupName</span></span>
<span data-ttu-id="89baa-132">Указывает имя группы ресурсов, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="89baa-132">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="89baa-133">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="89baa-133">-ResourceName</span></span>
<span data-ttu-id="89baa-134">Указывает имя ресурса, к которому применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="89baa-134">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="89baa-135">Например, чтобы указать базу данных, используйте следующий формат: `/` база данных сервера</span><span class="sxs-lookup"><span data-stu-id="89baa-135">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="89baa-136">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="89baa-136">-ResourceType</span></span>
<span data-ttu-id="89baa-137">Указывает тип ресурса, к которому относится блокировка.</span><span class="sxs-lookup"><span data-stu-id="89baa-137">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="89baa-138">-Scope</span><span class="sxs-lookup"><span data-stu-id="89baa-138">-Scope</span></span>
<span data-ttu-id="89baa-139">Указывает область, к которой применяется блокировка.</span><span class="sxs-lookup"><span data-stu-id="89baa-139">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="89baa-140">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="89baa-140">-TenantLevel</span></span>
<span data-ttu-id="89baa-141">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="89baa-141">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="89baa-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89baa-142">-Confirm</span></span>
<span data-ttu-id="89baa-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="89baa-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89baa-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89baa-144">-WhatIf</span></span>
<span data-ttu-id="89baa-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="89baa-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89baa-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="89baa-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89baa-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89baa-147">CommonParameters</span></span>
<span data-ttu-id="89baa-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="89baa-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89baa-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89baa-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89baa-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="89baa-150">INPUTS</span></span>

### <span data-ttu-id="89baa-151">System. String</span><span class="sxs-lookup"><span data-stu-id="89baa-151">System.String</span></span>

## <span data-ttu-id="89baa-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="89baa-152">OUTPUTS</span></span>

### <span data-ttu-id="89baa-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="89baa-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="89baa-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="89baa-154">NOTES</span></span>

## <span data-ttu-id="89baa-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89baa-155">RELATED LINKS</span></span>

[<span data-ttu-id="89baa-156">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="89baa-156">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="89baa-157">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="89baa-157">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="89baa-158">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="89baa-158">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


