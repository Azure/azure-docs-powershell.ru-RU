---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
ms.openlocfilehash: 554a754d8d7e6000556b2141807d2b6fe86cc230
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911770"
---
# <span data-ttu-id="cf08b-101">Set-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="cf08b-101">Set-AzDiagnosticSetting</span></span>

## <span data-ttu-id="cf08b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cf08b-102">SYNOPSIS</span></span>
<span data-ttu-id="cf08b-103">Задает параметры журналов и метрик для ресурса.</span><span class="sxs-lookup"><span data-stu-id="cf08b-103">Sets the logs and metrics settings for the resource.</span></span>

## <span data-ttu-id="cf08b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cf08b-104">SYNTAX</span></span>

### <span data-ttu-id="cf08b-105">OldSetDiagnosticSetting (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cf08b-105">OldSetDiagnosticSetting (Default)</span></span>
```
Set-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-Enabled <Boolean>] [-Category <System.Collections.Generic.List`1[System.String]>]
 [-MetricCategory <System.Collections.Generic.List`1[System.String]>]
 [-Timegrain <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-ExportToResourceSpecific] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf08b-106">NewSetDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="cf08b-106">NewSetDiagnosticSetting</span></span>
```
Set-AzDiagnosticSetting -InputObject <PSServiceDiagnosticSettings> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf08b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf08b-107">DESCRIPTION</span></span>
<span data-ttu-id="cf08b-108">Командлет **Set-AzDiagnosticSetting** включает или выключает каждый Временный промежуток и категорию журнала для определенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="cf08b-108">The **Set-AzDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>
<span data-ttu-id="cf08b-109">Журналы и метрики хранятся в указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="cf08b-109">The logs and metrics are stored in the specified storage account.</span></span>
<span data-ttu-id="cf08b-110">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно создать, изменить или удалить ресурс.</span><span class="sxs-lookup"><span data-stu-id="cf08b-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="cf08b-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cf08b-111">EXAMPLES</span></span>

### <span data-ttu-id="cf08b-112">Пример 1: включение всех метрик и журналов для ресурса</span><span class="sxs-lookup"><span data-stu-id="cf08b-112">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="cf08b-113">Эта команда включает все доступные метрики и журналы для Resource01.</span><span class="sxs-lookup"><span data-stu-id="cf08b-113">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="cf08b-114">Пример 2: Отключение всех метрик и журналов</span><span class="sxs-lookup"><span data-stu-id="cf08b-114">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="cf08b-115">Эта команда отключает все доступные метрики и журналы для Resource01 ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cf08b-115">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="cf08b-116">Пример 3: Включение и отключение нескольких категорий метрик</span><span class="sxs-lookup"><span data-stu-id="cf08b-116">Example 3: Enable/disable multiple metrics categories</span></span>
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

<span data-ttu-id="cf08b-117">Эта команда отключает категории метрики с именем Category1 и Category2.</span><span class="sxs-lookup"><span data-stu-id="cf08b-117">This command disables the metrics categories called Category1 and Category2.</span></span>
<span data-ttu-id="cf08b-118">Все остальные категории остаются прежними.</span><span class="sxs-lookup"><span data-stu-id="cf08b-118">All the other categories remain the same.</span></span>

### <span data-ttu-id="cf08b-119">Пример 4: Включение и отключение нескольких категорий журналов</span><span class="sxs-lookup"><span data-stu-id="cf08b-119">Example 4: Enable/disable multiple log categories</span></span>
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

<span data-ttu-id="cf08b-120">Эта команда включает Category1 и Category2.</span><span class="sxs-lookup"><span data-stu-id="cf08b-120">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="cf08b-121">Все другие категории метрики и журналы останутся прежними.</span><span class="sxs-lookup"><span data-stu-id="cf08b-121">All the other metrics and logs categories remain the same.</span></span>

### <span data-ttu-id="cf08b-122">Пример 4: включение многогранного интервала и нескольких категорий</span><span class="sxs-lookup"><span data-stu-id="cf08b-122">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Category Category1,Category2 -Timegrain PT1M
```

<span data-ttu-id="cf08b-123">Эта команда включает только Category1, Category2 и зернистость времени PT1M.</span><span class="sxs-lookup"><span data-stu-id="cf08b-123">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="cf08b-124">Все остальные временные Гранки и категории не изменяются.</span><span class="sxs-lookup"><span data-stu-id="cf08b-124">All other time grains and categories are unchanged.</span></span>

### <span data-ttu-id="cf08b-125">Пример 5: использование конвейера</span><span class="sxs-lookup"><span data-stu-id="cf08b-125">Example 5: Using pipeline</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "Resource01" | Set-AzDiagnosticSetting -Enabled $True -Category Category1,Category2
```

<span data-ttu-id="cf08b-126">Эта команда использует конвейер PowerShell для установки (без изменений) параметра диагностики.</span><span class="sxs-lookup"><span data-stu-id="cf08b-126">This command uses the PowerShell pipeline to set (no change made) a diagnostic setting.</span></span>

## <span data-ttu-id="cf08b-127">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cf08b-127">PARAMETERS</span></span>

### <span data-ttu-id="cf08b-128">-Категория</span><span class="sxs-lookup"><span data-stu-id="cf08b-128">-Category</span></span>
<span data-ttu-id="cf08b-129">Указывает список категорий журналов для включения или отключения в соответствии со значением *Enabled*.</span><span class="sxs-lookup"><span data-stu-id="cf08b-129">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="cf08b-130">Если категория не указана, эта команда работает со всеми поддерживаемыми категориями.</span><span class="sxs-lookup"><span data-stu-id="cf08b-130">If no category is specified, this command operates on all supported categories.</span></span> 

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

### <span data-ttu-id="cf08b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf08b-131">-DefaultProfile</span></span>
<span data-ttu-id="cf08b-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="cf08b-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf08b-133">-Включено</span><span class="sxs-lookup"><span data-stu-id="cf08b-133">-Enabled</span></span>
<span data-ttu-id="cf08b-134">Указывает, следует ли включить диагностику.</span><span class="sxs-lookup"><span data-stu-id="cf08b-134">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="cf08b-135">Укажите $True, чтобы включить диагностику, или $False, чтобы отключить диагностику.</span><span class="sxs-lookup"><span data-stu-id="cf08b-135">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

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

### <span data-ttu-id="cf08b-136">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="cf08b-136">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="cf08b-137">Идентификатор правила авторизации концентратора событий</span><span class="sxs-lookup"><span data-stu-id="cf08b-137">The event hub authorization rule id</span></span>

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

### <span data-ttu-id="cf08b-138">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="cf08b-138">-EventHubName</span></span>
<span data-ttu-id="cf08b-139">Имя концентратора событий</span><span class="sxs-lookup"><span data-stu-id="cf08b-139">The event hub name</span></span>

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

### <span data-ttu-id="cf08b-140">-ExportToResourceSpecific</span><span class="sxs-lookup"><span data-stu-id="cf08b-140">-ExportToResourceSpecific</span></span>
<span data-ttu-id="cf08b-141">Флаг, указывающий на то, что экспорт в LA должен выполняться для таблицы с определенным ресурсом, с указанием</span><span class="sxs-lookup"><span data-stu-id="cf08b-141">Flag indicating that the export to LA must be done to a resource specific table, a.k.a.</span></span> <span data-ttu-id="cf08b-142">выделенная или фиксированная Таблица схемы, а не динамическая таблица схемы, **используемая по умолчанию** с именем **AzureDiagnostics**.</span><span class="sxs-lookup"><span data-stu-id="cf08b-142">dedicated or fixed schema table, as opposed to the **default** dynamic schema table called **AzureDiagnostics**.</span></span>

<span data-ttu-id="cf08b-143">Этот аргумент действует только в том случае, если также задан аргумент **-workspaceId** .</span><span class="sxs-lookup"><span data-stu-id="cf08b-143">This argument is effective only when the argument **-workspaceId** is also given.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf08b-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf08b-144">-InputObject</span></span>
<span data-ttu-id="cf08b-145">Входной объект (возможно, из конвейера). Имя и resourceId будут извлечены из этого объекта.</span><span class="sxs-lookup"><span data-stu-id="cf08b-145">The input object (possible from the pipeline.) The name and resourceId will be extracted from this object.</span></span>

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

### <span data-ttu-id="cf08b-146">-MetricCategory</span><span class="sxs-lookup"><span data-stu-id="cf08b-146">-MetricCategory</span></span>
<span data-ttu-id="cf08b-147">Список категорий метрик.</span><span class="sxs-lookup"><span data-stu-id="cf08b-147">The list of metric categories.</span></span> <span data-ttu-id="cf08b-148">Если категория не указана, эта команда работает со всеми поддерживаемыми категориями.</span><span class="sxs-lookup"><span data-stu-id="cf08b-148">If no category is specified, this command operates on all supported categories.</span></span> 

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

### <span data-ttu-id="cf08b-149">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cf08b-149">-Name</span></span>
<span data-ttu-id="cf08b-150">Имя параметра диагностики.</span><span class="sxs-lookup"><span data-stu-id="cf08b-150">The name of the diagnostic setting.</span></span> <span data-ttu-id="cf08b-151">По умолчанию используется значение **Service**.</span><span class="sxs-lookup"><span data-stu-id="cf08b-151">The default value is **service**.</span></span>

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

### <span data-ttu-id="cf08b-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf08b-152">-ResourceId</span></span>
<span data-ttu-id="cf08b-153">Указывает идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="cf08b-153">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="cf08b-154">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="cf08b-154">-RetentionEnabled</span></span>
<span data-ttu-id="cf08b-155">Указывает, включена ли хранение диагностических данных.</span><span class="sxs-lookup"><span data-stu-id="cf08b-155">Indicates whether retention of diagnostic information is enabled.</span></span>

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

### <span data-ttu-id="cf08b-156">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="cf08b-156">-RetentionInDays</span></span>
<span data-ttu-id="cf08b-157">Указывает политику хранения в днях.</span><span class="sxs-lookup"><span data-stu-id="cf08b-157">Specifies the retention policy, in days.</span></span>

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

### <span data-ttu-id="cf08b-158">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="cf08b-158">-ServiceBusRuleId</span></span>
<span data-ttu-id="cf08b-159">Идентификатор правила служебной шины.</span><span class="sxs-lookup"><span data-stu-id="cf08b-159">The Service Bus Rule id.</span></span>

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

### <span data-ttu-id="cf08b-160">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="cf08b-160">-StorageAccountId</span></span>
<span data-ttu-id="cf08b-161">Указывает идентификатор учетной записи хранения, в которой нужно сохранить данные.</span><span class="sxs-lookup"><span data-stu-id="cf08b-161">Specifies the ID of the Storage account in which to save the data.</span></span>

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

### <span data-ttu-id="cf08b-162">-Timegrain</span><span class="sxs-lookup"><span data-stu-id="cf08b-162">-Timegrain</span></span>
<span data-ttu-id="cf08b-163">Задает временные зависимости для включения или отключения метрик в соответствии со значением *Enabled*.</span><span class="sxs-lookup"><span data-stu-id="cf08b-163">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="cf08b-164">Если вы не укажете промежуток времени, эта команда будет работать на всех доступных гранях времени.</span><span class="sxs-lookup"><span data-stu-id="cf08b-164">If you do not specify a time grain, this command operates on all available time grains.</span></span>

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

### <span data-ttu-id="cf08b-165">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="cf08b-165">-WorkspaceId</span></span>
<span data-ttu-id="cf08b-166">Идентификатор рабочей области.</span><span class="sxs-lookup"><span data-stu-id="cf08b-166">The Id of the workspace</span></span>

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

### <span data-ttu-id="cf08b-167">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf08b-167">-Confirm</span></span>
<span data-ttu-id="cf08b-168">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cf08b-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf08b-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf08b-169">-WhatIf</span></span>
<span data-ttu-id="cf08b-170">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cf08b-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf08b-171">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cf08b-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf08b-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf08b-172">CommonParameters</span></span>
<span data-ttu-id="cf08b-173">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cf08b-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf08b-174">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf08b-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf08b-175">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cf08b-175">INPUTS</span></span>

### <span data-ttu-id="cf08b-176">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="cf08b-176">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

### <span data-ttu-id="cf08b-177">System. String</span><span class="sxs-lookup"><span data-stu-id="cf08b-177">System.String</span></span>

### <span data-ttu-id="cf08b-178">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cf08b-178">System.Boolean</span></span>

### <span data-ttu-id="cf08b-179">System. Collections. Generic. List "1 [[System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cf08b-179">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="cf08b-180">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cf08b-180">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="cf08b-181">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cf08b-181">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="cf08b-182">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf08b-182">OUTPUTS</span></span>

### <span data-ttu-id="cf08b-183">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="cf08b-183">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="cf08b-184">Пуск</span><span class="sxs-lookup"><span data-stu-id="cf08b-184">NOTES</span></span>

## <span data-ttu-id="cf08b-185">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf08b-185">RELATED LINKS</span></span>

<span data-ttu-id="cf08b-186">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="cf08b-186">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
