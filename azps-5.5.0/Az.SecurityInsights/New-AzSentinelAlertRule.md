---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRule.md
ms.openlocfilehash: 97a07b515cff6cfd8521033dbe7380eb2a7bc1d1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235828"
---
# <span data-ttu-id="9a805-101">New-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="9a805-101">New-AzSentinelAlertRule</span></span>

## <span data-ttu-id="9a805-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a805-102">SYNOPSIS</span></span>
<span data-ttu-id="9a805-103">Создание аналитического правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="9a805-103">Create an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="9a805-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9a805-104">SYNTAX</span></span>

### <span data-ttu-id="9a805-105">ScheduledAlertRule (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9a805-105">ScheduledAlertRule (Default)</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> [-Scheduled]
 [-AlertRuleId <String>] [-AlertRuleTemplateName <String>] [-Enabled] -DisplayName <String>
 [-Description <String>] [-SuppressionDuration <TimeSpan>] [-SuppressionEnabled] -Query <String>
 -QueryFrequency <TimeSpan> -QueryPeriod <TimeSpan> -Severity <String>
 [-Tactics <System.Collections.Generic.IList`1[System.String]>] [-TriggerOperator <TriggerOperator>]
 -TriggerThreshold <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a805-106">2AlertRule</span><span class="sxs-lookup"><span data-stu-id="9a805-106">FusionAlertRule</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> [-Fusion] [-AlertRuleId <String>]
 -AlertRuleTemplateName <String> [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a805-107">MicrosoftSecurityIncidentCreationRule</span><span class="sxs-lookup"><span data-stu-id="9a805-107">MicrosoftSecurityIncidentCreationRule</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String>
 [-MicrosoftSecurityIncidentCreation] [-AlertRuleId <String>] [-AlertRuleTemplateName <String>] [-Enabled]
 -DisplayName <String> -ProductFilter <String> [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a805-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a805-108">DESCRIPTION</span></span>
<span data-ttu-id="9a805-109">Для создания правила оповещения **New-AzSentinelAlertRule** в указанной рабочей области создается правило аналитического оповещения.</span><span class="sxs-lookup"><span data-stu-id="9a805-109">The **New-AzSentinelAlertRule** cmdlet creates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="9a805-110">Необходимо указать один из трех параметров: *"План",*"Запланировано" или *"MicrosoftSecurityIncidentCreation",* чтобы указать тип созда создаемого правила оповещения. </span><span class="sxs-lookup"><span data-stu-id="9a805-110">You must specify one of the three parameters, *Fusion*, *Scheduled* or *MicrosoftSecurityIncidentCreation*, to specify the kind of Alert rule to create.</span></span>  <span data-ttu-id="9a805-111">У каждого типа есть разные параметры.</span><span class="sxs-lookup"><span data-stu-id="9a805-111">Each Kind has different required paramaters.</span></span>
<span data-ttu-id="9a805-112">С помощью переменных *Confirm* и $ConfirmPreference Windows PowerShell можно управлять запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a805-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="9a805-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9a805-113">EXAMPLES</span></span>

### <span data-ttu-id="9a805-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9a805-114">Example 1</span></span>
```powershell
PS C:\>$AlertRuleTemplateName = "f71aba3d-28fb-450b-b192-4e76a83015c8"
PS C:\>$AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Fusion -Enabled -AlertRuleTemplateName $AlertRuleTemplateName
```

<span data-ttu-id="9a805-115">В этом примере создается тип **AlertRule** типа *"Да",* основанный на шаблоне для *advanced Multistage Attack Detection,* и он сохраняется в переменной $AlertRule.</span><span class="sxs-lookup"><span data-stu-id="9a805-115">This example creates a **AlertRule** of the *Fusion* kind based on the Template for *Advanced Multistage Attack Detection*, and then stores it in the $AlertRule variable.</span></span>

### <span data-ttu-id="9a805-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9a805-116">Example 2</span></span>
```powershell
PS C:\> $AlertRuleTemplateName = "a2e0eb51-1f11-461a-999b-cd0ebe5c7a72"
PS C:\> $AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -MicrosoftSecurityIncidentCreation -Enabled -AlertRuleTemplateName $AlertRuleTemplateName -DisplayName "Create incidents based on Azure Security Center for IoT" -ProductFilter "Azure Security Center for IoT"
```

<span data-ttu-id="9a805-117">В этом примере создается предупреждение типа *MicrosoftSecurityIncidentCreation,* основанное на шаблоне "Создать инциденты" на основе оповещений Azure "Центр безопасности *для IoT",* и оно сохраняется в $AlertRule безопасности. </span><span class="sxs-lookup"><span data-stu-id="9a805-117">This example creates a **AlertRule** of the *MicrosoftSecurityIncidentCreation* kind based on the template for *Create incidents based on Azure Security Center for IoT alerts*, and then stores it in the $AlertRule varaible.</span></span>

### <span data-ttu-id="9a805-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9a805-118">Example 2</span></span>
```powershell
PS C:\> $AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Scheduled -Enabled -DisplayName "Powershell Exection Alert (Several Times per Hour)" -Severity Low -Query "SecurityEvent | where EventId == 4688" -QueryFrequency (New-TimeSpan -Hours 1) -QueryPeriod (New-TimeSpan -Hours 1) -TriggerThreshold 10
```

<span data-ttu-id="9a805-119">В этом примере создается  запланированный тип **DataConnector,** который затем сохраняется $AlertRule ненадегим.</span><span class="sxs-lookup"><span data-stu-id="9a805-119">This example creates a **DataConnector** of the *Scheduled* kind, and then stores it in the $AlertRule varaible.</span></span>

## <span data-ttu-id="9a805-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a805-120">PARAMETERS</span></span>

### <span data-ttu-id="9a805-121">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="9a805-121">-AlertRuleId</span></span>
<span data-ttu-id="9a805-122">ИД правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="9a805-122">Alert Rule Id.</span></span>

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

### <span data-ttu-id="9a805-123">-AlertRuleTemplateName</span><span class="sxs-lookup"><span data-stu-id="9a805-123">-AlertRuleTemplateName</span></span>
<span data-ttu-id="9a805-124">Шаблон правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="9a805-124">Alert Rule Template.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule, MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: FusionAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a805-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a805-125">-DefaultProfile</span></span>
<span data-ttu-id="9a805-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9a805-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a805-127">-Description</span><span class="sxs-lookup"><span data-stu-id="9a805-127">-Description</span></span>
<span data-ttu-id="9a805-128">Описание.</span><span class="sxs-lookup"><span data-stu-id="9a805-128">Description.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule, MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a805-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9a805-129">-DisplayName</span></span>
<span data-ttu-id="9a805-130">Отображаемая имя правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="9a805-130">Alert Rule Display Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule, MicrosoftSecurityIncidentCreationRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a805-131">-DisplayNamesExcludeFilter</span><span class="sxs-lookup"><span data-stu-id="9a805-131">-DisplayNamesExcludeFilter</span></span>
<span data-ttu-id="9a805-132">Отображаемая фильтрация имен в правиле оповещения.</span><span class="sxs-lookup"><span data-stu-id="9a805-132">Alert Rule Display Names Exclude Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a805-133">-DisplayNamesFilter</span><span class="sxs-lookup"><span data-stu-id="9a805-133">-DisplayNamesFilter</span></span>
<span data-ttu-id="9a805-134">Фильтр отображаемой области имен в правиле оповещения.</span><span class="sxs-lookup"><span data-stu-id="9a805-134">Alert Rule Display Names Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a805-135">-Enabled</span><span class="sxs-lookup"><span data-stu-id="9a805-135">-Enabled</span></span>
<span data-ttu-id="9a805-136">Правило оповещения включено.</span><span class="sxs-lookup"><span data-stu-id="9a805-136">Alert Rule Enabled.</span></span>

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

### <span data-ttu-id="9a805-137">-А</span><span class="sxs-lookup"><span data-stu-id="9a805-137">-Fusion</span></span>
<span data-ttu-id="9a805-138">Тип правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="9a805-138">Alert Rule Kind.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FusionAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a805-139">-MicrosoftSecurityIncidentCreation</span><span class="sxs-lookup"><span data-stu-id="9a805-139">-MicrosoftSecurityIncidentCreation</span></span>
<span data-ttu-id="9a805-140">Тип правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="9a805-140">Alert Rule Kind.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a805-141">-ProductFilter</span><span class="sxs-lookup"><span data-stu-id="9a805-141">-ProductFilter</span></span>
<span data-ttu-id="9a805-142">Фильтр по правилу оповещения.</span><span class="sxs-lookup"><span data-stu-id="9a805-142">Alert Rule Product Filter.</span></span>

```yaml
Type: System.String
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:
Accepted values: Azure Active Directory Identity Protection, Azure Advanced Threat Protection, Azure Security Center, Azure Security Center for IoT, Microsoft Cloud App Security, Microsoft Defender Advanced Threat Protection, Office 365 Advanced Threat Protection

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a805-143">-Query</span><span class="sxs-lookup"><span data-stu-id="9a805-143">-Query</span></span>
<span data-ttu-id="9a805-144">Запрос правил оповещения.</span><span class="sxs-lookup"><span data-stu-id="9a805-144">Alert Rule Query.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a805-145">-QueryFrequency</span><span class="sxs-lookup"><span data-stu-id="9a805-145">-QueryFrequency</span></span>
<span data-ttu-id="9a805-146">Частота запроса правил оповещения.</span><span class="sxs-lookup"><span data-stu-id="9a805-146">Alert Rule Query Frequency.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a805-147">-QueryPeriod</span><span class="sxs-lookup"><span data-stu-id="9a805-147">-QueryPeriod</span></span>
<span data-ttu-id="9a805-148">Период запроса правил оповещения.</span><span class="sxs-lookup"><span data-stu-id="9a805-148">Alert Rule Query Period.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a805-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a805-149">-ResourceGroupName</span></span>
<span data-ttu-id="9a805-150">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9a805-150">Resource group name.</span></span>

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

### <span data-ttu-id="9a805-151">-Запланировано</span><span class="sxs-lookup"><span data-stu-id="9a805-151">-Scheduled</span></span>
<span data-ttu-id="9a805-152">Тип правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="9a805-152">Alert Rule Kind.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a805-153">-SeveritiesFilter</span><span class="sxs-lookup"><span data-stu-id="9a805-153">-SeveritiesFilter</span></span>
<span data-ttu-id="9a805-154">Фильтр серьезности правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="9a805-154">Alert Rule Severities Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a805-155">-Severity</span><span class="sxs-lookup"><span data-stu-id="9a805-155">-Severity</span></span>
<span data-ttu-id="9a805-156">Серьезность инцидента.</span><span class="sxs-lookup"><span data-stu-id="9a805-156">Incident Severity.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule
Aliases:
Accepted values: High, Informational, Low, Medium

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a805-157">-SuppressionDuration</span><span class="sxs-lookup"><span data-stu-id="9a805-157">-SuppressionDuration</span></span>
<span data-ttu-id="9a805-158">Длительность подавляции правил оповещения.</span><span class="sxs-lookup"><span data-stu-id="9a805-158">Alert Rule Suppression Duration.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: ScheduledAlertRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a805-159">-SuppressionEnabled</span><span class="sxs-lookup"><span data-stu-id="9a805-159">-SuppressionEnabled</span></span>
<span data-ttu-id="9a805-160">Включено подавления правил оповещения.</span><span class="sxs-lookup"><span data-stu-id="9a805-160">Alert Rule Suppression Enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScheduledAlertRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a805-161">-Приемы</span><span class="sxs-lookup"><span data-stu-id="9a805-161">-Tactics</span></span>
<span data-ttu-id="9a805-162">Приемы правил оповещения.</span><span class="sxs-lookup"><span data-stu-id="9a805-162">Alert Rule Tactics.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a805-163">-TriggerOperator</span><span class="sxs-lookup"><span data-stu-id="9a805-163">-TriggerOperator</span></span>
<span data-ttu-id="9a805-164">Оператор триггера правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="9a805-164">Alert Rule Trigger Operator.</span></span>

```yaml
Type: Microsoft.Azure.Management.SecurityInsights.Models.TriggerOperator
Parameter Sets: ScheduledAlertRule
Aliases:
Accepted values: Equal, GreaterThan, LessThan, NotEqual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a805-165">-TriggerThreshold</span><span class="sxs-lookup"><span data-stu-id="9a805-165">-TriggerThreshold</span></span>
<span data-ttu-id="9a805-166">Пороговое значение триггера правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="9a805-166">Alert Rule Trigger Threshold.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a805-167">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9a805-167">-WorkspaceName</span></span>
<span data-ttu-id="9a805-168">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="9a805-168">Workspace Name.</span></span>

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

### <span data-ttu-id="9a805-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a805-169">-Confirm</span></span>
<span data-ttu-id="9a805-170">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a805-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a805-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a805-171">-WhatIf</span></span>
<span data-ttu-id="9a805-172">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a805-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a805-173">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9a805-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a805-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a805-174">CommonParameters</span></span>
<span data-ttu-id="9a805-175">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a805-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a805-176">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a805-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a805-177">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9a805-177">INPUTS</span></span>

### <span data-ttu-id="9a805-178">Нет</span><span class="sxs-lookup"><span data-stu-id="9a805-178">None</span></span>
## <span data-ttu-id="9a805-179">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9a805-179">OUTPUTS</span></span>

### <span data-ttu-id="9a805-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="9a805-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="9a805-181">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9a805-181">NOTES</span></span>

## <span data-ttu-id="9a805-182">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a805-182">RELATED LINKS</span></span>
