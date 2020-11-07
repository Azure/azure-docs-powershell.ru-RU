---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
ms.openlocfilehash: cea5b69b279b6f7f7a8e783d4ed328237377c18f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720898"
---
# <span data-ttu-id="d88ba-101">New-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="d88ba-101">New-AzFrontDoor</span></span>

## <span data-ttu-id="d88ba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d88ba-102">SYNOPSIS</span></span>
<span data-ttu-id="d88ba-103">Создание нового подсистемы балансировки нагрузки на передней дверцу Azure</span><span class="sxs-lookup"><span data-stu-id="d88ba-103">Create a new Azure Front Door load balancer</span></span>

## <span data-ttu-id="d88ba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d88ba-104">SYNTAX</span></span>

```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d88ba-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d88ba-105">DESCRIPTION</span></span>
<span data-ttu-id="d88ba-106">Командлет **New-AzFrontDoor** создает новую подсистему балансировки нагрузки для передней дверцы Azure в указанной группе ресурсов в разделе текущая подписка</span><span class="sxs-lookup"><span data-stu-id="d88ba-106">The **New-AzFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <span data-ttu-id="d88ba-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d88ba-107">EXAMPLES</span></span>

### <span data-ttu-id="d88ba-108">Пример 1: создание передней дверцы на основе заданных параметров.</span><span class="sxs-lookup"><span data-stu-id="d88ba-108">Example 1: Create a Front Door based on given parameters.</span></span>
```powershell
PS C:\> New-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "rg1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

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
Id                          : /subscriptions/{guid}/resourcegroups/rg1/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoors
```

<span data-ttu-id="d88ba-109">Создание передней дверцы на основе заданных параметров.</span><span class="sxs-lookup"><span data-stu-id="d88ba-109">Create a Front Door based on given parameters.</span></span>

## <span data-ttu-id="d88ba-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d88ba-110">PARAMETERS</span></span>

### <span data-ttu-id="d88ba-111">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="d88ba-111">-BackendPool</span></span>
<span data-ttu-id="d88ba-112">Backendpools доступно для правила маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="d88ba-112">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="d88ba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d88ba-113">-DefaultProfile</span></span>
<span data-ttu-id="d88ba-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d88ba-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d88ba-115">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="d88ba-115">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="d88ba-116">Следует ли отключить проверку имени сертификата для HTTPS – запросов для всех пулов баз данных.</span><span class="sxs-lookup"><span data-stu-id="d88ba-116">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="d88ba-117">Не влияет на запросы, не относящиеся к HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d88ba-117">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="d88ba-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="d88ba-118">-EnabledState</span></span>
<span data-ttu-id="d88ba-119">Состояние EnabledState для подсистемы балансировки нагрузки передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="d88ba-119">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="d88ba-120">Значение по умолчанию — Enabled</span><span class="sxs-lookup"><span data-stu-id="d88ba-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="d88ba-121">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="d88ba-121">-FrontendEndpoint</span></span>
<span data-ttu-id="d88ba-122">Конечные точки переднего плана, доступные для правила маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="d88ba-122">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="d88ba-123">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="d88ba-123">-HealthProbeSetting</span></span>
<span data-ttu-id="d88ba-124">Параметры проверки работоспособности, связанные с этим экземпляром передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="d88ba-124">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="d88ba-125">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="d88ba-125">-LoadBalancingSetting</span></span>
<span data-ttu-id="d88ba-126">Параметры балансировки нагрузки, связанные с этим экземпляром передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="d88ba-126">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="d88ba-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d88ba-127">-Name</span></span>
<span data-ttu-id="d88ba-128">Имя передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="d88ba-128">Front Door name.</span></span>

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

### <span data-ttu-id="d88ba-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d88ba-129">-ResourceGroupName</span></span>
<span data-ttu-id="d88ba-130">Имя группы ресурсов, в которой будет создана Передняя дверца.</span><span class="sxs-lookup"><span data-stu-id="d88ba-130">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="d88ba-131">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="d88ba-131">-RoutingRule</span></span>
<span data-ttu-id="d88ba-132">Правила маршрутизации, связанные с этим FrontDoor</span><span class="sxs-lookup"><span data-stu-id="d88ba-132">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="d88ba-133">-Тег</span><span class="sxs-lookup"><span data-stu-id="d88ba-133">-Tag</span></span>
<span data-ttu-id="d88ba-134">Теги сопоставлены с FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="d88ba-134">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="d88ba-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d88ba-135">-Confirm</span></span>
<span data-ttu-id="d88ba-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d88ba-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d88ba-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d88ba-137">-WhatIf</span></span>
<span data-ttu-id="d88ba-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d88ba-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d88ba-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d88ba-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d88ba-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d88ba-140">CommonParameters</span></span>
<span data-ttu-id="d88ba-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d88ba-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d88ba-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d88ba-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d88ba-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d88ba-143">INPUTS</span></span>

### <span data-ttu-id="d88ba-144">Ничего</span><span class="sxs-lookup"><span data-stu-id="d88ba-144">None</span></span>

## <span data-ttu-id="d88ba-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d88ba-145">OUTPUTS</span></span>

### <span data-ttu-id="d88ba-146">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="d88ba-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="d88ba-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="d88ba-147">NOTES</span></span>

## <span data-ttu-id="d88ba-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d88ba-148">RELATED LINKS</span></span>

<span data-ttu-id="d88ba-149">[Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="d88ba-149">[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>