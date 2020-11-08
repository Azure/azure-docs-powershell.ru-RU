---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/get-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Get-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: ed4a3e7c9b53bd481d4d30c4f6a555d8f42c44fd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247907"
---
# <span data-ttu-id="d93e9-101">Get-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="d93e9-101">Get-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="d93e9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d93e9-102">SYNOPSIS</span></span>
<span data-ttu-id="d93e9-103">Возвращает результирующий наборы данных с указанным именем в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="d93e9-103">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="d93e9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d93e9-104">SYNTAX</span></span>

### <span data-ttu-id="d93e9-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d93e9-105">List (Default)</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d93e9-106">Получить</span><span class="sxs-lookup"><span data-stu-id="d93e9-106">Get</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d93e9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d93e9-107">GetViaIdentity</span></span>
```
Get-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d93e9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d93e9-108">DESCRIPTION</span></span>
<span data-ttu-id="d93e9-109">Возвращает результирующий наборы данных с указанным именем в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="d93e9-109">Gets the reference data set with the specified name in the specified environment.</span></span>

## <span data-ttu-id="d93e9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d93e9-110">EXAMPLES</span></span>

### <span data-ttu-id="d93e9-111">Пример 1: список всех наборов эталонных данных в указанной среде</span><span class="sxs-lookup"><span data-stu-id="d93e9-111">Example 1: List all reference data sets under the specified environment</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
eastus   dstest002 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="d93e9-112">Эта команда перечисляет все наборы эталонных данных в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="d93e9-112">This command lists all reference data sets under the specified environment.</span></span>

### <span data-ttu-id="d93e9-113">Пример 2: получение указанного эталонного значения по имени</span><span class="sxs-lookup"><span data-stu-id="d93e9-113">Example 2: Get a specified reference data set by name</span></span>
```powershell
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="d93e9-114">Эта команда возвращает указанный набор эталонных данных.</span><span class="sxs-lookup"><span data-stu-id="d93e9-114">This command gets a specified reference data set.</span></span>

### <span data-ttu-id="d93e9-115">Пример 3: получение указанного объекта ссылочных данных</span><span class="sxs-lookup"><span data-stu-id="d93e9-115">Example 3: Get a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -ResourceGroupName tsi-test-i01k5l -EnvironmentName tsi-envv8u56x -Name tsirdsqwufij 
PS C:\> Get-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds

Location Name         Type
-------- ----         ----
eastus2  tsirdsqwufij Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="d93e9-116">Эта команда возвращает указанный набор эталонных данных.</span><span class="sxs-lookup"><span data-stu-id="d93e9-116">This command gets a specified reference data set.</span></span>

## <span data-ttu-id="d93e9-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d93e9-117">PARAMETERS</span></span>

### <span data-ttu-id="d93e9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d93e9-118">-DefaultProfile</span></span>
<span data-ttu-id="d93e9-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d93e9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d93e9-120">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="d93e9-120">-EnvironmentName</span></span>
<span data-ttu-id="d93e9-121">Название среды "анализ временной последовательности", связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d93e9-121">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="d93e9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d93e9-122">-InputObject</span></span>
<span data-ttu-id="d93e9-123">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="d93e9-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d93e9-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d93e9-124">-Name</span></span>
<span data-ttu-id="d93e9-125">Имя набора ссылочных данных временной последовательности, связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="d93e9-125">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

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

### <span data-ttu-id="d93e9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d93e9-126">-ResourceGroupName</span></span>
<span data-ttu-id="d93e9-127">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="d93e9-127">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="d93e9-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d93e9-128">-SubscriptionId</span></span>
<span data-ttu-id="d93e9-129">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="d93e9-129">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="d93e9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d93e9-130">CommonParameters</span></span>
<span data-ttu-id="d93e9-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d93e9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d93e9-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d93e9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d93e9-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d93e9-133">INPUTS</span></span>

### <span data-ttu-id="d93e9-134">Microsoft. Azure. PowerShell. командлеты. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="d93e9-134">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="d93e9-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d93e9-135">OUTPUTS</span></span>

### <span data-ttu-id="d93e9-136">Microsoft. Azure. PowerShell. командлеты. TimeSeriesInsights. Models. Api20200515. IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="d93e9-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="d93e9-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="d93e9-137">NOTES</span></span>

<span data-ttu-id="d93e9-138">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="d93e9-138">ALIASES</span></span>

<span data-ttu-id="d93e9-139">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="d93e9-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d93e9-140">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d93e9-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d93e9-141">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d93e9-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d93e9-142">INPUTOBJECT <ITimeSeriesInsightsIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="d93e9-142">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d93e9-143">`[AccessPolicyName <String>]`: Имя политики доступа.</span><span class="sxs-lookup"><span data-stu-id="d93e9-143">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="d93e9-144">`[EnvironmentName <String>]`: Имя среды</span><span class="sxs-lookup"><span data-stu-id="d93e9-144">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="d93e9-145">`[EventSourceName <String>]`: Имя источника событий анализа временной последовательности, связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="d93e9-145">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="d93e9-146">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="d93e9-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d93e9-147">`[ReferenceDataSetName <String>]`: Имя набора эталонных данных.</span><span class="sxs-lookup"><span data-stu-id="d93e9-147">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="d93e9-148">`[ResourceGroupName <String>]`: Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="d93e9-148">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="d93e9-149">`[SubscriptionId <String>]`: Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="d93e9-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="d93e9-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d93e9-150">RELATED LINKS</span></span>

