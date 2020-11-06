---
<span data-ttu-id="9c686-101">внешний файл справки: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml имя модуля: AzureRM. FrontDoor Online Version: соответствующий URL-адрес должен быть следующим: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoor Schema: 2.0.0 content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md</span><span class="sxs-lookup"><span data-stu-id="9c686-101">external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml Module Name: AzureRM.FrontDoor online version: The corresponding URL should be the following: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoor schema: 2.0.0 content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md</span></span>
---

# <a name="new-azurermfrontdoor"></a><span data-ttu-id="9c686-102">New-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="9c686-102">New-AzureRmFrontDoor</span></span>

## <a name="synopsis"></a><span data-ttu-id="9c686-103">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9c686-103">SYNOPSIS</span></span>
<span data-ttu-id="9c686-104">Создание нового подсистемы балансировки нагрузки на передней дверцу Azure</span><span class="sxs-lookup"><span data-stu-id="9c686-104">Create a new Azure Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <a name="syntax"></a><span data-ttu-id="9c686-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9c686-105">SYNTAX</span></span>

```
New-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <a name="description"></a><span data-ttu-id="9c686-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c686-106">DESCRIPTION</span></span>
<span data-ttu-id="9c686-107">Командлет **New-AzureRmFrontDoor** создает новую подсистему балансировки нагрузки для передней дверцы Azure в указанной группе ресурсов в разделе текущая подписка</span><span class="sxs-lookup"><span data-stu-id="9c686-107">The **New-AzureRmFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <a name="examples"></a><span data-ttu-id="9c686-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9c686-108">EXAMPLES</span></span>

### <a name="example-1-create-a-front-door-based-on-given-parameters"></a><span data-ttu-id="9c686-109">Пример 1: создание передней дверцы на основе заданных параметров.</span><span class="sxs-lookup"><span data-stu-id="9c686-109">Example 1: Create a Front Door based on given parameters.</span></span>
```powershell
PS C:\> New-AzureRmFrontDoor -Name "frontDoor1" -ResourceGroupName "rg1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

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
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="9c686-110">Создание передней дверцы на основе заданных параметров.</span><span class="sxs-lookup"><span data-stu-id="9c686-110">Create a Front Door based on given parameters.</span></span>

## <a name="parameters"></a><span data-ttu-id="9c686-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9c686-111">PARAMETERS</span></span>

### <a name="-backendpool"></a><span data-ttu-id="9c686-112">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="9c686-112">-BackendPool</span></span>
<span data-ttu-id="9c686-113">Backendpools доступно для правила маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="9c686-113">Backendpools available to routing rule.</span></span>

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

### <a name="-defaultprofile"></a><span data-ttu-id="9c686-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c686-114">-DefaultProfile</span></span>
<span data-ttu-id="9c686-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9c686-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <a name="-enabledstate"></a><span data-ttu-id="9c686-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="9c686-116">-EnabledState</span></span>
<span data-ttu-id="9c686-117">Состояние EnabledState для подсистемы балансировки нагрузки передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="9c686-117">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="9c686-118">Значение по умолчанию — Enabled</span><span class="sxs-lookup"><span data-stu-id="9c686-118">Default value is Enabled</span></span>

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

### <a name="-frontendendpoint"></a><span data-ttu-id="9c686-119">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="9c686-119">-FrontendEndpoint</span></span>
<span data-ttu-id="9c686-120">Конечные точки переднего плана, доступные для правила маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="9c686-120">Frontend endpoints available to routing rule.</span></span>

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

### <a name="-healthprobesetting"></a><span data-ttu-id="9c686-121">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="9c686-121">-HealthProbeSetting</span></span>
<span data-ttu-id="9c686-122">Параметры проверки работоспособности, связанные с этим экземпляром передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="9c686-122">Health probe settings associated with this Front Door instance.</span></span>

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

### <a name="-loadbalancingsetting"></a><span data-ttu-id="9c686-123">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="9c686-123">-LoadBalancingSetting</span></span>
<span data-ttu-id="9c686-124">Параметры балансировки нагрузки, связанные с этим экземпляром передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="9c686-124">Load balancing settings associated with this Front Door instance.</span></span>

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

### <a name="-name"></a><span data-ttu-id="9c686-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9c686-125">-Name</span></span>
<span data-ttu-id="9c686-126">Имя передней дверцы.</span><span class="sxs-lookup"><span data-stu-id="9c686-126">Front Door name.</span></span>

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

### <a name="-resourcegroupname"></a><span data-ttu-id="9c686-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c686-127">-ResourceGroupName</span></span>
<span data-ttu-id="9c686-128">Имя группы ресурсов, в которой будет создана Передняя дверца.</span><span class="sxs-lookup"><span data-stu-id="9c686-128">The resource group name that the Front Door will be created in.</span></span>

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

### <a name="-routingrule"></a><span data-ttu-id="9c686-129">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="9c686-129">-RoutingRule</span></span>
<span data-ttu-id="9c686-130">Правила маршрутизации, связанные с этим FrontDoor</span><span class="sxs-lookup"><span data-stu-id="9c686-130">Routing rules associated with this FrontDoor</span></span>

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

### <a name="-tag"></a><span data-ttu-id="9c686-131">-Тег</span><span class="sxs-lookup"><span data-stu-id="9c686-131">-Tag</span></span>
<span data-ttu-id="9c686-132">Теги сопоставлены с FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="9c686-132">The tags associate with the FrontDoor.</span></span>

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

### <a name="-confirm"></a><span data-ttu-id="9c686-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c686-133">-Confirm</span></span>
<span data-ttu-id="9c686-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9c686-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <a name="-whatif"></a><span data-ttu-id="9c686-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c686-135">-WhatIf</span></span>
<span data-ttu-id="9c686-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9c686-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c686-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9c686-137">The cmdlet is not run.</span></span>

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

### <a name="commonparameters"></a><span data-ttu-id="9c686-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c686-138">CommonParameters</span></span>
<span data-ttu-id="9c686-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9c686-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c686-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c686-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <a name="inputs"></a><span data-ttu-id="9c686-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9c686-141">INPUTS</span></span>

### <a name="systemstring"></a><span data-ttu-id="9c686-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9c686-142">System.String</span></span>

## <a name="outputs"></a><span data-ttu-id="9c686-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c686-143">OUTPUTS</span></span>

### <a name="microsoftazurecommandsfrontdoormodelspsfrontdoor"></a><span data-ttu-id="9c686-144">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="9c686-144">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <a name="notes"></a><span data-ttu-id="9c686-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="9c686-145">NOTES</span></span>

## <a name="related-links"></a><span data-ttu-id="9c686-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c686-146">RELATED LINKS</span></span>

<span data-ttu-id="9c686-147">[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md) 
 [Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md) 
 [New-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md) 
 [New-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md) 
 [New-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md) 
 [New-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md) 
 [New-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="9c686-147">[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)
[Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)
[New-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md)
[New-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md)
[New-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md)
[New-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md)
[New-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span></span>
