---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 56173c8ca384c817912395a536583fb26e9dfa76
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235188"
---
# <span data-ttu-id="9264e-101">Remove-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="9264e-101">Remove-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="9264e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9264e-102">SYNOPSIS</span></span>
<span data-ttu-id="9264e-103">Удаляет эталонные наборы данных с указанным именем в указанной подписке, группе ресурсов и среде.</span><span class="sxs-lookup"><span data-stu-id="9264e-103">Deletes the reference data set with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="9264e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9264e-104">SYNTAX</span></span>

### <span data-ttu-id="9264e-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9264e-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9264e-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9264e-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsReferenceDataSet -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9264e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9264e-107">DESCRIPTION</span></span>
<span data-ttu-id="9264e-108">Удаляет эталонные наборы данных с указанным именем в указанной подписке, группе ресурсов и среде.</span><span class="sxs-lookup"><span data-stu-id="9264e-108">Deletes the reference data set with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="9264e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9264e-109">EXAMPLES</span></span>

### <span data-ttu-id="9264e-110">Пример 1: Удаление указанного эталонных данных по имени</span><span class="sxs-lookup"><span data-stu-id="9264e-110">Example 1: Remove a specified reference data set by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup

```

<span data-ttu-id="9264e-111">Эта команда удаляет указанный набор эталонных данных.</span><span class="sxs-lookup"><span data-stu-id="9264e-111">This command removes a specified reference data set.</span></span>

### <span data-ttu-id="9264e-112">Пример 2: Удаление указанного эталонных данных, заданного объектом</span><span class="sxs-lookup"><span data-stu-id="9264e-112">Example 2: Remove a specified reference data set by object</span></span>
```powershell
PS C:\> $ds = Get-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup
PS C:\> Remove-AzTimeSeriesInsightsReferenceDataSet -InputObject $ds

```

<span data-ttu-id="9264e-113">Эта команда удаляет указанный набор эталонных данных.</span><span class="sxs-lookup"><span data-stu-id="9264e-113">This command removes a specified reference data set.</span></span>

## <span data-ttu-id="9264e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9264e-114">PARAMETERS</span></span>

### <span data-ttu-id="9264e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9264e-115">-DefaultProfile</span></span>
<span data-ttu-id="9264e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9264e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9264e-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="9264e-117">-EnvironmentName</span></span>
<span data-ttu-id="9264e-118">Название среды "анализ временной последовательности", связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9264e-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9264e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9264e-119">-InputObject</span></span>
<span data-ttu-id="9264e-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="9264e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9264e-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9264e-121">-Name</span></span>
<span data-ttu-id="9264e-122">Имя набора ссылочных данных временной последовательности, связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="9264e-122">The name of the Time Series Insights reference data set associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9264e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9264e-123">-PassThru</span></span>
<span data-ttu-id="9264e-124">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="9264e-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9264e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9264e-125">-ResourceGroupName</span></span>
<span data-ttu-id="9264e-126">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="9264e-126">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9264e-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9264e-127">-SubscriptionId</span></span>
<span data-ttu-id="9264e-128">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="9264e-128">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9264e-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9264e-129">-Confirm</span></span>
<span data-ttu-id="9264e-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9264e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9264e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9264e-131">-WhatIf</span></span>
<span data-ttu-id="9264e-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9264e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9264e-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9264e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9264e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9264e-134">CommonParameters</span></span>
<span data-ttu-id="9264e-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9264e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9264e-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9264e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9264e-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9264e-137">INPUTS</span></span>

### <span data-ttu-id="9264e-138">Microsoft. Azure. PowerShell. командлеты. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="9264e-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="9264e-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9264e-139">OUTPUTS</span></span>

### <span data-ttu-id="9264e-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9264e-140">System.Boolean</span></span>

## <span data-ttu-id="9264e-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="9264e-141">NOTES</span></span>

<span data-ttu-id="9264e-142">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="9264e-142">ALIASES</span></span>

<span data-ttu-id="9264e-143">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="9264e-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9264e-144">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9264e-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9264e-145">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9264e-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9264e-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="9264e-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9264e-147">`[AccessPolicyName <String>]`: Имя политики доступа.</span><span class="sxs-lookup"><span data-stu-id="9264e-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="9264e-148">`[EnvironmentName <String>]`: Имя среды</span><span class="sxs-lookup"><span data-stu-id="9264e-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="9264e-149">`[EventSourceName <String>]`: Имя источника событий анализа временной последовательности, связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="9264e-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="9264e-150">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="9264e-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9264e-151">`[ReferenceDataSetName <String>]`: Имя набора эталонных данных.</span><span class="sxs-lookup"><span data-stu-id="9264e-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="9264e-152">`[ResourceGroupName <String>]`: Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="9264e-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="9264e-153">`[SubscriptionId <String>]`: Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="9264e-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="9264e-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9264e-154">RELATED LINKS</span></span>

