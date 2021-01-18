---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
ms.openlocfilehash: 8763b270abccb2a43ab85e9034a23979b27a8355
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506568"
---
# <span data-ttu-id="f9d44-101">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="f9d44-101">Update-AzScheduledQueryRule</span></span>

## <span data-ttu-id="f9d44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9d44-102">SYNOPSIS</span></span>
<span data-ttu-id="f9d44-103">Обновление правила оповещения журнала</span><span class="sxs-lookup"><span data-stu-id="f9d44-103">Updates a Log Alert rule</span></span>

## <span data-ttu-id="f9d44-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f9d44-104">SYNTAX</span></span>

### <span data-ttu-id="f9d44-105">ByRuleName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f9d44-105">ByRuleName (Default)</span></span>
```
Update-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9d44-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f9d44-106">ByInputObject</span></span>
```
Update-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9d44-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f9d44-107">ByResourceId</span></span>
```
Update-AzScheduledQueryRule -ResourceId <String> -Enabled <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9d44-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9d44-108">DESCRIPTION</span></span>
<span data-ttu-id="f9d44-109">Обновляет правило оповещения журнала, обновление только свойства Enabled поддерживается данной командой.</span><span class="sxs-lookup"><span data-stu-id="f9d44-109">Updates a Log Alert rule, updating only "Enabled" property is supported by this command.</span></span>
<span data-ttu-id="f9d44-110">Чтобы обновить другие свойства, см. команду [Set-AzScheduledQueryRule.](https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule)</span><span class="sxs-lookup"><span data-stu-id="f9d44-110">To update other properties, see [Set-AzScheduledQueryRule](https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule) command.</span></span>

## <span data-ttu-id="f9d44-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f9d44-111">EXAMPLES</span></span>

### <span data-ttu-id="f9d44-112">Пример 1. Обновление по имени правила</span><span class="sxs-lookup"><span data-stu-id="f9d44-112">Example 1: Update by rule name</span></span>
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

### <span data-ttu-id="f9d44-113">Пример 2. Обновление по объекту ввода</span><span class="sxs-lookup"><span data-stu-id="f9d44-113">Example 2: Update by input object</span></span>
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

### <span data-ttu-id="f9d44-114">Пример 3. Обновление по ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="f9d44-114">Example 3: Update by resource Id</span></span>
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

## <span data-ttu-id="f9d44-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9d44-115">PARAMETERS</span></span>

### <span data-ttu-id="f9d44-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9d44-116">-DefaultProfile</span></span>
<span data-ttu-id="f9d44-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f9d44-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9d44-118">-Enabled</span><span class="sxs-lookup"><span data-stu-id="f9d44-118">-Enabled</span></span>
<span data-ttu-id="f9d44-119">Состояние оповещения Azure : допустимые значения — $true, $false</span><span class="sxs-lookup"><span data-stu-id="f9d44-119">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="f9d44-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9d44-120">-InputObject</span></span>
<span data-ttu-id="f9d44-121">Ресурс "Правило запланированного запроса"</span><span class="sxs-lookup"><span data-stu-id="f9d44-121">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="f9d44-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f9d44-122">-Name</span></span>
<span data-ttu-id="f9d44-123">Имя оповещения</span><span class="sxs-lookup"><span data-stu-id="f9d44-123">The alert name</span></span>

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

### <span data-ttu-id="f9d44-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9d44-124">-ResourceGroupName</span></span>
<span data-ttu-id="f9d44-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f9d44-125">The resource group name</span></span>

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

### <span data-ttu-id="f9d44-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9d44-126">-ResourceId</span></span>
<span data-ttu-id="f9d44-127">ИД ресурса</span><span class="sxs-lookup"><span data-stu-id="f9d44-127">The resource Id</span></span>

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

### <span data-ttu-id="f9d44-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9d44-128">-Confirm</span></span>
<span data-ttu-id="f9d44-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f9d44-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9d44-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9d44-130">-WhatIf</span></span>
<span data-ttu-id="f9d44-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9d44-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9d44-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f9d44-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9d44-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9d44-133">CommonParameters</span></span>
<span data-ttu-id="f9d44-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9d44-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9d44-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9d44-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9d44-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f9d44-136">INPUTS</span></span>

### <span data-ttu-id="f9d44-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="f9d44-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="f9d44-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f9d44-138">System.String</span></span>

## <span data-ttu-id="f9d44-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f9d44-139">OUTPUTS</span></span>

### <span data-ttu-id="f9d44-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="f9d44-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="f9d44-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f9d44-141">NOTES</span></span>

## <span data-ttu-id="f9d44-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f9d44-142">RELATED LINKS</span></span>
