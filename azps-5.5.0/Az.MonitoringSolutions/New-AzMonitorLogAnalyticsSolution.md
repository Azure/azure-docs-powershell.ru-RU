---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/new-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 6747a53f9e714926c5a4d1358e15cb387ddae69a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221412"
---
# <span data-ttu-id="fa4f4-101">New-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="fa4f4-101">New-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="fa4f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa4f4-102">SYNOPSIS</span></span>
<span data-ttu-id="fa4f4-103">Создает решение для аналитики журналов.</span><span class="sxs-lookup"><span data-stu-id="fa4f4-103">Creates a log analytics solution.</span></span>

## <span data-ttu-id="fa4f4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fa4f4-104">SYNTAX</span></span>

```
New-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> -Location <String> -Type <String>
 -WorkspaceResourceId <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fa4f4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa4f4-105">DESCRIPTION</span></span>
<span data-ttu-id="fa4f4-106">Создает решение для аналитики журналов.</span><span class="sxs-lookup"><span data-stu-id="fa4f4-106">Creates a log analytics solution.</span></span>

## <span data-ttu-id="fa4f4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fa4f4-107">EXAMPLES</span></span>

### <span data-ttu-id="fa4f4-108">Пример 1. Создание средства аналитики журналов для рабочей области для журнала</span><span class="sxs-lookup"><span data-stu-id="fa4f4-108">Example 1: Create a monitor log analytics solution for the log analytics workspace</span></span>
```powershell
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName azureps-manual-test -Name monitoringworkspace-2vob7n
PS C:\> New-AzMonitorLogAnalyticsSolution -Type Containers -ResourceGroupName azureps-manual-test -Location $workspace.Location -WorkspaceResourceId $workspace.ResourceId

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="fa4f4-109">Эта команда создает решение для анализа журнала журнала для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="fa4f4-109">This command creates a monitor log analytics solution for the log analytics workspace.</span></span>

<span data-ttu-id="fa4f4-110">Чаще всего используются:</span><span class="sxs-lookup"><span data-stu-id="fa4f4-110">Commonly used types are:</span></span>

| <span data-ttu-id="fa4f4-111">Тип</span><span class="sxs-lookup"><span data-stu-id="fa4f4-111">Type</span></span> | <span data-ttu-id="fa4f4-112">Описание</span><span class="sxs-lookup"><span data-stu-id="fa4f4-112">Description</span></span> |
| :-----| :----- |
| <span data-ttu-id="fa4f4-113">SecurityCenterFree</span><span class="sxs-lookup"><span data-stu-id="fa4f4-113">SecurityCenterFree</span></span> |  <span data-ttu-id="fa4f4-114">Центр безопасности Azure — бесплатная версия</span><span class="sxs-lookup"><span data-stu-id="fa4f4-114">Azure Security Center – Free Edition</span></span> |
| <span data-ttu-id="fa4f4-115">Безопасность</span><span class="sxs-lookup"><span data-stu-id="fa4f4-115">Security</span></span> | <span data-ttu-id="fa4f4-116">Центр безопасности Azure</span><span class="sxs-lookup"><span data-stu-id="fa4f4-116">Azure Security Center</span></span> |
| <span data-ttu-id="fa4f4-117">Обновления</span><span class="sxs-lookup"><span data-stu-id="fa4f4-117">Updates</span></span> | <span data-ttu-id="fa4f4-118">Управление обновлениями</span><span class="sxs-lookup"><span data-stu-id="fa4f4-118">Update Management</span></span> |
| <span data-ttu-id="fa4f4-119">ContainerInsights</span><span class="sxs-lookup"><span data-stu-id="fa4f4-119">ContainerInsights</span></span> | <span data-ttu-id="fa4f4-120">Azure Monitor for Containers</span><span class="sxs-lookup"><span data-stu-id="fa4f4-120">Azure Monitor for Containers</span></span> |
| <span data-ttu-id="fa4f4-121">ServiceMap</span><span class="sxs-lookup"><span data-stu-id="fa4f4-121">ServiceMap</span></span> | <span data-ttu-id="fa4f4-122">Карта службы</span><span class="sxs-lookup"><span data-stu-id="fa4f4-122">Service Map</span></span> |
| <span data-ttu-id="fa4f4-123">AzureActivity</span><span class="sxs-lookup"><span data-stu-id="fa4f4-123">AzureActivity</span></span> | <span data-ttu-id="fa4f4-124">Аналитика журналов действий</span><span class="sxs-lookup"><span data-stu-id="fa4f4-124">Activity log analytics</span></span> |
| <span data-ttu-id="fa4f4-125">ChangeTracking</span><span class="sxs-lookup"><span data-stu-id="fa4f4-125">ChangeTracking</span></span> | <span data-ttu-id="fa4f4-126">Отслеживание изменений и запасы</span><span class="sxs-lookup"><span data-stu-id="fa4f4-126">Change tracking and inventory</span></span> |
| <span data-ttu-id="fa4f4-127">VMInsights</span><span class="sxs-lookup"><span data-stu-id="fa4f4-127">VMInsights</span></span> | <span data-ttu-id="fa4f4-128">Azure Monitor для VMs</span><span class="sxs-lookup"><span data-stu-id="fa4f4-128">Azure Monitor for VMs</span></span> |
| <span data-ttu-id="fa4f4-129">SecurityInsights</span><span class="sxs-lookup"><span data-stu-id="fa4f4-129">SecurityInsights</span></span> | <span data-ttu-id="fa4f4-130">Azure Sentinel</span><span class="sxs-lookup"><span data-stu-id="fa4f4-130">Azure Sentinel</span></span> |
| <span data-ttu-id="fa4f4-131">NetworkMonitoring</span><span class="sxs-lookup"><span data-stu-id="fa4f4-131">NetworkMonitoring</span></span> | <span data-ttu-id="fa4f4-132">Монитор производительности сети</span><span class="sxs-lookup"><span data-stu-id="fa4f4-132">Network Performance Monitor</span></span> |
| <span data-ttu-id="fa4f4-133">SQLVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="fa4f4-133">SQLVulnerabilityAssessment</span></span> | <span data-ttu-id="fa4f4-134">SQL оценки уязвимости</span><span class="sxs-lookup"><span data-stu-id="fa4f4-134">SQL Vulnerability Assessment</span></span> |
| <span data-ttu-id="fa4f4-135">SQLAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="fa4f4-135">SQLAdvancedThreatProtection</span></span> | <span data-ttu-id="fa4f4-136">SQL Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="fa4f4-136">SQL Advanced Threat Protection</span></span> |
| <span data-ttu-id="fa4f4-137">AntiMalware</span><span class="sxs-lookup"><span data-stu-id="fa4f4-137">AntiMalware</span></span> | <span data-ttu-id="fa4f4-138">Antimalware Assessment</span><span class="sxs-lookup"><span data-stu-id="fa4f4-138">Antimalware Assessment</span></span> |
| <span data-ttu-id="fa4f4-139">AzureAutomation</span><span class="sxs-lookup"><span data-stu-id="fa4f4-139">AzureAutomation</span></span> | <span data-ttu-id="fa4f4-140">Гибридный работник автоматизации</span><span class="sxs-lookup"><span data-stu-id="fa4f4-140">Automation Hybrid Worker</span></span> |
| <span data-ttu-id="fa4f4-141">LogicAppsManagement</span><span class="sxs-lookup"><span data-stu-id="fa4f4-141">LogicAppsManagement</span></span> | <span data-ttu-id="fa4f4-142">Управление приложениями логики</span><span class="sxs-lookup"><span data-stu-id="fa4f4-142">Logic Apps Management</span></span> |
| <span data-ttu-id="fa4f4-143">SQLDataClassification</span><span class="sxs-lookup"><span data-stu-id="fa4f4-143">SQLDataClassification</span></span> | <span data-ttu-id="fa4f4-144">SQL классификации при & данных</span><span class="sxs-lookup"><span data-stu-id="fa4f4-144">SQL Data Discovery & Classification</span></span> |

## <span data-ttu-id="fa4f4-145">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa4f4-145">PARAMETERS</span></span>

### <span data-ttu-id="fa4f4-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa4f4-146">-DefaultProfile</span></span>
<span data-ttu-id="fa4f4-147">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fa4f4-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa4f4-148">-Location</span><span class="sxs-lookup"><span data-stu-id="fa4f4-148">-Location</span></span>
<span data-ttu-id="fa4f4-149">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="fa4f4-149">Resource location.</span></span>
<span data-ttu-id="fa4f4-150">Должен быть таким же, как в аналитической рабочей области журнала.</span><span class="sxs-lookup"><span data-stu-id="fa4f4-150">Must be the same as the log analytic workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa4f4-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa4f4-151">-ResourceGroupName</span></span>
<span data-ttu-id="fa4f4-152">Имя группы ресурсов, которая будет получаться.</span><span class="sxs-lookup"><span data-stu-id="fa4f4-152">The name of the resource group to get.</span></span>
<span data-ttu-id="fa4f4-153">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="fa4f4-153">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa4f4-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fa4f4-154">-SubscriptionId</span></span>
<span data-ttu-id="fa4f4-155">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fa4f4-155">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="fa4f4-156">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="fa4f4-156">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa4f4-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="fa4f4-157">-Tag</span></span>
<span data-ttu-id="fa4f4-158">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="fa4f4-158">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa4f4-159">-Type</span><span class="sxs-lookup"><span data-stu-id="fa4f4-159">-Type</span></span>
<span data-ttu-id="fa4f4-160">Тип созда создаемого решения.</span><span class="sxs-lookup"><span data-stu-id="fa4f4-160">Type of the solution to be created.</span></span>
<span data-ttu-id="fa4f4-161">Например, Container.</span><span class="sxs-lookup"><span data-stu-id="fa4f4-161">For example "Container".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SolutionType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa4f4-162">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="fa4f4-162">-WorkspaceResourceId</span></span>
<span data-ttu-id="fa4f4-163">ИД ресурсов Azure для рабочей области, в которой будет развернуто или включено решение.</span><span class="sxs-lookup"><span data-stu-id="fa4f4-163">The Azure resource ID for the workspace where the solution will be deployed/enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa4f4-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa4f4-164">-Confirm</span></span>
<span data-ttu-id="fa4f4-165">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa4f4-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa4f4-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa4f4-166">-WhatIf</span></span>
<span data-ttu-id="fa4f4-167">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa4f4-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa4f4-168">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fa4f4-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa4f4-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa4f4-169">CommonParameters</span></span>
<span data-ttu-id="fa4f4-170">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa4f4-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa4f4-171">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa4f4-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa4f4-172">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fa4f4-172">INPUTS</span></span>

## <span data-ttu-id="fa4f4-173">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fa4f4-173">OUTPUTS</span></span>

### <span data-ttu-id="fa4f4-174">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="fa4f4-174">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="fa4f4-175">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fa4f4-175">NOTES</span></span>

<span data-ttu-id="fa4f4-176">ALIASES</span><span class="sxs-lookup"><span data-stu-id="fa4f4-176">ALIASES</span></span>

## <span data-ttu-id="fa4f4-177">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fa4f4-177">RELATED LINKS</span></span>



[<span data-ttu-id="fa4f4-178">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="fa4f4-178">Get-AzOperationalInsightsWorkspace</span></span>](https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace)

