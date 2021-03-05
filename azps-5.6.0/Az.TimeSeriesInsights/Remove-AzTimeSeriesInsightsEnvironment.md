---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: 89fa39a5e6e1bb2ded61c41dd553b6d7d0473d4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963379"
---
# <span data-ttu-id="c63ea-101">Remove-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="c63ea-101">Remove-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="c63ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c63ea-102">SYNOPSIS</span></span>
<span data-ttu-id="c63ea-103">Удаляет среду с указанным именем в указанной группе подписок и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c63ea-103">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="c63ea-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c63ea-104">SYNTAX</span></span>

### <span data-ttu-id="c63ea-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c63ea-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c63ea-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c63ea-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsEnvironment -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c63ea-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c63ea-107">DESCRIPTION</span></span>
<span data-ttu-id="c63ea-108">Удаляет среду с указанным именем в указанной группе подписок и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c63ea-108">Deletes the environment with the specified name in the specified subscription and resource group.</span></span>

## <span data-ttu-id="c63ea-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c63ea-109">EXAMPLES</span></span>

### <span data-ttu-id="c63ea-110">Пример 1. Удаление среды с ряду времени по имени</span><span class="sxs-lookup"><span data-stu-id="c63ea-110">Example 1: Remove a time series insights environment by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill

```

<span data-ttu-id="c63ea-111">Эта команда удаляет среду статистики по рядам времени.</span><span class="sxs-lookup"><span data-stu-id="c63ea-111">This command removes a time series insights environment.</span></span>

### <span data-ttu-id="c63ea-112">Пример 2. Удаление среды статистики по рядам времени для объекта</span><span class="sxs-lookup"><span data-stu-id="c63ea-112">Example 2: Remove a time series insights environment by object</span></span>
```powershell
PS C:\> $env = Get-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsill
PS C:\> Remove-AzTimeSeriesInsightsEnvironment -InputObject $env

```

<span data-ttu-id="c63ea-113">Эта команда удаляет среду статистики по рядам времени.</span><span class="sxs-lookup"><span data-stu-id="c63ea-113">This command removes a time series insights environment.</span></span>

## <span data-ttu-id="c63ea-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c63ea-114">PARAMETERS</span></span>

### <span data-ttu-id="c63ea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c63ea-115">-DefaultProfile</span></span>
<span data-ttu-id="c63ea-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c63ea-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c63ea-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c63ea-117">-InputObject</span></span>
<span data-ttu-id="c63ea-118">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="c63ea-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c63ea-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c63ea-119">-Name</span></span>
<span data-ttu-id="c63ea-120">Имя среды Time Series Insights, связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c63ea-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c63ea-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c63ea-121">-PassThru</span></span>
<span data-ttu-id="c63ea-122">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="c63ea-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c63ea-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c63ea-123">-ResourceGroupName</span></span>
<span data-ttu-id="c63ea-124">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="c63ea-124">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="c63ea-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c63ea-125">-SubscriptionId</span></span>
<span data-ttu-id="c63ea-126">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="c63ea-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="c63ea-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c63ea-127">-Confirm</span></span>
<span data-ttu-id="c63ea-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c63ea-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c63ea-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c63ea-129">-WhatIf</span></span>
<span data-ttu-id="c63ea-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c63ea-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c63ea-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c63ea-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c63ea-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c63ea-132">CommonParameters</span></span>
<span data-ttu-id="c63ea-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c63ea-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c63ea-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c63ea-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c63ea-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c63ea-135">INPUTS</span></span>

### <span data-ttu-id="c63ea-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="c63ea-136">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="c63ea-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c63ea-137">OUTPUTS</span></span>

### <span data-ttu-id="c63ea-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c63ea-138">System.Boolean</span></span>

## <span data-ttu-id="c63ea-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c63ea-139">NOTES</span></span>

<span data-ttu-id="c63ea-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c63ea-140">ALIASES</span></span>

<span data-ttu-id="c63ea-141">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="c63ea-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c63ea-142">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="c63ea-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c63ea-143">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c63ea-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c63ea-144">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="c63ea-144">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c63ea-145">`[AccessPolicyName <String>]`: имя политики доступа.</span><span class="sxs-lookup"><span data-stu-id="c63ea-145">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="c63ea-146">`[EnvironmentName <String>]`: название среды</span><span class="sxs-lookup"><span data-stu-id="c63ea-146">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="c63ea-147">`[EventSourceName <String>]`: имя источника события "Time Series Insights", связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="c63ea-147">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="c63ea-148">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="c63ea-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c63ea-149">`[ReferenceDataSetName <String>]`: Имя набора справочных данных.</span><span class="sxs-lookup"><span data-stu-id="c63ea-149">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="c63ea-150">`[ResourceGroupName <String>]`: Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="c63ea-150">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="c63ea-151">`[SubscriptionId <String>]`: Azure Subscription ID.</span><span class="sxs-lookup"><span data-stu-id="c63ea-151">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="c63ea-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c63ea-152">RELATED LINKS</span></span>

