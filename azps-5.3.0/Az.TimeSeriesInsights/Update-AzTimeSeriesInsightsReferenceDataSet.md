---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 7dbced00ee2e39c536765bd16a19fbe7a66e291b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98423916"
---
# <span data-ttu-id="b43b7-101">Update-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="b43b7-101">Update-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="b43b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b43b7-102">SYNOPSIS</span></span>
<span data-ttu-id="b43b7-103">Обновляет набор справочных данных с указанным именем в указанной подписке, группе ресурсов и среде.</span><span class="sxs-lookup"><span data-stu-id="b43b7-103">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="b43b7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b43b7-104">SYNTAX</span></span>

### <span data-ttu-id="b43b7-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b43b7-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b43b7-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b43b7-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b43b7-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b43b7-107">DESCRIPTION</span></span>
<span data-ttu-id="b43b7-108">Обновляет набор справочных данных с указанным именем в указанной подписке, группе ресурсов и среде.</span><span class="sxs-lookup"><span data-stu-id="b43b7-108">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="b43b7-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b43b7-109">EXAMPLES</span></span>

### <span data-ttu-id="b43b7-110">Пример 1. Обновление указанного набора данных ссылки по имени</span><span class="sxs-lookup"><span data-stu-id="b43b7-110">Example 1: Update a specified reference data set by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="b43b7-111">Эта команда обновляет указанный набор справочных данных.</span><span class="sxs-lookup"><span data-stu-id="b43b7-111">This command updates a specified reference data set.</span></span>

### <span data-ttu-id="b43b7-112">Пример 2. Обновление указанного набора данных ссылки для объекта</span><span class="sxs-lookup"><span data-stu-id="b43b7-112">Example 2: Update a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="b43b7-113">Эта команда обновляет указанный набор справочных данных.</span><span class="sxs-lookup"><span data-stu-id="b43b7-113">This command updates a specified reference data set.</span></span>

## <span data-ttu-id="b43b7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b43b7-114">PARAMETERS</span></span>

### <span data-ttu-id="b43b7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b43b7-115">-DefaultProfile</span></span>
<span data-ttu-id="b43b7-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b43b7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b43b7-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="b43b7-117">-EnvironmentName</span></span>
<span data-ttu-id="b43b7-118">Имя среды Time Series Insights, связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b43b7-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="b43b7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b43b7-119">-InputObject</span></span>
<span data-ttu-id="b43b7-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="b43b7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b43b7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b43b7-121">-Name</span></span>
<span data-ttu-id="b43b7-122">Имя набора справочных данных по time series Insights, связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="b43b7-122">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b43b7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b43b7-123">-ResourceGroupName</span></span>
<span data-ttu-id="b43b7-124">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="b43b7-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="b43b7-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b43b7-125">-SubscriptionId</span></span>
<span data-ttu-id="b43b7-126">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="b43b7-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="b43b7-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="b43b7-127">-Tag</span></span>
<span data-ttu-id="b43b7-128">Пары ключевых значений дополнительных свойств для набора справочных данных.</span><span class="sxs-lookup"><span data-stu-id="b43b7-128">Key-value pairs of additional properties for the reference data set.</span></span>

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

### <span data-ttu-id="b43b7-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b43b7-129">-Confirm</span></span>
<span data-ttu-id="b43b7-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b43b7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b43b7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b43b7-131">-WhatIf</span></span>
<span data-ttu-id="b43b7-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b43b7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b43b7-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b43b7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b43b7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b43b7-134">CommonParameters</span></span>
<span data-ttu-id="b43b7-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b43b7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b43b7-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b43b7-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b43b7-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b43b7-137">INPUTS</span></span>

### <span data-ttu-id="b43b7-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="b43b7-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="b43b7-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b43b7-139">OUTPUTS</span></span>

### <span data-ttu-id="b43b7-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="b43b7-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="b43b7-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b43b7-141">NOTES</span></span>

<span data-ttu-id="b43b7-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b43b7-142">ALIASES</span></span>

<span data-ttu-id="b43b7-143">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="b43b7-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b43b7-144">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="b43b7-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b43b7-145">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b43b7-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b43b7-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="b43b7-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b43b7-147">`[AccessPolicyName <String>]`: имя политики доступа.</span><span class="sxs-lookup"><span data-stu-id="b43b7-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="b43b7-148">`[EnvironmentName <String>]`: название среды</span><span class="sxs-lookup"><span data-stu-id="b43b7-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="b43b7-149">`[EventSourceName <String>]`: имя источника события Time Series Insights, связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="b43b7-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="b43b7-150">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="b43b7-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b43b7-151">`[ReferenceDataSetName <String>]`: Имя набора справочных данных.</span><span class="sxs-lookup"><span data-stu-id="b43b7-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="b43b7-152">`[ResourceGroupName <String>]`: Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="b43b7-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="b43b7-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span><span class="sxs-lookup"><span data-stu-id="b43b7-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="b43b7-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b43b7-154">RELATED LINKS</span></span>

