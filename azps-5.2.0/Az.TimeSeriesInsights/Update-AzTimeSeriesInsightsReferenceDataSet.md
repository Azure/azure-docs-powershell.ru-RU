---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 7dbced00ee2e39c536765bd16a19fbe7a66e291b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401580"
---
# <span data-ttu-id="d7317-101">Update-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="d7317-101">Update-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="d7317-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7317-102">SYNOPSIS</span></span>
<span data-ttu-id="d7317-103">Обновляет набор справочных данных с указанным именем в указанной подписке, группе ресурсов и среде.</span><span class="sxs-lookup"><span data-stu-id="d7317-103">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="d7317-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d7317-104">SYNTAX</span></span>

### <span data-ttu-id="d7317-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d7317-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d7317-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d7317-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d7317-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7317-107">DESCRIPTION</span></span>
<span data-ttu-id="d7317-108">Обновляет набор справочных данных с указанным именем в указанной подписке, группе ресурсов и среде.</span><span class="sxs-lookup"><span data-stu-id="d7317-108">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="d7317-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d7317-109">EXAMPLES</span></span>

### <span data-ttu-id="d7317-110">Пример 1. Обновление указанного набора данных ссылки по имени</span><span class="sxs-lookup"><span data-stu-id="d7317-110">Example 1: Update a specified reference data set by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="d7317-111">Эта команда обновляет указанный набор справочных данных.</span><span class="sxs-lookup"><span data-stu-id="d7317-111">This command updates a specified reference data set.</span></span>

### <span data-ttu-id="d7317-112">Пример 2. Обновление указанного набора данных ссылки для объекта</span><span class="sxs-lookup"><span data-stu-id="d7317-112">Example 2: Update a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="d7317-113">Эта команда обновляет указанный набор справочных данных.</span><span class="sxs-lookup"><span data-stu-id="d7317-113">This command updates a specified reference data set.</span></span>

## <span data-ttu-id="d7317-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7317-114">PARAMETERS</span></span>

### <span data-ttu-id="d7317-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7317-115">-DefaultProfile</span></span>
<span data-ttu-id="d7317-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d7317-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7317-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="d7317-117">-EnvironmentName</span></span>
<span data-ttu-id="d7317-118">Имя среды Time Series Insights, связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d7317-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="d7317-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7317-119">-InputObject</span></span>
<span data-ttu-id="d7317-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="d7317-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d7317-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d7317-121">-Name</span></span>
<span data-ttu-id="d7317-122">Имя набора справочных данных по time series Insights, связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="d7317-122">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

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

### <span data-ttu-id="d7317-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7317-123">-ResourceGroupName</span></span>
<span data-ttu-id="d7317-124">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="d7317-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="d7317-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d7317-125">-SubscriptionId</span></span>
<span data-ttu-id="d7317-126">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="d7317-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="d7317-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="d7317-127">-Tag</span></span>
<span data-ttu-id="d7317-128">Пары значений ключа с дополнительными свойствами для набора справочных данных.</span><span class="sxs-lookup"><span data-stu-id="d7317-128">Key-value pairs of additional properties for the reference data set.</span></span>

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

### <span data-ttu-id="d7317-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7317-129">-Confirm</span></span>
<span data-ttu-id="d7317-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d7317-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7317-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7317-131">-WhatIf</span></span>
<span data-ttu-id="d7317-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7317-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7317-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d7317-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7317-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7317-134">CommonParameters</span></span>
<span data-ttu-id="d7317-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7317-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7317-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7317-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7317-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d7317-137">INPUTS</span></span>

### <span data-ttu-id="d7317-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="d7317-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="d7317-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d7317-139">OUTPUTS</span></span>

### <span data-ttu-id="d7317-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="d7317-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="d7317-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d7317-141">NOTES</span></span>

<span data-ttu-id="d7317-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d7317-142">ALIASES</span></span>

<span data-ttu-id="d7317-143">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="d7317-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d7317-144">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="d7317-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d7317-145">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d7317-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d7317-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="d7317-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d7317-147">`[AccessPolicyName <String>]`: имя политики доступа.</span><span class="sxs-lookup"><span data-stu-id="d7317-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="d7317-148">`[EnvironmentName <String>]`: название среды</span><span class="sxs-lookup"><span data-stu-id="d7317-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="d7317-149">`[EventSourceName <String>]`: имя источника события Time Series Insights, связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="d7317-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="d7317-150">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="d7317-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d7317-151">`[ReferenceDataSetName <String>]`: Имя набора справочных данных.</span><span class="sxs-lookup"><span data-stu-id="d7317-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="d7317-152">`[ResourceGroupName <String>]`: Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="d7317-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="d7317-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span><span class="sxs-lookup"><span data-stu-id="d7317-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="d7317-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d7317-154">RELATED LINKS</span></span>

