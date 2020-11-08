---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: 6668952ba07327482da7ed3c274eb003ac61c73c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245417"
---
# <span data-ttu-id="99f3f-101">Remove-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="99f3f-101">Remove-AzFunctionAppPlan</span></span>

## <span data-ttu-id="99f3f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="99f3f-102">SYNOPSIS</span></span>
<span data-ttu-id="99f3f-103">Удаляет план приложения функции.</span><span class="sxs-lookup"><span data-stu-id="99f3f-103">Deletes a function app plan.</span></span>

## <span data-ttu-id="99f3f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="99f3f-104">SYNTAX</span></span>

### <span data-ttu-id="99f3f-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="99f3f-105">ByName (Default)</span></span>
```
Remove-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="99f3f-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="99f3f-106">ByObjectInput</span></span>
```
Remove-AzFunctionAppPlan -InputObject <IAppServicePlan> [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="99f3f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="99f3f-107">DESCRIPTION</span></span>
<span data-ttu-id="99f3f-108">Удаляет план приложения функции.</span><span class="sxs-lookup"><span data-stu-id="99f3f-108">Deletes a function app plan.</span></span>

## <span data-ttu-id="99f3f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="99f3f-109">EXAMPLES</span></span>

### <span data-ttu-id="99f3f-110">Пример 1: получение плана приложения функции по имени и его удаление.</span><span class="sxs-lookup"><span data-stu-id="99f3f-110">Example 1: Get a function app plan by name and delete it.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

<span data-ttu-id="99f3f-111">Эта команда получает план приложения функции по имени и удаляет его.</span><span class="sxs-lookup"><span data-stu-id="99f3f-111">This command gets a function app plan by name and deletes it.</span></span>

### <span data-ttu-id="99f3f-112">Пример 2: Удаление плана приложения функции по имени.</span><span class="sxs-lookup"><span data-stu-id="99f3f-112">Example 2: Delete a function app plan by name.</span></span>
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

<span data-ttu-id="99f3f-113">Эта команда удаляет план приложения функции по имени.</span><span class="sxs-lookup"><span data-stu-id="99f3f-113">This command deletes a function app plan by name.</span></span>

## <span data-ttu-id="99f3f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="99f3f-114">PARAMETERS</span></span>

### <span data-ttu-id="99f3f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99f3f-115">-DefaultProfile</span></span>
<span data-ttu-id="99f3f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="99f3f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99f3f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="99f3f-117">-Force</span></span>
<span data-ttu-id="99f3f-118">Принудительное удаление плана приложения функции без запроса на подтверждение командлета.</span><span class="sxs-lookup"><span data-stu-id="99f3f-118">Forces the cmdlet to remove the function app plan without prompting for confirmation.</span></span>

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

### <span data-ttu-id="99f3f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99f3f-119">-InputObject</span></span>
<span data-ttu-id="99f3f-120">Для конструирования просмотрите раздел заметок о свойствах INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="99f3f-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="99f3f-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="99f3f-121">-Name</span></span>
<span data-ttu-id="99f3f-122">Имя приложения функции.</span><span class="sxs-lookup"><span data-stu-id="99f3f-122">The name of function app.</span></span>

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

### <span data-ttu-id="99f3f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99f3f-123">-PassThru</span></span>
<span data-ttu-id="99f3f-124">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="99f3f-124">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="99f3f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99f3f-125">-ResourceGroupName</span></span>


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

### <span data-ttu-id="99f3f-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="99f3f-126">-SubscriptionId</span></span>
<span data-ttu-id="99f3f-127">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="99f3f-127">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="99f3f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="99f3f-128">-Confirm</span></span>
<span data-ttu-id="99f3f-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="99f3f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99f3f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99f3f-130">-WhatIf</span></span>
<span data-ttu-id="99f3f-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="99f3f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99f3f-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="99f3f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99f3f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99f3f-133">CommonParameters</span></span>
<span data-ttu-id="99f3f-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="99f3f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99f3f-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99f3f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99f3f-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="99f3f-136">INPUTS</span></span>

### <span data-ttu-id="99f3f-137">Microsoft. Azure. PowerShell. командлеты. functions. Models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="99f3f-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="99f3f-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="99f3f-138">OUTPUTS</span></span>

### <span data-ttu-id="99f3f-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="99f3f-139">System.Boolean</span></span>

## <span data-ttu-id="99f3f-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="99f3f-140">NOTES</span></span>

<span data-ttu-id="99f3f-141">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="99f3f-141">ALIASES</span></span>

<span data-ttu-id="99f3f-142">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="99f3f-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="99f3f-143">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="99f3f-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="99f3f-144">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="99f3f-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="99f3f-145">INPUTOBJECT <IAppServicePlan> :</span><span class="sxs-lookup"><span data-stu-id="99f3f-145">INPUTOBJECT <IAppServicePlan>:</span></span> 
  - <span data-ttu-id="99f3f-146">`Location <String>`: Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="99f3f-146">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="99f3f-147">`[Kind <String>]`: Типа ресурса.</span><span class="sxs-lookup"><span data-stu-id="99f3f-147">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="99f3f-148">`[Tag <IResourceTags>]`: Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="99f3f-148">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="99f3f-149">`[(Any) <String>]`: Это указывает на то, что в этот объект можно добавить любое свойство.</span><span class="sxs-lookup"><span data-stu-id="99f3f-149">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="99f3f-150">`[Capacity <Int32?>]`: Текущее количество экземпляров, назначенных ресурсу.</span><span class="sxs-lookup"><span data-stu-id="99f3f-150">`[Capacity <Int32?>]`: Current number of instances assigned to the resource.</span></span>
  - <span data-ttu-id="99f3f-151">`[FreeOfferExpirationTime <DateTime?>]`: Время истечения срока действия бесплатного предложения фермы серверов.</span><span class="sxs-lookup"><span data-stu-id="99f3f-151">`[FreeOfferExpirationTime <DateTime?>]`: The time when the server farm free offer expires.</span></span>
  - <span data-ttu-id="99f3f-152">`[HostingEnvironmentProfileId <String>]`: Идентификатор ресурса среды службы приложений.</span><span class="sxs-lookup"><span data-stu-id="99f3f-152">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="99f3f-153">`[HyperV <Boolean?>]`: <code>true</code> В противном случае, если вы хотите, чтобы контейнеры службы приложений Hyper-V <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="99f3f-153">`[HyperV <Boolean?>]`: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="99f3f-154">`[IsSpot <Boolean?>]`: Если <code>true</code> , этот план служб приложений владеет плашечными экземплярами.</span><span class="sxs-lookup"><span data-stu-id="99f3f-154">`[IsSpot <Boolean?>]`: If <code>true</code>, this App Service Plan owns spot instances.</span></span>
  - <span data-ttu-id="99f3f-155">`[IsXenon <Boolean?>]`: Устаревший: Если в качестве контейнера службы приложений для контейнеров Hyper-V — <code>true</code> <code>false</code> в противном случае.</span><span class="sxs-lookup"><span data-stu-id="99f3f-155">`[IsXenon <Boolean?>]`: Obsolete: If Hyper-V container app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="99f3f-156">`[MaximumElasticWorkerCount <Int32?>]`: Максимальное количество сотрудников, разрешенных для этого плана служб приложений ElasticScaleEnabled</span><span class="sxs-lookup"><span data-stu-id="99f3f-156">`[MaximumElasticWorkerCount <Int32?>]`: Maximum number of total workers allowed for this ElasticScaleEnabled App Service Plan</span></span>
  - <span data-ttu-id="99f3f-157">`[PerSiteScaling <Boolean?>]`: Если <code>true</code> приложения, назначенные для этого плана служб приложений, можно масштабировать независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="99f3f-157">`[PerSiteScaling <Boolean?>]`: If <code>true</code>, apps assigned to this App Service plan can be scaled independently.</span></span>         <span data-ttu-id="99f3f-158">Если <code>false</code> приложения, назначенные для этого плана служб приложений, будут масштабироваться во всех экземплярах плана.</span><span class="sxs-lookup"><span data-stu-id="99f3f-158">If <code>false</code>, apps assigned to this App Service plan will scale to all instances of the plan.</span></span>
  - <span data-ttu-id="99f3f-159">`[Reserved <Boolean?>]`: Если план служб приложений для <code>true</code> Linux <code>false</code> в противном случае.</span><span class="sxs-lookup"><span data-stu-id="99f3f-159">`[Reserved <Boolean?>]`: If Linux app service plan <code>true</code>, <code>false</code> otherwise.</span></span>
  - <span data-ttu-id="99f3f-160">`[SkuCapability <ICapability[]>]`: Возможности SKU, например, включены ли диспетчер трафика?</span><span class="sxs-lookup"><span data-stu-id="99f3f-160">`[SkuCapability <ICapability[]>]`: Capabilities of the SKU, e.g., is traffic manager enabled?</span></span>
    - <span data-ttu-id="99f3f-161">`[Name <String>]`: Название возможности SKU.</span><span class="sxs-lookup"><span data-stu-id="99f3f-161">`[Name <String>]`: Name of the SKU capability.</span></span>
    - <span data-ttu-id="99f3f-162">`[Reason <String>]`: Причина возможности SKU.</span><span class="sxs-lookup"><span data-stu-id="99f3f-162">`[Reason <String>]`: Reason of the SKU capability.</span></span>
    - <span data-ttu-id="99f3f-163">`[Value <String>]`: Значение возможности SKU.</span><span class="sxs-lookup"><span data-stu-id="99f3f-163">`[Value <String>]`: Value of the SKU capability.</span></span>
  - <span data-ttu-id="99f3f-164">`[SkuCapacityDefault <Int32?>]`: Количество рабочих процессов по умолчанию для этого плана служб приложений SKU.</span><span class="sxs-lookup"><span data-stu-id="99f3f-164">`[SkuCapacityDefault <Int32?>]`: Default number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="99f3f-165">`[SkuCapacityMaximum <Int32?>]`: Максимальное количество сотрудников для этого плана служб приложений SKU.</span><span class="sxs-lookup"><span data-stu-id="99f3f-165">`[SkuCapacityMaximum <Int32?>]`: Maximum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="99f3f-166">`[SkuCapacityMinimum <Int32?>]`: Минимальное количество рабочих процессов для этого плана служб приложений SKU.</span><span class="sxs-lookup"><span data-stu-id="99f3f-166">`[SkuCapacityMinimum <Int32?>]`: Minimum number of workers for this App Service plan SKU.</span></span>
  - <span data-ttu-id="99f3f-167">`[SkuCapacityScaleType <String>]`: Доступные конфигурации масштабирования для плана служб приложений.</span><span class="sxs-lookup"><span data-stu-id="99f3f-167">`[SkuCapacityScaleType <String>]`: Available scale configurations for an App Service plan.</span></span>
  - <span data-ttu-id="99f3f-168">`[SkuFamily <String>]`: Код семейства SKU ресурса.</span><span class="sxs-lookup"><span data-stu-id="99f3f-168">`[SkuFamily <String>]`: Family code of the resource SKU.</span></span>
  - <span data-ttu-id="99f3f-169">`[SkuLocation <String[]>]`: Расположение SKU.</span><span class="sxs-lookup"><span data-stu-id="99f3f-169">`[SkuLocation <String[]>]`: Locations of the SKU.</span></span>
  - <span data-ttu-id="99f3f-170">`[SkuName <String>]`: Имя SKU ресурса.</span><span class="sxs-lookup"><span data-stu-id="99f3f-170">`[SkuName <String>]`: Name of the resource SKU.</span></span>
  - <span data-ttu-id="99f3f-171">`[SkuSize <String>]`: Указатель размера SKU ресурса.</span><span class="sxs-lookup"><span data-stu-id="99f3f-171">`[SkuSize <String>]`: Size specifier of the resource SKU.</span></span>
  - <span data-ttu-id="99f3f-172">`[SkuTier <String>]`: Уровень обслуживания SKU ресурса.</span><span class="sxs-lookup"><span data-stu-id="99f3f-172">`[SkuTier <String>]`: Service tier of the resource SKU.</span></span>
  - <span data-ttu-id="99f3f-173">`[SpotExpirationTime <DateTime?>]`: Время истечения срока действия фермы серверов.</span><span class="sxs-lookup"><span data-stu-id="99f3f-173">`[SpotExpirationTime <DateTime?>]`: The time when the server farm expires.</span></span> <span data-ttu-id="99f3f-174">Действует только в том случае, если это ферма серверов с плашечными серверами.</span><span class="sxs-lookup"><span data-stu-id="99f3f-174">Valid only if it is a spot server farm.</span></span>
  - <span data-ttu-id="99f3f-175">`[TargetWorkerCount <Int32?>]`: Масштабирование количества рабочих процессов.</span><span class="sxs-lookup"><span data-stu-id="99f3f-175">`[TargetWorkerCount <Int32?>]`: Scaling worker count.</span></span>
  - <span data-ttu-id="99f3f-176">`[TargetWorkerSizeId <Int32?>]`: Масштабирование кода размера рабочего процесса.</span><span class="sxs-lookup"><span data-stu-id="99f3f-176">`[TargetWorkerSizeId <Int32?>]`: Scaling worker size ID.</span></span>
  - <span data-ttu-id="99f3f-177">`[WorkerTierName <String>]`: Целевой рабочий уровень, назначенный плану служб приложений.</span><span class="sxs-lookup"><span data-stu-id="99f3f-177">`[WorkerTierName <String>]`: Target worker tier assigned to the App Service plan.</span></span>

## <span data-ttu-id="99f3f-178">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="99f3f-178">RELATED LINKS</span></span>

