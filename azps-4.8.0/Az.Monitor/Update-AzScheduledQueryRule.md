---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzScheduledQueryRule.md
ms.openlocfilehash: 1e591f9c6d631ab6b8c3a5246eb4e45655de841e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078179"
---
# <span data-ttu-id="ecee5-101">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ecee5-101">Update-AzScheduledQueryRule</span></span>

## <span data-ttu-id="ecee5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ecee5-102">SYNOPSIS</span></span>
<span data-ttu-id="ecee5-103">Обновляет правило оповещения в журнале</span><span class="sxs-lookup"><span data-stu-id="ecee5-103">Updates a Log Alert rule</span></span>

## <span data-ttu-id="ecee5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ecee5-104">SYNTAX</span></span>

### <span data-ttu-id="ecee5-105">ByRuleName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ecee5-105">ByRuleName (Default)</span></span>
```
Update-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecee5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ecee5-106">ByInputObject</span></span>
```
Update-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecee5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ecee5-107">ByResourceId</span></span>
```
Update-AzScheduledQueryRule -ResourceId <String> -Enabled <Boolean> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecee5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ecee5-108">DESCRIPTION</span></span>
<span data-ttu-id="ecee5-109">Обновляет правило оповещения журнала, в этой команде поддерживается только изменение свойства Enabled.</span><span class="sxs-lookup"><span data-stu-id="ecee5-109">Updates a Log Alert rule, updating only "Enabled" property is supported by this command.</span></span>
<span data-ttu-id="ecee5-110">Чтобы обновить другие свойства, ознакомьтесь с командой "Set-AzScheduledQueryRule".</span><span class="sxs-lookup"><span data-stu-id="ecee5-110">To update other properties, see "Set-AzScheduledQueryRule" command.</span></span>

## <span data-ttu-id="ecee5-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ecee5-111">EXAMPLES</span></span>

### <span data-ttu-id="ecee5-112">Пример 1: обновление по имени правила</span><span class="sxs-lookup"><span data-stu-id="ecee5-112">Example 1: Update by rule name</span></span>
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

### <span data-ttu-id="ecee5-113">Пример 2: обновление по объекту ввода</span><span class="sxs-lookup"><span data-stu-id="ecee5-113">Example 2: Update by input object</span></span>
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

### <span data-ttu-id="ecee5-114">Пример 3: обновление по идентификатору ресурса</span><span class="sxs-lookup"><span data-stu-id="ecee5-114">Example 3: Update by resource Id</span></span>
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

## <span data-ttu-id="ecee5-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ecee5-115">PARAMETERS</span></span>

### <span data-ttu-id="ecee5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecee5-116">-DefaultProfile</span></span>
<span data-ttu-id="ecee5-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ecee5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecee5-118">-Включено</span><span class="sxs-lookup"><span data-stu-id="ecee5-118">-Enabled</span></span>
<span data-ttu-id="ecee5-119">Состояние оповещения Azure — допустимые значения: $true, $false</span><span class="sxs-lookup"><span data-stu-id="ecee5-119">The azure alert state - valid values - $true, $false</span></span>

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

### <span data-ttu-id="ecee5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ecee5-120">-InputObject</span></span>
<span data-ttu-id="ecee5-121">Запланированный ресурс правила запроса</span><span class="sxs-lookup"><span data-stu-id="ecee5-121">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="ecee5-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ecee5-122">-Name</span></span>
<span data-ttu-id="ecee5-123">Имя оповещения</span><span class="sxs-lookup"><span data-stu-id="ecee5-123">The alert name</span></span>

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

### <span data-ttu-id="ecee5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecee5-124">-ResourceGroupName</span></span>
<span data-ttu-id="ecee5-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ecee5-125">The resource group name</span></span>

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

### <span data-ttu-id="ecee5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecee5-126">-ResourceId</span></span>
<span data-ttu-id="ecee5-127">Идентификатор ресурса</span><span class="sxs-lookup"><span data-stu-id="ecee5-127">The resource Id</span></span>

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

### <span data-ttu-id="ecee5-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ecee5-128">-Confirm</span></span>
<span data-ttu-id="ecee5-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ecee5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecee5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecee5-130">-WhatIf</span></span>
<span data-ttu-id="ecee5-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ecee5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecee5-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ecee5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecee5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecee5-133">CommonParameters</span></span>
<span data-ttu-id="ecee5-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ecee5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecee5-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ecee5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecee5-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ecee5-136">INPUTS</span></span>

### <span data-ttu-id="ecee5-137">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="ecee5-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="ecee5-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ecee5-138">System.String</span></span>

## <span data-ttu-id="ecee5-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ecee5-139">OUTPUTS</span></span>

### <span data-ttu-id="ecee5-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="ecee5-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

## <span data-ttu-id="ecee5-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="ecee5-141">NOTES</span></span>

## <span data-ttu-id="ecee5-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ecee5-142">RELATED LINKS</span></span>