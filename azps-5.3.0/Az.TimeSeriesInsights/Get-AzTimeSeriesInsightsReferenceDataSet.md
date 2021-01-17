---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: ed4a3e7c9b53bd481d4d30c4f6a555d8f42c44fd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422692"
---
# <span data-ttu-id="ea11f-101">Get-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="ea11f-101">Get-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="ea11f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea11f-102">SYNOPSIS</span></span>
<span data-ttu-id="ea11f-103">Возвращает набор справочных данных с указанным именем в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="ea11f-103">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="ea11f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ea11f-104">SYNTAX</span></span>

### <span data-ttu-id="ea11f-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ea11f-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ea11f-106">Получить</span><span class="sxs-lookup"><span data-stu-id="ea11f-106">Get</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ea11f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ea11f-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ea11f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea11f-108">DESCRIPTION</span></span>
<span data-ttu-id="ea11f-109">Возвращает набор справочных данных с указанным именем в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="ea11f-109">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="ea11f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ea11f-110">EXAMPLES</span></span>

### <span data-ttu-id="ea11f-111">Пример 1. Список всех наборов справочных данных в указанной среде</span><span class="sxs-lookup"><span data-stu-id="ea11f-111">Example 1: List all reference data sets under the specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
eastus   dstest002 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="ea11f-112">Эта команда содержит список всех наборов справочных данных в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="ea11f-112">This command lists all reference data sets under the specified environment.</span></span>

### <span data-ttu-id="ea11f-113">Пример 2. Получить заданную ссылку на данные по имени</span><span class="sxs-lookup"><span data-stu-id="ea11f-113">Example 2: Get a specified reference data set by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="ea11f-114">Эта команда получает указанный набор справочных данных.</span><span class="sxs-lookup"><span data-stu-id="ea11f-114">This command gets a specified reference data set.</span></span>

### <span data-ttu-id="ea11f-115">Пример 3. Получить заданную ссылку на данные, заданную объектом</span><span class="sxs-lookup"><span data-stu-id="ea11f-115">Example 3: Get a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -ResourceGroupName tsi-test-i01k5l -EnvironmentName tsi-envv8u56x -Name tsirdsqwufij 
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds

Location Name         Type
-------- ----         ----
eastus2  tsirdsqwufij Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="ea11f-116">Эта команда получает указанный набор справочных данных.</span><span class="sxs-lookup"><span data-stu-id="ea11f-116">This command gets a specified reference data set.</span></span>

## <span data-ttu-id="ea11f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea11f-117">PARAMETERS</span></span>

### <span data-ttu-id="ea11f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea11f-118">-DefaultProfile</span></span>
<span data-ttu-id="ea11f-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ea11f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea11f-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="ea11f-120">-EnvironmentName</span></span>
<span data-ttu-id="ea11f-121">Имя среды Time Series Insights, связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ea11f-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="ea11f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea11f-122">-InputObject</span></span>
<span data-ttu-id="ea11f-123">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="ea11f-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ea11f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="ea11f-124">-Name</span></span>
<span data-ttu-id="ea11f-125">Имя набора справочных данных по time series Insights, связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="ea11f-125">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea11f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea11f-126">-ResourceGroupName</span></span>
<span data-ttu-id="ea11f-127">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="ea11f-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="ea11f-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ea11f-128">-SubscriptionId</span></span>
<span data-ttu-id="ea11f-129">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="ea11f-129">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea11f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea11f-130">CommonParameters</span></span>
<span data-ttu-id="ea11f-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea11f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea11f-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea11f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea11f-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ea11f-133">INPUTS</span></span>

### <span data-ttu-id="ea11f-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="ea11f-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="ea11f-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ea11f-135">OUTPUTS</span></span>

### <span data-ttu-id="ea11f-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="ea11f-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="ea11f-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ea11f-137">NOTES</span></span>

<span data-ttu-id="ea11f-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ea11f-138">ALIASES</span></span>

<span data-ttu-id="ea11f-139">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="ea11f-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ea11f-140">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="ea11f-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ea11f-141">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ea11f-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ea11f-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="ea11f-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ea11f-143">`[AccessPolicyName <String>]`: имя политики доступа.</span><span class="sxs-lookup"><span data-stu-id="ea11f-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="ea11f-144">`[EnvironmentName <String>]`: название среды</span><span class="sxs-lookup"><span data-stu-id="ea11f-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="ea11f-145">`[EventSourceName <String>]`: имя источника события Time Series Insights, связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="ea11f-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="ea11f-146">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="ea11f-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ea11f-147">`[ReferenceDataSetName <String>]`: имя набора справочных данных.</span><span class="sxs-lookup"><span data-stu-id="ea11f-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="ea11f-148">`[ResourceGroupName <String>]`: Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="ea11f-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="ea11f-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span><span class="sxs-lookup"><span data-stu-id="ea11f-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="ea11f-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea11f-150">RELATED LINKS</span></span>

