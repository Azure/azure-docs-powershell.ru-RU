---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorRoutingRuleObject.md
ms.openlocfilehash: c03a76943857e3615269a9584a3975ae6ab86666
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566453"
---
# <span data-ttu-id="b08d6-101">New-AzureRmFrontDoorRoutingRuleObject</span><span class="sxs-lookup"><span data-stu-id="b08d6-101">New-AzureRmFrontDoorRoutingRuleObject</span></span>

## <span data-ttu-id="b08d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b08d6-102">SYNOPSIS</span></span>
<span data-ttu-id="b08d6-103">Создание PSRoutingRuleObject для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="b08d6-103">Create a PSRoutingRuleObject for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b08d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b08d6-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <PSForwardingProtocol>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <PSQueryParameterStripDirective>]
 [-DynamicCompression <PSEnabledState>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b08d6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b08d6-105">DESCRIPTION</span></span>
<span data-ttu-id="b08d6-106">Создание PSRoutingRuleObject для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="b08d6-106">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="b08d6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b08d6-107">EXAMPLES</span></span>

### <span data-ttu-id="b08d6-108">Пример 1: создание PSRoutingRuleObject для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="b08d6-108">Example 1: Create a PSRoutingRuleObject for Front Door creation</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName  -FrontendEndpointName "frontendEndpoint1" -BackendPoolName "backendPool1" 

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
ForwardingProtocol           : MatchRequest
CustomForwardingPath         :
QueryParameterStripDirective : StripAll
DynamicCompression           : Enabled
HealthProbeSettings          :
BackendPoolId                : /subscriptions/{subid}/resourceGroups/{rgname}/prov
                               iders/Microsoft.Network/frontDoors/{frontdoorname}/BackendPools/backendPool1
EnableCaching                : Disabled
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : routingrule1
Type                         :
```

<span data-ttu-id="b08d6-109">Создание PSRoutingRuleObject для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="b08d6-109">Create a PSRoutingRuleObject for Front Door creation</span></span>

## <span data-ttu-id="b08d6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b08d6-110">PARAMETERS</span></span>

### <span data-ttu-id="b08d6-111">-AcceptedProtocol</span><span class="sxs-lookup"><span data-stu-id="b08d6-111">-AcceptedProtocol</span></span>
<span data-ttu-id="b08d6-112">Схемы протоколов для сопоставления с этим правилом.</span><span class="sxs-lookup"><span data-stu-id="b08d6-112">Protocol schemes to match for this rule.</span></span>
<span data-ttu-id="b08d6-113">Значение по умолчанию: {HTTPS, http}</span><span class="sxs-lookup"><span data-stu-id="b08d6-113">Default value is {Https, Http}</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocol[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b08d6-114">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="b08d6-114">-BackendPoolName</span></span>
<span data-ttu-id="b08d6-115">Идентификатор ресурса для BackendPool, к которому это правило адресуется</span><span class="sxs-lookup"><span data-stu-id="b08d6-115">Resource id of the BackendPool which this rule routes to</span></span>

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

### <span data-ttu-id="b08d6-116">-CustomForwardingPath</span><span class="sxs-lookup"><span data-stu-id="b08d6-116">-CustomForwardingPath</span></span>
<span data-ttu-id="b08d6-117">Настраиваемый путь, используемый для перезаписи путей к ресурсам, подходящих для этого правила.</span><span class="sxs-lookup"><span data-stu-id="b08d6-117">The custom path used to rewrite resource paths matched by this rule.</span></span>
<span data-ttu-id="b08d6-118">Оставьте поле пустым, чтобы использовать входящий путь.</span><span class="sxs-lookup"><span data-stu-id="b08d6-118">Leave empty to use incoming path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b08d6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b08d6-119">-DefaultProfile</span></span>
<span data-ttu-id="b08d6-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b08d6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b08d6-121">-DynamicCompression</span><span class="sxs-lookup"><span data-stu-id="b08d6-121">-DynamicCompression</span></span>
<span data-ttu-id="b08d6-122">Следует ли включить динамическое сжатие для кэшированного содержимого, если включено кэширование.</span><span class="sxs-lookup"><span data-stu-id="b08d6-122">Whether to enable dynamic compression for cached content when caching is enabled.</span></span>
<span data-ttu-id="b08d6-123">Значение по умолчанию — Enabled</span><span class="sxs-lookup"><span data-stu-id="b08d6-123">Default value is Enabled</span></span>

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

### <span data-ttu-id="b08d6-124">-EnableCaching</span><span class="sxs-lookup"><span data-stu-id="b08d6-124">-EnableCaching</span></span>
<span data-ttu-id="b08d6-125">Следует ли включить кэширование для этого маршрута.</span><span class="sxs-lookup"><span data-stu-id="b08d6-125">Whether to enable caching for this route.</span></span> <span data-ttu-id="b08d6-126">Значение по умолчанию: ложь</span><span class="sxs-lookup"><span data-stu-id="b08d6-126">Default value is false</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b08d6-127">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="b08d6-127">-EnabledState</span></span>
<span data-ttu-id="b08d6-128">Следует ли включить использование этого правила.</span><span class="sxs-lookup"><span data-stu-id="b08d6-128">Whether to enable use of this rule.</span></span>
<span data-ttu-id="b08d6-129">Значение по умолчанию — Enabled</span><span class="sxs-lookup"><span data-stu-id="b08d6-129">Default value is Enabled</span></span>

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

### <span data-ttu-id="b08d6-130">-ForwardingProtocol</span><span class="sxs-lookup"><span data-stu-id="b08d6-130">-ForwardingProtocol</span></span>
<span data-ttu-id="b08d6-131">Протокол, который будет использоваться этим правилом при пересылке трафика по умолчанию, имеет значение MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="b08d6-131">The protocol this rule will use when forwarding traffic to backends Default value is MatchRequest.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingProtocol
Parameter Sets: (All)
Aliases:
Accepted values: HttpOnly, HttpsOnly, MatchRequest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b08d6-132">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="b08d6-132">-FrontDoorName</span></span>
<span data-ttu-id="b08d6-133">Имя передней дверцы, к которой относится данное правило маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="b08d6-133">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="b08d6-134">-FrontendEndpointName</span><span class="sxs-lookup"><span data-stu-id="b08d6-134">-FrontendEndpointName</span></span>
<span data-ttu-id="b08d6-135">Имена конечных точек с интерфейсом, связанных с этим правилом</span><span class="sxs-lookup"><span data-stu-id="b08d6-135">The names of Frontend endpoints associated with this rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b08d6-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b08d6-136">-Name</span></span>
<span data-ttu-id="b08d6-137">RoutingRule имя.</span><span class="sxs-lookup"><span data-stu-id="b08d6-137">RoutingRule name.</span></span>

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

### <span data-ttu-id="b08d6-138">-PatternToMatch</span><span class="sxs-lookup"><span data-stu-id="b08d6-138">-PatternToMatch</span></span>
<span data-ttu-id="b08d6-139">В шаблонах маршрутов правила не должно быть каких-либо знаков \* за исключением случаев, когда это возможно после конечной точки или в конце пути.</span><span class="sxs-lookup"><span data-stu-id="b08d6-139">The route patterns of the rule,  Must not have any \* except possibly after the final / at the end of the path.</span></span> <span data-ttu-id="b08d6-140">Значение по умолчанию —/\*</span><span class="sxs-lookup"><span data-stu-id="b08d6-140">Default value is /\*</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b08d6-141">-QueryParameterStripDirective</span><span class="sxs-lookup"><span data-stu-id="b08d6-141">-QueryParameterStripDirective</span></span>
<span data-ttu-id="b08d6-142">Обработка терминов запроса URL-адреса при создании ключа кэша.</span><span class="sxs-lookup"><span data-stu-id="b08d6-142">The treatment of URL query terms when forming the cache key.</span></span>
<span data-ttu-id="b08d6-143">Значение по умолчанию — StripAll</span><span class="sxs-lookup"><span data-stu-id="b08d6-143">Default value is StripAll</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSQueryParameterStripDirective
Parameter Sets: (All)
Aliases:
Accepted values: StripNone, StripAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b08d6-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b08d6-144">-ResourceGroupName</span></span>
<span data-ttu-id="b08d6-145">Имя группы ресурсов, в которой будет создано RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="b08d6-145">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="b08d6-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b08d6-146">CommonParameters</span></span>
<span data-ttu-id="b08d6-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b08d6-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b08d6-148">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b08d6-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b08d6-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b08d6-149">INPUTS</span></span>

### <span data-ttu-id="b08d6-150">Ничего</span><span class="sxs-lookup"><span data-stu-id="b08d6-150">None</span></span>

## <span data-ttu-id="b08d6-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b08d6-151">OUTPUTS</span></span>

### <span data-ttu-id="b08d6-152">Microsoft. Azure. Commands. FrontDoor. Models. PSRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b08d6-152">Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule</span></span>

## <span data-ttu-id="b08d6-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="b08d6-153">NOTES</span></span>

## <span data-ttu-id="b08d6-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b08d6-154">RELATED LINKS</span></span>

<span data-ttu-id="b08d6-155">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="b08d6-155">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
