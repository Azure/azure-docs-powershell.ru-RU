---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ec2eede30b6aef81210582b95b775200c8145943
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518005"
---
# <span data-ttu-id="2665d-101">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2665d-101">Set-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="2665d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2665d-102">SYNOPSIS</span></span>
<span data-ttu-id="2665d-103">Задает конфигурацию для массива сопоставлений URL-путей с пулом серверов серверов.</span><span class="sxs-lookup"><span data-stu-id="2665d-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="2665d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2665d-104">SYNTAX</span></span>

### <span data-ttu-id="2665d-105">BackendSetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2665d-105">BackendSetByResource (Default)</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2665d-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2665d-106">BackendSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2665d-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="2665d-107">RedirectSetByResource</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2665d-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2665d-108">RedirectSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2665d-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2665d-109">DESCRIPTION</span></span>
<span data-ttu-id="2665d-110">Для массива сопоставлений URL-путей с пулом серверов серверов устанавливается конфигурация **set-AzApplicationGatewayUrlPathMapConfig.**</span><span class="sxs-lookup"><span data-stu-id="2665d-110">The **Set-AzApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="2665d-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2665d-111">EXAMPLES</span></span>

### <span data-ttu-id="2665d-112">Пример 1. Обновление сопоставления URL-пути</span><span class="sxs-lookup"><span data-stu-id="2665d-112">Example 1: Update an URL path mapping</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="2665d-113">Первая команда получает шлюз приложения appGwName и сохраняет результат в переменной $appgw.</span><span class="sxs-lookup"><span data-stu-id="2665d-113">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="2665d-114">Вторая команда обновляет сопоставление URL-пути с именем map01 в шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="2665d-114">The second command updates the URL path mapping named map01 in the application gateway.</span></span>
<span data-ttu-id="2665d-115">Третья команда обновляет шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="2665d-115">The third command updates the application gateway.</span></span>

## <span data-ttu-id="2665d-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2665d-116">PARAMETERS</span></span>

### <span data-ttu-id="2665d-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2665d-117">-ApplicationGateway</span></span>
<span data-ttu-id="2665d-118">Указывает шлюз приложения, для которого этот cmdlet задает конфигурацию карты URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="2665d-118">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2665d-119">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2665d-119">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="2665d-120">Определяет пул адресов для маршрутируемого по умолчанию, если ни одно из правил, указанных в параметре *pathRules.*</span><span class="sxs-lookup"><span data-stu-id="2665d-120">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2665d-121">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="2665d-121">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="2665d-122">Определяет стандартный ИД пула адресов для backend.</span><span class="sxs-lookup"><span data-stu-id="2665d-122">Specifies the default backend address pool ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2665d-123">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2665d-123">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="2665d-124">Определяет параметры HTTP по умолчанию, которые будут применяться, если ни одно из правил, указанных в *параметре pathRules.*</span><span class="sxs-lookup"><span data-stu-id="2665d-124">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2665d-125">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="2665d-125">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="2665d-126">Определяет стандартный ИД параметров HTTP по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2665d-126">Specifies the default backend HTTP settings ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2665d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2665d-127">-DefaultProfile</span></span>
<span data-ttu-id="2665d-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2665d-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2665d-129">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2665d-129">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="2665d-130">ПеренаправлениеConfiguration шлюза приложения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2665d-130">Application gateway default RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: RedirectSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2665d-131">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="2665d-131">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="2665d-132">ID of the application gateway default RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2665d-132">ID of the application gateway default RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: RedirectSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2665d-133">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2665d-133">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="2665d-134">Набор правил переописи шлюза приложений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2665d-134">Application gateway default rewrite rule set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: BackendSetByResource, RedirectSetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2665d-135">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="2665d-135">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="2665d-136">ID of the application gateway default rewrite rule set</span><span class="sxs-lookup"><span data-stu-id="2665d-136">ID of the application gateway default rewrite rule set</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId, RedirectSetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2665d-137">-Name</span><span class="sxs-lookup"><span data-stu-id="2665d-137">-Name</span></span>
<span data-ttu-id="2665d-138">Указывает имя карты URL-адреса, для которой этот cmdlet задает конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="2665d-138">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="2665d-139">-PathRules</span><span class="sxs-lookup"><span data-stu-id="2665d-139">-PathRules</span></span>
<span data-ttu-id="2665d-140">Определяет список правил пути.</span><span class="sxs-lookup"><span data-stu-id="2665d-140">Specifies a list of path rules.</span></span>
<span data-ttu-id="2665d-141">Обратите внимание на то, что правила пути в порядке с конфиденциальной порядок они применяются в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="2665d-141">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2665d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2665d-142">CommonParameters</span></span>
<span data-ttu-id="2665d-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2665d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2665d-144">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2665d-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2665d-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2665d-145">INPUTS</span></span>

### <span data-ttu-id="2665d-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2665d-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2665d-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2665d-147">OUTPUTS</span></span>

### <span data-ttu-id="2665d-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2665d-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2665d-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2665d-149">NOTES</span></span>

## <span data-ttu-id="2665d-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2665d-150">RELATED LINKS</span></span>

[<span data-ttu-id="2665d-151">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2665d-151">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2665d-152">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2665d-152">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2665d-153">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2665d-153">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2665d-154">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2665d-154">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)


