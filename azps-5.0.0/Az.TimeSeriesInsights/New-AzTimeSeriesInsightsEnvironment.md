---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: b4f27c31ebc3eb54727d6df1139409529c20eed9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248451"
---
# <span data-ttu-id="3e236-101">New-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="3e236-101">New-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="3e236-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e236-102">SYNOPSIS</span></span>
<span data-ttu-id="3e236-103">Создание среды в указанной подписке и группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3e236-103">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="3e236-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e236-104">SYNTAX</span></span>

### <span data-ttu-id="3e236-105">Gen1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3e236-105">Gen1 (Default)</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Capacity <Int32>
 -DataRetentionTime <TimeSpan> -Kind <Kind> -Location <String> -Sku <SkuName> [-SubscriptionId <String>]
 [-PartitionKeyProperty <ITimeSeriesIdProperty[]>] [-StorageLimitExceededBehavior <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3e236-106">Gen2</span><span class="sxs-lookup"><span data-stu-id="3e236-106">Gen2</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Kind <Kind> -Location <String>
 -Sku <SkuName> -StorageAccountKey <SecureString> -StorageAccountName <String>
 -TimeSeriesIdProperty <ITimeSeriesIdProperty[]> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-WarmStoreDataRetentionTime <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="3e236-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e236-107">DESCRIPTION</span></span>
<span data-ttu-id="3e236-108">Создание среды в указанной подписке и группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3e236-108">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="3e236-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e236-109">EXAMPLES</span></span>

### <span data-ttu-id="3e236-110">Пример 1: создание среды Gen1 Time серии Insights</span><span class="sxs-lookup"><span data-stu-id="3e236-110">Example 1: Create a Gen1 time series insights environment</span></span>
```powershell
PS C:\> $TimeSpan = New-TimeSpan -Days 1 -Hours 1 -Minutes 25
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001 -Kind Gen1 -Location eastus -Sku S1 -DataRetentionTime $TimeSpan -Capacity 2

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen1 eastus   tsitest001 2           S1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="3e236-111">Эта команда создает среду Gen1 временной последовательности.</span><span class="sxs-lookup"><span data-stu-id="3e236-111">This command creates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="3e236-112">Пример 2: создание среды Gen2 временных рядов</span><span class="sxs-lookup"><span data-stu-id="3e236-112">Example 2: Create a Gen2 time series insights environment</span></span>
```powershell
PS C:\> $ks = Get-AzStorageAccountKey -ResourceGroupName "testgroup" -Name "staccount001"
PS C:\> $k  = $ks[0].Value | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest002 -Kind Gen2 -Location eastus -Sku L1 -StorageAccountName staccount001 -StorageAccountKey $k -TimeSeriesIdProperty @{name='cdc';type='string'}

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen2 eastus   tsitest002 1           L1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="3e236-113">Эта команда создает среду Gen2 временной последовательности.</span><span class="sxs-lookup"><span data-stu-id="3e236-113">This command creates a Gen2 time series insights environment.</span></span>

## <span data-ttu-id="3e236-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e236-114">PARAMETERS</span></span>

### <span data-ttu-id="3e236-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e236-115">-AsJob</span></span>
<span data-ttu-id="3e236-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="3e236-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3e236-117">-Capacity</span><span class="sxs-lookup"><span data-stu-id="3e236-117">-Capacity</span></span>
<span data-ttu-id="3e236-118">Емкость SKU.</span><span class="sxs-lookup"><span data-stu-id="3e236-118">The capacity of the sku.</span></span>
<span data-ttu-id="3e236-119">Для сред Gen1 это значение может быть изменено для поддержки масштабирования из среды после их создания.</span><span class="sxs-lookup"><span data-stu-id="3e236-119">For Gen1 environments, this value can be changed to support scale out of environments after they have been created.</span></span>

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

### <span data-ttu-id="3e236-120">-DataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="3e236-120">-DataRetentionTime</span></span>
<span data-ttu-id="3e236-121">Время хранения данных.</span><span class="sxs-lookup"><span data-stu-id="3e236-121">The data retention time.</span></span>

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

### <span data-ttu-id="3e236-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e236-122">-DefaultProfile</span></span>
<span data-ttu-id="3e236-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3e236-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e236-124">-Видах</span><span class="sxs-lookup"><span data-stu-id="3e236-124">-Kind</span></span>
<span data-ttu-id="3e236-125">Этот вариант среды.</span><span class="sxs-lookup"><span data-stu-id="3e236-125">The kind of the environment.</span></span>

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

### <span data-ttu-id="3e236-126">-Location</span><span class="sxs-lookup"><span data-stu-id="3e236-126">-Location</span></span>
<span data-ttu-id="3e236-127">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="3e236-127">The location of the resource.</span></span>

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

### <span data-ttu-id="3e236-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3e236-128">-Name</span></span>
<span data-ttu-id="3e236-129">Имя среды</span><span class="sxs-lookup"><span data-stu-id="3e236-129">Name of the environment</span></span>

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

### <span data-ttu-id="3e236-130">-Wait</span><span class="sxs-lookup"><span data-stu-id="3e236-130">-NoWait</span></span>
<span data-ttu-id="3e236-131">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="3e236-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3e236-132">-PartitionKeyProperty</span><span class="sxs-lookup"><span data-stu-id="3e236-132">-PartitionKeyProperty</span></span>
<span data-ttu-id="3e236-133">Список свойств событий, которые будут использоваться для секционирования данных в среде.</span><span class="sxs-lookup"><span data-stu-id="3e236-133">The list of event properties which will be used to partition data in the environment.</span></span>
<span data-ttu-id="3e236-134">Для конструирования ознакомьтесь с разделом "Заметки" для свойств PARTITIONKEYPROPERTY и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="3e236-134">To construct, see NOTES section for PARTITIONKEYPROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="3e236-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e236-135">-ResourceGroupName</span></span>
<span data-ttu-id="3e236-136">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="3e236-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="3e236-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="3e236-137">-Sku</span></span>
<span data-ttu-id="3e236-138">Имя этого SKU.</span><span class="sxs-lookup"><span data-stu-id="3e236-138">The name of this SKU.</span></span>

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

### <span data-ttu-id="3e236-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="3e236-139">-StorageAccountKey</span></span>
<span data-ttu-id="3e236-140">Значение ключа управления, предоставляющего доступ к учетной записи хранения службой аналитики временной последовательности.</span><span class="sxs-lookup"><span data-stu-id="3e236-140">The value of the management key that grants the Time Series Insights service write access to the storage account.</span></span>

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

### <span data-ttu-id="3e236-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3e236-141">-StorageAccountName</span></span>
<span data-ttu-id="3e236-142">Имя учетной записи хранения, которая будет хранить долгосрочные данные среды.</span><span class="sxs-lookup"><span data-stu-id="3e236-142">The name of the storage account that will hold the environment's long term data.</span></span>

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

### <span data-ttu-id="3e236-143">-StorageLimitExceededBehavior</span><span class="sxs-lookup"><span data-stu-id="3e236-143">-StorageLimitExceededBehavior</span></span>
<span data-ttu-id="3e236-144">Поведение службы аналитики временной последовательности, которая должна быть выполнена в случае превышения емкости среды</span><span class="sxs-lookup"><span data-stu-id="3e236-144">The behavior the Time Series Insights service should take when the environment's capacity has been exceeded</span></span>

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

### <span data-ttu-id="3e236-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3e236-145">-SubscriptionId</span></span>
<span data-ttu-id="3e236-146">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="3e236-146">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="3e236-147">-Тег</span><span class="sxs-lookup"><span data-stu-id="3e236-147">-Tag</span></span>
<span data-ttu-id="3e236-148">Пары "ключ-значение" дополнительных свойств ресурса.</span><span class="sxs-lookup"><span data-stu-id="3e236-148">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="3e236-149">-TimeSeriesIdProperty</span><span class="sxs-lookup"><span data-stu-id="3e236-149">-TimeSeriesIdProperty</span></span>
<span data-ttu-id="3e236-150">Список свойств событий, которые будут использоваться для определения идентификатора временного ряда среды. Для конструирования ознакомьтесь с разделом "Заметки" для свойств TIMESERIESIDPROPERTY и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="3e236-150">The list of event properties which will be used to define the environment's time series id. To construct, see NOTES section for TIMESERIESIDPROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="3e236-151">-WarmStoreDataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="3e236-151">-WarmStoreDataRetentionTime</span></span>
<span data-ttu-id="3e236-152">ISO8601 TimeSpan, задающий количество дней, в течение которых события среды будут доступны для запроса из горячего магазина.</span><span class="sxs-lookup"><span data-stu-id="3e236-152">ISO8601 timespan specifying the number of days the environment's events will be available for query from the warm store.</span></span>

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

### <span data-ttu-id="3e236-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e236-153">-Confirm</span></span>
<span data-ttu-id="3e236-154">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3e236-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e236-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e236-155">-WhatIf</span></span>
<span data-ttu-id="3e236-156">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3e236-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e236-157">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3e236-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e236-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e236-158">CommonParameters</span></span>
<span data-ttu-id="3e236-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e236-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e236-160">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e236-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e236-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e236-161">INPUTS</span></span>

## <span data-ttu-id="3e236-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e236-162">OUTPUTS</span></span>

### <span data-ttu-id="3e236-163">Microsoft. Azure. PowerShell. командлеты. TimeSeriesInsights. Models. Api20200515. IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="3e236-163">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="3e236-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e236-164">NOTES</span></span>

<span data-ttu-id="3e236-165">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="3e236-165">ALIASES</span></span>

<span data-ttu-id="3e236-166">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="3e236-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3e236-167">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3e236-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3e236-168">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3e236-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3e236-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty [] >: список свойств событий, которые будут использоваться для секционирования данных в среде.</span><span class="sxs-lookup"><span data-stu-id="3e236-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to partition data in the environment.</span></span>
  - <span data-ttu-id="3e236-170">`[Name <String>]`: Имя свойства.</span><span class="sxs-lookup"><span data-stu-id="3e236-170">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="3e236-171">`[Type <PropertyType?>]`: Тип свойства.</span><span class="sxs-lookup"><span data-stu-id="3e236-171">`[Type <PropertyType?>]`: The type of the property.</span></span>

<span data-ttu-id="3e236-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty [] >: список свойств событий, которые будут использоваться для определения идентификатора временного ряда среды.</span><span class="sxs-lookup"><span data-stu-id="3e236-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to define the environment's time series id.</span></span>
  - <span data-ttu-id="3e236-173">`[Name <String>]`: Имя свойства.</span><span class="sxs-lookup"><span data-stu-id="3e236-173">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="3e236-174">`[Type <PropertyType?>]`: Тип свойства.</span><span class="sxs-lookup"><span data-stu-id="3e236-174">`[Type <PropertyType?>]`: The type of the property.</span></span>

## <span data-ttu-id="3e236-175">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e236-175">RELATED LINKS</span></span>

