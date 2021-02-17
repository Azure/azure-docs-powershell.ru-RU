---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 7f647da2543a4675dad53f88e2494aa7f6c39419
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216665"
---
# <span data-ttu-id="92b43-101">Remove-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="92b43-101">Remove-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="92b43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92b43-102">SYNOPSIS</span></span>
<span data-ttu-id="92b43-103">Удаляет источник события с указанным именем в указанной подписке, группе ресурсов и среде.</span><span class="sxs-lookup"><span data-stu-id="92b43-103">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="92b43-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="92b43-104">SYNTAX</span></span>

### <span data-ttu-id="92b43-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="92b43-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="92b43-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="92b43-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="92b43-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="92b43-107">DESCRIPTION</span></span>
<span data-ttu-id="92b43-108">Удаляет источник события с указанным именем в указанной подписке, группе ресурсов и среде.</span><span class="sxs-lookup"><span data-stu-id="92b43-108">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="92b43-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="92b43-109">EXAMPLES</span></span>

### <span data-ttu-id="92b43-110">Пример 1. Удаление указанного источника события по имени</span><span class="sxs-lookup"><span data-stu-id="92b43-110">Example 1: Remove a specified event source by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -Name iots001 -ResourceGroupName testgroup

```

<span data-ttu-id="92b43-111">При этом удаляется определенный источник события.</span><span class="sxs-lookup"><span data-stu-id="92b43-111">This removes a specific event source.</span></span>

### <span data-ttu-id="92b43-112">Пример 2. Удаление источника события, заданного объектом</span><span class="sxs-lookup"><span data-stu-id="92b43-112">Example 2: Remove a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name iots001
PS C:\> Remove-AzTimeSeriesInsightsEventSource -InputObject $es

```

<span data-ttu-id="92b43-113">При этом удаляется определенный источник события.</span><span class="sxs-lookup"><span data-stu-id="92b43-113">This removes a specific event source.</span></span>

## <span data-ttu-id="92b43-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92b43-114">PARAMETERS</span></span>

### <span data-ttu-id="92b43-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92b43-115">-DefaultProfile</span></span>
<span data-ttu-id="92b43-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="92b43-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92b43-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="92b43-117">-EnvironmentName</span></span>
<span data-ttu-id="92b43-118">Имя среды Time Series Insights, связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="92b43-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="92b43-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92b43-119">-InputObject</span></span>
<span data-ttu-id="92b43-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="92b43-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="92b43-121">-Name</span><span class="sxs-lookup"><span data-stu-id="92b43-121">-Name</span></span>
<span data-ttu-id="92b43-122">Имя источника события Time Series Insights, связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="92b43-122">The name of the Time Series Insights event source associated with the specified environment.</span></span>

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

### <span data-ttu-id="92b43-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92b43-123">-PassThru</span></span>
<span data-ttu-id="92b43-124">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="92b43-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="92b43-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92b43-125">-ResourceGroupName</span></span>
<span data-ttu-id="92b43-126">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="92b43-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="92b43-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="92b43-127">-SubscriptionId</span></span>
<span data-ttu-id="92b43-128">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="92b43-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="92b43-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="92b43-129">-Confirm</span></span>
<span data-ttu-id="92b43-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92b43-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92b43-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92b43-131">-WhatIf</span></span>
<span data-ttu-id="92b43-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92b43-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92b43-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="92b43-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92b43-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92b43-134">CommonParameters</span></span>
<span data-ttu-id="92b43-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92b43-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92b43-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92b43-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92b43-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="92b43-137">INPUTS</span></span>

### <span data-ttu-id="92b43-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="92b43-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="92b43-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="92b43-139">OUTPUTS</span></span>

### <span data-ttu-id="92b43-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="92b43-140">System.Boolean</span></span>

## <span data-ttu-id="92b43-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="92b43-141">NOTES</span></span>

<span data-ttu-id="92b43-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="92b43-142">ALIASES</span></span>

<span data-ttu-id="92b43-143">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="92b43-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="92b43-144">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="92b43-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="92b43-145">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="92b43-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="92b43-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="92b43-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="92b43-147">`[AccessPolicyName <String>]`: имя политики доступа.</span><span class="sxs-lookup"><span data-stu-id="92b43-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="92b43-148">`[EnvironmentName <String>]`: название среды</span><span class="sxs-lookup"><span data-stu-id="92b43-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="92b43-149">`[EventSourceName <String>]`: имя источника события Time Series Insights, связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="92b43-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="92b43-150">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="92b43-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="92b43-151">`[ReferenceDataSetName <String>]`: Имя набора справочных данных.</span><span class="sxs-lookup"><span data-stu-id="92b43-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="92b43-152">`[ResourceGroupName <String>]`: Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="92b43-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="92b43-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span><span class="sxs-lookup"><span data-stu-id="92b43-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="92b43-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="92b43-154">RELATED LINKS</span></span>

