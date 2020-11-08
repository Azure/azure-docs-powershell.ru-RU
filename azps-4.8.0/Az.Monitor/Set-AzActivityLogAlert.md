---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActivityLogAlert.md
ms.openlocfilehash: 2ce25f0881fff9ee684bcf234d13d847b7f28850
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078183"
---
# <span data-ttu-id="1f9a3-101">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1f9a3-101">Set-AzActivityLogAlert</span></span>

## <span data-ttu-id="1f9a3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1f9a3-102">SYNOPSIS</span></span>
<span data-ttu-id="1f9a3-103">Создание нового или установка существующего оповещения журнала активности.</span><span class="sxs-lookup"><span data-stu-id="1f9a3-103">Creates a new or sets an existing activity log alert.</span></span>

## <span data-ttu-id="1f9a3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1f9a3-104">SYNTAX</span></span>

### <span data-ttu-id="1f9a3-105">SetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1f9a3-105">SetByNameAndResourceGroup</span></span>
```
Set-AzActivityLogAlert -Location <String> -Name <String> -ResourceGroupName <String>
 -Scope <System.Collections.Generic.List`1[System.String]>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>
 -Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f9a3-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1f9a3-106">SetByResourceId</span></span>
```
Set-AzActivityLogAlert [-Location <String>] [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f9a3-107">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="1f9a3-107">SetByInputObject</span></span>
```
Set-AzActivityLogAlert [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-Description <String>] [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f9a3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f9a3-108">DESCRIPTION</span></span>
<span data-ttu-id="1f9a3-109">Командлет **Set-AzActivityLogAlert** создает новый или устанавливает существующее оповещение журнала активности.</span><span class="sxs-lookup"><span data-stu-id="1f9a3-109">The **Set-AzActivityLogAlert** cmdlet creates a new or sets an existing activity log alert.</span></span>
<span data-ttu-id="1f9a3-110">Для тегов, условий и действий объекты должны быть созданы заранее и передаваться в качестве параметров в этом вызове в виде разделителей запятыми (см. пример ниже).</span><span class="sxs-lookup"><span data-stu-id="1f9a3-110">For tags, conditions, and actions the objects must be created in advance and passed as parameters in this call as a comma separated (see the example below).</span></span>
<span data-ttu-id="1f9a3-111">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно создать или изменить ресурс.</span><span class="sxs-lookup"><span data-stu-id="1f9a3-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating/modifying the resource.</span></span>
<span data-ttu-id="1f9a3-112">**Примечание**. Этот командлет и связанные с ним свойства заменяют устаревшее (Ноябрь 2017) **Add-AzLogAlertRule**.</span><span class="sxs-lookup"><span data-stu-id="1f9a3-112">**NOTE** : This cmdlet and its related ones replaces the deprecated (November 2017) **Add-AzLogAlertRule**.</span></span>

## <span data-ttu-id="1f9a3-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1f9a3-113">EXAMPLES</span></span>

### <span data-ttu-id="1f9a3-114">Пример 1: Создание оповещения журнала активности</span><span class="sxs-lookup"><span data-stu-id="1f9a3-114">Example 1: Create an Activity Log Alert</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzActivityLogAlertCondition -Field 'field1' -Equal 'equals1'
PS C:\>$condition2 = New-AzActivityLogAlertCondition -Field 'field2' -Equal 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
PS C:\>Set-AzActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2
```

<span data-ttu-id="1f9a3-115">Первые четыре команды создают конечные условия и группы действий.</span><span class="sxs-lookup"><span data-stu-id="1f9a3-115">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="1f9a3-116">Последняя команда создает оповещение журнала активности с помощью условия и группы действий.</span><span class="sxs-lookup"><span data-stu-id="1f9a3-116">The final command creates an Activity Log Alert using the condition and the action group.</span></span>

### <span data-ttu-id="1f9a3-117">Пример 2: Создание оповещения журнала действий отключено</span><span class="sxs-lookup"><span data-stu-id="1f9a3-117">Example 2: Create an Activity Log Alert disabled</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzActivityLogAlertCondition -Field 'field1' -Equal 'equals1'
PS C:\>$condition2 = New-AzActivityLogAlertCondition -Field 'field2' -Equal 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
PS C:\>Set-AzActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2 -DisableAlert
```

<span data-ttu-id="1f9a3-118">Первые четыре команды создают конечные условия и группы действий.</span><span class="sxs-lookup"><span data-stu-id="1f9a3-118">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="1f9a3-119">Последняя команда создает оповещение журнала активности с помощью условия и группы действий, но создает оповещение отключено.</span><span class="sxs-lookup"><span data-stu-id="1f9a3-119">The final command creates an Activity Log Alert using the condition and the action group, but it creates the alert disabled.</span></span>

### <span data-ttu-id="1f9a3-120">Пример 3: Настройка оповещения журнала активности на основе значения из канала или параметра InputObject</span><span class="sxs-lookup"><span data-stu-id="1f9a3-120">Example 3: Set an activity log alert based using a value from the pipe or the InputObject parameter</span></span>
```
PS C:\>Get-AzActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName | Set-AzActivityLogAlert
PS C:\>$alert = Get-AzActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName
PS C:\>$alert.Description = 'Changing the description'
PS C:\>$alert.Enabled = $false
PS C:\>Set-AzActivityLogAlert -InputObject $alert
```

<span data-ttu-id="1f9a3-121">Первая команда похожа на NOP, она задает оповещение с теми же значениями, которые уже содержатся в остальных командах. получите правило оповещения, измените описание и отключите его, а затем используйте параметр InputObject, чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="1f9a3-121">The first command is similar to a nop, it sets the alert with the same values it already contained The rest of the commands retrieve the alert rule, change the description and disable it, then use the InputObject parameter to persist those changes</span></span>

### <span data-ttu-id="1f9a3-122">Пример 4: Настройка оповещения журнала активности с помощью значения ResourceId из канала</span><span class="sxs-lookup"><span data-stu-id="1f9a3-122">Example 4: Set an activity log alert based using the ResourceId value from the pipe</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Set-AzActivityLogAlert -DisableAlert
```

<span data-ttu-id="1f9a3-123">Если существует данное правило оповещения журнала, эта команда отключает ее.</span><span class="sxs-lookup"><span data-stu-id="1f9a3-123">If the given log alert rule exists this command disables it.</span></span>

## <span data-ttu-id="1f9a3-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1f9a3-124">PARAMETERS</span></span>

### <span data-ttu-id="1f9a3-125">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="1f9a3-125">-Action</span></span>
<span data-ttu-id="1f9a3-126">Список групп действий для оповещения журнала активности.</span><span class="sxs-lookup"><span data-stu-id="1f9a3-126">The list of action groups for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f9a3-127">-Условие</span><span class="sxs-lookup"><span data-stu-id="1f9a3-127">-Condition</span></span>
<span data-ttu-id="1f9a3-128">Список условий для оповещения журнала активности.</span><span class="sxs-lookup"><span data-stu-id="1f9a3-128">The list of conditions for the activity log alert.</span></span>
<span data-ttu-id="1f9a3-129">**Примечание**. в списке условий должно быть по крайней мере одно поле, равное "Category".</span><span class="sxs-lookup"><span data-stu-id="1f9a3-129">**NOTE** : In the list of conditions there must be at least one with the Field equal to "Category".</span></span> <span data-ttu-id="1f9a3-130">Серверная часть реагирует на 400 (BadRequest), если это условие не задано.</span><span class="sxs-lookup"><span data-stu-id="1f9a3-130">The backend responds with 400 (BadRequest) if this condition is not present.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f9a3-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f9a3-131">-DefaultProfile</span></span>
<span data-ttu-id="1f9a3-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1f9a3-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f9a3-133">-Описание</span><span class="sxs-lookup"><span data-stu-id="1f9a3-133">-Description</span></span>
<span data-ttu-id="1f9a3-134">Описание ресурса оповещения.</span><span class="sxs-lookup"><span data-stu-id="1f9a3-134">The description of the alert resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f9a3-135">-DisableAlert</span><span class="sxs-lookup"><span data-stu-id="1f9a3-135">-DisableAlert</span></span>
<span data-ttu-id="1f9a3-136">Позволяет пользователю создавать незаблокированное оповещение журнала активности.</span><span class="sxs-lookup"><span data-stu-id="1f9a3-136">Allows the user to create a disabled the activity log alert.</span></span> <span data-ttu-id="1f9a3-137">Если не задано, оповещения создаются.</span><span class="sxs-lookup"><span data-stu-id="1f9a3-137">If not given, the alerts are created enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f9a3-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f9a3-138">-InputObject</span></span>
<span data-ttu-id="1f9a3-139">Задает свойство Tags (Теги InputObject) для вызова, чтобы извлечь требуемое имя и свойства имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1f9a3-139">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f9a3-140">-Location</span><span class="sxs-lookup"><span data-stu-id="1f9a3-140">-Location</span></span>
<span data-ttu-id="1f9a3-141">Расположение, в котором будет содержаться предупреждение журнала активности.</span><span class="sxs-lookup"><span data-stu-id="1f9a3-141">The location where the activity log alert will exist.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f9a3-142">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1f9a3-142">-Name</span></span>
<span data-ttu-id="1f9a3-143">Имя оповещения журнала активности.</span><span class="sxs-lookup"><span data-stu-id="1f9a3-143">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f9a3-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f9a3-144">-ResourceGroupName</span></span>
<span data-ttu-id="1f9a3-145">Имя группы ресурсов, в которой будет находиться ресурс оповещения.</span><span class="sxs-lookup"><span data-stu-id="1f9a3-145">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f9a3-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f9a3-146">-ResourceId</span></span>
<span data-ttu-id="1f9a3-147">Задает свойство Tags (Теги) для вызова, чтобы извлечь требуемое имя, свойства имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1f9a3-147">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f9a3-148">-Scope</span><span class="sxs-lookup"><span data-stu-id="1f9a3-148">-Scope</span></span>
<span data-ttu-id="1f9a3-149">Список областей для оповещения журнала активности.</span><span class="sxs-lookup"><span data-stu-id="1f9a3-149">The list of scopes for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f9a3-150">-Тег</span><span class="sxs-lookup"><span data-stu-id="1f9a3-150">-Tag</span></span>
<span data-ttu-id="1f9a3-151">Задает свойство Tags для ресурса Alert журнала событий.</span><span class="sxs-lookup"><span data-stu-id="1f9a3-151">Sets the tags property of the activity log alert resource.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f9a3-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f9a3-152">-Confirm</span></span>
<span data-ttu-id="1f9a3-153">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1f9a3-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f9a3-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f9a3-154">-WhatIf</span></span>
<span data-ttu-id="1f9a3-155">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1f9a3-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f9a3-156">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1f9a3-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f9a3-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f9a3-157">CommonParameters</span></span>
<span data-ttu-id="1f9a3-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1f9a3-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f9a3-159">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f9a3-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f9a3-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1f9a3-160">INPUTS</span></span>

### <span data-ttu-id="1f9a3-161">System. String</span><span class="sxs-lookup"><span data-stu-id="1f9a3-161">System.String</span></span>

### <span data-ttu-id="1f9a3-162">System. Collections. Generic. List "1 [[System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1f9a3-162">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1f9a3-163">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Models. ActivityLogAlertLeafCondition; Microsoft. Azure. PowerShell. командлеты. Monitor, версия = 1.0.0.0, культура = нейтральная, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="1f9a3-163">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="1f9a3-164">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Models. ActivityLogAlertActionGroup; Microsoft. Azure. PowerShell. командлеты. Monitor, версия = 1.0.0.0, культура = нейтральная, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="1f9a3-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="1f9a3-165">System. Collections. Generic. Dictionary "2 [[System. String, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]; [System. String; System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1f9a3-165">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1f9a3-166">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="1f9a3-166">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="1f9a3-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f9a3-167">OUTPUTS</span></span>

### <span data-ttu-id="1f9a3-168">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="1f9a3-168">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="1f9a3-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="1f9a3-169">NOTES</span></span>

## <span data-ttu-id="1f9a3-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f9a3-170">RELATED LINKS</span></span>

[<span data-ttu-id="1f9a3-171">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1f9a3-171">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="1f9a3-172">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1f9a3-172">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="1f9a3-173">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1f9a3-173">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="1f9a3-174">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1f9a3-174">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="1f9a3-175">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="1f9a3-175">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="1f9a3-176">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="1f9a3-176">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)