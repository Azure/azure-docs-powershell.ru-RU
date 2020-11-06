---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/set-azurermfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoor.md
ms.openlocfilehash: 250fa8a5638e1aa9d67d212fd45352c7756d2aef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556631"
---
# <span data-ttu-id="e8b22-101">Set-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="e8b22-101">Set-AzureRmFrontDoor</span></span>

## <span data-ttu-id="e8b22-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e8b22-102">SYNOPSIS</span></span>
<span data-ttu-id="e8b22-103">Обновление подсистемы балансировки нагрузки на передней дверце</span><span class="sxs-lookup"><span data-stu-id="e8b22-103">Update a Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8b22-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e8b22-104">SYNTAX</span></span>

### <span data-ttu-id="e8b22-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e8b22-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8b22-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8b22-106">ByObjectParameterSet</span></span>
```
Set-AzureRmFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8b22-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8b22-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8b22-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8b22-108">DESCRIPTION</span></span>
<span data-ttu-id="e8b22-109">Командлет **Set-AzureRmFrontDoor** обновляет подсистему балансировки нагрузки передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="e8b22-109">The **Set-AzureRmFrontDoor** cmdlet updates a Front Door load balancer.</span></span> <span data-ttu-id="e8b22-110">Если входные параметры не предоставлены, будут использоваться старые параметры существующей передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="e8b22-110">If input parameters are not provided, old parameters from the existing Front Door will be used.</span></span>

## <span data-ttu-id="e8b22-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e8b22-111">EXAMPLES</span></span>

### <span data-ttu-id="e8b22-112">Пример 1: обновление существующей передней дверцы с помощью FrontDoorName и ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="e8b22-112">Example 1: update an existing Front Door with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoor -Name "frontDoor1" -ResourceGroupName "resourceGroup1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="e8b22-113">Обновление существующего FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="e8b22-113">update an existing FrontDoor.</span></span>

### <span data-ttu-id="e8b22-114">Пример 2: обновление существующей передней дверцы с помощью объекта PSFrontDoor.</span><span class="sxs-lookup"><span data-stu-id="e8b22-114">Example 2: update an existing Front Door with PSFrontDoor object.</span></span>
```powershell
PS C:\>  Set-AzureRmFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="e8b22-115">Обновление существующего FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="e8b22-115">update an existing FrontDoor.</span></span>

### <span data-ttu-id="e8b22-116">Пример 3: обновление существующей передней дверцы с ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8b22-116">Example 3: update an existing Front Door with ResourceId</span></span>
```powershell
PS C:\>  Set-AzureRmFrontDoor -ResourceId {resourceId} -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="e8b22-117">Обновление существующего FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="e8b22-117">update an existing FrontDoor.</span></span>

## <span data-ttu-id="e8b22-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e8b22-118">PARAMETERS</span></span>

### <span data-ttu-id="e8b22-119">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="e8b22-119">-BackendPool</span></span>
<span data-ttu-id="e8b22-120">Backendpools доступно для правила маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="e8b22-120">Backendpools available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8b22-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8b22-121">-DefaultProfile</span></span>
<span data-ttu-id="e8b22-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e8b22-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8b22-123">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="e8b22-123">-EnabledState</span></span>
<span data-ttu-id="e8b22-124">Рабочее состояние подсистемы балансировки нагрузки для передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="e8b22-124">Operational status of the Front Door load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8b22-125">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="e8b22-125">-FrontendEndpoint</span></span>
<span data-ttu-id="e8b22-126">Конечные точки переднего плана, доступные для правила маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="e8b22-126">Frontend endpoints available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8b22-127">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="e8b22-127">-HealthProbeSetting</span></span>
<span data-ttu-id="e8b22-128">Параметры проверки работоспособности, связанные с этим экземпляром передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="e8b22-128">Health probe settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8b22-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8b22-129">-InputObject</span></span>
<span data-ttu-id="e8b22-130">Объект передней дверцы для обновления.</span><span class="sxs-lookup"><span data-stu-id="e8b22-130">The Front Door object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b22-131">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="e8b22-131">-LoadBalancingSetting</span></span>
<span data-ttu-id="e8b22-132">Параметры балансировки нагрузки, связанные с этим экземпляром передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="e8b22-132">Load balancing settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8b22-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e8b22-133">-Name</span></span>
<span data-ttu-id="e8b22-134">Имя передней дверцы для обновления.</span><span class="sxs-lookup"><span data-stu-id="e8b22-134">The name of the Front Door to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8b22-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8b22-135">-ResourceGroupName</span></span>
<span data-ttu-id="e8b22-136">Группа ресурсов, к которой принадлежит передняя дверь.</span><span class="sxs-lookup"><span data-stu-id="e8b22-136">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8b22-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8b22-137">-ResourceId</span></span>
<span data-ttu-id="e8b22-138">Идентификатор ресурса передней дверцы для обновления</span><span class="sxs-lookup"><span data-stu-id="e8b22-138">Resource Id of the Front Door to update</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b22-139">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="e8b22-139">-RoutingRule</span></span>
<span data-ttu-id="e8b22-140">Правила маршрутизации, связанные с этим FrontDoor</span><span class="sxs-lookup"><span data-stu-id="e8b22-140">Routing rules associated with this FrontDoor</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8b22-141">-Тег</span><span class="sxs-lookup"><span data-stu-id="e8b22-141">-Tag</span></span>
<span data-ttu-id="e8b22-142">Теги сопоставлены с FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="e8b22-142">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="e8b22-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8b22-143">-Confirm</span></span>
<span data-ttu-id="e8b22-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e8b22-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8b22-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8b22-145">-WhatIf</span></span>
<span data-ttu-id="e8b22-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e8b22-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8b22-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e8b22-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8b22-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8b22-148">CommonParameters</span></span>
<span data-ttu-id="e8b22-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e8b22-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8b22-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8b22-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8b22-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e8b22-151">INPUTS</span></span>

### <span data-ttu-id="e8b22-152">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="e8b22-152">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="e8b22-153">System. String</span><span class="sxs-lookup"><span data-stu-id="e8b22-153">System.String</span></span>

## <span data-ttu-id="e8b22-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8b22-154">OUTPUTS</span></span>

### <span data-ttu-id="e8b22-155">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="e8b22-155">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="e8b22-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="e8b22-156">NOTES</span></span>

## <span data-ttu-id="e8b22-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8b22-157">RELATED LINKS</span></span>

<span data-ttu-id="e8b22-158">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md) 
 [Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md) 
 [New-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md) 
 [New-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md) 
 [New-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md) 
 [New-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md) 
 [New-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="e8b22-158">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)
[Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)
[New-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md)
[New-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md)
[New-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md)
[New-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md)
[New-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span></span>
