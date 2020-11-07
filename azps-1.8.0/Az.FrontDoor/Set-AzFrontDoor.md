---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/set-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
ms.openlocfilehash: 57f1bf57495e75167a1936799c24aff5e6387722
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900570"
---
# <span data-ttu-id="73be4-101">Set-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="73be4-101">Set-AzFrontDoor</span></span>

## <span data-ttu-id="73be4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="73be4-102">SYNOPSIS</span></span>
<span data-ttu-id="73be4-103">Обновление подсистемы балансировки нагрузки на передней дверце</span><span class="sxs-lookup"><span data-stu-id="73be4-103">Update a Front Door load balancer</span></span>

## <span data-ttu-id="73be4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="73be4-104">SYNTAX</span></span>

### <span data-ttu-id="73be4-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="73be4-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73be4-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73be4-106">ByObjectParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="73be4-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73be4-107">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="73be4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73be4-108">DESCRIPTION</span></span>
<span data-ttu-id="73be4-109">Командлет **Set-AzFrontDoor** обновляет подсистему балансировки нагрузки передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="73be4-109">The **Set-AzFrontDoor** cmdlet updates a Front Door load balancer.</span></span> <span data-ttu-id="73be4-110">Если входные параметры не предоставлены, будут использоваться старые параметры существующей передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="73be4-110">If input parameters are not provided, old parameters from the existing Front Door will be used.</span></span>

## <span data-ttu-id="73be4-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="73be4-111">EXAMPLES</span></span>

### <span data-ttu-id="73be4-112">Пример 1: обновление существующей передней дверцы с помощью FrontDoorName и ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="73be4-112">Example 1: update an existing Front Door with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Set-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "resourceGroup1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
EnforceCertificateNameCheck : Enabled
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoors
```

<span data-ttu-id="73be4-113">Обновление существующего FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="73be4-113">update an existing FrontDoor.</span></span>

### <span data-ttu-id="73be4-114">Пример 2: обновление существующей передней дверцы с помощью объекта PSFrontDoor.</span><span class="sxs-lookup"><span data-stu-id="73be4-114">Example 2: update an existing Front Door with PSFrontDoor object.</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
EnforceCertificateNameCheck : Enabled
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoor1
```

<span data-ttu-id="73be4-115">Обновление существующего FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="73be4-115">update an existing FrontDoor.</span></span>

### <span data-ttu-id="73be4-116">Пример 3: обновление существующей передней дверцы с ResourceId</span><span class="sxs-lookup"><span data-stu-id="73be4-116">Example 3: update an existing Front Door with ResourceId</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -ResourceId {resourceId} -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
EnforceCertificateNameCheck : Enabled
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoor1
```

<span data-ttu-id="73be4-117">Обновление существующего FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="73be4-117">update an existing FrontDoor.</span></span>

## <span data-ttu-id="73be4-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="73be4-118">PARAMETERS</span></span>

### <span data-ttu-id="73be4-119">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="73be4-119">-BackendPool</span></span>
<span data-ttu-id="73be4-120">Backendpools доступно для правила маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="73be4-120">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="73be4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73be4-121">-DefaultProfile</span></span>
<span data-ttu-id="73be4-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="73be4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73be4-123">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="73be4-123">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="73be4-124">Следует ли отключить проверку имени сертификата для HTTPS – запросов для всех пулов баз данных.</span><span class="sxs-lookup"><span data-stu-id="73be4-124">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="73be4-125">Не влияет на запросы, не относящиеся к HTTPS.</span><span class="sxs-lookup"><span data-stu-id="73be4-125">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="73be4-126">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="73be4-126">-EnabledState</span></span>
<span data-ttu-id="73be4-127">Рабочее состояние подсистемы балансировки нагрузки для передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="73be4-127">Operational status of the Front Door load balancer.</span></span>

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

### <span data-ttu-id="73be4-128">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="73be4-128">-FrontendEndpoint</span></span>
<span data-ttu-id="73be4-129">Конечные точки переднего плана, доступные для правила маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="73be4-129">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="73be4-130">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="73be4-130">-HealthProbeSetting</span></span>
<span data-ttu-id="73be4-131">Параметры проверки работоспособности, связанные с этим экземпляром передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="73be4-131">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="73be4-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73be4-132">-InputObject</span></span>
<span data-ttu-id="73be4-133">Объект передней дверцы для обновления.</span><span class="sxs-lookup"><span data-stu-id="73be4-133">The Front Door object to update.</span></span>

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

### <span data-ttu-id="73be4-134">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="73be4-134">-LoadBalancingSetting</span></span>
<span data-ttu-id="73be4-135">Параметры балансировки нагрузки, связанные с этим экземпляром передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="73be4-135">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="73be4-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="73be4-136">-Name</span></span>
<span data-ttu-id="73be4-137">Имя передней дверцы для обновления.</span><span class="sxs-lookup"><span data-stu-id="73be4-137">The name of the Front Door to update.</span></span>

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

### <span data-ttu-id="73be4-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73be4-138">-ResourceGroupName</span></span>
<span data-ttu-id="73be4-139">Группа ресурсов, к которой принадлежит передняя дверь.</span><span class="sxs-lookup"><span data-stu-id="73be4-139">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="73be4-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73be4-140">-ResourceId</span></span>
<span data-ttu-id="73be4-141">Идентификатор ресурса передней дверцы для обновления</span><span class="sxs-lookup"><span data-stu-id="73be4-141">Resource Id of the Front Door to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73be4-142">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="73be4-142">-RoutingRule</span></span>
<span data-ttu-id="73be4-143">Правила маршрутизации, связанные с этим FrontDoor</span><span class="sxs-lookup"><span data-stu-id="73be4-143">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="73be4-144">-Тег</span><span class="sxs-lookup"><span data-stu-id="73be4-144">-Tag</span></span>
<span data-ttu-id="73be4-145">Теги сопоставлены с FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="73be4-145">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="73be4-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73be4-146">-Confirm</span></span>
<span data-ttu-id="73be4-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="73be4-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73be4-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73be4-148">-WhatIf</span></span>
<span data-ttu-id="73be4-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="73be4-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73be4-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="73be4-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73be4-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73be4-151">CommonParameters</span></span>
<span data-ttu-id="73be4-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="73be4-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73be4-153">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73be4-153">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73be4-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="73be4-154">INPUTS</span></span>

### <span data-ttu-id="73be4-155">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="73be4-155">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="73be4-156">System. String</span><span class="sxs-lookup"><span data-stu-id="73be4-156">System.String</span></span>

## <span data-ttu-id="73be4-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="73be4-157">OUTPUTS</span></span>

### <span data-ttu-id="73be4-158">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="73be4-158">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="73be4-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="73be4-159">NOTES</span></span>

## <span data-ttu-id="73be4-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73be4-160">RELATED LINKS</span></span>

<span data-ttu-id="73be4-161">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="73be4-161">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>
