---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 7f647da2543a4675dad53f88e2494aa7f6c39419
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397084"
---
# <span data-ttu-id="97b6a-101">Remove-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="97b6a-101">Remove-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="97b6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97b6a-102">SYNOPSIS</span></span>
<span data-ttu-id="97b6a-103">Удаляет источник события с указанным именем в указанной подписке, группе ресурсов и среде.</span><span class="sxs-lookup"><span data-stu-id="97b6a-103">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="97b6a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="97b6a-104">SYNTAX</span></span>

### <span data-ttu-id="97b6a-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="97b6a-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="97b6a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="97b6a-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="97b6a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="97b6a-107">DESCRIPTION</span></span>
<span data-ttu-id="97b6a-108">Удаляет источник события с указанным именем в указанной подписке, группе ресурсов и среде.</span><span class="sxs-lookup"><span data-stu-id="97b6a-108">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="97b6a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="97b6a-109">EXAMPLES</span></span>

### <span data-ttu-id="97b6a-110">Пример 1. Удаление указанного источника события по имени</span><span class="sxs-lookup"><span data-stu-id="97b6a-110">Example 1: Remove a specified event source by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -Name iots001 -ResourceGroupName testgroup

```

<span data-ttu-id="97b6a-111">При этом удаляется определенный источник события.</span><span class="sxs-lookup"><span data-stu-id="97b6a-111">This removes a specific event source.</span></span>

### <span data-ttu-id="97b6a-112">Пример 2. Удаление источника события для объекта</span><span class="sxs-lookup"><span data-stu-id="97b6a-112">Example 2: Remove a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name iots001
PS C:\> Remove-AzTimeSeriesInsightsEventSource -InputObject $es

```

<span data-ttu-id="97b6a-113">При этом удаляется определенный источник события.</span><span class="sxs-lookup"><span data-stu-id="97b6a-113">This removes a specific event source.</span></span>

## <span data-ttu-id="97b6a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97b6a-114">PARAMETERS</span></span>

### <span data-ttu-id="97b6a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97b6a-115">-DefaultProfile</span></span>
<span data-ttu-id="97b6a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="97b6a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97b6a-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="97b6a-117">-EnvironmentName</span></span>
<span data-ttu-id="97b6a-118">Имя среды Time Series Insights, связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="97b6a-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="97b6a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97b6a-119">-InputObject</span></span>
<span data-ttu-id="97b6a-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="97b6a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="97b6a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="97b6a-121">-Name</span></span>
<span data-ttu-id="97b6a-122">Имя источника события Time Series Insights, связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="97b6a-122">The name of the Time Series Insights event source associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b6a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97b6a-123">-PassThru</span></span>
<span data-ttu-id="97b6a-124">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="97b6a-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="97b6a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97b6a-125">-ResourceGroupName</span></span>
<span data-ttu-id="97b6a-126">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="97b6a-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="97b6a-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="97b6a-127">-SubscriptionId</span></span>
<span data-ttu-id="97b6a-128">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="97b6a-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="97b6a-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="97b6a-129">-Confirm</span></span>
<span data-ttu-id="97b6a-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="97b6a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97b6a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97b6a-131">-WhatIf</span></span>
<span data-ttu-id="97b6a-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97b6a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97b6a-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="97b6a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97b6a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97b6a-134">CommonParameters</span></span>
<span data-ttu-id="97b6a-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97b6a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97b6a-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97b6a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97b6a-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="97b6a-137">INPUTS</span></span>

### <span data-ttu-id="97b6a-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="97b6a-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="97b6a-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="97b6a-139">OUTPUTS</span></span>

### <span data-ttu-id="97b6a-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="97b6a-140">System.Boolean</span></span>

## <span data-ttu-id="97b6a-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="97b6a-141">NOTES</span></span>

<span data-ttu-id="97b6a-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="97b6a-142">ALIASES</span></span>

<span data-ttu-id="97b6a-143">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="97b6a-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="97b6a-144">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="97b6a-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="97b6a-145">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="97b6a-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="97b6a-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="97b6a-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="97b6a-147">`[AccessPolicyName <String>]`: имя политики доступа.</span><span class="sxs-lookup"><span data-stu-id="97b6a-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="97b6a-148">`[EnvironmentName <String>]`: название среды</span><span class="sxs-lookup"><span data-stu-id="97b6a-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="97b6a-149">`[EventSourceName <String>]`: имя источника события Time Series Insights, связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="97b6a-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="97b6a-150">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="97b6a-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="97b6a-151">`[ReferenceDataSetName <String>]`: Имя набора справочных данных.</span><span class="sxs-lookup"><span data-stu-id="97b6a-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="97b6a-152">`[ResourceGroupName <String>]`: Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="97b6a-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="97b6a-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span><span class="sxs-lookup"><span data-stu-id="97b6a-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="97b6a-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="97b6a-154">RELATED LINKS</span></span>

