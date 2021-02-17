---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
ms.openlocfilehash: d41d99993961906f88dc500603f74fc1a0d4fdf0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404927"
---
# <span data-ttu-id="7a245-101">Set-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="7a245-101">Set-AzDiagnosticSetting</span></span>

## <span data-ttu-id="7a245-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a245-102">SYNOPSIS</span></span>
<span data-ttu-id="7a245-103">Задает параметры журналов и метрик для ресурса.</span><span class="sxs-lookup"><span data-stu-id="7a245-103">Sets the logs and metrics settings for the resource.</span></span>

## <span data-ttu-id="7a245-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7a245-104">SYNTAX</span></span>

### <span data-ttu-id="7a245-105">OldSetDiagnosticSetting (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7a245-105">OldSetDiagnosticSetting (Default)</span></span>
```
Set-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-Enabled <Boolean>] [-Category <System.Collections.Generic.List`1[System.String]>]
 [-MetricCategory <System.Collections.Generic.List`1[System.String]>]
 [-Timegrain <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a245-106">NewSetDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="7a245-106">NewSetDiagnosticSetting</span></span>
```
Set-AzDiagnosticSetting -InputObject <PSServiceDiagnosticSettings> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a245-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a245-107">DESCRIPTION</span></span>
<span data-ttu-id="7a245-108">С **помощью cmdlet Set-AzDiagnosticSetting можно** включить или отключить каждый раз, когда для определенного ресурса настроена категория "вес и журнал".</span><span class="sxs-lookup"><span data-stu-id="7a245-108">The **Set-AzDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>
<span data-ttu-id="7a245-109">Журналы и метрики хранятся в указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="7a245-109">The logs and metrics are stored in the specified storage account.</span></span>
<span data-ttu-id="7a245-110">Этот cmdlet реализует шаблон ShouldProcess, то есть может запросить подтверждение у пользователя перед созданием, изменением или удалением ресурса.</span><span class="sxs-lookup"><span data-stu-id="7a245-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="7a245-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7a245-111">EXAMPLES</span></span>

### <span data-ttu-id="7a245-112">Пример 1. Включить все метрики и журналы для ресурса</span><span class="sxs-lookup"><span data-stu-id="7a245-112">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="7a245-113">Эта команда позволяет включить все доступные метрики и журналы для Resource01.</span><span class="sxs-lookup"><span data-stu-id="7a245-113">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="7a245-114">Пример 2. Отключение всех метрик и журналов</span><span class="sxs-lookup"><span data-stu-id="7a245-114">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="7a245-115">Эта команда отключает все доступные метрики и журналы для ресурса Resource01.</span><span class="sxs-lookup"><span data-stu-id="7a245-115">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="7a245-116">Пример 3. Включив/отключив несколько категорий метрик</span><span class="sxs-lookup"><span data-stu-id="7a245-116">Example 3: Enable/disable multiple metrics categories</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $False -MetricCategory MetricCategory1,MetricCategory2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
   Enabled   : False
   Category  : MetricCategory1
   Timegrain : PT1M
   Enabled   : False
   Category  : MetricCategory2
   Timegrain : PT1H
   Enabled   : True
   Category  : MetricCategory3
   Timegrain : PT1H
Logs
   Enabled  : True
   Category : Category1
   Enabled  : True
   Category : Category2
   Enabled  : True
   Category : Category3
   Enabled  : False
   Category : Category4
```

<span data-ttu-id="7a245-117">Эта команда отключает категории метрик, которые называются Категория1 и Категория2.</span><span class="sxs-lookup"><span data-stu-id="7a245-117">This command disables the metrics categories called Category1 and Category2.</span></span>
<span data-ttu-id="7a245-118">Все остальные категории остаются одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="7a245-118">All the other categories remain the same.</span></span>

### <span data-ttu-id="7a245-119">Пример 4. Включив или отключив несколько категорий журналов</span><span class="sxs-lookup"><span data-stu-id="7a245-119">Example 4: Enable/disable multiple log categories</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Category Category1,Category2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
   Enabled   : False
   Category  : MetricCategory1
   Timegrain : PT1M
   Enabled   : False
   Category  : MetricCategory2
   Timegrain : PT1H
   Enabled   : True
   Category  : MetricCategory3
   Timegrain : PT1H
Logs
   Enabled  : True
   Category : Category1
   Enabled  : True
   Category : Category2
   Enabled  : True
   Category : Category3
   Enabled  : False
   Category : Category4
```

<span data-ttu-id="7a245-120">Эта команда позволяет использовать категории "Категория1" и "Категория2".</span><span class="sxs-lookup"><span data-stu-id="7a245-120">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="7a245-121">Все остальные категории метрик и журналов остаются одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="7a245-121">All the other metrics and logs categories remain the same.</span></span>

### <span data-ttu-id="7a245-122">Пример 4. В этом примере можно включить временную зерну и несколько категорий</span><span class="sxs-lookup"><span data-stu-id="7a245-122">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Category Category1,Category2 -Timegrain PT1M
```

<span data-ttu-id="7a245-123">Эта команда позволяет использовать только категории1, категории2 и время в PT1M.</span><span class="sxs-lookup"><span data-stu-id="7a245-123">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="7a245-124">Все остальные времена и категории остаются без изменений.</span><span class="sxs-lookup"><span data-stu-id="7a245-124">All other time grains and categories are unchanged.</span></span>

### <span data-ttu-id="7a245-125">Пример 5. Использование конвейера</span><span class="sxs-lookup"><span data-stu-id="7a245-125">Example 5: Using pipeline</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "Resource01" | Set-AzDiagnosticSetting
```

<span data-ttu-id="7a245-126">Эта команда использует конвейер PowerShell для настройки (но не изменения) диагностических параметров.</span><span class="sxs-lookup"><span data-stu-id="7a245-126">This command uses the PowerShell pipeline to set (not change made) a diagnostic setting.</span></span>

## <span data-ttu-id="7a245-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a245-127">PARAMETERS</span></span>

### <span data-ttu-id="7a245-128">-Category</span><span class="sxs-lookup"><span data-stu-id="7a245-128">-Category</span></span>
<span data-ttu-id="7a245-129">Список категорий журналов, которые нужно включить или отключить в соответствии со значением *enabled.*</span><span class="sxs-lookup"><span data-stu-id="7a245-129">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="7a245-130">Если категория не указана, эта команда выполняет все поддерживаемые категории.</span><span class="sxs-lookup"><span data-stu-id="7a245-130">If no category is specified, this command operates on all supported categories.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a245-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a245-131">-DefaultProfile</span></span>
<span data-ttu-id="7a245-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7a245-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a245-133">-Enabled</span><span class="sxs-lookup"><span data-stu-id="7a245-133">-Enabled</span></span>
<span data-ttu-id="7a245-134">Указывает, следует ли включить диагностику.</span><span class="sxs-lookup"><span data-stu-id="7a245-134">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="7a245-135">Укажите $True включить или отключить $False.</span><span class="sxs-lookup"><span data-stu-id="7a245-135">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a245-136">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="7a245-136">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="7a245-137">The event hub authorization id</span><span class="sxs-lookup"><span data-stu-id="7a245-137">The event hub authorization rule id</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a245-138">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="7a245-138">-EventHubName</span></span>
<span data-ttu-id="7a245-139">Имя концентратора событий</span><span class="sxs-lookup"><span data-stu-id="7a245-139">The event hub name</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a245-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a245-140">-InputObject</span></span>
<span data-ttu-id="7a245-141">Входной объект (возможно из конвейера). Имена и ид ресурса будут извлечены из этого объекта.</span><span class="sxs-lookup"><span data-stu-id="7a245-141">The input object (possible from the pipeline.) The name and resourceId will be extracted from this object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings
Parameter Sets: NewSetDiagnosticSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a245-142">-MetricCategory</span><span class="sxs-lookup"><span data-stu-id="7a245-142">-MetricCategory</span></span>
<span data-ttu-id="7a245-143">Список категорий метрик.</span><span class="sxs-lookup"><span data-stu-id="7a245-143">The list of metric categories.</span></span>
<span data-ttu-id="7a245-144">Если категория не указана, эта команда выполняет все поддерживаемые категории.</span><span class="sxs-lookup"><span data-stu-id="7a245-144">If no category is specified, this command operates on all supported categories.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a245-145">-Name</span><span class="sxs-lookup"><span data-stu-id="7a245-145">-Name</span></span>
<span data-ttu-id="7a245-146">Имя параметра диагностики.</span><span class="sxs-lookup"><span data-stu-id="7a245-146">The name of the diagnostic setting.</span></span> <span data-ttu-id="7a245-147">Значением по умолчанию является **служба.**</span><span class="sxs-lookup"><span data-stu-id="7a245-147">The default value is **service**.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a245-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a245-148">-ResourceId</span></span>
<span data-ttu-id="7a245-149">Определяет ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="7a245-149">Specifies the ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a245-150">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="7a245-150">-RetentionEnabled</span></span>
<span data-ttu-id="7a245-151">Указывает на то, включено ли хранение диагностических сведений.</span><span class="sxs-lookup"><span data-stu-id="7a245-151">Indicates whether retention of diagnostic information is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a245-152">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="7a245-152">-RetentionInDays</span></span>
<span data-ttu-id="7a245-153">Определяет политику хранения в днях.</span><span class="sxs-lookup"><span data-stu-id="7a245-153">Specifies the retention policy, in days.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a245-154">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="7a245-154">-ServiceBusRuleId</span></span>
<span data-ttu-id="7a245-155">The Service Bus Rule id.</span><span class="sxs-lookup"><span data-stu-id="7a245-155">The Service Bus Rule id.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a245-156">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7a245-156">-StorageAccountId</span></span>
<span data-ttu-id="7a245-157">Определяет ИД учетной записи хранения, в которой нужно сохранить данные.</span><span class="sxs-lookup"><span data-stu-id="7a245-157">Specifies the ID of the Storage account in which to save the data.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a245-158">-Timegrain</span><span class="sxs-lookup"><span data-stu-id="7a245-158">-Timegrain</span></span>
<span data-ttu-id="7a245-159">Определяет значения времени, заданные для включения или отключения метрик, в соответствии со значением *Enabled.*</span><span class="sxs-lookup"><span data-stu-id="7a245-159">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="7a245-160">Если не указать время, эта команда выполняется со всеми доступными зернами времени.</span><span class="sxs-lookup"><span data-stu-id="7a245-160">If you do not specify a time grain, this command operates on all available time grains.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a245-161">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="7a245-161">-WorkspaceId</span></span>
<span data-ttu-id="7a245-162">ИД ресурса рабочей области "Аналитика журналов" для отправки журналов и метрик в</span><span class="sxs-lookup"><span data-stu-id="7a245-162">The resource Id of the Log Analytics workspace to send logs/metrics to</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a245-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a245-163">-Confirm</span></span>
<span data-ttu-id="7a245-164">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="7a245-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a245-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a245-165">-WhatIf</span></span>
<span data-ttu-id="7a245-166">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a245-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7a245-167">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7a245-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a245-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a245-168">CommonParameters</span></span>
<span data-ttu-id="7a245-169">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a245-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a245-170">Дополнительные сведения см. [в about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a245-170">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a245-171">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a245-171">INPUTS</span></span>

### <span data-ttu-id="7a245-172">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="7a245-172">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

### <span data-ttu-id="7a245-173">System.String</span><span class="sxs-lookup"><span data-stu-id="7a245-173">System.String</span></span>

### <span data-ttu-id="7a245-174">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7a245-174">System.Boolean</span></span>

### <span data-ttu-id="7a245-175">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7a245-175">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7a245-176">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7a245-176">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7a245-177">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7a245-177">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7a245-178">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7a245-178">OUTPUTS</span></span>

### <span data-ttu-id="7a245-179">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="7a245-179">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="7a245-180">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7a245-180">NOTES</span></span>

## <span data-ttu-id="7a245-181">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a245-181">RELATED LINKS</span></span>

<span data-ttu-id="7a245-182">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="7a245-182">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
