---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: e930a0848f39ec94cb6eeb4ef290b1842ea6793a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994230"
---
# <span data-ttu-id="7a0bd-101">Remove-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="7a0bd-101">Remove-AzFunctionAppPlan</span></span>

## <span data-ttu-id="7a0bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a0bd-102">SYNOPSIS</span></span>
<span data-ttu-id="7a0bd-103">Удаляет план приложения с функцией.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-103">Deletes a function app plan.</span></span>

## <span data-ttu-id="7a0bd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7a0bd-104">SYNTAX</span></span>

### <span data-ttu-id="7a0bd-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7a0bd-105">ByName (Default)</span></span>
```
Remove-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7a0bd-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="7a0bd-106">ByObjectInput</span></span>
```
Remove-AzFunctionAppPlan -InputObject <IAppServicePlan> [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7a0bd-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a0bd-107">DESCRIPTION</span></span>
<span data-ttu-id="7a0bd-108">Удаляет план приложения с функцией.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-108">Deletes a function app plan.</span></span>

## <span data-ttu-id="7a0bd-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7a0bd-109">EXAMPLES</span></span>

### <span data-ttu-id="7a0bd-110">Пример 1. Получите план приложения функции по имени и удалите его.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-110">Example 1: Get a function app plan by name and delete it.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

<span data-ttu-id="7a0bd-111">Эта команда получает план приложения функции по имени и удаляет его.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-111">This command gets a function app plan by name and deletes it.</span></span>

### <span data-ttu-id="7a0bd-112">Пример 2. Удаление плана приложения функции по имени.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-112">Example 2: Delete a function app plan by name.</span></span>
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

<span data-ttu-id="7a0bd-113">Эта команда удаляет план приложения функции по имени.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-113">This command deletes a function app plan by name.</span></span>

## <span data-ttu-id="7a0bd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a0bd-114">PARAMETERS</span></span>

### <span data-ttu-id="7a0bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a0bd-115">-DefaultProfile</span></span>
<span data-ttu-id="7a0bd-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a0bd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7a0bd-117">-Force</span></span>
<span data-ttu-id="7a0bd-118">Позволяет удалить план приложения с функцией, не запросив подтверждение.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-118">Forces the cmdlet to remove the function app plan without prompting for confirmation.</span></span>

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

### <span data-ttu-id="7a0bd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a0bd-119">-InputObject</span></span>
<span data-ttu-id="7a0bd-120">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7a0bd-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7a0bd-121">-Name</span></span>
<span data-ttu-id="7a0bd-122">Имя приложения функции.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-122">The name of function app.</span></span>

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

### <span data-ttu-id="7a0bd-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a0bd-123">-PassThru</span></span>
<span data-ttu-id="7a0bd-124">Возвращает "Истина" в случае успешного достижения команды.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-124">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="7a0bd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a0bd-125">-ResourceGroupName</span></span>


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

### <span data-ttu-id="7a0bd-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7a0bd-126">-SubscriptionId</span></span>
<span data-ttu-id="7a0bd-127">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-127">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="7a0bd-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a0bd-128">-Confirm</span></span>
<span data-ttu-id="7a0bd-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a0bd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a0bd-130">-WhatIf</span></span>
<span data-ttu-id="7a0bd-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a0bd-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a0bd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a0bd-133">CommonParameters</span></span>
<span data-ttu-id="7a0bd-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a0bd-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a0bd-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a0bd-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a0bd-136">INPUTS</span></span>

### <span data-ttu-id="7a0bd-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7a0bd-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="7a0bd-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7a0bd-138">OUTPUTS</span></span>

### <span data-ttu-id="7a0bd-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7a0bd-139">System.Boolean</span></span>

## <span data-ttu-id="7a0bd-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7a0bd-140">NOTES</span></span>

<span data-ttu-id="7a0bd-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="7a0bd-141">ALIASES</span></span>

<span data-ttu-id="7a0bd-142">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="7a0bd-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7a0bd-143">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7a0bd-144">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7a0bd-145"><IAppServicePlan>INPUTOBJECT:</span><span class="sxs-lookup"><span data-stu-id="7a0bd-145">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="7a0bd-146">`Location <String>`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-146">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="7a0bd-147">`[Kind <String>]`: Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-147">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="7a0bd-148">`[Tag <IResourceTags>]`: теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-148">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="7a0bd-149">`[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-149">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="7a0bd-150">`[Capacity <Int32?>]`: Текущее количество экземпляров, которые назначены ресурсу.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-150">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="7a0bd-151">`[FreeOfferExpirationTime <DateTime?>]`. Время истечения срока действия бесплатного предложения фермы серверов.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-151">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="7a0bd-152">`[HostingEnvironmentProfileId <String>]`: ИД ресурса среды служб приложений.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-152">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="7a0bd-153">`[HyperV <Boolean?>]`. Если Hyper-V план обслуживания контейнера <code>true</code> приложения, <code>false</code> в противном случае.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-153">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="7a0bd-154">`[IsSpot <Boolean?>]`. Если этот план служб приложения принадлежит spot <code>true</code> экземплярам.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-154">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="7a0bd-155">`[IsXenon <Boolean?>]`: Устарело: если Hyper-V план обслуживания контейнера <code>true</code> приложения, <code>false</code> в противном случае.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-155">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="7a0bd-156">`[MaximumElasticWorkerCount <Int32?>]`: Максимальное количество сотрудников, разрешенных для этого плана обслуживания приложения ВадимScaleEnabled</span><span class="sxs-lookup"><span data-stu-id="7a0bd-156">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="7a0bd-157">`[PerSiteScaling <Boolean?>]`. Если приложения, которые назначены этому плану обслуживания приложений, <code>true</code> можно масштабировать независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-157">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="7a0bd-158">Если приложения, которые назначены этому плану обслуживания приложений, будут масштабироваться во всех <code>false</code> его экземплярах.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-158">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="7a0bd-159">`[Reserved <Boolean?>]`. Если вы планируете службу приложения <code>true</code> Linux, <code>false</code> в противном случае.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-159">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="7a0bd-160">`[SkuCapability <ICapability[]>]`. Возможности SKU, например, включен ли диспетчер трафика?</span><span class="sxs-lookup"><span data-stu-id="7a0bd-160">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="7a0bd-161">`[Name <String>]`: Имя возможности SKU.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-161">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="7a0bd-162">`[Reason <String>]`: Причина возможности SKU.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-162">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="7a0bd-163">`[Value <String>]`: значение возможности SKU.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-163">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="7a0bd-164">`[SkuCapacityDefault <Int32?>]`: Число сотрудников по умолчанию для этого плана обслуживания приложений.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-164">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="7a0bd-165">`[SkuCapacityMaximum <Int32?>]`: Максимальное количество сотрудников для этого плана обслуживания приложений.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-165">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="7a0bd-166">`[SkuCapacityMinimum <Int32?>]`: Минимальное количество сотрудников для этого плана обслуживания приложений.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-166">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="7a0bd-167">`[SkuCapacityScaleType <String>]`: Доступны масштаб конфигурации для плана службы приложений.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-167">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="7a0bd-168">`[SkuFamily <String>]`: Семейный код SKU ресурса.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-168">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="7a0bd-169">`[SkuLocation <String[]>]`: Местоположения SKU.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-169">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="7a0bd-170">`[SkuName <String>]`: Имя SKU ресурса.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-170">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="7a0bd-171">`[SkuSize <String>]`: Заданный размер SKU ресурса.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-171">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="7a0bd-172">`[SkuTier <String>]`: уровень обслуживания SKU ресурса.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-172">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="7a0bd-173">`[SpotExpirationTime <DateTime?>]`Время истечения срока действия фермы серверов.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-173">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="7a0bd-174">Допустимо только в том случае, если это ферма точественных серверов.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-174">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="7a0bd-175">`[TargetWorkerCount <Int32?>]`: количество масштабируемых сотрудников.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-175">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="7a0bd-176">`[TargetWorkerSizeId <Int32?>]`: ИД размера масштабируемой работники.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-176">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="7a0bd-177">`[WorkerTierName <String>]`: уровень целевого сотрудника, который назначен плану службы приложений.</span><span class="sxs-lookup"><span data-stu-id="7a0bd-177">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="7a0bd-178">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a0bd-178">RELATED LINKS</span></span>

