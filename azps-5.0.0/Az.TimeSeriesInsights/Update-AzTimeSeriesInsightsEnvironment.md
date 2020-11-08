---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: e2b7fa000251a12e09dfd7cd345f54f967962839
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245741"
---
# <span data-ttu-id="3185b-101">Update-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="3185b-101">Update-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="3185b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3185b-102">SYNOPSIS</span></span>
<span data-ttu-id="3185b-103">Обновляет среду с указанным именем в указанной подписке и группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3185b-103">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="3185b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3185b-104">SYNTAX</span></span>

### <span data-ttu-id="3185b-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3185b-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3185b-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3185b-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3185b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3185b-107">DESCRIPTION</span></span>
<span data-ttu-id="3185b-108">Обновляет среду с указанным именем в указанной подписке и группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3185b-108">Updates the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="3185b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3185b-109">EXAMPLES</span></span>

### <span data-ttu-id="3185b-110">Пример 1: обновление среды Gen1 Time Series Insights</span><span class="sxs-lookup"><span data-stu-id="3185b-110">Example 1: Update a Gen1 time series insights environment</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001 -Tag @{'key1'='val1'}

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
SkuCapacity                  : 5
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="3185b-111">Эта команда обновляет среду Gen1 Time Series.</span><span class="sxs-lookup"><span data-stu-id="3185b-111">This command updates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="3185b-112">Пример 2: обновление среды Gen1 Time Series Insights</span><span class="sxs-lookup"><span data-stu-id="3185b-112">Example 2:  Update a Gen1 time series insights environment</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001
PS C:\> Update-AzTimeSeriesInsightsEnvironment -InputObject $env -Tag @{'key2'='val2'}

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
SkuCapacity                  : 5
SkuName                      : S1
StateDetailCode              :
StateDetailCurrentCount      :
StateDetailMaxCount          :
StateDetailMessage           :
StorageLimitExceededBehavior : PurgeOldData
Tag                          : Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20180815Preview.TrackedResourceTags
Type                         : Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="3185b-113">Эта команда обновляет среду Gen1 Time Series.</span><span class="sxs-lookup"><span data-stu-id="3185b-113">This command updates a Gen1 time series insights environment.</span></span>

## <span data-ttu-id="3185b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3185b-114">PARAMETERS</span></span>

### <span data-ttu-id="3185b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3185b-115">-AsJob</span></span>
<span data-ttu-id="3185b-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="3185b-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3185b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3185b-117">-DefaultProfile</span></span>
<span data-ttu-id="3185b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3185b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3185b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3185b-119">-InputObject</span></span>
<span data-ttu-id="3185b-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="3185b-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3185b-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3185b-121">-Name</span></span>
<span data-ttu-id="3185b-122">Название среды "анализ временной последовательности", связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3185b-122">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3185b-123">-Wait</span><span class="sxs-lookup"><span data-stu-id="3185b-123">-NoWait</span></span>
<span data-ttu-id="3185b-124">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="3185b-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3185b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3185b-125">-ResourceGroupName</span></span>
<span data-ttu-id="3185b-126">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="3185b-126">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3185b-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3185b-127">-SubscriptionId</span></span>
<span data-ttu-id="3185b-128">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="3185b-128">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3185b-129">-Тег</span><span class="sxs-lookup"><span data-stu-id="3185b-129">-Tag</span></span>
<span data-ttu-id="3185b-130">Пары "ключ-значение" дополнительных свойств среды.</span><span class="sxs-lookup"><span data-stu-id="3185b-130">Key-value pairs of additional properties for the environment.</span></span>

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

### <span data-ttu-id="3185b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3185b-131">-Confirm</span></span>
<span data-ttu-id="3185b-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3185b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3185b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3185b-133">-WhatIf</span></span>
<span data-ttu-id="3185b-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3185b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3185b-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3185b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3185b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3185b-136">CommonParameters</span></span>
<span data-ttu-id="3185b-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3185b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3185b-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3185b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3185b-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3185b-139">INPUTS</span></span>

### <span data-ttu-id="3185b-140">Microsoft. Azure. PowerShell. командлеты. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="3185b-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="3185b-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3185b-141">OUTPUTS</span></span>

### <span data-ttu-id="3185b-142">Microsoft. Azure. PowerShell. командлеты. TimeSeriesInsights. Models. Api20200515. IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="3185b-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="3185b-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="3185b-143">NOTES</span></span>

<span data-ttu-id="3185b-144">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="3185b-144">ALIASES</span></span>

<span data-ttu-id="3185b-145">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="3185b-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3185b-146">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3185b-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3185b-147">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3185b-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3185b-148">INPUTOBJECT <ITimeSeriesInsightsIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="3185b-148">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3185b-149">`[AccessPolicyName <String>]`: Имя политики доступа.</span><span class="sxs-lookup"><span data-stu-id="3185b-149">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="3185b-150">`[EnvironmentName <String>]`: Имя среды</span><span class="sxs-lookup"><span data-stu-id="3185b-150">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="3185b-151">`[EventSourceName <String>]`: Имя источника событий анализа временной последовательности, связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="3185b-151">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="3185b-152">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="3185b-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3185b-153">`[ReferenceDataSetName <String>]`: Имя набора эталонных данных.</span><span class="sxs-lookup"><span data-stu-id="3185b-153">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="3185b-154">`[ResourceGroupName <String>]`: Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="3185b-154">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="3185b-155">`[SubscriptionId <String>]`: Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="3185b-155">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="3185b-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3185b-156">RELATED LINKS</span></span>

