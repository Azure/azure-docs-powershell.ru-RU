---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
ms.openlocfilehash: 3f08ada3dd485a1e18bb6f0a91037ba1df0b5f25
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405215"
---
# <span data-ttu-id="29adb-101">New-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="29adb-101">New-AzFrontDoor</span></span>

## <span data-ttu-id="29adb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29adb-102">SYNOPSIS</span></span>
<span data-ttu-id="29adb-103">Создание балансировки загрузки на переднем клиенте Azure</span><span class="sxs-lookup"><span data-stu-id="29adb-103">Create a new Azure Front Door load balancer</span></span>

## <span data-ttu-id="29adb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="29adb-104">SYNTAX</span></span>

### <span data-ttu-id="29adb-105">ByFieldsWithBackendPoolsSettingParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="29adb-105">ByFieldsWithBackendPoolsSettingParameterSet (Default)</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-BackendPoolsSetting <PSBackendPoolsSetting>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29adb-106">ByFieldsWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="29adb-106">ByFieldsWithCertificateNameCheckParameterSet</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29adb-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="29adb-107">DESCRIPTION</span></span>
<span data-ttu-id="29adb-108">С **его использованием** создается новый баланс нагрузки Azure Front Door в указанной группе ресурсов в рамках текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="29adb-108">The **New-AzFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <span data-ttu-id="29adb-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="29adb-109">EXAMPLES</span></span>

### <span data-ttu-id="29adb-110">Пример 1. Создание переднего входа на основе заданных параметров.</span><span class="sxs-lookup"><span data-stu-id="29adb-110">Example 1: Create a Front Door based on given parameters.</span></span>
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

<span data-ttu-id="29adb-111">Создайте переднюю дверь на основе заданных параметров.</span><span class="sxs-lookup"><span data-stu-id="29adb-111">Create a Front Door based on given parameters.</span></span>

## <span data-ttu-id="29adb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29adb-112">PARAMETERS</span></span>

### <span data-ttu-id="29adb-113">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="29adb-113">-BackendPool</span></span>
<span data-ttu-id="29adb-114">Backendpools available to routing rule.</span><span class="sxs-lookup"><span data-stu-id="29adb-114">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="29adb-115">-BackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="29adb-115">-BackendPoolsSetting</span></span>
<span data-ttu-id="29adb-116">Параметры всех backendPools</span><span class="sxs-lookup"><span data-stu-id="29adb-116">Settings for all backendPools</span></span>

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

### <span data-ttu-id="29adb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29adb-117">-DefaultProfile</span></span>
<span data-ttu-id="29adb-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="29adb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29adb-119">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="29adb-119">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="29adb-120">Следует ли отключить проверку имени сертификата по HTTPS-запросам во все пулы backend.</span><span class="sxs-lookup"><span data-stu-id="29adb-120">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="29adb-121">Никакие действия с запросами, не относясьми к HTTPS-запросам.</span><span class="sxs-lookup"><span data-stu-id="29adb-121">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="29adb-122">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="29adb-122">-EnabledState</span></span>
<span data-ttu-id="29adb-123">EnabledState балансира загрузки front Door.</span><span class="sxs-lookup"><span data-stu-id="29adb-123">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="29adb-124">Значение по умолчанию включено</span><span class="sxs-lookup"><span data-stu-id="29adb-124">Default value is Enabled</span></span>

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

### <span data-ttu-id="29adb-125">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="29adb-125">-FrontendEndpoint</span></span>
<span data-ttu-id="29adb-126">Конечные точки переднего входа, доступные для правила маршрутки.</span><span class="sxs-lookup"><span data-stu-id="29adb-126">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="29adb-127">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="29adb-127">-HealthProbeSetting</span></span>
<span data-ttu-id="29adb-128">Параметры безопасности, связанные с этим экземпляром передней двери.</span><span class="sxs-lookup"><span data-stu-id="29adb-128">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="29adb-129">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="29adb-129">-LoadBalancingSetting</span></span>
<span data-ttu-id="29adb-130">Параметры балансировки нагрузки, связанные с этим экземпляром передней двери.</span><span class="sxs-lookup"><span data-stu-id="29adb-130">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="29adb-131">-Name</span><span class="sxs-lookup"><span data-stu-id="29adb-131">-Name</span></span>
<span data-ttu-id="29adb-132">Имя передней двери.</span><span class="sxs-lookup"><span data-stu-id="29adb-132">Front Door name.</span></span>

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

### <span data-ttu-id="29adb-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29adb-133">-ResourceGroupName</span></span>
<span data-ttu-id="29adb-134">Имя группы ресурсов, в которую будет создана front Door.</span><span class="sxs-lookup"><span data-stu-id="29adb-134">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="29adb-135">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="29adb-135">-RoutingRule</span></span>
<span data-ttu-id="29adb-136">Правила маршрутов, связанные с этим frontDoor</span><span class="sxs-lookup"><span data-stu-id="29adb-136">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="29adb-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="29adb-137">-Tag</span></span>
<span data-ttu-id="29adb-138">Теги, которые связываются с FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="29adb-138">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="29adb-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29adb-139">-Confirm</span></span>
<span data-ttu-id="29adb-140">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29adb-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29adb-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29adb-141">-WhatIf</span></span>
<span data-ttu-id="29adb-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29adb-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29adb-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="29adb-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29adb-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29adb-144">CommonParameters</span></span>
<span data-ttu-id="29adb-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29adb-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29adb-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="29adb-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29adb-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="29adb-147">INPUTS</span></span>

### <span data-ttu-id="29adb-148">Нет</span><span class="sxs-lookup"><span data-stu-id="29adb-148">None</span></span>
## <span data-ttu-id="29adb-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="29adb-149">OUTPUTS</span></span>

### <span data-ttu-id="29adb-150">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="29adb-150">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
## <span data-ttu-id="29adb-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="29adb-151">NOTES</span></span>

## <span data-ttu-id="29adb-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="29adb-152">RELATED LINKS</span></span>

<span data-ttu-id="29adb-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="29adb-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>