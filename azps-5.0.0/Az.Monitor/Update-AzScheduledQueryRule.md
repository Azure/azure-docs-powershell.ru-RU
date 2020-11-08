---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
ms.openlocfilehash: 8763b270abccb2a43ab85e9034a23979b27a8355
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250027"
---
# <span data-ttu-id="abc24-101">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="abc24-101">Update-AzScheduledQueryRule</span></span>

## <span data-ttu-id="abc24-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="abc24-102">SYNOPSIS</span></span>
<span data-ttu-id="abc24-103">Обновляет правило оповещения в журнале</span><span class="sxs-lookup"><span data-stu-id="abc24-103">Updates a Log Alert rule</span></span>

## <span data-ttu-id="abc24-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="abc24-104">SYNTAX</span></span>

### <span data-ttu-id="abc24-105">ByRuleName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="abc24-105">ByRuleName (Default)</span></span>
```
Update-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abc24-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="abc24-106">ByInputObject</span></span>
```
Update-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abc24-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="abc24-107">ByResourceId</span></span>
```
Update-AzScheduledQueryRule -ResourceId <String> -Enabled <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abc24-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="abc24-108">DESCRIPTION</span></span>
<span data-ttu-id="abc24-109">Обновляет правило оповещения журнала, в этой команде поддерживается только изменение свойства Enabled.</span><span class="sxs-lookup"><span data-stu-id="abc24-109">Updates a Log Alert rule, updating only "Enabled" property is supported by this command.</span></span>
<span data-ttu-id="abc24-110">Чтобы обновить другие свойства, ознакомьтесь с командой [Set-AzScheduledQueryRule](https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule) .</span><span class="sxs-lookup"><span data-stu-id="abc24-110">To update other properties, see [Set-AzScheduledQueryRule](https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azscheduledqueryrule) command.</span></span>

## <span data-ttu-id="abc24-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="abc24-111">EXAMPLES</span></span>

### <span data-ttu-id="abc24-112">Пример 1: обновление по имени правила</span><span class="sxs-lookup"><span data-stu-id="abc24-112">Example 1: Update by rule name</span></span>
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

### <span data-ttu-id="abc24-113">Пример 2: обновление по объекту ввода</span><span class="sxs-lookup"><span data-stu-id="abc24-113">Example 2: Update by input object</span></span>
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

### <span data-ttu-id="abc24-114">Пример 3: обновление по идентификатору ресурса</span><span class="sxs-lookup"><span data-stu-id="abc24-114">Example 3: Update by resource Id</span></span>
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

## <span data-ttu-id="abc24-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="abc24-115">PARAMETERS</span></span>

### <span data-ttu-id="abc24-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abc24-116">-DefaultProfile</span></span>
<span data-ttu-id="abc24-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="abc24-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abc24-118">-Включено</span><span class="sxs-lookup"><span data-stu-id="abc24-118">-Enabled</span></span>
<span data-ttu-id="abc24-119">Состояние оповещения Azure — допустимые значения: $true, $false</span><span class="sxs-lookup"><span data-stu-id="abc24-119">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="abc24-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abc24-120">-InputObject</span></span>
<span data-ttu-id="abc24-121">Запланированный ресурс правила запроса</span><span class="sxs-lookup"><span data-stu-id="abc24-121">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="abc24-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="abc24-122">-Name</span></span>
<span data-ttu-id="abc24-123">Имя оповещения</span><span class="sxs-lookup"><span data-stu-id="abc24-123">The alert name</span></span>

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

### <span data-ttu-id="abc24-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abc24-124">-ResourceGroupName</span></span>
<span data-ttu-id="abc24-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="abc24-125">The resource group name</span></span>

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

### <span data-ttu-id="abc24-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="abc24-126">-ResourceId</span></span>
<span data-ttu-id="abc24-127">Идентификатор ресурса</span><span class="sxs-lookup"><span data-stu-id="abc24-127">The resource Id</span></span>

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

### <span data-ttu-id="abc24-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="abc24-128">-Confirm</span></span>
<span data-ttu-id="abc24-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="abc24-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abc24-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abc24-130">-WhatIf</span></span>
<span data-ttu-id="abc24-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="abc24-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abc24-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="abc24-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abc24-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abc24-133">CommonParameters</span></span>
<span data-ttu-id="abc24-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="abc24-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abc24-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="abc24-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abc24-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="abc24-136">INPUTS</span></span>

### <span data-ttu-id="abc24-137">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="abc24-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="abc24-138">System. String</span><span class="sxs-lookup"><span data-stu-id="abc24-138">System.String</span></span>

## <span data-ttu-id="abc24-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="abc24-139">OUTPUTS</span></span>

### <span data-ttu-id="abc24-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="abc24-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="abc24-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="abc24-141">NOTES</span></span>

## <span data-ttu-id="abc24-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="abc24-142">RELATED LINKS</span></span>
