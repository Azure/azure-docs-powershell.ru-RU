---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
ms.openlocfilehash: 3f08ada3dd485a1e18bb6f0a91037ba1df0b5f25
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247431"
---
# <span data-ttu-id="b802e-101">New-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="b802e-101">New-AzFrontDoor</span></span>

## <span data-ttu-id="b802e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b802e-102">SYNOPSIS</span></span>
<span data-ttu-id="b802e-103">Создание нового подсистемы балансировки нагрузки на передней дверцу Azure</span><span class="sxs-lookup"><span data-stu-id="b802e-103">Create a new Azure Front Door load balancer</span></span>

## <span data-ttu-id="b802e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b802e-104">SYNTAX</span></span>

### <span data-ttu-id="b802e-105">ByFieldsWithBackendPoolsSettingParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b802e-105">ByFieldsWithBackendPoolsSettingParameterSet (Default)</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-BackendPoolsSetting <PSBackendPoolsSetting>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b802e-106">ByFieldsWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="b802e-106">ByFieldsWithCertificateNameCheckParameterSet</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b802e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b802e-107">DESCRIPTION</span></span>
<span data-ttu-id="b802e-108">Командлет **New-AzFrontDoor** создает новую подсистему балансировки нагрузки для передней дверцы Azure в указанной группе ресурсов в разделе текущая подписка</span><span class="sxs-lookup"><span data-stu-id="b802e-108">The **New-AzFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <span data-ttu-id="b802e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b802e-109">EXAMPLES</span></span>

### <span data-ttu-id="b802e-110">Пример 1: создание передней дверцы на основе заданных параметров.</span><span class="sxs-lookup"><span data-stu-id="b802e-110">Example 1: Create a Front Door based on given parameters.</span></span>
```powershell
PS C:\> New-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "rg1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

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
Id                          : /subscriptions/{guid}/resourcegroups/rg1/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoors
```

<span data-ttu-id="b802e-111">Создание передней дверцы на основе заданных параметров.</span><span class="sxs-lookup"><span data-stu-id="b802e-111">Create a Front Door based on given parameters.</span></span>

## <span data-ttu-id="b802e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b802e-112">PARAMETERS</span></span>

### <span data-ttu-id="b802e-113">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="b802e-113">-BackendPool</span></span>
<span data-ttu-id="b802e-114">Backendpools доступно для правила маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="b802e-114">Backendpools available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b802e-115">-BackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="b802e-115">-BackendPoolsSetting</span></span>
<span data-ttu-id="b802e-116">Параметры для всех backendPools</span><span class="sxs-lookup"><span data-stu-id="b802e-116">Settings for all backendPools</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting
Parameter Sets: ByFieldsWithBackendPoolsSettingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b802e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b802e-117">-DefaultProfile</span></span>
<span data-ttu-id="b802e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b802e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b802e-119">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="b802e-119">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="b802e-120">Следует ли отключить проверку имени сертификата для HTTPS – запросов для всех пулов баз данных.</span><span class="sxs-lookup"><span data-stu-id="b802e-120">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="b802e-121">Не влияет на запросы, не относящиеся к HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b802e-121">No effect on non-HTTPS requests.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFieldsWithCertificateNameCheckParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b802e-122">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="b802e-122">-EnabledState</span></span>
<span data-ttu-id="b802e-123">Состояние EnabledState для подсистемы балансировки нагрузки передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="b802e-123">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="b802e-124">Значение по умолчанию — Enabled</span><span class="sxs-lookup"><span data-stu-id="b802e-124">Default value is Enabled</span></span>

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

### <span data-ttu-id="b802e-125">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="b802e-125">-FrontendEndpoint</span></span>
<span data-ttu-id="b802e-126">Конечные точки переднего плана, доступные для правила маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="b802e-126">Frontend endpoints available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b802e-127">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="b802e-127">-HealthProbeSetting</span></span>
<span data-ttu-id="b802e-128">Параметры проверки работоспособности, связанные с этим экземпляром передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="b802e-128">Health probe settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b802e-129">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="b802e-129">-LoadBalancingSetting</span></span>
<span data-ttu-id="b802e-130">Параметры балансировки нагрузки, связанные с этим экземпляром передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="b802e-130">Load balancing settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b802e-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b802e-131">-Name</span></span>
<span data-ttu-id="b802e-132">Имя передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="b802e-132">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b802e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b802e-133">-ResourceGroupName</span></span>
<span data-ttu-id="b802e-134">Имя группы ресурсов, в которой будет создана Передняя дверца.</span><span class="sxs-lookup"><span data-stu-id="b802e-134">The resource group name that the Front Door will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b802e-135">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="b802e-135">-RoutingRule</span></span>
<span data-ttu-id="b802e-136">Правила маршрутизации, связанные с этим FrontDoor</span><span class="sxs-lookup"><span data-stu-id="b802e-136">Routing rules associated with this FrontDoor</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b802e-137">-Тег</span><span class="sxs-lookup"><span data-stu-id="b802e-137">-Tag</span></span>
<span data-ttu-id="b802e-138">Теги сопоставлены с FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="b802e-138">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="b802e-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b802e-139">-Confirm</span></span>
<span data-ttu-id="b802e-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b802e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b802e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b802e-141">-WhatIf</span></span>
<span data-ttu-id="b802e-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b802e-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b802e-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b802e-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b802e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b802e-144">CommonParameters</span></span>
<span data-ttu-id="b802e-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b802e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b802e-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b802e-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b802e-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b802e-147">INPUTS</span></span>

### <span data-ttu-id="b802e-148">Ничего</span><span class="sxs-lookup"><span data-stu-id="b802e-148">None</span></span>
## <span data-ttu-id="b802e-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b802e-149">OUTPUTS</span></span>

### <span data-ttu-id="b802e-150">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="b802e-150">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
## <span data-ttu-id="b802e-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="b802e-151">NOTES</span></span>

## <span data-ttu-id="b802e-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b802e-152">RELATED LINKS</span></span>

<span data-ttu-id="b802e-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="b802e-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>