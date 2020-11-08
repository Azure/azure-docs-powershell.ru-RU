---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/update-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Update-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 7dbced00ee2e39c536765bd16a19fbe7a66e291b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245152"
---
# <span data-ttu-id="467b9-101">Update-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="467b9-101">Update-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="467b9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="467b9-102">SYNOPSIS</span></span>
<span data-ttu-id="467b9-103">Обновляет эталонный наборы данных с указанным именем в указанной подписке, группе ресурсов и среде.</span><span class="sxs-lookup"><span data-stu-id="467b9-103">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="467b9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="467b9-104">SYNTAX</span></span>

### <span data-ttu-id="467b9-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="467b9-105">UpdateExpanded (Default)</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="467b9-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="467b9-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="467b9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="467b9-107">DESCRIPTION</span></span>
<span data-ttu-id="467b9-108">Обновляет эталонный наборы данных с указанным именем в указанной подписке, группе ресурсов и среде.</span><span class="sxs-lookup"><span data-stu-id="467b9-108">Updates the reference data set with the specified name in the specified subscription, resource group, and environment.</span></span>

## <span data-ttu-id="467b9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="467b9-109">EXAMPLES</span></span>

### <span data-ttu-id="467b9-110">Пример 1: обновление указанного ссылочного значения по имени</span><span class="sxs-lookup"><span data-stu-id="467b9-110">Example 1: Update a specified reference data set by name</span></span>
```powershell
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="467b9-111">Эта команда обновляет указанный набор эталонных данных.</span><span class="sxs-lookup"><span data-stu-id="467b9-111">This command updates a specified reference data set.</span></span>

### <span data-ttu-id="467b9-112">Пример 2: обновление указанного объекта ссылочных данных, установленного объектом</span><span class="sxs-lookup"><span data-stu-id="467b9-112">Example 2: Update a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -ResourceGroupName testgroup -ReferenceDataSetName dstest001
PS C:\> Update-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds -Tag @{"tstg"="lb001"}

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="467b9-113">Эта команда обновляет указанный набор эталонных данных.</span><span class="sxs-lookup"><span data-stu-id="467b9-113">This command updates a specified reference data set.</span></span>

## <span data-ttu-id="467b9-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="467b9-114">PARAMETERS</span></span>

### <span data-ttu-id="467b9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="467b9-115">-DefaultProfile</span></span>
<span data-ttu-id="467b9-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="467b9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="467b9-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="467b9-117">-EnvironmentName</span></span>
<span data-ttu-id="467b9-118">Название среды "анализ временной последовательности", связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="467b9-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="467b9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="467b9-119">-InputObject</span></span>
<span data-ttu-id="467b9-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="467b9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="467b9-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="467b9-121">-Name</span></span>
<span data-ttu-id="467b9-122">Имя набора ссылочных данных временной последовательности, связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="467b9-122">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

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

### <span data-ttu-id="467b9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="467b9-123">-ResourceGroupName</span></span>
<span data-ttu-id="467b9-124">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="467b9-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="467b9-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="467b9-125">-SubscriptionId</span></span>
<span data-ttu-id="467b9-126">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="467b9-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="467b9-127">-Тег</span><span class="sxs-lookup"><span data-stu-id="467b9-127">-Tag</span></span>
<span data-ttu-id="467b9-128">Пары "ключ-значение" дополнительных свойств для набора эталонных данных.</span><span class="sxs-lookup"><span data-stu-id="467b9-128">Key-value pairs of additional properties for the reference data set.</span></span>

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

### <span data-ttu-id="467b9-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="467b9-129">-Confirm</span></span>
<span data-ttu-id="467b9-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="467b9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="467b9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="467b9-131">-WhatIf</span></span>
<span data-ttu-id="467b9-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="467b9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="467b9-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="467b9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="467b9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="467b9-134">CommonParameters</span></span>
<span data-ttu-id="467b9-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="467b9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="467b9-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="467b9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="467b9-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="467b9-137">INPUTS</span></span>

### <span data-ttu-id="467b9-138">Microsoft. Azure. PowerShell. командлеты. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="467b9-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="467b9-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="467b9-139">OUTPUTS</span></span>

### <span data-ttu-id="467b9-140">Microsoft. Azure. PowerShell. командлеты. TimeSeriesInsights. Models. Api20200515. IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="467b9-140">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="467b9-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="467b9-141">NOTES</span></span>

<span data-ttu-id="467b9-142">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="467b9-142">ALIASES</span></span>

<span data-ttu-id="467b9-143">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="467b9-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="467b9-144">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="467b9-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="467b9-145">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="467b9-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="467b9-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="467b9-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="467b9-147">`[AccessPolicyName <String>]`: Имя политики доступа.</span><span class="sxs-lookup"><span data-stu-id="467b9-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="467b9-148">`[EnvironmentName <String>]`: Имя среды</span><span class="sxs-lookup"><span data-stu-id="467b9-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="467b9-149">`[EventSourceName <String>]`: Имя источника событий анализа временной последовательности, связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="467b9-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="467b9-150">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="467b9-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="467b9-151">`[ReferenceDataSetName <String>]`: Имя набора эталонных данных.</span><span class="sxs-lookup"><span data-stu-id="467b9-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="467b9-152">`[ResourceGroupName <String>]`: Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="467b9-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="467b9-153">`[SubscriptionId <String>]`: Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="467b9-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="467b9-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="467b9-154">RELATED LINKS</span></span>

