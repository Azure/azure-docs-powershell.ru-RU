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
ms.locfileid: "93900642"
---
# <span data-ttu-id="6d9a9-101">New-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="6d9a9-101">New-AzFrontDoor</span></span>

## <span data-ttu-id="6d9a9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6d9a9-102">SYNOPSIS</span></span>
<span data-ttu-id="6d9a9-103">Создание нового подсистемы балансировки нагрузки на передней дверцу Azure</span><span class="sxs-lookup"><span data-stu-id="6d9a9-103">Create a new Azure Front Door load balancer</span></span>

## <span data-ttu-id="6d9a9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6d9a9-104">SYNTAX</span></span>

```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d9a9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d9a9-105">DESCRIPTION</span></span>
<span data-ttu-id="6d9a9-106">Командлет **New-AzFrontDoor** создает новую подсистему балансировки нагрузки для передней дверцы Azure в указанной группе ресурсов в разделе текущая подписка</span><span class="sxs-lookup"><span data-stu-id="6d9a9-106">The **New-AzFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <span data-ttu-id="6d9a9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6d9a9-107">EXAMPLES</span></span>

### <span data-ttu-id="6d9a9-108">Пример 1: создание передней дверцы на основе заданных параметров.</span><span class="sxs-lookup"><span data-stu-id="6d9a9-108">Example 1: Create a Front Door based on given parameters.</span></span>
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

<span data-ttu-id="6d9a9-109">Создание передней дверцы на основе заданных параметров.</span><span class="sxs-lookup"><span data-stu-id="6d9a9-109">Create a Front Door based on given parameters.</span></span>

## <span data-ttu-id="6d9a9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6d9a9-110">PARAMETERS</span></span>

### <span data-ttu-id="6d9a9-111">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="6d9a9-111">-BackendPool</span></span>
<span data-ttu-id="6d9a9-112">Backendpools доступно для правила маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="6d9a9-112">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="6d9a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d9a9-113">-DefaultProfile</span></span>
<span data-ttu-id="6d9a9-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6d9a9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d9a9-115">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="6d9a9-115">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="6d9a9-116">Следует ли отключить проверку имени сертификата для HTTPS – запросов для всех пулов баз данных.</span><span class="sxs-lookup"><span data-stu-id="6d9a9-116">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="6d9a9-117">Не влияет на запросы, не относящиеся к HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6d9a9-117">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="6d9a9-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="6d9a9-118">-EnabledState</span></span>
<span data-ttu-id="6d9a9-119">Состояние EnabledState для подсистемы балансировки нагрузки передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="6d9a9-119">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="6d9a9-120">Значение по умолчанию — Enabled</span><span class="sxs-lookup"><span data-stu-id="6d9a9-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="6d9a9-121">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="6d9a9-121">-FrontendEndpoint</span></span>
<span data-ttu-id="6d9a9-122">Конечные точки переднего плана, доступные для правила маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="6d9a9-122">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="6d9a9-123">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="6d9a9-123">-HealthProbeSetting</span></span>
<span data-ttu-id="6d9a9-124">Параметры проверки работоспособности, связанные с этим экземпляром передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="6d9a9-124">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="6d9a9-125">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="6d9a9-125">-LoadBalancingSetting</span></span>
<span data-ttu-id="6d9a9-126">Параметры балансировки нагрузки, связанные с этим экземпляром передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="6d9a9-126">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="6d9a9-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6d9a9-127">-Name</span></span>
<span data-ttu-id="6d9a9-128">Имя передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="6d9a9-128">Front Door name.</span></span>

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

### <span data-ttu-id="6d9a9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d9a9-129">-ResourceGroupName</span></span>
<span data-ttu-id="6d9a9-130">Имя группы ресурсов, в которой будет создана Передняя дверца.</span><span class="sxs-lookup"><span data-stu-id="6d9a9-130">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="6d9a9-131">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="6d9a9-131">-RoutingRule</span></span>
<span data-ttu-id="6d9a9-132">Правила маршрутизации, связанные с этим FrontDoor</span><span class="sxs-lookup"><span data-stu-id="6d9a9-132">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="6d9a9-133">-Тег</span><span class="sxs-lookup"><span data-stu-id="6d9a9-133">-Tag</span></span>
<span data-ttu-id="6d9a9-134">Теги сопоставлены с FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="6d9a9-134">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="6d9a9-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d9a9-135">-Confirm</span></span>
<span data-ttu-id="6d9a9-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6d9a9-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d9a9-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d9a9-137">-WhatIf</span></span>
<span data-ttu-id="6d9a9-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6d9a9-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d9a9-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6d9a9-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d9a9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d9a9-140">CommonParameters</span></span>
<span data-ttu-id="6d9a9-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6d9a9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d9a9-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d9a9-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d9a9-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6d9a9-143">INPUTS</span></span>

### <span data-ttu-id="6d9a9-144">Ничего</span><span class="sxs-lookup"><span data-stu-id="6d9a9-144">None</span></span>

## <span data-ttu-id="6d9a9-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d9a9-145">OUTPUTS</span></span>

### <span data-ttu-id="6d9a9-146">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="6d9a9-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="6d9a9-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="6d9a9-147">NOTES</span></span>

## <span data-ttu-id="6d9a9-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d9a9-148">RELATED LINKS</span></span>

<span data-ttu-id="6d9a9-149">[Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="6d9a9-149">[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>