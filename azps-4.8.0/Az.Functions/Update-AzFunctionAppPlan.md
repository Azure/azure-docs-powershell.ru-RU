---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: e0831e95a5601d3558af7089825684cc48e7838c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078267"
---
# <span data-ttu-id="0419a-101">Update-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="0419a-101">Update-AzFunctionAppPlan</span></span>

## <span data-ttu-id="0419a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0419a-102">SYNOPSIS</span></span>
<span data-ttu-id="0419a-103">Обновляет функциональный план служб приложений.</span><span class="sxs-lookup"><span data-stu-id="0419a-103">Updates a function app service plan.</span></span>

## <span data-ttu-id="0419a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0419a-104">SYNTAX</span></span>

### <span data-ttu-id="0419a-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0419a-105">ByName (Default)</span></span>
```
Update-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0419a-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="0419a-106">ByObjectInput</span></span>
```
Update-AzFunctionAppPlan -InputObject <IAppServicePlan> [-MaximumWorkerCount <Int32>]
 [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0419a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0419a-107">DESCRIPTION</span></span>
<span data-ttu-id="0419a-108">Обновляет функциональный план служб приложений.</span><span class="sxs-lookup"><span data-stu-id="0419a-108">Updates a function app service plan.</span></span>

## <span data-ttu-id="0419a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0419a-109">EXAMPLES</span></span>

### <span data-ttu-id="0419a-110">Пример 1: Обновление плана служб приложений до EP2 SKU с двадцатью максимальными сотрудниками.</span><span class="sxs-lookup"><span data-stu-id="0419a-110">Example 1: Update an app service plan to EP2 sku with twenty maximum workers.</span></span>
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

<span data-ttu-id="0419a-111">Эта команда обновляет план служб приложений на EP2 SKU, используя двадцать максимум сотрудников.</span><span class="sxs-lookup"><span data-stu-id="0419a-111">This command updates an app service plan to EP2 sku with twenty maximum workers.</span></span>

## <span data-ttu-id="0419a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0419a-112">PARAMETERS</span></span>

### <span data-ttu-id="0419a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0419a-113">-AsJob</span></span>
<span data-ttu-id="0419a-114">Выполнить команду как задание.</span><span class="sxs-lookup"><span data-stu-id="0419a-114">Run the command as a job.</span></span>

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

### <span data-ttu-id="0419a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0419a-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="0419a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0419a-116">-InputObject</span></span>
<span data-ttu-id="0419a-117">Для конструирования просмотрите раздел заметок о свойствах INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="0419a-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0419a-118">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="0419a-118">-MaximumWorkerCount</span></span>
<span data-ttu-id="0419a-119">Максимальное количество рабочих процессов для плана служб приложений.</span><span class="sxs-lookup"><span data-stu-id="0419a-119">The maximum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="0419a-120">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="0419a-120">-MinimumWorkerCount</span></span>
<span data-ttu-id="0419a-121">Минимальное количество рабочих процессов для плана служб приложений.</span><span class="sxs-lookup"><span data-stu-id="0419a-121">The minimum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="0419a-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0419a-122">-Name</span></span>
<span data-ttu-id="0419a-123">Имя плана служб приложений.</span><span class="sxs-lookup"><span data-stu-id="0419a-123">Name of the App Service plan.</span></span>

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

### <span data-ttu-id="0419a-124">-Wait</span><span class="sxs-lookup"><span data-stu-id="0419a-124">-NoWait</span></span>
<span data-ttu-id="0419a-125">Выполните команду асинхронно.</span><span class="sxs-lookup"><span data-stu-id="0419a-125">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="0419a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0419a-126">-ResourceGroupName</span></span>
<span data-ttu-id="0419a-127">Имя группы ресурсов, к которой принадлежит ресурс.</span><span class="sxs-lookup"><span data-stu-id="0419a-127">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="0419a-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="0419a-128">-Sku</span></span>
<span data-ttu-id="0419a-129">SKU плана.</span><span class="sxs-lookup"><span data-stu-id="0419a-129">The plan sku.</span></span>
<span data-ttu-id="0419a-130">Допустимые входные значения: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="0419a-130">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="0419a-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0419a-131">-SubscriptionId</span></span>
<span data-ttu-id="0419a-132">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="0419a-132">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="0419a-133">-Тег</span><span class="sxs-lookup"><span data-stu-id="0419a-133">-Tag</span></span>
<span data-ttu-id="0419a-134">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0419a-134">Resource tags.</span></span>

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

### <span data-ttu-id="0419a-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0419a-135">-Confirm</span></span>
<span data-ttu-id="0419a-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0419a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0419a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0419a-137">-WhatIf</span></span>
<span data-ttu-id="0419a-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0419a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0419a-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0419a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0419a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0419a-140">CommonParameters</span></span>
<span data-ttu-id="0419a-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0419a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0419a-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0419a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0419a-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0419a-143">INPUTS</span></span>

### <span data-ttu-id="0419a-144">Microsoft. Azure. PowerShell. командлеты. functions. Models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0419a-144">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="0419a-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0419a-145">OUTPUTS</span></span>

### <span data-ttu-id="0419a-146">Microsoft. Azure. PowerShell. командлеты. functions. Models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0419a-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="0419a-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="0419a-147">NOTES</span></span>

<span data-ttu-id="0419a-148">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="0419a-148">ALIASES</span></span>

<span data-ttu-id="0419a-149">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="0419a-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0419a-150">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0419a-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0419a-151">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0419a-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0419a-152">INPUTOBJECT <IAppServicePlan> :</span><span class="sxs-lookup"><span data-stu-id="0419a-152">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="0419a-153">`Location <String>`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="0419a-153">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="0419a-154">`[Kind <String>]`: Типа ресурса.</span><span class="sxs-lookup"><span data-stu-id="0419a-154">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="0419a-155">`[Tag <IResourceTags>]`: Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0419a-155">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="0419a-156">`[(Any) <String>]`: Это указывает на то, что в этот объект можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="0419a-156">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="0419a-157">`[Capacity <Int32?>]`: Текущее количество экземпляров, назначенных ресурсу.</span><span class="sxs-lookup"><span data-stu-id="0419a-157">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="0419a-158">`[FreeOfferExpirationTime <DateTime?>]`: Время истечения срока действия бесплатного предложения фермы серверов.</span><span class="sxs-lookup"><span data-stu-id="0419a-158">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="0419a-159">`[HostingEnvironmentProfileId <String>]`: Идентификатор ресурса среды службы приложений.</span><span class="sxs-lookup"><span data-stu-id="0419a-159">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="0419a-160">`[HyperV <Boolean?>]`: <code>true</code> В противном случае, если вы хотите, чтобы контейнеры службы приложений Hyper-V <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="0419a-160">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="0419a-161">`[IsSpot <Boolean?>]`: Если <code>true</code> , этот план служб приложений владеет плашечными экземплярами.</span><span class="sxs-lookup"><span data-stu-id="0419a-161">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="0419a-162">`[IsXenon <Boolean?>]`: Устаревший: Если в качестве контейнера службы приложений для контейнеров Hyper-V — <code>true</code> <code>false</code> в противном случае.</span><span class="sxs-lookup"><span data-stu-id="0419a-162">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="0419a-163">`[MaximumElasticWorkerCount <Int32?>]`: Максимальное количество сотрудников, разрешенных для этого плана служб приложений ElasticScaleEnabled</span><span class="sxs-lookup"><span data-stu-id="0419a-163">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="0419a-164">`[PerSiteScaling <Boolean?>]`: Если <code>true</code> приложения, назначенные для этого плана служб приложений, можно масштабировать независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="0419a-164">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="0419a-165">Если <code>false</code> приложения, назначенные для этого плана служб приложений, будут масштабироваться во всех экземплярах плана.</span><span class="sxs-lookup"><span data-stu-id="0419a-165">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="0419a-166">`[Reserved <Boolean?>]`: Если план служб приложений для <code>true</code> Linux <code>false</code> в противном случае.</span><span class="sxs-lookup"><span data-stu-id="0419a-166">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="0419a-167">`[SkuCapability <ICapability[]>]`: Возможности SKU, например, включены ли диспетчер трафика?</span><span class="sxs-lookup"><span data-stu-id="0419a-167">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="0419a-168">`[Name <String>]`: Название возможности SKU.</span><span class="sxs-lookup"><span data-stu-id="0419a-168">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="0419a-169">`[Reason <String>]`: Причина возможности SKU.</span><span class="sxs-lookup"><span data-stu-id="0419a-169">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="0419a-170">`[Value <String>]`: Значение возможности SKU.</span><span class="sxs-lookup"><span data-stu-id="0419a-170">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="0419a-171">`[SkuCapacityDefault <Int32?>]`: Количество рабочих процессов по умолчанию для этого плана служб приложений SKU.</span><span class="sxs-lookup"><span data-stu-id="0419a-171">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="0419a-172">`[SkuCapacityMaximum <Int32?>]`: Максимальное количество сотрудников для этого плана служб приложений SKU.</span><span class="sxs-lookup"><span data-stu-id="0419a-172">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="0419a-173">`[SkuCapacityMinimum <Int32?>]`: Минимальное количество рабочих процессов для этого плана служб приложений SKU.</span><span class="sxs-lookup"><span data-stu-id="0419a-173">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="0419a-174">`[SkuCapacityScaleType <String>]`: Доступные конфигурации масштабирования для плана служб приложений.</span><span class="sxs-lookup"><span data-stu-id="0419a-174">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="0419a-175">`[SkuFamily <String>]`: Код семейства SKU ресурса.</span><span class="sxs-lookup"><span data-stu-id="0419a-175">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="0419a-176">`[SkuLocation <String[]>]`: Расположение SKU.</span><span class="sxs-lookup"><span data-stu-id="0419a-176">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="0419a-177">`[SkuName <String>]`: Имя SKU ресурса.</span><span class="sxs-lookup"><span data-stu-id="0419a-177">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="0419a-178">`[SkuSize <String>]`: Указатель размера SKU ресурса.</span><span class="sxs-lookup"><span data-stu-id="0419a-178">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="0419a-179">`[SkuTier <String>]`: Уровень обслуживания SKU ресурса.</span><span class="sxs-lookup"><span data-stu-id="0419a-179">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="0419a-180">`[SpotExpirationTime <DateTime?>]`: Время истечения срока действия фермы серверов.</span><span class="sxs-lookup"><span data-stu-id="0419a-180">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="0419a-181">Действует только в том случае, если это ферма серверов с плашечными серверами.</span><span class="sxs-lookup"><span data-stu-id="0419a-181">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="0419a-182">`[TargetWorkerCount <Int32?>]`: Масштабирование количества рабочих процессов.</span><span class="sxs-lookup"><span data-stu-id="0419a-182">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="0419a-183">`[TargetWorkerSizeId <Int32?>]`: Масштабирование кода размера рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="0419a-183">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="0419a-184">`[WorkerTierName <String>]`: Целевой рабочий уровень, назначенный плану служб приложений.</span><span class="sxs-lookup"><span data-stu-id="0419a-184">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="0419a-185">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0419a-185">RELATED LINKS</span></span>

