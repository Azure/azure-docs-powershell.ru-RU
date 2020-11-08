---
external help file: ''
Module Name: Az.MonitoringSolutions
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitoringsolutions/new-azmonitorloganalyticssolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MonitoringSolutions/help/New-AzMonitorLogAnalyticsSolution.md
ms.openlocfilehash: 6747a53f9e714926c5a4d1358e15cb387ddae69a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249405"
---
# <span data-ttu-id="632ba-101">New-AzMonitorLogAnalyticsSolution</span><span class="sxs-lookup"><span data-stu-id="632ba-101">New-AzMonitorLogAnalyticsSolution</span></span>

## <span data-ttu-id="632ba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="632ba-102">SYNOPSIS</span></span>
<span data-ttu-id="632ba-103">Создание решения для службы анализа журналов.</span><span class="sxs-lookup"><span data-stu-id="632ba-103">Creates a log analytics solution.</span></span>

## <span data-ttu-id="632ba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="632ba-104">SYNTAX</span></span>

```
New-AzMonitorLogAnalyticsSolution -ResourceGroupName <String> -Location <String> -Type <String>
 -WorkspaceResourceId <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="632ba-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="632ba-105">DESCRIPTION</span></span>
<span data-ttu-id="632ba-106">Создание решения для службы анализа журналов.</span><span class="sxs-lookup"><span data-stu-id="632ba-106">Creates a log analytics solution.</span></span>

## <span data-ttu-id="632ba-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="632ba-107">EXAMPLES</span></span>

### <span data-ttu-id="632ba-108">Пример 1: создание решения для анализа журнала на мониторе для рабочей области "анализ журналов"</span><span class="sxs-lookup"><span data-stu-id="632ba-108">Example 1: Create a monitor log analytics solution for the log analytics workspace</span></span>
```powershell
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName azureps-manual-test -Name monitoringworkspace-2vob7n
PS C:\> New-AzMonitorLogAnalyticsSolution -Type Containers -ResourceGroupName azureps-manual-test -Location $workspace.Location -WorkspaceResourceId $workspace.ResourceId

Name                                   Type                                     Location
----                                   ----                                     --------
Containers(monitoringworkspace-2vob7n) Microsoft.OperationsManagement/solutions East US
```

<span data-ttu-id="632ba-109">Эта команда создает решение для аналитики журнала мониторинга для рабочей области "анализ журналов".</span><span class="sxs-lookup"><span data-stu-id="632ba-109">This command creates a monitor log analytics solution for the log analytics workspace.</span></span>

<span data-ttu-id="632ba-110">Чаще всего используются следующие типы:</span><span class="sxs-lookup"><span data-stu-id="632ba-110">Commonly used types are:</span></span>

| <span data-ttu-id="632ba-111">Команду</span><span class="sxs-lookup"><span data-stu-id="632ba-111">Type</span></span> | <span data-ttu-id="632ba-112">Nописание</span><span class="sxs-lookup"><span data-stu-id="632ba-112">Description</span></span> |
| :-----| :----- |
| <span data-ttu-id="632ba-113">SecurityCenterFree</span><span class="sxs-lookup"><span data-stu-id="632ba-113">SecurityCenterFree</span></span> |  <span data-ttu-id="632ba-114">Центр безопасности Azure — бесплатная версия</span><span class="sxs-lookup"><span data-stu-id="632ba-114">Azure Security Center – Free Edition</span></span> |
| <span data-ttu-id="632ba-115">Разрешения</span><span class="sxs-lookup"><span data-stu-id="632ba-115">Security</span></span> | <span data-ttu-id="632ba-116">Центр безопасности Azure</span><span class="sxs-lookup"><span data-stu-id="632ba-116">Azure Security Center</span></span> |
| <span data-ttu-id="632ba-117">Обновлении</span><span class="sxs-lookup"><span data-stu-id="632ba-117">Updates</span></span> | <span data-ttu-id="632ba-118">Управление обновлениями</span><span class="sxs-lookup"><span data-stu-id="632ba-118">Update Management</span></span> |
| <span data-ttu-id="632ba-119">ContainerInsights</span><span class="sxs-lookup"><span data-stu-id="632ba-119">ContainerInsights</span></span> | <span data-ttu-id="632ba-120">Монитор Azure для контейнеров</span><span class="sxs-lookup"><span data-stu-id="632ba-120">Azure Monitor for Containers</span></span> |
| <span data-ttu-id="632ba-121">ServiceMap</span><span class="sxs-lookup"><span data-stu-id="632ba-121">ServiceMap</span></span> | <span data-ttu-id="632ba-122">Карта обслуживания</span><span class="sxs-lookup"><span data-stu-id="632ba-122">Service Map</span></span> |
| <span data-ttu-id="632ba-123">AzureActivity</span><span class="sxs-lookup"><span data-stu-id="632ba-123">AzureActivity</span></span> | <span data-ttu-id="632ba-124">Анализ журнала активности</span><span class="sxs-lookup"><span data-stu-id="632ba-124">Activity log analytics</span></span> |
| <span data-ttu-id="632ba-125">ChangeTracking</span><span class="sxs-lookup"><span data-stu-id="632ba-125">ChangeTracking</span></span> | <span data-ttu-id="632ba-126">Отслеживание изменений и Инвентаризация</span><span class="sxs-lookup"><span data-stu-id="632ba-126">Change tracking and inventory</span></span> |
| <span data-ttu-id="632ba-127">VMInsights</span><span class="sxs-lookup"><span data-stu-id="632ba-127">VMInsights</span></span> | <span data-ttu-id="632ba-128">Монитор Azure для ВМ</span><span class="sxs-lookup"><span data-stu-id="632ba-128">Azure Monitor for VMs</span></span> |
| <span data-ttu-id="632ba-129">SecurityInsights</span><span class="sxs-lookup"><span data-stu-id="632ba-129">SecurityInsights</span></span> | <span data-ttu-id="632ba-130">Sentinel "Azure"</span><span class="sxs-lookup"><span data-stu-id="632ba-130">Azure Sentinel</span></span> |
| <span data-ttu-id="632ba-131">NetworkMonitoring</span><span class="sxs-lookup"><span data-stu-id="632ba-131">NetworkMonitoring</span></span> | <span data-ttu-id="632ba-132">Монитор производительности сети</span><span class="sxs-lookup"><span data-stu-id="632ba-132">Network Performance Monitor</span></span> |
| <span data-ttu-id="632ba-133">SQLVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="632ba-133">SQLVulnerabilityAssessment</span></span> | <span data-ttu-id="632ba-134">Оценка уязвимости SQL</span><span class="sxs-lookup"><span data-stu-id="632ba-134">SQL Vulnerability Assessment</span></span> |
| <span data-ttu-id="632ba-135">SQLAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="632ba-135">SQLAdvancedThreatProtection</span></span> | <span data-ttu-id="632ba-136">Расширенная защита от угроз SQL</span><span class="sxs-lookup"><span data-stu-id="632ba-136">SQL Advanced Threat Protection</span></span> |
| <span data-ttu-id="632ba-137">Антивредоносные программы</span><span class="sxs-lookup"><span data-stu-id="632ba-137">AntiMalware</span></span> | <span data-ttu-id="632ba-138">Оценка защиты от вредоносных программ</span><span class="sxs-lookup"><span data-stu-id="632ba-138">Antimalware Assessment</span></span> |
| <span data-ttu-id="632ba-139">AzureAutomation</span><span class="sxs-lookup"><span data-stu-id="632ba-139">AzureAutomation</span></span> | <span data-ttu-id="632ba-140">Гибридный рабочий процесс автоматизации</span><span class="sxs-lookup"><span data-stu-id="632ba-140">Automation Hybrid Worker</span></span> |
| <span data-ttu-id="632ba-141">LogicAppsManagement</span><span class="sxs-lookup"><span data-stu-id="632ba-141">LogicAppsManagement</span></span> | <span data-ttu-id="632ba-142">Управление логическими приложениями</span><span class="sxs-lookup"><span data-stu-id="632ba-142">Logic Apps Management</span></span> |
| <span data-ttu-id="632ba-143">SQLDataClassification</span><span class="sxs-lookup"><span data-stu-id="632ba-143">SQLDataClassification</span></span> | <span data-ttu-id="632ba-144">Классификация & обнаружения данных SQL</span><span class="sxs-lookup"><span data-stu-id="632ba-144">SQL Data Discovery & Classification</span></span> |

## <span data-ttu-id="632ba-145">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="632ba-145">PARAMETERS</span></span>

### <span data-ttu-id="632ba-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="632ba-146">-DefaultProfile</span></span>
<span data-ttu-id="632ba-147">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="632ba-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="632ba-148">-Location</span><span class="sxs-lookup"><span data-stu-id="632ba-148">-Location</span></span>
<span data-ttu-id="632ba-149">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="632ba-149">Resource location.</span></span>
<span data-ttu-id="632ba-150">Должно совпадать с аналитической рабочей областью журнала.</span><span class="sxs-lookup"><span data-stu-id="632ba-150">Must be the same as the log analytic workspace.</span></span>

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

### <span data-ttu-id="632ba-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="632ba-151">-ResourceGroupName</span></span>
<span data-ttu-id="632ba-152">Имя получаемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="632ba-152">The name of the resource group to get.</span></span>
<span data-ttu-id="632ba-153">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="632ba-153">The name is case insensitive.</span></span>

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

### <span data-ttu-id="632ba-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="632ba-154">-SubscriptionId</span></span>
<span data-ttu-id="632ba-155">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="632ba-155">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="632ba-156">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="632ba-156">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="632ba-157">-Тег</span><span class="sxs-lookup"><span data-stu-id="632ba-157">-Tag</span></span>
<span data-ttu-id="632ba-158">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="632ba-158">Resource tags</span></span>

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

### <span data-ttu-id="632ba-159">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="632ba-159">-Type</span></span>
<span data-ttu-id="632ba-160">Тип создаваемого решения.</span><span class="sxs-lookup"><span data-stu-id="632ba-160">Type of the solution to be created.</span></span>
<span data-ttu-id="632ba-161">Например, "контейнер".</span><span class="sxs-lookup"><span data-stu-id="632ba-161">For example "Container".</span></span>

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

### <span data-ttu-id="632ba-162">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="632ba-162">-WorkspaceResourceId</span></span>
<span data-ttu-id="632ba-163">Идентификатор ресурса Azure для рабочей области, в которой будет развернуто или включено решение.</span><span class="sxs-lookup"><span data-stu-id="632ba-163">The Azure resource ID for the workspace where the solution will be deployed/enabled.</span></span>

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

### <span data-ttu-id="632ba-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="632ba-164">-Confirm</span></span>
<span data-ttu-id="632ba-165">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="632ba-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="632ba-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="632ba-166">-WhatIf</span></span>
<span data-ttu-id="632ba-167">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="632ba-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="632ba-168">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="632ba-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="632ba-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="632ba-169">CommonParameters</span></span>
<span data-ttu-id="632ba-170">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="632ba-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="632ba-171">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="632ba-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="632ba-172">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="632ba-172">INPUTS</span></span>

## <span data-ttu-id="632ba-173">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="632ba-173">OUTPUTS</span></span>

### <span data-ttu-id="632ba-174">Microsoft. Azure. PowerShell. командлеты. MonitoringSolutions. Models. Api20151101Preview. ISolution</span><span class="sxs-lookup"><span data-stu-id="632ba-174">Microsoft.Azure.PowerShell.Cmdlets.MonitoringSolutions.Models.Api20151101Preview.ISolution</span></span>

## <span data-ttu-id="632ba-175">Пуск</span><span class="sxs-lookup"><span data-stu-id="632ba-175">NOTES</span></span>

<span data-ttu-id="632ba-176">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="632ba-176">ALIASES</span></span>

## <span data-ttu-id="632ba-177">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="632ba-177">RELATED LINKS</span></span>



[<span data-ttu-id="632ba-178">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="632ba-178">Get-AzOperationalInsightsWorkspace</span></span>](https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace)

