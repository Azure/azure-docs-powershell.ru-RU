---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
ms.openlocfilehash: c0c77f0adc726d04dc7039c56539b0988b298ce8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910173"
---
# <span data-ttu-id="e9f41-101">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="e9f41-101">Update-AzScheduledQueryRule</span></span>

## <span data-ttu-id="e9f41-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e9f41-102">SYNOPSIS</span></span>
<span data-ttu-id="e9f41-103">Обновляет правило оповещения в журнале</span><span class="sxs-lookup"><span data-stu-id="e9f41-103">Updates a Log Alert rule</span></span>

## <span data-ttu-id="e9f41-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e9f41-104">SYNTAX</span></span>

### <span data-ttu-id="e9f41-105">ByRuleName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e9f41-105">ByRuleName (Default)</span></span>
```
Update-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9f41-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e9f41-106">ByInputObject</span></span>
```
Update-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9f41-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e9f41-107">ByResourceId</span></span>
```
Update-AzScheduledQueryRule -ResourceId <String> -Enabled <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9f41-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9f41-108">DESCRIPTION</span></span>
<span data-ttu-id="e9f41-109">Обновляет правило оповещения журнала, в этой команде поддерживается только изменение свойства Enabled.</span><span class="sxs-lookup"><span data-stu-id="e9f41-109">Updates a Log Alert rule, updating only "Enabled" property is supported by this command.</span></span>
<span data-ttu-id="e9f41-110">Чтобы обновить другие свойства, ознакомьтесь с командой "Set-AzScheduledQueryRule".</span><span class="sxs-lookup"><span data-stu-id="e9f41-110">To update other properties, see "Set-AzScheduledQueryRule" command.</span></span>

## <span data-ttu-id="e9f41-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e9f41-111">EXAMPLES</span></span>

### <span data-ttu-id="e9f41-112">Пример 1: обновление по имени правила</span><span class="sxs-lookup"><span data-stu-id="e9f41-112">Example 1 - Update by rule name</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1" -Enabled $false

Description       : description
Enabled           : false
LastUpdatedTime   : 19-Apr-19 12:49:15 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="e9f41-113">Пример 2: обновление по объекту ввода</span><span class="sxs-lookup"><span data-stu-id="e9f41-113">Example 2 - Update by input object</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -InputObject $sqr -Enabled $false

Description       : description
Enabled           : false
LastUpdatedTime   : 19-Apr-19 12:50:18 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

### <span data-ttu-id="e9f41-114">Пример 3: обновление по идентификатору ресурса</span><span class="sxs-lookup"><span data-stu-id="e9f41-114">Example 3 - Update by resource Id</span></span>
```powershell
PS C:\> Update-AzScheduledQueryRule -ResourceId /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1 -Enabled $true

Description       : description
Enabled           : true
LastUpdatedTime   : 19-Apr-19 12:51:14 PM
ProvisioningState : Succeeded
Source            : Microsoft.Azure.Management.Monitor.Models.Source
Schedule          : Microsoft.Azure.Management.Monitor.Models.Schedule
Action            : Microsoft.Azure.Management.Monitor.Models.AlertingAction
Id                : /subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledqueryrules/LogAlertRule1
Name              : LogAlertRule1
Type              : microsoft.insights/scheduledqueryrules
Location          : centralindia
Tags              : {[hidden-link:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/MyResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace, Resource]}
```

## <span data-ttu-id="e9f41-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e9f41-115">PARAMETERS</span></span>

### <span data-ttu-id="e9f41-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9f41-116">-DefaultProfile</span></span>
<span data-ttu-id="e9f41-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e9f41-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9f41-118">-Включено</span><span class="sxs-lookup"><span data-stu-id="e9f41-118">-Enabled</span></span>
<span data-ttu-id="e9f41-119">Состояние оповещения Azure — допустимые значения: $true, $false</span><span class="sxs-lookup"><span data-stu-id="e9f41-119">The azure alert state - valid values - $true, $false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f41-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9f41-120">-InputObject</span></span>
<span data-ttu-id="e9f41-121">Запланированный ресурс правила запроса</span><span class="sxs-lookup"><span data-stu-id="e9f41-121">The Scheduled Query Rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9f41-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e9f41-122">-Name</span></span>
<span data-ttu-id="e9f41-123">Имя оповещения</span><span class="sxs-lookup"><span data-stu-id="e9f41-123">The alert name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f41-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9f41-124">-ResourceGroupName</span></span>
<span data-ttu-id="e9f41-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e9f41-125">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f41-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9f41-126">-ResourceId</span></span>
<span data-ttu-id="e9f41-127">Идентификатор ресурса</span><span class="sxs-lookup"><span data-stu-id="e9f41-127">The resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9f41-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9f41-128">-Confirm</span></span>
<span data-ttu-id="e9f41-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e9f41-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9f41-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9f41-130">-WhatIf</span></span>
<span data-ttu-id="e9f41-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e9f41-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9f41-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e9f41-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9f41-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9f41-133">CommonParameters</span></span>
<span data-ttu-id="e9f41-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e9f41-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9f41-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9f41-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9f41-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e9f41-136">INPUTS</span></span>

### <span data-ttu-id="e9f41-137">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="e9f41-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="e9f41-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e9f41-138">System.String</span></span>

## <span data-ttu-id="e9f41-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9f41-139">OUTPUTS</span></span>

### <span data-ttu-id="e9f41-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="e9f41-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="e9f41-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="e9f41-141">NOTES</span></span>

## <span data-ttu-id="e9f41-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e9f41-142">RELATED LINKS</span></span>
