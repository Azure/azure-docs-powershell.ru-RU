---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/set-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
ms.openlocfilehash: 344041291f0d7f52aeebb0c968e99268ac042188
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245442"
---
# <span data-ttu-id="0d4a5-101">Set-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="0d4a5-101">Set-AzFrontDoor</span></span>

## <span data-ttu-id="0d4a5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d4a5-102">SYNOPSIS</span></span>
<span data-ttu-id="0d4a5-103">Обновление подсистемы балансировки нагрузки на передней дверце</span><span class="sxs-lookup"><span data-stu-id="0d4a5-103">Update a Front Door load balancer</span></span>

## <span data-ttu-id="0d4a5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d4a5-104">SYNTAX</span></span>

### <span data-ttu-id="0d4a5-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0d4a5-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d4a5-106">ByFieldsWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d4a5-106">ByFieldsWithCertificateNameCheckParameterSet</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d4a5-107">ByFieldsWithBackendPoolsSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d4a5-107">ByFieldsWithBackendPoolsSettingParameterSet</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] -BackendPoolsSetting <PSBackendPoolsSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d4a5-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d4a5-108">ByObjectParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d4a5-109">ByObjectWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d4a5-109">ByObjectWithCertificateNameCheckParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d4a5-110">ByObjectWithBackendPoolsSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d4a5-110">ByObjectWithBackendPoolsSettingParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 -BackendPoolsSetting <PSBackendPoolsSetting> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d4a5-111">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d4a5-111">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d4a5-112">ByResourceIdWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d4a5-112">ByResourceIdWithCertificateNameCheckParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d4a5-113">ByResourceIdWithBackendPoolsSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d4a5-113">ByResourceIdWithBackendPoolsSettingParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 -BackendPoolsSetting <PSBackendPoolsSetting> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0d4a5-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d4a5-114">DESCRIPTION</span></span>
<span data-ttu-id="0d4a5-115">Командлет **Set-AzFrontDoor** обновляет подсистему балансировки нагрузки передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="0d4a5-115">The **Set-AzFrontDoor** cmdlet updates a Front Door load balancer.</span></span> <span data-ttu-id="0d4a5-116">Если входные параметры не предоставлены, будут использоваться старые параметры существующей передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="0d4a5-116">If input parameters are not provided, old parameters from the existing Front Door will be used.</span></span>

## <span data-ttu-id="0d4a5-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d4a5-117">EXAMPLES</span></span>

### <span data-ttu-id="0d4a5-118">Пример 1: обновление существующей передней дверцы с помощью FrontDoorName и ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="0d4a5-118">Example 1: update an existing Front Door with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Set-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "resourceGroup1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
BackendPoolsSetting         : {backendPoolsSetting1}
EnforceCertificateNameCheck : {backendPoolsSetting1.EnforceCertificateNameCheck}
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

<span data-ttu-id="0d4a5-119">Обновление существующего FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="0d4a5-119">update an existing FrontDoor.</span></span>

### <span data-ttu-id="0d4a5-120">Пример 2: обновление существующей передней дверцы с помощью объекта PSFrontDoor.</span><span class="sxs-lookup"><span data-stu-id="0d4a5-120">Example 2: update an existing Front Door with PSFrontDoor object.</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
BackendPoolsSetting         : {backendPoolsSetting1}
EnforceCertificateNameCheck : {backendPoolsSetting1.EnforceCertificateNameCheck}
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

<span data-ttu-id="0d4a5-121">Обновление существующего FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="0d4a5-121">update an existing FrontDoor.</span></span>

### <span data-ttu-id="0d4a5-122">Пример 3: обновление существующей передней дверцы с ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d4a5-122">Example 3: update an existing Front Door with ResourceId</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -ResourceId {resourceId} -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
BackendPoolsSetting         : {backendPoolsSetting1}
EnforceCertificateNameCheck : {backendPoolsSetting1.EnforceCertificateNameCheck}
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

<span data-ttu-id="0d4a5-123">Обновление существующего FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="0d4a5-123">update an existing FrontDoor.</span></span>

### <span data-ttu-id="0d4a5-124">Пример 4: обновление свойства BackendPoolSetting EnforceCertificateNameCheck существующей передней дверцы с помощью параметра-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="0d4a5-124">Example 4: update BackendPoolSetting property EnforceCertificateNameCheck of an existing Front Door with -DisableCertificateNameCheck switch parameter</span></span>
<span data-ttu-id="0d4a5-125">Для идентификации передней дверцы можно использовать FrontoorName и ResourceGroupName, объект PSFrontDoor или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="0d4a5-125">Front Door to be updated can be identified using FrontoorName and ResourceGroupName, PSFrontDoor object, or ResourceId.</span></span> <span data-ttu-id="0d4a5-126">(См. выше 3 примера) В приведенном ниже примере используется объект PSFrontDoor.</span><span class="sxs-lookup"><span data-stu-id="0d4a5-126">(See above 3 examples for example) The below example uses PSFrontDoor object.</span></span>

```powershell
PS C:\>  Set-AzFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -DisableCertificateNameCheck

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
BackendPoolsSetting         : {PSBackendPoolsSetting object with EnforceCertificateNameCheck is set to Disabled}
EnforceCertificateNameCheck : Disabled
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

<span data-ttu-id="0d4a5-127">Обновление существующего FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="0d4a5-127">update an existing FrontDoor.</span></span>

## <span data-ttu-id="0d4a5-128">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d4a5-128">PARAMETERS</span></span>

### <span data-ttu-id="0d4a5-129">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="0d4a5-129">-BackendPool</span></span>
<span data-ttu-id="0d4a5-130">Backendpools доступно для правила маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="0d4a5-130">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="0d4a5-131">-BackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="0d4a5-131">-BackendPoolsSetting</span></span>
<span data-ttu-id="0d4a5-132">Параметры для всех backendPools.</span><span class="sxs-lookup"><span data-stu-id="0d4a5-132">Settings for all backendPools.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting
Parameter Sets: ByFieldsWithBackendPoolsSettingParameterSet, ByObjectWithBackendPoolsSettingParameterSet, ByResourceIdWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d4a5-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d4a5-133">-DefaultProfile</span></span>
<span data-ttu-id="0d4a5-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0d4a5-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d4a5-135">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="0d4a5-135">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="0d4a5-136">Следует ли отключить проверку имени сертификата для HTTPS – запросов для всех пулов баз данных.</span><span class="sxs-lookup"><span data-stu-id="0d4a5-136">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="0d4a5-137">Не влияет на запросы, не относящиеся к HTTPS.</span><span class="sxs-lookup"><span data-stu-id="0d4a5-137">No effect on non-HTTPS requests.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFieldsWithCertificateNameCheckParameterSet, ByObjectWithCertificateNameCheckParameterSet, ByResourceIdWithCertificateNameCheckParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d4a5-138">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="0d4a5-138">-EnabledState</span></span>
<span data-ttu-id="0d4a5-139">Рабочее состояние подсистемы балансировки нагрузки для передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="0d4a5-139">Operational status of the Front Door load balancer.</span></span>

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

### <span data-ttu-id="0d4a5-140">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="0d4a5-140">-FrontendEndpoint</span></span>
<span data-ttu-id="0d4a5-141">Конечные точки переднего плана, доступные для правила маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="0d4a5-141">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="0d4a5-142">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="0d4a5-142">-HealthProbeSetting</span></span>
<span data-ttu-id="0d4a5-143">Параметры проверки работоспособности, связанные с этим экземпляром передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="0d4a5-143">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="0d4a5-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d4a5-144">-InputObject</span></span>
<span data-ttu-id="0d4a5-145">Объект передней дверцы для обновления.</span><span class="sxs-lookup"><span data-stu-id="0d4a5-145">The Front Door object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet, ByObjectWithCertificateNameCheckParameterSet, ByObjectWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d4a5-146">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="0d4a5-146">-LoadBalancingSetting</span></span>
<span data-ttu-id="0d4a5-147">Параметры балансировки нагрузки, связанные с этим экземпляром передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="0d4a5-147">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="0d4a5-148">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0d4a5-148">-Name</span></span>
<span data-ttu-id="0d4a5-149">Имя передней дверцы для обновления.</span><span class="sxs-lookup"><span data-stu-id="0d4a5-149">The name of the Front Door to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithCertificateNameCheckParameterSet, ByFieldsWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d4a5-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d4a5-150">-ResourceGroupName</span></span>
<span data-ttu-id="0d4a5-151">Группа ресурсов, к которой принадлежит передняя дверь.</span><span class="sxs-lookup"><span data-stu-id="0d4a5-151">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithCertificateNameCheckParameterSet, ByFieldsWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d4a5-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d4a5-152">-ResourceId</span></span>
<span data-ttu-id="0d4a5-153">Идентификатор ресурса передней дверцы для обновления</span><span class="sxs-lookup"><span data-stu-id="0d4a5-153">Resource Id of the Front Door to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet, ByResourceIdWithCertificateNameCheckParameterSet, ByResourceIdWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d4a5-154">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="0d4a5-154">-RoutingRule</span></span>
<span data-ttu-id="0d4a5-155">Правила маршрутизации, связанные с этим FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0d4a5-155">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="0d4a5-156">-Тег</span><span class="sxs-lookup"><span data-stu-id="0d4a5-156">-Tag</span></span>
<span data-ttu-id="0d4a5-157">Теги сопоставлены с FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="0d4a5-157">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="0d4a5-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d4a5-158">-Confirm</span></span>
<span data-ttu-id="0d4a5-159">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0d4a5-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d4a5-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d4a5-160">-WhatIf</span></span>
<span data-ttu-id="0d4a5-161">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0d4a5-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d4a5-162">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0d4a5-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d4a5-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d4a5-163">CommonParameters</span></span>
<span data-ttu-id="0d4a5-164">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d4a5-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d4a5-165">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d4a5-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d4a5-166">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d4a5-166">INPUTS</span></span>

### <span data-ttu-id="0d4a5-167">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="0d4a5-167">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
### <span data-ttu-id="0d4a5-168">System. String</span><span class="sxs-lookup"><span data-stu-id="0d4a5-168">System.String</span></span>
## <span data-ttu-id="0d4a5-169">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d4a5-169">OUTPUTS</span></span>

### <span data-ttu-id="0d4a5-170">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="0d4a5-170">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
## <span data-ttu-id="0d4a5-171">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d4a5-171">NOTES</span></span>

## <span data-ttu-id="0d4a5-172">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d4a5-172">RELATED LINKS</span></span>

<span data-ttu-id="0d4a5-173">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="0d4a5-173">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>
