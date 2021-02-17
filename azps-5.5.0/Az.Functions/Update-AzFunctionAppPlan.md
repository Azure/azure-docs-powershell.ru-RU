---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: e0831e95a5601d3558af7089825684cc48e7838c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234348"
---
# <span data-ttu-id="696ca-101">Update-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="696ca-101">Update-AzFunctionAppPlan</span></span>

## <span data-ttu-id="696ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="696ca-102">SYNOPSIS</span></span>
<span data-ttu-id="696ca-103">Обновляет план обслуживания приложения для функций.</span><span class="sxs-lookup"><span data-stu-id="696ca-103">Updates a function app service plan.</span></span>

## <span data-ttu-id="696ca-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="696ca-104">SYNTAX</span></span>

### <span data-ttu-id="696ca-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="696ca-105">ByName (Default)</span></span>
```
Update-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="696ca-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="696ca-106">ByObjectInput</span></span>
```
Update-AzFunctionAppPlan -InputObject <IAppServicePlan> [-MaximumWorkerCount <Int32>]
 [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="696ca-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="696ca-107">DESCRIPTION</span></span>
<span data-ttu-id="696ca-108">Обновляет план обслуживания приложения для функций.</span><span class="sxs-lookup"><span data-stu-id="696ca-108">Updates a function app service plan.</span></span>

## <span data-ttu-id="696ca-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="696ca-109">EXAMPLES</span></span>

### <span data-ttu-id="696ca-110">Пример 1. Обновив план обслуживания приложений до 2 SKU для двадцати максимального предела сотрудников.</span><span class="sxs-lookup"><span data-stu-id="696ca-110">Example 1: Update an app service plan to EP2 sku with twenty maximum workers.</span></span>
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

<span data-ttu-id="696ca-111">Эта команда обновляет план обслуживания приложений до SKU EP2 для двадцати максимально допустимых сотрудников.</span><span class="sxs-lookup"><span data-stu-id="696ca-111">This command updates an app service plan to EP2 sku with twenty maximum workers.</span></span>

## <span data-ttu-id="696ca-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="696ca-112">PARAMETERS</span></span>

### <span data-ttu-id="696ca-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="696ca-113">-AsJob</span></span>
<span data-ttu-id="696ca-114">Выполнить команду как задание.</span><span class="sxs-lookup"><span data-stu-id="696ca-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="696ca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="696ca-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="696ca-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="696ca-116">-InputObject</span></span>
<span data-ttu-id="696ca-117">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="696ca-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="696ca-118">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="696ca-118">-MaximumWorkerCount</span></span>
<span data-ttu-id="696ca-119">Максимальное количество сотрудников для плана обслуживания приложений.</span><span class="sxs-lookup"><span data-stu-id="696ca-119">The maximum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MaxBurst

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696ca-120">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="696ca-120">-MinimumWorkerCount</span></span>
<span data-ttu-id="696ca-121">Минимальное количество сотрудников для плана обслуживания приложений.</span><span class="sxs-lookup"><span data-stu-id="696ca-121">The minimum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MinInstances

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696ca-122">-Name</span><span class="sxs-lookup"><span data-stu-id="696ca-122">-Name</span></span>
<span data-ttu-id="696ca-123">Имя плана службы приложений.</span><span class="sxs-lookup"><span data-stu-id="696ca-123">Name of the App Service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696ca-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="696ca-124">-NoWait</span></span>
<span data-ttu-id="696ca-125">Запустите команду асинхронно.</span><span class="sxs-lookup"><span data-stu-id="696ca-125">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="696ca-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="696ca-126">-ResourceGroupName</span></span>
<span data-ttu-id="696ca-127">Имя группы ресурсов, к которой принадлежит ресурс.</span><span class="sxs-lookup"><span data-stu-id="696ca-127">Name of the resource group to which the resource belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696ca-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="696ca-128">-Sku</span></span>
<span data-ttu-id="696ca-129">SKU плана.</span><span class="sxs-lookup"><span data-stu-id="696ca-129">The plan sku.</span></span>
<span data-ttu-id="696ca-130">Допустимые входные данные: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="696ca-130">Valid inputs are: EP1, EP2, EP3</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696ca-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="696ca-131">-SubscriptionId</span></span>
<span data-ttu-id="696ca-132">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="696ca-132">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696ca-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="696ca-133">-Tag</span></span>
<span data-ttu-id="696ca-134">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="696ca-134">Resource tags.</span></span>

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

### <span data-ttu-id="696ca-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="696ca-135">-Confirm</span></span>
<span data-ttu-id="696ca-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="696ca-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="696ca-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="696ca-137">-WhatIf</span></span>
<span data-ttu-id="696ca-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="696ca-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="696ca-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="696ca-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="696ca-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="696ca-140">CommonParameters</span></span>
<span data-ttu-id="696ca-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="696ca-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="696ca-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="696ca-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="696ca-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="696ca-143">INPUTS</span></span>

### <span data-ttu-id="696ca-144">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="696ca-144">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="696ca-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="696ca-145">OUTPUTS</span></span>

### <span data-ttu-id="696ca-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="696ca-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="696ca-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="696ca-147">NOTES</span></span>

<span data-ttu-id="696ca-148">ALIASES</span><span class="sxs-lookup"><span data-stu-id="696ca-148">ALIASES</span></span>

<span data-ttu-id="696ca-149">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="696ca-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="696ca-150">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="696ca-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="696ca-151">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="696ca-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="696ca-152"><IAppServicePlan>INPUTOBJECT:</span><span class="sxs-lookup"><span data-stu-id="696ca-152">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="696ca-153">`Location <String>`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="696ca-153">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="696ca-154">`[Kind <String>]`: Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="696ca-154">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="696ca-155">`[Tag <IResourceTags>]`: теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="696ca-155">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="696ca-156">`[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="696ca-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="696ca-157">`[Capacity <Int32?>]`— текущее количество экземпляров, которые назначены ресурсу.</span><span class="sxs-lookup"><span data-stu-id="696ca-157">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="696ca-158">`[FreeOfferExpirationTime <DateTime?>]`. Время истечения срока действия бесплатного предложения фермы серверов.</span><span class="sxs-lookup"><span data-stu-id="696ca-158">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="696ca-159">`[HostingEnvironmentProfileId <String>]`: ИД ресурса среды служб приложений.</span><span class="sxs-lookup"><span data-stu-id="696ca-159">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="696ca-160">`[HyperV <Boolean?>]`: Если это план обслуживания контейнера Hyper-V, <code>true</code> <code>false</code> в противном случае.</span><span class="sxs-lookup"><span data-stu-id="696ca-160">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="696ca-161">`[IsSpot <Boolean?>]`. Если этот план служб приложения является владельцем <code>true</code> точековых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="696ca-161">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="696ca-162">`[IsXenon <Boolean?>]`: Устарело: план обслуживания контейнера Hyper-V, в <code>true</code> <code>false</code> противном случае.</span><span class="sxs-lookup"><span data-stu-id="696ca-162">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="696ca-163">`[MaximumElasticWorkerCount <Int32?>]`: Максимальное количество сотрудников, разрешенных для этого плана обслуживания приложения ВадимScaleEnabled</span><span class="sxs-lookup"><span data-stu-id="696ca-163">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="696ca-164">`[PerSiteScaling <Boolean?>]`: Если приложения, которые назначены этому плану обслуживания приложений, <code>true</code> можно масштабировать независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="696ca-164">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="696ca-165">Если приложения, которые назначены этому плану обслуживания приложений, будут масштабироваться во всех <code>false</code> его экземплярах.</span><span class="sxs-lookup"><span data-stu-id="696ca-165">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="696ca-166">`[Reserved <Boolean?>]`. Если вы планируете службу приложения <code>true</code> Linux, <code>false</code> в противном случае.</span><span class="sxs-lookup"><span data-stu-id="696ca-166">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="696ca-167">`[SkuCapability <ICapability[]>]`. Возможности SKU, например, включен ли диспетчер трафика?</span><span class="sxs-lookup"><span data-stu-id="696ca-167">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="696ca-168">`[Name <String>]`: Имя возможности SKU.</span><span class="sxs-lookup"><span data-stu-id="696ca-168">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="696ca-169">`[Reason <String>]`: Причина возможности SKU.</span><span class="sxs-lookup"><span data-stu-id="696ca-169">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="696ca-170">`[Value <String>]`: значение возможности SKU.</span><span class="sxs-lookup"><span data-stu-id="696ca-170">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="696ca-171">`[SkuCapacityDefault <Int32?>]`: Число сотрудников по умолчанию для этого плана обслуживания приложений.</span><span class="sxs-lookup"><span data-stu-id="696ca-171">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="696ca-172">`[SkuCapacityMaximum <Int32?>]`: Максимальное количество сотрудников для этого плана обслуживания приложений.</span><span class="sxs-lookup"><span data-stu-id="696ca-172">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="696ca-173">`[SkuCapacityMinimum <Int32?>]`: Минимальное количество сотрудников для этого SKU плана обслуживания приложений.</span><span class="sxs-lookup"><span data-stu-id="696ca-173">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="696ca-174">`[SkuCapacityScaleType <String>]`: Доступные масштабные конфигурации для плана службы приложений.</span><span class="sxs-lookup"><span data-stu-id="696ca-174">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="696ca-175">`[SkuFamily <String>]`: Семейный код SKU ресурса.</span><span class="sxs-lookup"><span data-stu-id="696ca-175">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="696ca-176">`[SkuLocation <String[]>]`: Местоположения SKU.</span><span class="sxs-lookup"><span data-stu-id="696ca-176">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="696ca-177">`[SkuName <String>]`: Имя SKU ресурса.</span><span class="sxs-lookup"><span data-stu-id="696ca-177">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="696ca-178">`[SkuSize <String>]`: Заданный размер SKU ресурса.</span><span class="sxs-lookup"><span data-stu-id="696ca-178">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="696ca-179">`[SkuTier <String>]`: уровень обслуживания SKU ресурса.</span><span class="sxs-lookup"><span data-stu-id="696ca-179">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="696ca-180">`[SpotExpirationTime <DateTime?>]`Время истечения срока действия фермы серверов.</span><span class="sxs-lookup"><span data-stu-id="696ca-180">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="696ca-181">Допустимо только в том случае, если это ферма точественных серверов.</span><span class="sxs-lookup"><span data-stu-id="696ca-181">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="696ca-182">`[TargetWorkerCount <Int32?>]`: количество масштабируемых сотрудников.</span><span class="sxs-lookup"><span data-stu-id="696ca-182">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="696ca-183">`[TargetWorkerSizeId <Int32?>]`: ИД размера масштабируемой работой.</span><span class="sxs-lookup"><span data-stu-id="696ca-183">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="696ca-184">`[WorkerTierName <String>]`: уровень целевого сотрудника, который назначен плану службы приложений.</span><span class="sxs-lookup"><span data-stu-id="696ca-184">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="696ca-185">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="696ca-185">RELATED LINKS</span></span>

