---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: 6668952ba07327482da7ed3c274eb003ac61c73c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326776"
---
# <span data-ttu-id="62b31-101">Remove-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="62b31-101">Remove-AzFunctionAppPlan</span></span>

## <span data-ttu-id="62b31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62b31-102">SYNOPSIS</span></span>
<span data-ttu-id="62b31-103">Удаляет план приложения с функцией.</span><span class="sxs-lookup"><span data-stu-id="62b31-103">Deletes a function app plan.</span></span>

## <span data-ttu-id="62b31-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="62b31-104">SYNTAX</span></span>

### <span data-ttu-id="62b31-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="62b31-105">ByName (Default)</span></span>
```
Remove-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="62b31-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="62b31-106">ByObjectInput</span></span>
```
Remove-AzFunctionAppPlan -InputObject <IAppServicePlan> [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="62b31-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62b31-107">DESCRIPTION</span></span>
<span data-ttu-id="62b31-108">Удаляет план приложения с функцией.</span><span class="sxs-lookup"><span data-stu-id="62b31-108">Deletes a function app plan.</span></span>

## <span data-ttu-id="62b31-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="62b31-109">EXAMPLES</span></span>

### <span data-ttu-id="62b31-110">Пример 1. Получите план приложения функции по имени и удалите его.</span><span class="sxs-lookup"><span data-stu-id="62b31-110">Example 1: Get a function app plan by name and delete it.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

<span data-ttu-id="62b31-111">Эта команда получает план приложения функции по имени и удаляет его.</span><span class="sxs-lookup"><span data-stu-id="62b31-111">This command gets a function app plan by name and deletes it.</span></span>

### <span data-ttu-id="62b31-112">Пример 2. Удаление плана приложения функции по имени.</span><span class="sxs-lookup"><span data-stu-id="62b31-112">Example 2: Delete a function app plan by name.</span></span>
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

<span data-ttu-id="62b31-113">Эта команда удаляет план приложения функции по имени.</span><span class="sxs-lookup"><span data-stu-id="62b31-113">This command deletes a function app plan by name.</span></span>

## <span data-ttu-id="62b31-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62b31-114">PARAMETERS</span></span>

### <span data-ttu-id="62b31-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62b31-115">-DefaultProfile</span></span>
<span data-ttu-id="62b31-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62b31-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62b31-117">-Force</span><span class="sxs-lookup"><span data-stu-id="62b31-117">-Force</span></span>
<span data-ttu-id="62b31-118">Позволяет удалить план приложения с функцией, не запросив подтверждение.</span><span class="sxs-lookup"><span data-stu-id="62b31-118">Forces the cmdlet to remove the function app plan without prompting for confirmation.</span></span>

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

### <span data-ttu-id="62b31-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62b31-119">-InputObject</span></span>
<span data-ttu-id="62b31-120">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="62b31-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="62b31-121">-Name</span><span class="sxs-lookup"><span data-stu-id="62b31-121">-Name</span></span>
<span data-ttu-id="62b31-122">Имя приложения функции.</span><span class="sxs-lookup"><span data-stu-id="62b31-122">The name of function app.</span></span>

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

### <span data-ttu-id="62b31-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62b31-123">-PassThru</span></span>
<span data-ttu-id="62b31-124">Возвращает "Истина" в случае успешного достижения команды.</span><span class="sxs-lookup"><span data-stu-id="62b31-124">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="62b31-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62b31-125">-ResourceGroupName</span></span>


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

### <span data-ttu-id="62b31-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="62b31-126">-SubscriptionId</span></span>
<span data-ttu-id="62b31-127">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="62b31-127">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="62b31-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62b31-128">-Confirm</span></span>
<span data-ttu-id="62b31-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62b31-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62b31-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62b31-130">-WhatIf</span></span>
<span data-ttu-id="62b31-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62b31-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62b31-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="62b31-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62b31-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62b31-133">CommonParameters</span></span>
<span data-ttu-id="62b31-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62b31-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62b31-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62b31-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62b31-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="62b31-136">INPUTS</span></span>

### <span data-ttu-id="62b31-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="62b31-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="62b31-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="62b31-138">OUTPUTS</span></span>

### <span data-ttu-id="62b31-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="62b31-139">System.Boolean</span></span>

## <span data-ttu-id="62b31-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="62b31-140">NOTES</span></span>

<span data-ttu-id="62b31-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="62b31-141">ALIASES</span></span>

<span data-ttu-id="62b31-142">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="62b31-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="62b31-143">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="62b31-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="62b31-144">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="62b31-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="62b31-145"><IAppServicePlan>INPUTOBJECT:</span><span class="sxs-lookup"><span data-stu-id="62b31-145">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="62b31-146">`Location <String>`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="62b31-146">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="62b31-147">`[Kind <String>]`: Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="62b31-147">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="62b31-148">`[Tag <IResourceTags>]`: теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="62b31-148">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="62b31-149">`[(Any) <String>]`— это означает, что к этому объекту можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="62b31-149">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="62b31-150">`[Capacity <Int32?>]`: Текущее количество экземпляров, которые назначены ресурсу.</span><span class="sxs-lookup"><span data-stu-id="62b31-150">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="62b31-151">`[FreeOfferExpirationTime <DateTime?>]`. Время истечения срока действия бесплатного предложения фермы серверов.</span><span class="sxs-lookup"><span data-stu-id="62b31-151">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="62b31-152">`[HostingEnvironmentProfileId <String>]`: ИД ресурса среды служб приложений.</span><span class="sxs-lookup"><span data-stu-id="62b31-152">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="62b31-153">`[HyperV <Boolean?>]`: Если это план обслуживания контейнера Hyper-V, <code>true</code> <code>false</code> в противном случае.</span><span class="sxs-lookup"><span data-stu-id="62b31-153">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="62b31-154">`[IsSpot <Boolean?>]`. Если этот план служб приложения является владельцем <code>true</code> точековых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="62b31-154">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="62b31-155">`[IsXenon <Boolean?>]`: Устарело: план обслуживания контейнера Hyper-V, в <code>true</code> <code>false</code> противном случае.</span><span class="sxs-lookup"><span data-stu-id="62b31-155">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="62b31-156">`[MaximumElasticWorkerCount <Int32?>]`: Максимальное количество сотрудников, разрешенных для этого плана обслуживания приложения ВадимScaleEnabled</span><span class="sxs-lookup"><span data-stu-id="62b31-156">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="62b31-157">`[PerSiteScaling <Boolean?>]`: Если приложения, которые назначены этому плану обслуживания приложений, <code>true</code> можно масштабировать независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="62b31-157">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="62b31-158">Если приложения, которые назначены этому плану обслуживания приложений, будут масштабироваться во всех <code>false</code> его экземплярах.</span><span class="sxs-lookup"><span data-stu-id="62b31-158">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="62b31-159">`[Reserved <Boolean?>]`. Если вы планируете службу приложения <code>true</code> Linux, <code>false</code> в противном случае.</span><span class="sxs-lookup"><span data-stu-id="62b31-159">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="62b31-160">`[SkuCapability <ICapability[]>]`. Возможности SKU, например, включен ли диспетчер трафика?</span><span class="sxs-lookup"><span data-stu-id="62b31-160">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="62b31-161">`[Name <String>]`: Имя возможности SKU.</span><span class="sxs-lookup"><span data-stu-id="62b31-161">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="62b31-162">`[Reason <String>]`: Причина возможности SKU.</span><span class="sxs-lookup"><span data-stu-id="62b31-162">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="62b31-163">`[Value <String>]`: значение возможности SKU.</span><span class="sxs-lookup"><span data-stu-id="62b31-163">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="62b31-164">`[SkuCapacityDefault <Int32?>]`: Число сотрудников по умолчанию для этого плана обслуживания приложений.</span><span class="sxs-lookup"><span data-stu-id="62b31-164">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="62b31-165">`[SkuCapacityMaximum <Int32?>]`: Максимальное количество сотрудников для этого плана обслуживания приложений.</span><span class="sxs-lookup"><span data-stu-id="62b31-165">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="62b31-166">`[SkuCapacityMinimum <Int32?>]`: Минимальное количество сотрудников для этого SKU плана обслуживания приложений.</span><span class="sxs-lookup"><span data-stu-id="62b31-166">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="62b31-167">`[SkuCapacityScaleType <String>]`: Доступны масштаб конфигурации для плана службы приложений.</span><span class="sxs-lookup"><span data-stu-id="62b31-167">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="62b31-168">`[SkuFamily <String>]`: семейный код SKU ресурса.</span><span class="sxs-lookup"><span data-stu-id="62b31-168">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="62b31-169">`[SkuLocation <String[]>]`: Местоположения SKU.</span><span class="sxs-lookup"><span data-stu-id="62b31-169">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="62b31-170">`[SkuName <String>]`: Имя SKU ресурса.</span><span class="sxs-lookup"><span data-stu-id="62b31-170">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="62b31-171">`[SkuSize <String>]`: Заданный размер SKU ресурса.</span><span class="sxs-lookup"><span data-stu-id="62b31-171">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="62b31-172">`[SkuTier <String>]`: уровень обслуживания SKU ресурса.</span><span class="sxs-lookup"><span data-stu-id="62b31-172">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="62b31-173">`[SpotExpirationTime <DateTime?>]`Время истечения срока действия фермы серверов.</span><span class="sxs-lookup"><span data-stu-id="62b31-173">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="62b31-174">Допустимо только в том случае, если это ферма точественных серверов.</span><span class="sxs-lookup"><span data-stu-id="62b31-174">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="62b31-175">`[TargetWorkerCount <Int32?>]`: количество масштабируемых сотрудников.</span><span class="sxs-lookup"><span data-stu-id="62b31-175">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="62b31-176">`[TargetWorkerSizeId <Int32?>]`: ИД размера масштабируемой работой.</span><span class="sxs-lookup"><span data-stu-id="62b31-176">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="62b31-177">`[WorkerTierName <String>]`: уровень целевого сотрудника, который назначен плану службы приложений.</span><span class="sxs-lookup"><span data-stu-id="62b31-177">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="62b31-178">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62b31-178">RELATED LINKS</span></span>

