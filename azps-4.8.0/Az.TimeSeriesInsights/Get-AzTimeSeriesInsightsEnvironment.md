---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: f4f42b257c5ce54085214c8cd9d2f79d9e8a6387
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244673"
---
# <span data-ttu-id="892e1-101">Get-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="892e1-101">Get-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="892e1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="892e1-102">SYNOPSIS</span></span>
<span data-ttu-id="892e1-103">Возвращает среду с указанным именем в указанной подписке и группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="892e1-103">Gets the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="892e1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="892e1-104">SYNTAX</span></span>

### <span data-ttu-id="892e1-105">List1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="892e1-105">List1 (Default)</span></span>
```
Get-AzTimeSeriesInsightsEnvironment [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="892e1-106">Получить</span><span class="sxs-lookup"><span data-stu-id="892e1-106">Get</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="892e1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="892e1-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Expand <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="892e1-108">Список</span><span class="sxs-lookup"><span data-stu-id="892e1-108">List</span></span>
```
Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="892e1-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="892e1-109">DESCRIPTION</span></span>
<span data-ttu-id="892e1-110">Возвращает среду с указанным именем в указанной подписке и группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="892e1-110">Gets the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="892e1-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="892e1-111">EXAMPLES</span></span>

### <span data-ttu-id="892e1-112">Пример 1: получение среды с подробным представлением временной последовательности</span><span class="sxs-lookup"><span data-stu-id="892e1-112">Example 1: Get a time series insights environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001

DataAccessFqdn               : b6d113a4-0865-405f-b09e-ad4355b5d046.env.timeseries.azure.com
DataAccessId                 : b6d113a4-0865-405f-b09e-ad4355b5d046
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest 
                               001
IngressState                 :
Kind                         : Gen1
Location                     : eastus
Name                         : tsitest001
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 2
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="892e1-113">Эта команда возвращает среду с подробным анализом временной последовательности.</span><span class="sxs-lookup"><span data-stu-id="892e1-113">This command gets a time series insights environment.</span></span>

### <span data-ttu-id="892e1-114">Пример 2: список всех сред для анализа временных рядов</span><span class="sxs-lookup"><span data-stu-id="892e1-114">Example 2: List all time series insights environments</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup

DataAccessFqdn                      : 3de1d1e1-4f9b-4bc6-aad3-a835597dcd86.env.timeseries.azure.com
DataAccessId                        : 3de1d1e1-4f9b-4bc6-aad3-a835597dcd86
Id                                  : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/ 
                                      tsill
IngressState                        :
Kind                                : Gen2
Location                            : EastUs
Name                                : tsill
PropertyUsageState                  :
Sku                                 : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                         : 1
SkuName                             : L1
StateDetailCode                     :
StateDetailCurrentCount             :
StateDetailMaxCount                 :
StateDetailMessage                  :
StorageConfigurationAccountName     : cdolauli
Tag                                 : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
TimeSeriesIdProperty                : {ccc}
Type                                : Microsoft.TimeSeriesInsights/Environments
WarmStoreConfigurationDataRetention : 00:00:00

DataAccessFqdn               : b6d113a4-0865-405f-b09e-ad4355b5d046.env.timeseries.azure.com
DataAccessId                 : b6d113a4-0865-405f-b09e-ad4355b5d046
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/testgroup/providers/Microsoft.TimeSeriesInsights/environments/tsitest 
                               001
IngressState                 :
Kind                         : Gen1
Location                     : eastus
Name                         : tsitest001
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 2
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="892e1-115">Эта команда выводит список всех сред "анализ временной последовательности" в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="892e1-115">This command lists all time series insights environments in a resource group.</span></span>

### <span data-ttu-id="892e1-116">Пример 3: получение средой анализа временных рядов по объекту</span><span class="sxs-lookup"><span data-stu-id="892e1-116">Example 3: Get a time series insights environment by object</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName tsi-test-i01k5l -Name tsi-envv8u56x 
PS C:\> Get-AzTimeSeriesInsightsEnvironment -InputObject $env

DataAccessFqdn               : d76a61f2-8a30-41a5-9587-f241eb9b48d9.env.timeseries.azure.com
DataAccessId                 : d76a61f2-8a30-41a5-9587-f241eb9b48d9
DataRetentionTime            : 1.01:25:00
Id                           : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/tsi-test-i01k5l/providers/Microsoft.TimeSeriesInsights/environments/tsi-envv8u56x
IngressState                 :
Kind                         : Gen1
Location                     : eastus2
Name                         : tsi-envv8u56x
PartitionKeyProperty         :
PropertyUsageState           :
Sku                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.Sku
SkuCapacity                  : 1
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="892e1-117">Эта команда получает сведения о средах с подробными сведениями о временной последовательности.</span><span class="sxs-lookup"><span data-stu-id="892e1-117">This command gets a time series insights environments.</span></span>

## <span data-ttu-id="892e1-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="892e1-118">PARAMETERS</span></span>

### <span data-ttu-id="892e1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="892e1-119">-DefaultProfile</span></span>
<span data-ttu-id="892e1-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="892e1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="892e1-121">-Expand</span><span class="sxs-lookup"><span data-stu-id="892e1-121">-Expand</span></span>
<span data-ttu-id="892e1-122">При задании $expand = Status будут включены сведения о состоянии внутренних служб среды в службе аналитики временной последовательности.</span><span class="sxs-lookup"><span data-stu-id="892e1-122">Setting $expand=status will include the status of the internal services of the environment in the Time Series Insights service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="892e1-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="892e1-123">-InputObject</span></span>
<span data-ttu-id="892e1-124">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="892e1-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="892e1-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="892e1-125">-Name</span></span>
<span data-ttu-id="892e1-126">Название среды "анализ временной последовательности", связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="892e1-126">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="892e1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="892e1-127">-ResourceGroupName</span></span>
<span data-ttu-id="892e1-128">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="892e1-128">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="892e1-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="892e1-129">-SubscriptionId</span></span>
<span data-ttu-id="892e1-130">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="892e1-130">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="892e1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="892e1-131">CommonParameters</span></span>
<span data-ttu-id="892e1-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="892e1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="892e1-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="892e1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="892e1-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="892e1-134">INPUTS</span></span>

### <span data-ttu-id="892e1-135">Microsoft. Azure. PowerShell. командлеты. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="892e1-135">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="892e1-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="892e1-136">OUTPUTS</span></span>

### <span data-ttu-id="892e1-137">Microsoft. Azure. PowerShell. командлеты. TimeSeriesInsights. Models. Api20200515. IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="892e1-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="892e1-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="892e1-138">NOTES</span></span>

<span data-ttu-id="892e1-139">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="892e1-139">ALIASES</span></span>

<span data-ttu-id="892e1-140">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="892e1-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="892e1-141">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="892e1-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="892e1-142">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="892e1-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="892e1-143">INPUTOBJECT <ITimeSeriesInsightsIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="892e1-143">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="892e1-144">`[AccessPolicyName <String>]`: Имя политики доступа.</span><span class="sxs-lookup"><span data-stu-id="892e1-144">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="892e1-145">`[EnvironmentName <String>]`: Имя среды</span><span class="sxs-lookup"><span data-stu-id="892e1-145">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="892e1-146">`[EventSourceName <String>]`: Имя источника событий анализа временной последовательности, связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="892e1-146">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="892e1-147">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="892e1-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="892e1-148">`[ReferenceDataSetName <String>]`: Имя набора эталонных данных.</span><span class="sxs-lookup"><span data-stu-id="892e1-148">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="892e1-149">`[ResourceGroupName <String>]`: Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="892e1-149">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="892e1-150">`[SubscriptionId <String>]`: Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="892e1-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="892e1-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="892e1-151">RELATED LINKS</span></span>

