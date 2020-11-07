---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermactivitylogalert
schema: 2.0.0
ms.openlocfilehash: 993e1b9cde421bad1039f94f4557ee58f781c20b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913364"
---
# <span data-ttu-id="6b664-101">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6b664-101">Set-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="6b664-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6b664-102">SYNOPSIS</span></span>
<span data-ttu-id="6b664-103">Создание нового или установка существующего оповещения журнала активности.</span><span class="sxs-lookup"><span data-stu-id="6b664-103">Creates a new or sets an existing activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b664-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6b664-104">SYNTAX</span></span>

### <span data-ttu-id="6b664-105">SetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6b664-105">SetByNameAndResourceGroup</span></span>
```
Set-AzureRmActivityLogAlert -Location <String> -Name <String> -ResourceGroupName <String>
 -Scope <System.Collections.Generic.List`1[System.String]>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>
 -Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b664-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6b664-106">SetByResourceId</span></span>
```
Set-AzureRmActivityLogAlert [-Location <String>] [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b664-107">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="6b664-107">SetByInputObject</span></span>
```
Set-AzureRmActivityLogAlert [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-Description <String>] [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6b664-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b664-108">DESCRIPTION</span></span>
<span data-ttu-id="6b664-109">Командлет **Set-AzureRmActivityLogAlert** создает новый или устанавливает существующее оповещение журнала активности.</span><span class="sxs-lookup"><span data-stu-id="6b664-109">The **Set-AzureRmActivityLogAlert** cmdlet creates a new or sets an existing activity log alert.</span></span>
<span data-ttu-id="6b664-110">Для тегов, условий и действий объекты должны быть созданы заранее и передаваться в качестве параметров в этом вызове в виде разделителей запятыми (см. пример ниже).</span><span class="sxs-lookup"><span data-stu-id="6b664-110">For tags, conditions, and actions the objects must be created in advance and passed as parameters in this call as a comma separated (see the example below).</span></span>
<span data-ttu-id="6b664-111">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно создать или изменить ресурс.</span><span class="sxs-lookup"><span data-stu-id="6b664-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating/modifying the resource.</span></span>
<span data-ttu-id="6b664-112">**Примечание**. Этот командлет и связанные с ним свойства заменяют устаревшее (Ноябрь 2017) **Add-AzureRmLogAlertRule**.</span><span class="sxs-lookup"><span data-stu-id="6b664-112">**NOTE** : This cmdlet and its related ones replaces the deprecated (November 2017) **Add-AzureRmLogAlertRule**.</span></span>

## <span data-ttu-id="6b664-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6b664-113">EXAMPLES</span></span>

### <span data-ttu-id="6b664-114">Пример 1: Создание оповещения журнала активности</span><span class="sxs-lookup"><span data-stu-id="6b664-114">Example 1: Create an Activity Log Alert</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzureRmActivityLogAlertCondition -Field 'field1' -Equals 'equals1'
PS C:\>$condition2 = New-AzureRmActivityLogAlertCondition -Field 'field2' -Equals 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
PS C:\>Set-AzureRmActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2
```

<span data-ttu-id="6b664-115">Первые четыре команды создают конечные условия и группы действий.</span><span class="sxs-lookup"><span data-stu-id="6b664-115">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="6b664-116">Последняя команда создает оповещение журнала активности с помощью условия и группы действий.</span><span class="sxs-lookup"><span data-stu-id="6b664-116">The final command creates an Activity Log Alert using the condition and the action group.</span></span>

### <span data-ttu-id="6b664-117">Пример 2: Создание оповещения журнала действий отключено</span><span class="sxs-lookup"><span data-stu-id="6b664-117">Example 2: Create an Activity Log Alert disabled</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzureRmActivityLogAlertCondition -Field 'field1' -Equals 'equals1'
PS C:\>$condition2 = New-AzureRmActivityLogAlertCondition -Field 'field2' -Equals 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
PS C:\>Set-AzureRmActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2 -DisableAlert
```

<span data-ttu-id="6b664-118">Первые четыре команды создают конечные условия и группы действий.</span><span class="sxs-lookup"><span data-stu-id="6b664-118">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="6b664-119">Последняя команда создает оповещение журнала активности с помощью условия и группы действий, но создает оповещение отключено.</span><span class="sxs-lookup"><span data-stu-id="6b664-119">The final command creates an Activity Log Alert using the condition and the action group, but it creates the alert disabled.</span></span>

### <span data-ttu-id="6b664-120">Пример 3: Настройка оповещения журнала активности на основе значения из канала или параметра InputObject</span><span class="sxs-lookup"><span data-stu-id="6b664-120">Example 3: Set an activity log alert based using a value from the pipe or the InputObject parameter</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName | Set-AzureRmActivityLogAlert
PS C:\>$alert = Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName
PS C:\>$alert.Description = 'Changing the description'
PS C:\>$alert.Enabled = $false
PS C:\>Set-AzureRmActivityLogAlert -InputObject $alert
```

<span data-ttu-id="6b664-121">Первая команда похожа на NOP, она задает оповещение с теми же значениями, которые уже содержатся в остальных командах. получите правило оповещения, измените описание и отключите его, а затем используйте параметр InputObject, чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="6b664-121">The first command is similar to a nop, it sets the alert with the same values it already contained The rest of the commands retrieve the alert rule, change the description and disable it, then use the InputObject parameter to persist those changes</span></span>

### <span data-ttu-id="6b664-122">Пример 4: Настройка оповещения журнала активности с помощью значения ResourceId из канала</span><span class="sxs-lookup"><span data-stu-id="6b664-122">Example 4: Set an activity log alert based using the ResourceId value from the pipe</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Set-AzureRmActivityLogAlert -DisableAlert
```

<span data-ttu-id="6b664-123">Если существует данное правило оповещения журнала, эта команда отключает ее.</span><span class="sxs-lookup"><span data-stu-id="6b664-123">If the given log alert rule exists this command disables it.</span></span>

## <span data-ttu-id="6b664-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6b664-124">PARAMETERS</span></span>

### <span data-ttu-id="6b664-125">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="6b664-125">-Action</span></span>
<span data-ttu-id="6b664-126">Список групп действий для оповещения журнала активности.</span><span class="sxs-lookup"><span data-stu-id="6b664-126">The list of action groups for the activity log alert.</span></span>

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

### <span data-ttu-id="6b664-127">-Условие</span><span class="sxs-lookup"><span data-stu-id="6b664-127">-Condition</span></span>
<span data-ttu-id="6b664-128">Список условий для оповещения журнала активности.</span><span class="sxs-lookup"><span data-stu-id="6b664-128">The list of conditions for the activity log alert.</span></span>
<span data-ttu-id="6b664-129">**Примечание**. в списке условий должно быть по крайней мере одно поле, равное "Category".</span><span class="sxs-lookup"><span data-stu-id="6b664-129">**NOTE** : In the list of conditions there must be at least one with the Field equal to "Category".</span></span> <span data-ttu-id="6b664-130">Серверная часть реагирует на 400 (BadRequest), если это условие не задано.</span><span class="sxs-lookup"><span data-stu-id="6b664-130">The backend responds with 400 (BadRequest) if this condition is not present.</span></span>

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

### <span data-ttu-id="6b664-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b664-131">-DefaultProfile</span></span>
<span data-ttu-id="6b664-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6b664-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b664-133">-Описание</span><span class="sxs-lookup"><span data-stu-id="6b664-133">-Description</span></span>
<span data-ttu-id="6b664-134">Описание ресурса оповещения.</span><span class="sxs-lookup"><span data-stu-id="6b664-134">The description of the alert resource.</span></span>

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

### <span data-ttu-id="6b664-135">-DisableAlert</span><span class="sxs-lookup"><span data-stu-id="6b664-135">-DisableAlert</span></span>
<span data-ttu-id="6b664-136">Позволяет пользователю создавать незаблокированное оповещение журнала активности.</span><span class="sxs-lookup"><span data-stu-id="6b664-136">Allows the user to create a disabled the activity log alert.</span></span> <span data-ttu-id="6b664-137">Если не задано, оповещения создаются.</span><span class="sxs-lookup"><span data-stu-id="6b664-137">If not given, the alerts are created enabled.</span></span>

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

### <span data-ttu-id="6b664-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b664-138">-InputObject</span></span>
<span data-ttu-id="6b664-139">Задает свойство Tags (Теги InputObject) для вызова, чтобы извлечь требуемое имя и свойства имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6b664-139">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

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

### <span data-ttu-id="6b664-140">-Location</span><span class="sxs-lookup"><span data-stu-id="6b664-140">-Location</span></span>
<span data-ttu-id="6b664-141">Расположение, в котором будет содержаться предупреждение журнала активности.</span><span class="sxs-lookup"><span data-stu-id="6b664-141">The location where the activity log alert will exist.</span></span>

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

### <span data-ttu-id="6b664-142">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6b664-142">-Name</span></span>
<span data-ttu-id="6b664-143">Имя оповещения журнала активности.</span><span class="sxs-lookup"><span data-stu-id="6b664-143">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="6b664-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b664-144">-ResourceGroupName</span></span>
<span data-ttu-id="6b664-145">Имя группы ресурсов, в которой будет находиться ресурс оповещения.</span><span class="sxs-lookup"><span data-stu-id="6b664-145">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="6b664-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b664-146">-ResourceId</span></span>
<span data-ttu-id="6b664-147">Задает свойство Tags (Теги) для вызова, чтобы извлечь требуемое имя, свойства имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6b664-147">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="6b664-148">-Scope</span><span class="sxs-lookup"><span data-stu-id="6b664-148">-Scope</span></span>
<span data-ttu-id="6b664-149">Список областей для оповещения журнала активности.</span><span class="sxs-lookup"><span data-stu-id="6b664-149">The list of scopes for the activity log alert.</span></span>

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

### <span data-ttu-id="6b664-150">-Тег</span><span class="sxs-lookup"><span data-stu-id="6b664-150">-Tag</span></span>
<span data-ttu-id="6b664-151">Задает свойство Tags для ресурса Alert журнала событий.</span><span class="sxs-lookup"><span data-stu-id="6b664-151">Sets the tags property of the activity log alert resource.</span></span>

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

### <span data-ttu-id="6b664-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b664-152">-Confirm</span></span>
<span data-ttu-id="6b664-153">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6b664-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b664-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b664-154">-WhatIf</span></span>
<span data-ttu-id="6b664-155">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6b664-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6b664-156">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6b664-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b664-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b664-157">CommonParameters</span></span>
<span data-ttu-id="6b664-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6b664-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b664-159">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b664-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b664-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6b664-160">INPUTS</span></span>

### <span data-ttu-id="6b664-161">System. String</span><span class="sxs-lookup"><span data-stu-id="6b664-161">System.String</span></span>

### <span data-ttu-id="6b664-162">System. Collections. Generic. List "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="6b664-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="6b664-163">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Models. ActivityLogAlertLeafCondition, Microsoft. Azure. Commands. Insights, Version = 5.1.0.0, культура = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="6b664-163">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="6b664-164">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Models. ActivityLogAlertActionGroup, Microsoft. Azure. Commands. Insights, Version = 5.1.0.0, культура = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="6b664-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="6b664-165">System. Collections. Generic. Dictionary "2 [[System. String, mscorlib, Version = 4.0.0.0, культура = нейтраль, PublicKeyToken = b77a5c561934e089], [System. String, mscorlib, Version = 4.0.0.0, культура = нейтральная, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="6b664-165">System.Collections.Generic.Dictionary\`2[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089],[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="6b664-166">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="6b664-166">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>
<span data-ttu-id="6b664-167">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6b664-167">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="6b664-168">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b664-168">OUTPUTS</span></span>

### <span data-ttu-id="6b664-169">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="6b664-169">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="6b664-170">Пуск</span><span class="sxs-lookup"><span data-stu-id="6b664-170">NOTES</span></span>

## <span data-ttu-id="6b664-171">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b664-171">RELATED LINKS</span></span>

[<span data-ttu-id="6b664-172">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6b664-172">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="6b664-173">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6b664-173">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="6b664-174">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6b664-174">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="6b664-175">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="6b664-175">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="6b664-176">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="6b664-176">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="6b664-177">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="6b664-177">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
