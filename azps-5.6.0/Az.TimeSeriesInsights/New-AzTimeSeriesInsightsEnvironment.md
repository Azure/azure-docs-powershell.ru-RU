---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 51cbe7cd6d4e08543feadb5ddd096330763b7236
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955048"
---
# <span data-ttu-id="597b5-101">New-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="597b5-101">New-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="597b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="597b5-102">SYNOPSIS</span></span>
<span data-ttu-id="597b5-103">Создайте среду в указанной группе подписок и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="597b5-103">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="597b5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="597b5-104">SYNTAX</span></span>

### <span data-ttu-id="597b5-105">Gen1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="597b5-105">Gen1 (Default)</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Capacity <Int32>
 -DataRetentionTime <TimeSpan> -Kind <Kind> -Location <String> -Sku <SkuName> [-SubscriptionId <String>]
 [-PartitionKeyProperty <ITimeSeriesIdProperty[]>] [-StorageLimitExceededBehavior <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="597b5-106">Gen2</span><span class="sxs-lookup"><span data-stu-id="597b5-106">Gen2</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Kind <Kind> -Location <String>
 -Sku <SkuName> -StorageAccountKey <SecureString> -StorageAccountName <String>
 -TimeSeriesIdProperty <ITimeSeriesIdProperty[]> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-WarmStoreDataRetentionTime <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="597b5-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="597b5-107">DESCRIPTION</span></span>
<span data-ttu-id="597b5-108">Создайте среду в указанной группе подписок и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="597b5-108">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="597b5-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="597b5-109">EXAMPLES</span></span>

### <span data-ttu-id="597b5-110">Пример 1. Создание среды для анализа ряда времени «Один»"</span><span class="sxs-lookup"><span data-stu-id="597b5-110">Example 1: Create a Gen1 time series insights environment</span></span>
```powershell
PS C:\> $TimeSpan = New-TimeSpan -Days 1 -Hours 1 -Minutes 25
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001 -Kind Gen1 -Location eastus -Sku S1 -DataRetentionTime $TimeSpan -Capacity 2

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen1 eastus   tsitest001 2           S1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="597b5-111">Эта команда создает среду для анализа рядов времени поколения 1.</span><span class="sxs-lookup"><span data-stu-id="597b5-111">This command creates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="597b5-112">Пример 2. Создание среды для анализа ряда времени (Gen2)</span><span class="sxs-lookup"><span data-stu-id="597b5-112">Example 2: Create a Gen2 time series insights environment</span></span>
```powershell
PS C:\> $ks = Get-AzStorageAccountKey -ResourceGroupName "testgroup" -Name "staccount001"
PS C:\> $k  = $ks[0].Value | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest002 -Kind Gen2 -Location eastus -Sku L1 -StorageAccountName staccount001 -StorageAccountKey $k -TimeSeriesIdProperty @{name='cdc';type='string'}

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen2 eastus   tsitest002 1           L1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="597b5-113">Эта команда создает среду статистики по ряду времени (Gen2).</span><span class="sxs-lookup"><span data-stu-id="597b5-113">This command creates a Gen2 time series insights environment.</span></span>

## <span data-ttu-id="597b5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="597b5-114">PARAMETERS</span></span>

### <span data-ttu-id="597b5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="597b5-115">-AsJob</span></span>
<span data-ttu-id="597b5-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="597b5-116">Run the command as a job</span></span>

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

### <span data-ttu-id="597b5-117">-Capacity</span><span class="sxs-lookup"><span data-stu-id="597b5-117">-Capacity</span></span>
<span data-ttu-id="597b5-118">Емкость SKU.</span><span class="sxs-lookup"><span data-stu-id="597b5-118">The capacity of the sku.</span></span>
<span data-ttu-id="597b5-119">В средах Gen1 это значение можно изменить, чтобы масштабировать уже созданные среды.</span><span class="sxs-lookup"><span data-stu-id="597b5-119">For Gen1 environments, this value can be changed to support scale out of environments after they have been created.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Gen1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597b5-120">-DataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="597b5-120">-DataRetentionTime</span></span>
<span data-ttu-id="597b5-121">Время хранения данных.</span><span class="sxs-lookup"><span data-stu-id="597b5-121">The data retention time.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Gen1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597b5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="597b5-122">-DefaultProfile</span></span>
<span data-ttu-id="597b5-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="597b5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="597b5-124">-Kind</span><span class="sxs-lookup"><span data-stu-id="597b5-124">-Kind</span></span>
<span data-ttu-id="597b5-125">Тип среды.</span><span class="sxs-lookup"><span data-stu-id="597b5-125">The kind of the environment.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597b5-126">-Location</span><span class="sxs-lookup"><span data-stu-id="597b5-126">-Location</span></span>
<span data-ttu-id="597b5-127">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="597b5-127">The location of the resource.</span></span>

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

### <span data-ttu-id="597b5-128">-Name</span><span class="sxs-lookup"><span data-stu-id="597b5-128">-Name</span></span>
<span data-ttu-id="597b5-129">Название среды</span><span class="sxs-lookup"><span data-stu-id="597b5-129">Name of the environment</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597b5-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="597b5-130">-NoWait</span></span>
<span data-ttu-id="597b5-131">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="597b5-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="597b5-132">-PartitionKeyProperty</span><span class="sxs-lookup"><span data-stu-id="597b5-132">-PartitionKeyProperty</span></span>
<span data-ttu-id="597b5-133">Список свойств событий, которые будут использоваться для разгона данных в среде.</span><span class="sxs-lookup"><span data-stu-id="597b5-133">The list of event properties which will be used to partition data in the environment.</span></span>
<span data-ttu-id="597b5-134">Чтобы построить новую таблицу, см. раздел "ЗАМЕТКИ" для свойств PARTITIONKEYPROPERTY и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="597b5-134">To construct, see NOTES section for PARTITIONKEYPROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.ITimeSeriesIdProperty[]
Parameter Sets: Gen1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597b5-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="597b5-135">-ResourceGroupName</span></span>
<span data-ttu-id="597b5-136">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="597b5-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="597b5-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="597b5-137">-Sku</span></span>
<span data-ttu-id="597b5-138">Имя этого SKU.</span><span class="sxs-lookup"><span data-stu-id="597b5-138">The name of this SKU.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597b5-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="597b5-139">-StorageAccountKey</span></span>
<span data-ttu-id="597b5-140">Значение ключа управления, предоставляемого службе Time Series Insights для записи доступа к учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="597b5-140">The value of the management key that grants the Time Series Insights service write access to the storage account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: Gen2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597b5-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="597b5-141">-StorageAccountName</span></span>
<span data-ttu-id="597b5-142">Имя учетной записи хранения, которая будет хранением долгосрочных данных среды.</span><span class="sxs-lookup"><span data-stu-id="597b5-142">The name of the storage account that will hold the environment's long term data.</span></span>

```yaml
Type: System.String
Parameter Sets: Gen2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597b5-143">-StorageLimitExceededBehavior</span><span class="sxs-lookup"><span data-stu-id="597b5-143">-StorageLimitExceededBehavior</span></span>
<span data-ttu-id="597b5-144">Поведение службы Time Series Insights должно происходить при превышении емкости среды</span><span class="sxs-lookup"><span data-stu-id="597b5-144">The behavior the Time Series Insights service should take when the environment's capacity has been exceeded</span></span>

```yaml
Type: System.String
Parameter Sets: Gen1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597b5-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="597b5-145">-SubscriptionId</span></span>
<span data-ttu-id="597b5-146">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="597b5-146">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="597b5-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="597b5-147">-Tag</span></span>
<span data-ttu-id="597b5-148">Пары ключевых значений дополнительных свойств для ресурса.</span><span class="sxs-lookup"><span data-stu-id="597b5-148">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="597b5-149">-TimeSeriesIdProperty</span><span class="sxs-lookup"><span data-stu-id="597b5-149">-TimeSeriesIdProperty</span></span>
<span data-ttu-id="597b5-150">Список свойств событий, которые будут использоваться для определения свойства ряда времени среды. Чтобы построить новую таблицу, см. раздел "ПРИМЕЧАНИЯ" для свойств TIMESERIESIDPROPERTY и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="597b5-150">The list of event properties which will be used to define the environment's time series id. To construct, see NOTES section for TIMESERIESIDPROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.ITimeSeriesIdProperty[]
Parameter Sets: Gen2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597b5-151">-WarmStoreDataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="597b5-151">-WarmStoreDataRetentionTime</span></span>
<span data-ttu-id="597b5-152">Период времени ISO8601, определяющий, в течение каких дней события среды будут доступны для запроса из теплого магазина.</span><span class="sxs-lookup"><span data-stu-id="597b5-152">ISO8601 timespan specifying the number of days the environment's events will be available for query from the warm store.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Gen2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597b5-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="597b5-153">-Confirm</span></span>
<span data-ttu-id="597b5-154">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="597b5-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="597b5-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="597b5-155">-WhatIf</span></span>
<span data-ttu-id="597b5-156">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="597b5-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="597b5-157">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="597b5-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="597b5-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="597b5-158">CommonParameters</span></span>
<span data-ttu-id="597b5-159">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="597b5-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="597b5-160">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="597b5-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="597b5-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="597b5-161">INPUTS</span></span>

## <span data-ttu-id="597b5-162">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="597b5-162">OUTPUTS</span></span>

### <span data-ttu-id="597b5-163">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="597b5-163">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="597b5-164">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="597b5-164">NOTES</span></span>

<span data-ttu-id="597b5-165">ALIASES</span><span class="sxs-lookup"><span data-stu-id="597b5-165">ALIASES</span></span>

<span data-ttu-id="597b5-166">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="597b5-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="597b5-167">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="597b5-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="597b5-168">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="597b5-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="597b5-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty[]>: список свойств событий, которые будут использоваться для секционния данных в среде.</span><span class="sxs-lookup"><span data-stu-id="597b5-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to partition data in the environment.</span></span>
  - <span data-ttu-id="597b5-170">`[Name <String>]`: Имя свойства.</span><span class="sxs-lookup"><span data-stu-id="597b5-170">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="597b5-171">`[Type <PropertyType?>]`Тип свойства.</span><span class="sxs-lookup"><span data-stu-id="597b5-171">`[Type <PropertyType?>]`: The type of the property.</span></span>

<span data-ttu-id="597b5-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty[]>: список свойств событий, которые будут использоваться для определения свойства ряда времени среды.</span><span class="sxs-lookup"><span data-stu-id="597b5-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to define the environment's time series id.</span></span>
  - <span data-ttu-id="597b5-173">`[Name <String>]`: Имя свойства.</span><span class="sxs-lookup"><span data-stu-id="597b5-173">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="597b5-174">`[Type <PropertyType?>]`Тип свойства.</span><span class="sxs-lookup"><span data-stu-id="597b5-174">`[Type <PropertyType?>]`: The type of the property.</span></span>

## <span data-ttu-id="597b5-175">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="597b5-175">RELATED LINKS</span></span>

