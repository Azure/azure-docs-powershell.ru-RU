---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/update-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
ms.openlocfilehash: 86b6067e13a7b4d1d90e8fcb3d308af797dab354
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969880"
---
# <span data-ttu-id="b0fbc-101">Update-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="b0fbc-101">Update-AzSentinelAlertRule</span></span>

## <span data-ttu-id="b0fbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0fbc-102">SYNOPSIS</span></span>
<span data-ttu-id="b0fbc-103">Создание аналитического правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-103">Create an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="b0fbc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b0fbc-104">SYNTAX</span></span>

### <span data-ttu-id="b0fbc-105">AlertRuleId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b0fbc-105">AlertRuleId (Default)</span></span>
```
Update-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-AlertRuleTemplateName <String>] [-Enabled] [-Disabled] [-DisplayName <String>]
 [-ProductFilter <String>] [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>] [-SuppressionDuration <TimeSpan>]
 [-SuppressionEnabled] [-SuppressionDisabled] [-Query <String>] [-QueryFrequency <TimeSpan>]
 [-QueryPeriod <TimeSpan>] [-Severity <String>] [-Tactics <System.Collections.Generic.IList`1[System.String]>]
 [-TriggerOperator <TriggerOperator>] [-TriggerThreshold <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0fbc-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b0fbc-106">InputObject</span></span>
```
Update-AzSentinelAlertRule [-AlertRuleTemplateName <String>] [-Enabled] [-Disabled]
 [-DisplayName <String>] [-ProductFilter <String>] [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>] [-SuppressionDuration <TimeSpan>]
 [-SuppressionEnabled] [-SuppressionDisabled] [-Query <String>] [-QueryFrequency <TimeSpan>]
 [-QueryPeriod <TimeSpan>] [-Severity <String>] [-Tactics <System.Collections.Generic.IList`1[System.String]>]
 [-TriggerOperator <TriggerOperator>] [-TriggerThreshold <Int32>] -InputObject <PSSentinelAlertRule>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0fbc-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0fbc-107">ResourceId</span></span>
```
Update-AzSentinelAlertRule [-AlertRuleTemplateName <String>] [-Enabled] [-Disabled]
 [-DisplayName <String>] [-ProductFilter <String>] [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>] [-SuppressionDuration <TimeSpan>]
 [-SuppressionEnabled] [-SuppressionDisabled] [-Query <String>] [-QueryFrequency <TimeSpan>]
 [-QueryPeriod <TimeSpan>] [-Severity <String>] [-Tactics <System.Collections.Generic.IList`1[System.String]>]
 [-TriggerOperator <TriggerOperator>] [-TriggerThreshold <Int32>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0fbc-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0fbc-108">DESCRIPTION</span></span>
<span data-ttu-id="b0fbc-109">Для обновления правила оповещения в указанной рабочей области обновляется **cmdlet Update-AzSentinelAlertRule.**</span><span class="sxs-lookup"><span data-stu-id="b0fbc-109">The **Update-AzSentinelAlertRule** cmdlet updates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="b0fbc-110">Можно использовать -InputObject или -ResourceId или -AlertId.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-110">You can use an -InputObject or -ResourceId or -AlertId.</span></span>  <span data-ttu-id="b0fbc-111">Вы можете обновить один или несколько дополнительных партераров.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-111">You can update 1 or more proprtery parmaters.</span></span>
<span data-ttu-id="b0fbc-112">Параметр Confirm  и переменная $ConfirmPreference Windows PowerShell можно использовать для управления запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>


## <span data-ttu-id="b0fbc-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b0fbc-113">EXAMPLES</span></span>

### <span data-ttu-id="b0fbc-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b0fbc-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -Disabled -DisplayName "Disabled-AlertRuleDisplayName"
```

<span data-ttu-id="b0fbc-115">В этом примере обновление параметра **AlertRule** для параметра *Disabled* и переименования *disabled-AlertRuleDisplayName.*</span><span class="sxs-lookup"><span data-stu-id="b0fbc-115">This example updates an **AlertRule** setting it to *Disabled* and renames to *Disabled-AlertRuleDisplayName*.</span></span>  <span data-ttu-id="b0fbc-116">Все остальные свойства останутся без сухую.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-116">All other properties will remain the same.</span></span>

### <span data-ttu-id="b0fbc-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b0fbc-117">Example 2</span></span>
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
PS C:\> Update-AzSentinelAlertRule -InputObject $AlertRule -Disabled
```

<span data-ttu-id="b0fbc-118">В этом примере обновление параметра **AlertRule** с помощью параметра InputObject, который он *отключил.*</span><span class="sxs-lookup"><span data-stu-id="b0fbc-118">This example updates an **AlertRule** using an InputObject setting it to *Disabled*.</span></span>  <span data-ttu-id="b0fbc-119">Все остальные свойства останутся без сухую.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-119">All other properties will remain the same.</span></span>


## <span data-ttu-id="b0fbc-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0fbc-120">PARAMETERS</span></span>

### <span data-ttu-id="b0fbc-121">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="b0fbc-121">-AlertRuleId</span></span>
<span data-ttu-id="b0fbc-122">ИД правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-122">Alert Rule Id.</span></span>

```yaml
Type: String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fbc-123">-AlertRuleTemplateName</span><span class="sxs-lookup"><span data-stu-id="b0fbc-123">-AlertRuleTemplateName</span></span>
<span data-ttu-id="b0fbc-124">Шаблон правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-124">Alert Rule Template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fbc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0fbc-125">-DefaultProfile</span></span>
<span data-ttu-id="b0fbc-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fbc-127">-Description</span><span class="sxs-lookup"><span data-stu-id="b0fbc-127">-Description</span></span>
<span data-ttu-id="b0fbc-128">Описание.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-128">Description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fbc-129">-Disabled</span><span class="sxs-lookup"><span data-stu-id="b0fbc-129">-Disabled</span></span>
<span data-ttu-id="b0fbc-130">Правило оповещения отключено.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-130">Alert Rule Disabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fbc-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b0fbc-131">-DisplayName</span></span>
<span data-ttu-id="b0fbc-132">Отображаемая имя правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-132">Alert Rule Display Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fbc-133">-DisplayNamesExcludeFilter</span><span class="sxs-lookup"><span data-stu-id="b0fbc-133">-DisplayNamesExcludeFilter</span></span>
<span data-ttu-id="b0fbc-134">Отображаемая фильтрация имен в правиле оповещения.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-134">Alert Rule Display Names Exclude Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fbc-135">-DisplayNamesFilter</span><span class="sxs-lookup"><span data-stu-id="b0fbc-135">-DisplayNamesFilter</span></span>
<span data-ttu-id="b0fbc-136">Фильтр отображаемой области имен в правиле оповещения.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-136">Alert Rule Display Names Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fbc-137">-Enabled</span><span class="sxs-lookup"><span data-stu-id="b0fbc-137">-Enabled</span></span>
<span data-ttu-id="b0fbc-138">Правило оповещения включено.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-138">Alert Rule Enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fbc-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0fbc-139">-InputObject</span></span>
<span data-ttu-id="b0fbc-140">InputObject.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-140">InputObject.</span></span>

```yaml
Type: PSSentinelAlertRule
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0fbc-141">-ProductFilter</span><span class="sxs-lookup"><span data-stu-id="b0fbc-141">-ProductFilter</span></span>
<span data-ttu-id="b0fbc-142">Фильтр по правилу оповещения.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-142">Alert Rule Product Filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Azure Active Directory Identity Protection, Azure Advanced Threat Protection, Azure Security Center, Azure Security Center for IoT, Microsoft Cloud App Security, Microsoft Defender Advanced Threat Protection, Office 365 Advanced Threat Protection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fbc-143">-Query</span><span class="sxs-lookup"><span data-stu-id="b0fbc-143">-Query</span></span>
<span data-ttu-id="b0fbc-144">Запрос правил оповещения.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-144">Alert Rule Query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fbc-145">-QueryFrequency</span><span class="sxs-lookup"><span data-stu-id="b0fbc-145">-QueryFrequency</span></span>
<span data-ttu-id="b0fbc-146">Частота запроса правил оповещения.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-146">Alert Rule Query Frequency.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fbc-147">-QueryPeriod</span><span class="sxs-lookup"><span data-stu-id="b0fbc-147">-QueryPeriod</span></span>
<span data-ttu-id="b0fbc-148">Период запроса правил оповещения.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-148">Alert Rule Query Period.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fbc-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0fbc-149">-ResourceGroupName</span></span>
<span data-ttu-id="b0fbc-150">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-150">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fbc-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0fbc-151">-ResourceId</span></span>
<span data-ttu-id="b0fbc-152">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-152">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0fbc-153">-SeveritiesFilter</span><span class="sxs-lookup"><span data-stu-id="b0fbc-153">-SeveritiesFilter</span></span>
<span data-ttu-id="b0fbc-154">Фильтр серьезности правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-154">Alert Rule Severities Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fbc-155">-Severity</span><span class="sxs-lookup"><span data-stu-id="b0fbc-155">-Severity</span></span>
<span data-ttu-id="b0fbc-156">Серьезность инцидента.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-156">Incident Severity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fbc-157">-SuppressionDisabled</span><span class="sxs-lookup"><span data-stu-id="b0fbc-157">-SuppressionDisabled</span></span>
<span data-ttu-id="b0fbc-158">Отключено правило оповещения.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-158">Alert Rule Suppression Disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fbc-159">-SuppressionDuration</span><span class="sxs-lookup"><span data-stu-id="b0fbc-159">-SuppressionDuration</span></span>
<span data-ttu-id="b0fbc-160">Длительность подавляции правил оповещения.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-160">Alert Rule Suppression Duration.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fbc-161">-SuppressionEnabled</span><span class="sxs-lookup"><span data-stu-id="b0fbc-161">-SuppressionEnabled</span></span>
<span data-ttu-id="b0fbc-162">Включено подавления правил оповещения.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-162">Alert Rule Suppression Enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fbc-163">-Ит-приемы</span><span class="sxs-lookup"><span data-stu-id="b0fbc-163">-Tactics</span></span>
<span data-ttu-id="b0fbc-164">Приемы правил оповещения.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-164">Alert Rule Tactics.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fbc-165">-TriggerOperator</span><span class="sxs-lookup"><span data-stu-id="b0fbc-165">-TriggerOperator</span></span>
<span data-ttu-id="b0fbc-166">Оператор триггера правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-166">Alert Rule Trigger Operator.</span></span>

```yaml
Type: TriggerOperator
Parameter Sets: (All)
Aliases:
Accepted values: GreaterThan, LessThan, Equal, NotEqual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fbc-167">-TriggerThreshold</span><span class="sxs-lookup"><span data-stu-id="b0fbc-167">-TriggerThreshold</span></span>
<span data-ttu-id="b0fbc-168">Пороговое значение триггера правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-168">Alert Rule Trigger Threshold.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fbc-169">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b0fbc-169">-WorkspaceName</span></span>
<span data-ttu-id="b0fbc-170">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-170">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fbc-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0fbc-171">-Confirm</span></span>
<span data-ttu-id="b0fbc-172">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-172">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fbc-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0fbc-173">-WhatIf</span></span>
<span data-ttu-id="b0fbc-174">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0fbc-175">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-175">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0fbc-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0fbc-176">CommonParameters</span></span>
<span data-ttu-id="b0fbc-177">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0fbc-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0fbc-178">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0fbc-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0fbc-179">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0fbc-179">INPUTS</span></span>

### <span data-ttu-id="b0fbc-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="b0fbc-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

### <span data-ttu-id="b0fbc-181">System.String</span><span class="sxs-lookup"><span data-stu-id="b0fbc-181">System.String</span></span>

## <span data-ttu-id="b0fbc-182">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b0fbc-182">OUTPUTS</span></span>

### <span data-ttu-id="b0fbc-183">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="b0fbc-183">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

## <span data-ttu-id="b0fbc-184">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b0fbc-184">NOTES</span></span>

## <span data-ttu-id="b0fbc-185">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b0fbc-185">RELATED LINKS</span></span>
