---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 2bc6a8eed22660d966256afbc9783e4edfc04947
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986779"
---
# <span data-ttu-id="5a332-101">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5a332-101">Add-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="5a332-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a332-102">SYNOPSIS</span></span>
<span data-ttu-id="5a332-103">Добавляет массив сопоставлений URL-путей в пул серверов серверов.</span><span class="sxs-lookup"><span data-stu-id="5a332-103">Adds an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="5a332-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5a332-104">SYNTAX</span></span>

### <span data-ttu-id="5a332-105">BackendSetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5a332-105">BackendSetByResource (Default)</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5a332-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5a332-106">BackendSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a332-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="5a332-107">RedirectSetByResource</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a332-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5a332-108">RedirectSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a332-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a332-109">DESCRIPTION</span></span>
<span data-ttu-id="5a332-110">**Cmdlet Add-AzApplicationGatewayUrlPathMapConfig** добавляет массив сопоставлений URL-путей в пул серверов.</span><span class="sxs-lookup"><span data-stu-id="5a332-110">The **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="5a332-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5a332-111">EXAMPLES</span></span>

### <span data-ttu-id="5a332-112">Пример 1. Добавление сопоставления URL-пути к шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="5a332-112">Example 1: Add an URL path mapping to an application gateway.</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $pool = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $appgw -Name "pool01"
PS C:\> $poolSettings = Get-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $appgw -Name "poolSettings01"
PS C:\> $pathRule = New-AzApplicationGatewayPathRuleConfig -Name "rule01" -Paths "/path" -BackendAddressPool $pool -BackendHttpSettings $poolSettings
PS C:\> $appgw = Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "url01" -PathRules $pathRule -DefaultBackendAddressPool $pool -DefaultBackendHttpSettings $poolSettings
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="5a332-113">Первая команда получает шлюз приложения appGwName и сохраняет его в $appgw переменной.</span><span class="sxs-lookup"><span data-stu-id="5a332-113">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="5a332-114">Вторая команда получает пул адресов для запасов и сохраняет его в $pool переменной.</span><span class="sxs-lookup"><span data-stu-id="5a332-114">The second command gets backend address pool and stores it in $pool variable.</span></span>
<span data-ttu-id="5a332-115">Третья команда возвращает параметры http и сохраняет их в $poolSettings переменной.</span><span class="sxs-lookup"><span data-stu-id="5a332-115">The third command gets backend http settings and stores it in $poolSettings variable.</span></span>
<span data-ttu-id="5a332-116">Четвертая команда создает новую конфигурацию правила пути с именем "правило01" и сохраняет ее в $pathRule переменной.</span><span class="sxs-lookup"><span data-stu-id="5a332-116">The fourth command create new path rule configuration named rule01 and stores it in $pathRule variable.</span></span>
<span data-ttu-id="5a332-117">Пятая команда добавляет конфигурацию сопоставления url-пути с именем URL01 к шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="5a332-117">The fifth command adds url path mapping configuration named url01 to the application gateway.</span></span>
<span data-ttu-id="5a332-118">Шестая команда обновляет шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="5a332-118">The sixth command updates the application gateway.</span></span>

## <span data-ttu-id="5a332-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a332-119">PARAMETERS</span></span>

### <span data-ttu-id="5a332-120">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5a332-120">-ApplicationGateway</span></span>
<span data-ttu-id="5a332-121">Указывает шлюз приложения, к которому этот cmdlet добавляет конфигурацию карты URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="5a332-121">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="5a332-122">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5a332-122">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="5a332-123">Указывает стандартный пул адресов для перенаправляемого обратного адреса на случай, если ни одно из правил, указанных в параметре *pathRules.*</span><span class="sxs-lookup"><span data-stu-id="5a332-123">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="5a332-124">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="5a332-124">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="5a332-125">Определяет стандартный ИД пула адресов для backend.</span><span class="sxs-lookup"><span data-stu-id="5a332-125">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="5a332-126">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="5a332-126">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="5a332-127">Определяет параметры HTTP по умолчанию, которые будут применяться, если ни одно из правил, указанных в *параметре pathRules.*</span><span class="sxs-lookup"><span data-stu-id="5a332-127">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="5a332-128">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="5a332-128">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="5a332-129">Определяет стандартный ИД параметров HTTP по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5a332-129">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="5a332-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a332-130">-DefaultProfile</span></span>
<span data-ttu-id="5a332-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5a332-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a332-132">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a332-132">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="5a332-133">Перенаправление RedirectConfiguration шлюза приложения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5a332-133">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="5a332-134">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5a332-134">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="5a332-135">ID of the application gateway default RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a332-135">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="5a332-136">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5a332-136">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="5a332-137">Набор правил переописи шлюза приложений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5a332-137">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="5a332-138">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="5a332-138">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="5a332-139">ID of the application gateway default rewrite rule set</span><span class="sxs-lookup"><span data-stu-id="5a332-139">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="5a332-140">-Name</span><span class="sxs-lookup"><span data-stu-id="5a332-140">-Name</span></span>
<span data-ttu-id="5a332-141">Указывает имя карты URL-адреса, которое этот cmdlet добавляет в пул серверов серверов.</span><span class="sxs-lookup"><span data-stu-id="5a332-141">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="5a332-142">-PathRules</span><span class="sxs-lookup"><span data-stu-id="5a332-142">-PathRules</span></span>
<span data-ttu-id="5a332-143">Определяет список правил пути.</span><span class="sxs-lookup"><span data-stu-id="5a332-143">Specifies a list of path rules.</span></span>
<span data-ttu-id="5a332-144">Правила пути должны порядок, они применяются в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="5a332-144">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="5a332-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a332-145">CommonParameters</span></span>
<span data-ttu-id="5a332-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a332-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a332-147">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a332-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a332-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a332-148">INPUTS</span></span>

### <span data-ttu-id="5a332-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5a332-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5a332-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5a332-150">OUTPUTS</span></span>

### <span data-ttu-id="5a332-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5a332-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5a332-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5a332-152">NOTES</span></span>

## <span data-ttu-id="5a332-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a332-153">RELATED LINKS</span></span>

[<span data-ttu-id="5a332-154">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5a332-154">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5a332-155">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5a332-155">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5a332-156">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5a332-156">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5a332-157">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5a332-157">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


