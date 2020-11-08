---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 7f647da2543a4675dad53f88e2494aa7f6c39419
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077455"
---
# <span data-ttu-id="4ffe5-101">Remove-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="4ffe5-101">Remove-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="4ffe5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4ffe5-102">SYNOPSIS</span></span>
<span data-ttu-id="4ffe5-103">Удаляет источник событий с указанным именем в указанной подписке, группе ресурсов и среде.</span><span class="sxs-lookup"><span data-stu-id="4ffe5-103">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="4ffe5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4ffe5-104">SYNTAX</span></span>

### <span data-ttu-id="4ffe5-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4ffe5-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4ffe5-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4ffe5-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4ffe5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ffe5-107">DESCRIPTION</span></span>
<span data-ttu-id="4ffe5-108">Удаляет источник событий с указанным именем в указанной подписке, группе ресурсов и среде.</span><span class="sxs-lookup"><span data-stu-id="4ffe5-108">Deletes the event source with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="4ffe5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4ffe5-109">EXAMPLES</span></span>

### <span data-ttu-id="4ffe5-110">Пример 1: Удаление указанного источника событий по имени</span><span class="sxs-lookup"><span data-stu-id="4ffe5-110">Example 1: Remove a specified event source by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -Name iots001 -ResourceGroupName testgroup

```

<span data-ttu-id="4ffe5-111">Это приведет к удалению определенного источника событий.</span><span class="sxs-lookup"><span data-stu-id="4ffe5-111">This removes a specific event source.</span></span>

### <span data-ttu-id="4ffe5-112">Пример 2: Удаление указанного источника событий по объекту</span><span class="sxs-lookup"><span data-stu-id="4ffe5-112">Example 2: Remove a specified event source by object</span></span>
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name iots001
PS C:\> Remove-AzTimeSeriesInsightsEventSource -InputObject $es

```

<span data-ttu-id="4ffe5-113">Это приведет к удалению определенного источника событий.</span><span class="sxs-lookup"><span data-stu-id="4ffe5-113">This removes a specific event source.</span></span>

## <span data-ttu-id="4ffe5-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4ffe5-114">PARAMETERS</span></span>

### <span data-ttu-id="4ffe5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ffe5-115">-DefaultProfile</span></span>
<span data-ttu-id="4ffe5-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ffe5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ffe5-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="4ffe5-117">-EnvironmentName</span></span>
<span data-ttu-id="4ffe5-118">Название среды "анализ временной последовательности", связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4ffe5-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="4ffe5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ffe5-119">-InputObject</span></span>
<span data-ttu-id="4ffe5-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="4ffe5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4ffe5-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4ffe5-121">-Name</span></span>
<span data-ttu-id="4ffe5-122">Название источника событий анализа временной последовательности, связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="4ffe5-122">The name of the Time Series Insights event source associated with the specified environment.</span></span>

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

### <span data-ttu-id="4ffe5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ffe5-123">-PassThru</span></span>
<span data-ttu-id="4ffe5-124">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="4ffe5-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4ffe5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ffe5-125">-ResourceGroupName</span></span>
<span data-ttu-id="4ffe5-126">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="4ffe5-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="4ffe5-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4ffe5-127">-SubscriptionId</span></span>
<span data-ttu-id="4ffe5-128">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="4ffe5-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="4ffe5-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ffe5-129">-Confirm</span></span>
<span data-ttu-id="4ffe5-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4ffe5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ffe5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ffe5-131">-WhatIf</span></span>
<span data-ttu-id="4ffe5-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4ffe5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ffe5-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4ffe5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ffe5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ffe5-134">CommonParameters</span></span>
<span data-ttu-id="4ffe5-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4ffe5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ffe5-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ffe5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ffe5-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4ffe5-137">INPUTS</span></span>

### <span data-ttu-id="4ffe5-138">Microsoft. Azure. PowerShell. командлеты. TimeSeriesInsights. Models. ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="4ffe5-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="4ffe5-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ffe5-139">OUTPUTS</span></span>

### <span data-ttu-id="4ffe5-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4ffe5-140">System.Boolean</span></span>

## <span data-ttu-id="4ffe5-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="4ffe5-141">NOTES</span></span>

<span data-ttu-id="4ffe5-142">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="4ffe5-142">ALIASES</span></span>

<span data-ttu-id="4ffe5-143">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="4ffe5-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4ffe5-144">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4ffe5-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4ffe5-145">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4ffe5-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4ffe5-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="4ffe5-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4ffe5-147">`[AccessPolicyName <String>]`: Имя политики доступа.</span><span class="sxs-lookup"><span data-stu-id="4ffe5-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="4ffe5-148">`[EnvironmentName <String>]`: Имя среды</span><span class="sxs-lookup"><span data-stu-id="4ffe5-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="4ffe5-149">`[EventSourceName <String>]`: Имя источника событий анализа временной последовательности, связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="4ffe5-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="4ffe5-150">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="4ffe5-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4ffe5-151">`[ReferenceDataSetName <String>]`: Имя набора эталонных данных.</span><span class="sxs-lookup"><span data-stu-id="4ffe5-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="4ffe5-152">`[ResourceGroupName <String>]`: Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="4ffe5-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="4ffe5-153">`[SubscriptionId <String>]`: Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="4ffe5-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="4ffe5-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ffe5-154">RELATED LINKS</span></span>

