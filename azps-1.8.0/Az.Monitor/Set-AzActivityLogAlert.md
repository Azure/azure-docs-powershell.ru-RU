---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActivityLogAlert.md
ms.openlocfilehash: 6c7b867add359edec8379f20e630c9aca5fed00e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402887"
---
# <span data-ttu-id="a605f-101">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a605f-101">Set-AzActivityLogAlert</span></span>

## <span data-ttu-id="a605f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a605f-102">SYNOPSIS</span></span>
<span data-ttu-id="a605f-103">Создает новое оповещение или настраивает существующее оповещение журнала действий.</span><span class="sxs-lookup"><span data-stu-id="a605f-103">Creates a new or sets an existing activity log alert.</span></span>

## <span data-ttu-id="a605f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a605f-104">SYNTAX</span></span>

### <span data-ttu-id="a605f-105">SetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a605f-105">SetByNameAndResourceGroup</span></span>
```
Set-AzActivityLogAlert -Location <String> -Name <String> -ResourceGroupName <String>
 -Scope <System.Collections.Generic.List`1[System.String]>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>
 -Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a605f-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a605f-106">SetByResourceId</span></span>
```
Set-AzActivityLogAlert [-Location <String>] [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a605f-107">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="a605f-107">SetByInputObject</span></span>
```
Set-AzActivityLogAlert [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-Description <String>] [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a605f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a605f-108">DESCRIPTION</span></span>
<span data-ttu-id="a605f-109">С **его учетом** создается новое оповещение журнала действий или настраивается существующее оповещение.</span><span class="sxs-lookup"><span data-stu-id="a605f-109">The **Set-AzActivityLogAlert** cmdlet creates a new or sets an existing activity log alert.</span></span>
<span data-ttu-id="a605f-110">Для тегов, условий и действий объекты должны быть созданы заранее и переданы в качестве параметров этого вызова в качестве разделяемой запятой (см. пример ниже).</span><span class="sxs-lookup"><span data-stu-id="a605f-110">For tags, conditions, and actions the objects must be created in advance and passed as parameters in this call as a comma separated (see the example below).</span></span>
<span data-ttu-id="a605f-111">Этот cmdlet реализует шаблон ShouldProcess, то есть может запросить подтверждение у пользователя перед фактическим созданием или изменением ресурса.</span><span class="sxs-lookup"><span data-stu-id="a605f-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating/modifying the resource.</span></span>
<span data-ttu-id="a605f-112">**ПРИМЕЧАНИЕ.** Этот и связанные с ним cmdlet заменяют неподготовленное (ноябрь 2017 г.) **add-AzLogAlertRule.**</span><span class="sxs-lookup"><span data-stu-id="a605f-112">**NOTE**: This cmdlet and its related ones replaces the deprecated (November 2017) **Add-AzLogAlertRule**.</span></span>

## <span data-ttu-id="a605f-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a605f-113">EXAMPLES</span></span>

### <span data-ttu-id="a605f-114">Пример 1. Создание оповещения журнала действий</span><span class="sxs-lookup"><span data-stu-id="a605f-114">Example 1: Create an Activity Log Alert</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzActivityLogAlertCondition -Field 'field1' -Equals 'equals1'
PS C:\>$condition2 = New-AzActivityLogAlertCondition -Field 'field2' -Equals 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
PS C:\>Set-AzActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2
```

<span data-ttu-id="a605f-115">Первые четыре команды создают условие и группу действий листа.</span><span class="sxs-lookup"><span data-stu-id="a605f-115">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="a605f-116">Конечная команда создает оповещение журнала действий с использованием условия и группы действий.</span><span class="sxs-lookup"><span data-stu-id="a605f-116">The final command creates an Activity Log Alert using the condition and the action group.</span></span>

### <span data-ttu-id="a605f-117">Пример 2. Отключение оповещения журнала действий</span><span class="sxs-lookup"><span data-stu-id="a605f-117">Example 2: Create an Activity Log Alert disabled</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzActivityLogAlertCondition -Field 'field1' -Equals 'equals1'
PS C:\>$condition2 = New-AzActivityLogAlertCondition -Field 'field2' -Equals 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
PS C:\>Set-AzActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2 -DisableAlert
```

<span data-ttu-id="a605f-118">Первые четыре команды создают условие и группу действий листа.</span><span class="sxs-lookup"><span data-stu-id="a605f-118">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="a605f-119">Конечная команда создает оповещение журнала действий с использованием условия и группы действий, но оповещение отключается.</span><span class="sxs-lookup"><span data-stu-id="a605f-119">The final command creates an Activity Log Alert using the condition and the action group, but it creates the alert disabled.</span></span>

### <span data-ttu-id="a605f-120">Пример 3. Настройка оповещения журнала действий на основе значения из канала или параметра InputObject</span><span class="sxs-lookup"><span data-stu-id="a605f-120">Example 3: Set an activity log alert based using a value from the pipe or the InputObject parameter</span></span>
```
PS C:\>Get-AzActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName | Set-AzActivityLogAlert
PS C:\>$alert = Get-AzActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName
PS C:\>$alert.Description = 'Changing the description'
PS C:\>$alert.Enabled = $false
PS C:\>Set-AzActivityLogAlert -InputObject $alert
```

<span data-ttu-id="a605f-121">Первая команда похожа на "nop", она задает оповещение с теми же значениями, которые уже содержатся для остальных команд, извлекает правило оповещения, изменяет описание и отключает его, а затем сохраняет эти изменения с помощью параметра InputObject.</span><span class="sxs-lookup"><span data-stu-id="a605f-121">The first command is similar to a nop, it sets the alert with the same values it already contained The rest of the commands retrieve the alert rule, change the description and disable it, then use the InputObject parameter to persist those changes</span></span>

### <span data-ttu-id="a605f-122">Пример 4. Настройка оповещения журнала действий на основе значения ResourceId из трубы</span><span class="sxs-lookup"><span data-stu-id="a605f-122">Example 4: Set an activity log alert based using the ResourceId value from the pipe</span></span>
```
PS C:\>Find-AzResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Set-AzActivityLogAlert -DisableAlert
```

<span data-ttu-id="a605f-123">Если имеется правило оповещения журнала, эта команда отключает его.</span><span class="sxs-lookup"><span data-stu-id="a605f-123">If the given log alert rule exists this command disables it.</span></span>

## <span data-ttu-id="a605f-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a605f-124">PARAMETERS</span></span>

### <span data-ttu-id="a605f-125">-Action</span><span class="sxs-lookup"><span data-stu-id="a605f-125">-Action</span></span>
<span data-ttu-id="a605f-126">Список групп действий для оповещения журнала действий.</span><span class="sxs-lookup"><span data-stu-id="a605f-126">The list of action groups for the activity log alert.</span></span>

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

### <span data-ttu-id="a605f-127">-Условие</span><span class="sxs-lookup"><span data-stu-id="a605f-127">-Condition</span></span>
<span data-ttu-id="a605f-128">Список условий для оповещения журнала действий.</span><span class="sxs-lookup"><span data-stu-id="a605f-128">The list of conditions for the activity log alert.</span></span>
<span data-ttu-id="a605f-129">**ПРИМЕЧАНИЕ.** В списке условий должно быть хотя бы одно с полем , равным "Категория".</span><span class="sxs-lookup"><span data-stu-id="a605f-129">**NOTE**: In the list of conditions there must be at least one with the Field equal to "Category".</span></span> <span data-ttu-id="a605f-130">Если это условие не задано, в ответе на запрос к backend возвращается 400 (BadRequest).</span><span class="sxs-lookup"><span data-stu-id="a605f-130">The backend responds with 400 (BadRequest) if this condition is not present.</span></span>

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

### <span data-ttu-id="a605f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a605f-131">-DefaultProfile</span></span>
<span data-ttu-id="a605f-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a605f-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a605f-133">-Description</span><span class="sxs-lookup"><span data-stu-id="a605f-133">-Description</span></span>
<span data-ttu-id="a605f-134">Описание ресурса оповещения.</span><span class="sxs-lookup"><span data-stu-id="a605f-134">The description of the alert resource.</span></span>

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

### <span data-ttu-id="a605f-135">-DisableAlert</span><span class="sxs-lookup"><span data-stu-id="a605f-135">-DisableAlert</span></span>
<span data-ttu-id="a605f-136">Позволяет пользователю создать отключенную оповещение журнала действий.</span><span class="sxs-lookup"><span data-stu-id="a605f-136">Allows the user to create a disabled the activity log alert.</span></span> <span data-ttu-id="a605f-137">Если они не даются, оповещения создаются.</span><span class="sxs-lookup"><span data-stu-id="a605f-137">If not given, the alerts are created enabled.</span></span>

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

### <span data-ttu-id="a605f-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a605f-138">-InputObject</span></span>
<span data-ttu-id="a605f-139">Задает свойство "Теги InputObject" для извлечения требуемого имени и свойств имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a605f-139">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

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

### <span data-ttu-id="a605f-140">-Location</span><span class="sxs-lookup"><span data-stu-id="a605f-140">-Location</span></span>
<span data-ttu-id="a605f-141">Расположение, в котором будет существовать оповещение журнала действий.</span><span class="sxs-lookup"><span data-stu-id="a605f-141">The location where the activity log alert will exist.</span></span>

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

### <span data-ttu-id="a605f-142">-Name</span><span class="sxs-lookup"><span data-stu-id="a605f-142">-Name</span></span>
<span data-ttu-id="a605f-143">Имя оповещения журнала действий.</span><span class="sxs-lookup"><span data-stu-id="a605f-143">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="a605f-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a605f-144">-ResourceGroupName</span></span>
<span data-ttu-id="a605f-145">Имя группы ресурсов, в которой должен существовать оповещение.</span><span class="sxs-lookup"><span data-stu-id="a605f-145">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="a605f-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a605f-146">-ResourceId</span></span>
<span data-ttu-id="a605f-147">Задает свойство "Теги ResourceId" звонка для извлечения требуемого имени (свойства имени группы ресурсов).</span><span class="sxs-lookup"><span data-stu-id="a605f-147">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="a605f-148">-Scope</span><span class="sxs-lookup"><span data-stu-id="a605f-148">-Scope</span></span>
<span data-ttu-id="a605f-149">Список областей оповещения журнала действий.</span><span class="sxs-lookup"><span data-stu-id="a605f-149">The list of scopes for the activity log alert.</span></span>

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

### <span data-ttu-id="a605f-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="a605f-150">-Tag</span></span>
<span data-ttu-id="a605f-151">Задает свойство "Теги" для ресурса оповещения журнала действий.</span><span class="sxs-lookup"><span data-stu-id="a605f-151">Sets the tags property of the activity log alert resource.</span></span>

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

### <span data-ttu-id="a605f-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a605f-152">-Confirm</span></span>
<span data-ttu-id="a605f-153">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a605f-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a605f-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a605f-154">-WhatIf</span></span>
<span data-ttu-id="a605f-155">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a605f-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a605f-156">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a605f-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a605f-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a605f-157">CommonParameters</span></span>
<span data-ttu-id="a605f-158">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a605f-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a605f-159">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a605f-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a605f-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a605f-160">INPUTS</span></span>

### <span data-ttu-id="a605f-161">System.String</span><span class="sxs-lookup"><span data-stu-id="a605f-161">System.String</span></span>

### <span data-ttu-id="a605f-162">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a605f-162">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a605f-163">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="a605f-163">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="a605f-164">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="a605f-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="a605f-165">System.Collections.Generic.Dictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a605f-165">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a605f-166">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="a605f-166">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="a605f-167">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a605f-167">OUTPUTS</span></span>

### <span data-ttu-id="a605f-168">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="a605f-168">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="a605f-169">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a605f-169">NOTES</span></span>

## <span data-ttu-id="a605f-170">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a605f-170">RELATED LINKS</span></span>

[<span data-ttu-id="a605f-171">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a605f-171">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="a605f-172">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a605f-172">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="a605f-173">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a605f-173">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="a605f-174">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a605f-174">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="a605f-175">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="a605f-175">New-AzActionGroup</span></span>](./New-AzActionGroup.md)
