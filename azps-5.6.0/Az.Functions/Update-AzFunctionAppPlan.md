---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: 522de6721d92b76938843b28322b94b5cc6ce481
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963043"
---
# <span data-ttu-id="a1d1d-101">Update-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="a1d1d-101">Update-AzFunctionAppPlan</span></span>

## <span data-ttu-id="a1d1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1d1d-102">SYNOPSIS</span></span>
<span data-ttu-id="a1d1d-103">Обновляет план обслуживания приложения для функций.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-103">Updates a function app service plan.</span></span>

## <span data-ttu-id="a1d1d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a1d1d-104">SYNTAX</span></span>

### <span data-ttu-id="a1d1d-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a1d1d-105">ByName (Default)</span></span>
```
Update-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a1d1d-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="a1d1d-106">ByObjectInput</span></span>
```
Update-AzFunctionAppPlan -InputObject <IAppServicePlan> [-MaximumWorkerCount <Int32>]
 [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a1d1d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1d1d-107">DESCRIPTION</span></span>
<span data-ttu-id="a1d1d-108">Обновляет план обслуживания приложения для функций.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-108">Updates a function app service plan.</span></span>

## <span data-ttu-id="a1d1d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a1d1d-109">EXAMPLES</span></span>

### <span data-ttu-id="a1d1d-110">Пример 1. Обновив план обслуживания приложений до 2 SKU для двадцати максимально допустимых сотрудников.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-110">Example 1: Update an app service plan to EP2 sku with twenty maximum workers.</span></span>
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

<span data-ttu-id="a1d1d-111">Эта команда обновляет план обслуживания приложений до SKU EP2 для двадцати максимально допустимых сотрудников.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-111">This command updates an app service plan to EP2 sku with twenty maximum workers.</span></span>

## <span data-ttu-id="a1d1d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1d1d-112">PARAMETERS</span></span>

### <span data-ttu-id="a1d1d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1d1d-113">-AsJob</span></span>
<span data-ttu-id="a1d1d-114">Выполнить команду как задание.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="a1d1d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1d1d-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="a1d1d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1d1d-116">-InputObject</span></span>
<span data-ttu-id="a1d1d-117">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a1d1d-118">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="a1d1d-118">-MaximumWorkerCount</span></span>
<span data-ttu-id="a1d1d-119">Максимальное количество сотрудников для плана обслуживания приложений.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-119">The maximum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="a1d1d-120">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="a1d1d-120">-MinimumWorkerCount</span></span>
<span data-ttu-id="a1d1d-121">Минимальное количество сотрудников для плана обслуживания приложений.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-121">The minimum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="a1d1d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a1d1d-122">-Name</span></span>
<span data-ttu-id="a1d1d-123">Имя плана службы приложений.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-123">Name of the App Service plan.</span></span>

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

### <span data-ttu-id="a1d1d-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a1d1d-124">-NoWait</span></span>
<span data-ttu-id="a1d1d-125">Запустите команду асинхронно.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-125">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="a1d1d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1d1d-126">-ResourceGroupName</span></span>
<span data-ttu-id="a1d1d-127">Имя группы ресурсов, к которой принадлежит ресурс.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-127">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="a1d1d-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="a1d1d-128">-Sku</span></span>
<span data-ttu-id="a1d1d-129">SKU плана.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-129">The plan sku.</span></span>
<span data-ttu-id="a1d1d-130">Допустимые входные данные: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="a1d1d-130">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="a1d1d-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a1d1d-131">-SubscriptionId</span></span>
<span data-ttu-id="a1d1d-132">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-132">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="a1d1d-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="a1d1d-133">-Tag</span></span>
<span data-ttu-id="a1d1d-134">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-134">Resource tags.</span></span>

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

### <span data-ttu-id="a1d1d-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1d1d-135">-Confirm</span></span>
<span data-ttu-id="a1d1d-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1d1d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1d1d-137">-WhatIf</span></span>
<span data-ttu-id="a1d1d-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1d1d-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1d1d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1d1d-140">CommonParameters</span></span>
<span data-ttu-id="a1d1d-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1d1d-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1d1d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1d1d-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a1d1d-143">INPUTS</span></span>

### <span data-ttu-id="a1d1d-144">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a1d1d-144">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="a1d1d-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a1d1d-145">OUTPUTS</span></span>

### <span data-ttu-id="a1d1d-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a1d1d-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="a1d1d-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a1d1d-147">NOTES</span></span>

<span data-ttu-id="a1d1d-148">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a1d1d-148">ALIASES</span></span>

<span data-ttu-id="a1d1d-149">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="a1d1d-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a1d1d-150">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a1d1d-151">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a1d1d-152"><IAppServicePlan>INPUTOBJECT:</span><span class="sxs-lookup"><span data-stu-id="a1d1d-152">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="a1d1d-153">`Location <String>`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-153">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="a1d1d-154">`[Kind <String>]`: Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-154">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="a1d1d-155">`[Tag <IResourceTags>]`: теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-155">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="a1d1d-156">`[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="a1d1d-157">`[Capacity <Int32?>]`: Текущее количество экземпляров, которые назначены ресурсу.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-157">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="a1d1d-158">`[FreeOfferExpirationTime <DateTime?>]`. Время истечения срока действия бесплатного предложения фермы серверов.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-158">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="a1d1d-159">`[HostingEnvironmentProfileId <String>]`: ИД ресурса среды служб приложений.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-159">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="a1d1d-160">`[HyperV <Boolean?>]`. Если Hyper-V план обслуживания контейнера <code>true</code> приложения, <code>false</code> в противном случае.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-160">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="a1d1d-161">`[IsSpot <Boolean?>]`. Если этот план служб приложения принадлежит spot <code>true</code> экземплярам.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-161">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="a1d1d-162">`[IsXenon <Boolean?>]`: Устарело: если Hyper-V план обслуживания контейнера <code>true</code> приложения, <code>false</code> в противном случае.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-162">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="a1d1d-163">`[MaximumElasticWorkerCount <Int32?>]`: Максимальное количество сотрудников, разрешенных для этого плана обслуживания приложения ВадимScaleEnabled</span><span class="sxs-lookup"><span data-stu-id="a1d1d-163">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="a1d1d-164">`[PerSiteScaling <Boolean?>]`. Если приложения, которые назначены этому плану обслуживания приложений, <code>true</code> можно масштабировать независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-164">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="a1d1d-165">Если приложения, которые назначены этому плану обслуживания приложений, будут масштабироваться во всех <code>false</code> его экземплярах.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-165">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="a1d1d-166">`[Reserved <Boolean?>]`. Если вы планируете службу приложения <code>true</code> Linux, <code>false</code> в противном случае.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-166">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="a1d1d-167">`[SkuCapability <ICapability[]>]`. Возможности SKU, например, включен ли диспетчер трафика?</span><span class="sxs-lookup"><span data-stu-id="a1d1d-167">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="a1d1d-168">`[Name <String>]`: Имя возможности SKU.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-168">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="a1d1d-169">`[Reason <String>]`: Причина возможности SKU.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-169">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="a1d1d-170">`[Value <String>]`: значение возможности SKU.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-170">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="a1d1d-171">`[SkuCapacityDefault <Int32?>]`: Число сотрудников по умолчанию для этого плана обслуживания приложений.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-171">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="a1d1d-172">`[SkuCapacityMaximum <Int32?>]`: Максимальное количество сотрудников для этого плана обслуживания приложений.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-172">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="a1d1d-173">`[SkuCapacityMinimum <Int32?>]`: Минимальное количество сотрудников для этого плана обслуживания приложений.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-173">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="a1d1d-174">`[SkuCapacityScaleType <String>]`: Доступны масштаб конфигурации для плана службы приложений.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-174">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="a1d1d-175">`[SkuFamily <String>]`: Семейный код SKU ресурса.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-175">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="a1d1d-176">`[SkuLocation <String[]>]`: Местоположения SKU.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-176">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="a1d1d-177">`[SkuName <String>]`: Имя SKU ресурса.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-177">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="a1d1d-178">`[SkuSize <String>]`: Заданный размер SKU ресурса.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-178">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="a1d1d-179">`[SkuTier <String>]`: уровень обслуживания SKU ресурса.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-179">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="a1d1d-180">`[SpotExpirationTime <DateTime?>]`Время истечения срока действия фермы серверов.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-180">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="a1d1d-181">Допустимо только в том случае, если это ферма точественных серверов.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-181">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="a1d1d-182">`[TargetWorkerCount <Int32?>]`: количество масштабируемых сотрудников.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-182">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="a1d1d-183">`[TargetWorkerSizeId <Int32?>]`: ИД размера масштабируемой работники.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-183">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="a1d1d-184">`[WorkerTierName <String>]`: уровень целевого сотрудника, который назначен плану службы приложений.</span><span class="sxs-lookup"><span data-stu-id="a1d1d-184">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="a1d1d-185">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1d1d-185">RELATED LINKS</span></span>

