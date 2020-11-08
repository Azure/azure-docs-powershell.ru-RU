---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
ms.openlocfilehash: eeadf64c83f62a8d245a7ace8f750b34ddc230ce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236094"
---
# <span data-ttu-id="9e4b9-101">Set-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="9e4b9-101">Set-AzDiagnosticSetting</span></span>

## <span data-ttu-id="9e4b9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9e4b9-102">SYNOPSIS</span></span>
<span data-ttu-id="9e4b9-103">Задает параметры журналов и метрик для ресурса.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-103">Sets the logs and metrics settings for the resource.</span></span>

## <span data-ttu-id="9e4b9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9e4b9-104">SYNTAX</span></span>

### <span data-ttu-id="9e4b9-105">OldSetDiagnosticSetting (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9e4b9-105">OldSetDiagnosticSetting (Default)</span></span>
```
Set-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-Enabled <Boolean>] [-Category <System.Collections.Generic.List`1[System.String]>]
 [-MetricCategory <System.Collections.Generic.List`1[System.String]>]
 [-Timegrain <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-ExportToResourceSpecific] [-EnableLog <Boolean>]
 [-EnableMetrics <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9e4b9-106">NewSetDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="9e4b9-106">NewSetDiagnosticSetting</span></span>
```
Set-AzDiagnosticSetting -InputObject <PSServiceDiagnosticSettings> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e4b9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e4b9-107">DESCRIPTION</span></span>
<span data-ttu-id="9e4b9-108">Командлет **Set-AzDiagnosticSetting** включает или выключает каждый Временный промежуток и категорию журнала для определенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-108">The **Set-AzDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>
<span data-ttu-id="9e4b9-109">Журналы и метрики хранятся в указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-109">The logs and metrics are stored in the specified storage account.</span></span>
<span data-ttu-id="9e4b9-110">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно создать, изменить или удалить ресурс.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="9e4b9-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9e4b9-111">EXAMPLES</span></span>

### <span data-ttu-id="9e4b9-112">Пример 1: включение всех метрик и журналов для ресурса</span><span class="sxs-lookup"><span data-stu-id="9e4b9-112">Example 1: Enable all metrics and logs for a resource</span></span>
```powershell
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="9e4b9-113">Эта команда включает все доступные метрики и журналы для Resource01.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-113">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="9e4b9-114">Пример 2: Отключение всех метрик и журналов</span><span class="sxs-lookup"><span data-stu-id="9e4b9-114">Example 2: Disable all metrics and logs</span></span>
```powershell
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="9e4b9-115">Эта команда отключает все доступные метрики и журналы для Resource01 ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-115">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="9e4b9-116">Пример 3: Включение и отключение нескольких категорий метрик</span><span class="sxs-lookup"><span data-stu-id="9e4b9-116">Example 3: Enable/disable multiple metrics categories</span></span>
```powershell
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

<span data-ttu-id="9e4b9-117">Эта команда отключает категории метрики с именем Category1 и Category2.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-117">This command disables the metrics categories called Category1 and Category2.</span></span>
<span data-ttu-id="9e4b9-118">Все остальные категории остаются прежними.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-118">All the other categories remain the same.</span></span>

### <span data-ttu-id="9e4b9-119">Пример 4: Включение и отключение нескольких категорий журналов</span><span class="sxs-lookup"><span data-stu-id="9e4b9-119">Example 4: Enable/disable multiple log categories</span></span>
```powershell
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

<span data-ttu-id="9e4b9-120">Эта команда включает Category1 и Category2.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-120">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="9e4b9-121">Все другие категории метрики и журналы останутся прежними.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-121">All the other metrics and logs categories remain the same.</span></span>

### <span data-ttu-id="9e4b9-122">Пример 5: включение многогранного интервала и нескольких категорий</span><span class="sxs-lookup"><span data-stu-id="9e4b9-122">Example 5: Enable a time grain and multiple categories</span></span>
```powershell
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Category Category1,Category2 -Timegrain PT1M
```

<span data-ttu-id="9e4b9-123">Эта команда включает только Category1, Category2 и зернистость времени PT1M.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-123">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="9e4b9-124">Все остальные временные Гранки и категории не изменяются.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-124">All other time grains and categories are unchanged.</span></span>

### <span data-ttu-id="9e4b9-125">Пример 6: использование конвейера</span><span class="sxs-lookup"><span data-stu-id="9e4b9-125">Example 6: Using pipeline</span></span>
```powershell
PS C:\>Get-AzDiagnosticSetting -ResourceId "Resource01" | Set-AzDiagnosticSetting -Enabled $True -Category Category1,Category2
```

<span data-ttu-id="9e4b9-126">Эта команда использует конвейер PowerShell для установки (без изменений) параметра диагностики.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-126">This command uses the PowerShell pipeline to set (no change made) a diagnostic setting.</span></span>

## <span data-ttu-id="9e4b9-127">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9e4b9-127">PARAMETERS</span></span>

### <span data-ttu-id="9e4b9-128">-Категория</span><span class="sxs-lookup"><span data-stu-id="9e4b9-128">-Category</span></span>
<span data-ttu-id="9e4b9-129">Указывает список категорий журналов для включения или отключения в соответствии со значением *Enabled*.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-129">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="9e4b9-130">Если категория не указана, эта команда работает со всеми поддерживаемыми категориями.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-130">If no category is specified, this command operates on all supported categories.</span></span> 

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

### <span data-ttu-id="9e4b9-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e4b9-131">-DefaultProfile</span></span>
<span data-ttu-id="9e4b9-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9e4b9-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e4b9-133">-Включено</span><span class="sxs-lookup"><span data-stu-id="9e4b9-133">-Enabled</span></span>
<span data-ttu-id="9e4b9-134">Указывает, следует ли включить диагностику.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-134">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="9e4b9-135">Укажите $True, чтобы включить диагностику, или $False, чтобы отключить диагностику.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-135">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

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

### <span data-ttu-id="9e4b9-136">-EnableLog</span><span class="sxs-lookup"><span data-stu-id="9e4b9-136">-EnableLog</span></span>
<span data-ttu-id="9e4b9-137">Значение, указывающее, следует ли включать или отключать журналы диагностики</span><span class="sxs-lookup"><span data-stu-id="9e4b9-137">The value indicating whether the diagnostic logs should be enabled or disabled</span></span>

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

### <span data-ttu-id="9e4b9-138">-EnableMetrics</span><span class="sxs-lookup"><span data-stu-id="9e4b9-138">-EnableMetrics</span></span>
<span data-ttu-id="9e4b9-139">Значение, указывающее, следует ли включить или отключить метрики диагностики</span><span class="sxs-lookup"><span data-stu-id="9e4b9-139">The value indicating whether the diagnostic metrics should be enabled or disabled</span></span>

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

### <span data-ttu-id="9e4b9-140">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="9e4b9-140">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="9e4b9-141">Идентификатор правила авторизации концентратора событий</span><span class="sxs-lookup"><span data-stu-id="9e4b9-141">The event hub authorization rule id</span></span>

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

### <span data-ttu-id="9e4b9-142">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="9e4b9-142">-EventHubName</span></span>
<span data-ttu-id="9e4b9-143">Имя концентратора событий</span><span class="sxs-lookup"><span data-stu-id="9e4b9-143">The event hub name</span></span>

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

### <span data-ttu-id="9e4b9-144">-ExportToResourceSpecific</span><span class="sxs-lookup"><span data-stu-id="9e4b9-144">-ExportToResourceSpecific</span></span>
<span data-ttu-id="9e4b9-145">Флаг, указывающий на то, что экспорт в LA должен выполняться для таблицы с определенным ресурсом, с указанием</span><span class="sxs-lookup"><span data-stu-id="9e4b9-145">Flag indicating that the export to LA must be done to a resource specific table, a.k.a.</span></span> <span data-ttu-id="9e4b9-146">выделенная или фиксированная Таблица схемы, а не динамическая таблица схемы, **используемая по умолчанию** с именем **AzureDiagnostics**.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-146">dedicated or fixed schema table, as opposed to the **default** dynamic schema table called **AzureDiagnostics**.</span></span>

<span data-ttu-id="9e4b9-147">Этот аргумент действует только в том случае, если также задан аргумент **-workspaceId** .</span><span class="sxs-lookup"><span data-stu-id="9e4b9-147">This argument is effective only when the argument **-workspaceId** is also given.</span></span>

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

### <span data-ttu-id="9e4b9-148">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e4b9-148">-InputObject</span></span>
<span data-ttu-id="9e4b9-149">Входной объект (возможно, из конвейера). Имя и resourceId будут извлечены из этого объекта.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-149">The input object (possible from the pipeline.) The name and resourceId will be extracted from this object.</span></span>

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

### <span data-ttu-id="9e4b9-150">-MetricCategory</span><span class="sxs-lookup"><span data-stu-id="9e4b9-150">-MetricCategory</span></span>
<span data-ttu-id="9e4b9-151">Список категорий метрик.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-151">The list of metric categories.</span></span> <span data-ttu-id="9e4b9-152">Если категория не указана, эта команда работает со всеми поддерживаемыми категориями.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-152">If no category is specified, this command operates on all supported categories.</span></span> 

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

### <span data-ttu-id="9e4b9-153">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9e4b9-153">-Name</span></span>
<span data-ttu-id="9e4b9-154">Имя параметра диагностики.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-154">The name of the diagnostic setting.</span></span> <span data-ttu-id="9e4b9-155">По умолчанию используется значение **Service**.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-155">The default value is **service**.</span></span>

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

### <span data-ttu-id="9e4b9-156">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e4b9-156">-ResourceId</span></span>
<span data-ttu-id="9e4b9-157">Указывает идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-157">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="9e4b9-158">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="9e4b9-158">-RetentionEnabled</span></span>
<span data-ttu-id="9e4b9-159">Указывает, включена ли хранение диагностических данных.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-159">Indicates whether retention of diagnostic information is enabled.</span></span>

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

### <span data-ttu-id="9e4b9-160">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="9e4b9-160">-RetentionInDays</span></span>
<span data-ttu-id="9e4b9-161">Указывает политику хранения в днях.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-161">Specifies the retention policy, in days.</span></span>

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

### <span data-ttu-id="9e4b9-162">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="9e4b9-162">-ServiceBusRuleId</span></span>
<span data-ttu-id="9e4b9-163">Идентификатор правила служебной шины.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-163">The Service Bus Rule id.</span></span>

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

### <span data-ttu-id="9e4b9-164">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="9e4b9-164">-StorageAccountId</span></span>
<span data-ttu-id="9e4b9-165">Указывает идентификатор учетной записи хранения, в которой нужно сохранить данные.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-165">Specifies the ID of the Storage account in which to save the data.</span></span>

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

### <span data-ttu-id="9e4b9-166">-Timegrain</span><span class="sxs-lookup"><span data-stu-id="9e4b9-166">-Timegrain</span></span>
<span data-ttu-id="9e4b9-167">Задает временные зависимости для включения или отключения метрик в соответствии со значением *Enabled*.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-167">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="9e4b9-168">Если вы не укажете промежуток времени, эта команда будет работать на всех доступных гранях времени.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-168">If you do not specify a time grain, this command operates on all available time grains.</span></span>

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

### <span data-ttu-id="9e4b9-169">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="9e4b9-169">-WorkspaceId</span></span>
<span data-ttu-id="9e4b9-170">Идентификатор ресурса рабочей области службы анализа журналов для отправки журналов и метрик</span><span class="sxs-lookup"><span data-stu-id="9e4b9-170">The resource Id of the Log Analytics workspace to send logs/metrics to</span></span>

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

### <span data-ttu-id="9e4b9-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e4b9-171">-Confirm</span></span>
<span data-ttu-id="9e4b9-172">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e4b9-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e4b9-173">-WhatIf</span></span>
<span data-ttu-id="9e4b9-174">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-174">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e4b9-175">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e4b9-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e4b9-176">CommonParameters</span></span>
<span data-ttu-id="9e4b9-177">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9e4b9-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e4b9-178">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e4b9-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e4b9-179">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9e4b9-179">INPUTS</span></span>

### <span data-ttu-id="9e4b9-180">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="9e4b9-180">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

### <span data-ttu-id="9e4b9-181">System. String</span><span class="sxs-lookup"><span data-stu-id="9e4b9-181">System.String</span></span>

### <span data-ttu-id="9e4b9-182">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9e4b9-182">System.Boolean</span></span>

### <span data-ttu-id="9e4b9-183">System. Collections. Generic. List "1 [[System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9e4b9-183">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9e4b9-184">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9e4b9-184">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9e4b9-185">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9e4b9-185">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9e4b9-186">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e4b9-186">OUTPUTS</span></span>

### <span data-ttu-id="9e4b9-187">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="9e4b9-187">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="9e4b9-188">Пуск</span><span class="sxs-lookup"><span data-stu-id="9e4b9-188">NOTES</span></span>

## <span data-ttu-id="9e4b9-189">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e4b9-189">RELATED LINKS</span></span>

<span data-ttu-id="9e4b9-190">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="9e4b9-190">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
