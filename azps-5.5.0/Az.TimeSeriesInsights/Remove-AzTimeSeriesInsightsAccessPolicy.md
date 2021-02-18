---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: 2a6c58729d08c5bd060434c7a21720f87a3f7de3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224612"
---
# <span data-ttu-id="5e6dc-101">Remove-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5e6dc-101">Remove-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="5e6dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e6dc-102">SYNOPSIS</span></span>
<span data-ttu-id="5e6dc-103">Удаляет политику доступа с указанным именем в указанной подписке, группе ресурсов и среде.</span><span class="sxs-lookup"><span data-stu-id="5e6dc-103">Deletes the access policy with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="5e6dc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5e6dc-104">SYNTAX</span></span>

### <span data-ttu-id="5e6dc-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5e6dc-105">Delete (Default)</span></span>
```
Remove-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5e6dc-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5e6dc-106">DeleteViaIdentity</span></span>
```
Remove-AzTimeSeriesInsightsAccessPolicy -InputObject <ITimeSeriesInsightsIdentity>
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5e6dc-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e6dc-107">DESCRIPTION</span></span>
<span data-ttu-id="5e6dc-108">Удаляет политику доступа с указанным именем в указанной подписке, группе ресурсов и среде.</span><span class="sxs-lookup"><span data-stu-id="5e6dc-108">Deletes the access policy with the specified name in the specified subscription, resource group, and environment</span></span>

## <span data-ttu-id="5e6dc-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5e6dc-109">EXAMPLES</span></span>

### <span data-ttu-id="5e6dc-110">Пример 1. Удаление указанной политики доступа по имени</span><span class="sxs-lookup"><span data-stu-id="5e6dc-110">Example 1: Remove a specified access policy by name</span></span>
```powershell
PS C:\> Remove-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup

```

<span data-ttu-id="5e6dc-111">Эта команда удаляет указанную политику доступа.</span><span class="sxs-lookup"><span data-stu-id="5e6dc-111">This command removes a specified access policy.</span></span>

### <span data-ttu-id="5e6dc-112">Пример 2. Удаление указанной политики доступа для объекта</span><span class="sxs-lookup"><span data-stu-id="5e6dc-112">Example 2: Remove a specified access policy by object</span></span>
```powershell
PS C:\> $policy = Get-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -Name policy001 -ResourceGroupName testgroup
PS C:\> Remove-AzTimeSeriesInsightsAccessPolicy -InputObject $policy

```

<span data-ttu-id="5e6dc-113">Эта команда удаляет указанную политику доступа.</span><span class="sxs-lookup"><span data-stu-id="5e6dc-113">This command removes a specified access policy.</span></span>

## <span data-ttu-id="5e6dc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e6dc-114">PARAMETERS</span></span>

### <span data-ttu-id="5e6dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e6dc-115">-DefaultProfile</span></span>
<span data-ttu-id="5e6dc-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5e6dc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e6dc-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="5e6dc-117">-EnvironmentName</span></span>
<span data-ttu-id="5e6dc-118">Имя среды Time Series Insights, связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5e6dc-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="5e6dc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e6dc-119">-InputObject</span></span>
<span data-ttu-id="5e6dc-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="5e6dc-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5e6dc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5e6dc-121">-Name</span></span>
<span data-ttu-id="5e6dc-122">Имя политики доступа к time Series Insights, связанной с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="5e6dc-122">The name of the Time Series Insights access policy associated with the specified environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e6dc-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e6dc-123">-PassThru</span></span>
<span data-ttu-id="5e6dc-124">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="5e6dc-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5e6dc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e6dc-125">-ResourceGroupName</span></span>
<span data-ttu-id="5e6dc-126">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="5e6dc-126">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="5e6dc-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5e6dc-127">-SubscriptionId</span></span>
<span data-ttu-id="5e6dc-128">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="5e6dc-128">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="5e6dc-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e6dc-129">-Confirm</span></span>
<span data-ttu-id="5e6dc-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5e6dc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e6dc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e6dc-131">-WhatIf</span></span>
<span data-ttu-id="5e6dc-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e6dc-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e6dc-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5e6dc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e6dc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e6dc-134">CommonParameters</span></span>
<span data-ttu-id="5e6dc-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e6dc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e6dc-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e6dc-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e6dc-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5e6dc-137">INPUTS</span></span>

### <span data-ttu-id="5e6dc-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span><span class="sxs-lookup"><span data-stu-id="5e6dc-138">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity</span></span>

## <span data-ttu-id="5e6dc-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5e6dc-139">OUTPUTS</span></span>

### <span data-ttu-id="5e6dc-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5e6dc-140">System.Boolean</span></span>

## <span data-ttu-id="5e6dc-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5e6dc-141">NOTES</span></span>

<span data-ttu-id="5e6dc-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="5e6dc-142">ALIASES</span></span>

<span data-ttu-id="5e6dc-143">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="5e6dc-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5e6dc-144">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="5e6dc-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5e6dc-145">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5e6dc-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5e6dc-146">INPUTOBJECT <ITimeSeriesInsightsIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="5e6dc-146">INPUTOBJECT <ITimeSeriesInsightsIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5e6dc-147">`[AccessPolicyName <String>]`: имя политики доступа.</span><span class="sxs-lookup"><span data-stu-id="5e6dc-147">`[AccessPolicyName <String>]`: Name of the access policy.</span></span>
  - <span data-ttu-id="5e6dc-148">`[EnvironmentName <String>]`: название среды</span><span class="sxs-lookup"><span data-stu-id="5e6dc-148">`[EnvironmentName <String>]`: Name of the environment</span></span>
  - <span data-ttu-id="5e6dc-149">`[EventSourceName <String>]`: имя источника события "Time Series Insights", связанного с указанной средой.</span><span class="sxs-lookup"><span data-stu-id="5e6dc-149">`[EventSourceName <String>]`: The name of the Time Series Insights event source associated with the specified environment.</span></span>
  - <span data-ttu-id="5e6dc-150">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="5e6dc-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5e6dc-151">`[ReferenceDataSetName <String>]`: Имя набора справочных данных.</span><span class="sxs-lookup"><span data-stu-id="5e6dc-151">`[ReferenceDataSetName <String>]`: Name of the reference data set.</span></span>
  - <span data-ttu-id="5e6dc-152">`[ResourceGroupName <String>]`: Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="5e6dc-152">`[ResourceGroupName <String>]`: Name of an Azure Resource group.</span></span>
  - <span data-ttu-id="5e6dc-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span><span class="sxs-lookup"><span data-stu-id="5e6dc-153">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="5e6dc-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e6dc-154">RELATED LINKS</span></span>

