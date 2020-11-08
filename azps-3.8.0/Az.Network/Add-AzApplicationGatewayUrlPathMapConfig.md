---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 7808b663b53cc33309a3de5f705eca798c297acc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065580"
---
# <span data-ttu-id="b5c5a-101">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b5c5a-101">Add-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="b5c5a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b5c5a-102">SYNOPSIS</span></span>
<span data-ttu-id="b5c5a-103">Добавляет массив сопоставлений URL-путей в пул серверов внутренней базы данных.</span><span class="sxs-lookup"><span data-stu-id="b5c5a-103">Adds an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="b5c5a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b5c5a-104">SYNTAX</span></span>

### <span data-ttu-id="b5c5a-105">BackendSetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b5c5a-105">BackendSetByResource (Default)</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5c5a-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b5c5a-106">BackendSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5c5a-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="b5c5a-107">RedirectSetByResource</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5c5a-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b5c5a-108">RedirectSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5c5a-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5c5a-109">DESCRIPTION</span></span>
<span data-ttu-id="b5c5a-110">Командлет **Add-AzApplicationGatewayUrlPathMapConfig** Добавляет массив сопоставлений URL-путей в пул серверов заднего уровня.</span><span class="sxs-lookup"><span data-stu-id="b5c5a-110">The **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="b5c5a-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b5c5a-111">EXAMPLES</span></span>

### <span data-ttu-id="b5c5a-112">Пример 1: Добавление сопоставления URL-пути на шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="b5c5a-112">Example 1: Add an URL path mapping to an application gateway.</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $pool = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $appgw -Name "pool01"
PS C:\> $poolSettings = Get-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $appgw -Name "poolSettings01"
PS C:\> $pathRule = New-AzApplicationGatewayPathRuleConfig -Name "rule01" -Paths "/path" -BackendAddressPool $pool -BackendHttpSettings $poolSettings
PS C:\> $appgw = Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "url01" -PathRules $pathRule -DefaultBackendAddressPool $pool -DefaultBackendHttpSettings $poolSettings
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="b5c5a-113">Первая команда получает шлюз приложения с именем appGwName и сохраняет его в $appgw переменной.</span><span class="sxs-lookup"><span data-stu-id="b5c5a-113">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="b5c5a-114">Вторая команда становится пулом адресных адресов и сохраняет их в $pool переменной.</span><span class="sxs-lookup"><span data-stu-id="b5c5a-114">The second command gets backend address pool and stores it in $pool variable.</span></span>
<span data-ttu-id="b5c5a-115">Третья команда получает серверные параметры HTTP и сохраняет их в $poolSettings переменной.</span><span class="sxs-lookup"><span data-stu-id="b5c5a-115">The third command gets backend http settings and stores it in $poolSettings variable.</span></span>
<span data-ttu-id="b5c5a-116">Четвертая команда создает новую конфигурацию правила для пути с именем rule01 и сохраняет ее в $pathRule переменной.</span><span class="sxs-lookup"><span data-stu-id="b5c5a-116">The fourth command create new path rule configuration named rule01 and stores it in $pathRule variable.</span></span>
<span data-ttu-id="b5c5a-117">Пятая команда добавляет конфигурацию сопоставления URL-пути с именем url01 на шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="b5c5a-117">The fifth command adds url path mapping configuration named url01 to the application gateway.</span></span>
<span data-ttu-id="b5c5a-118">Шестая команда обновляет шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="b5c5a-118">The sixth command updates the application gateway.</span></span>

## <span data-ttu-id="b5c5a-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b5c5a-119">PARAMETERS</span></span>

### <span data-ttu-id="b5c5a-120">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b5c5a-120">-ApplicationGateway</span></span>
<span data-ttu-id="b5c5a-121">Указывает шлюз приложений, с которым этот командлет добавляет конфигурацию карты URL-пути.</span><span class="sxs-lookup"><span data-stu-id="b5c5a-121">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="b5c5a-122">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b5c5a-122">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="b5c5a-123">Указывает используемый по умолчанию пул серверных адресов для маршрутизации на случай, если ни одно из правил, указанных в параметре *pathRules* , не совпадает.</span><span class="sxs-lookup"><span data-stu-id="b5c5a-123">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="b5c5a-124">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="b5c5a-124">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="b5c5a-125">Указывает идентификатор пула адресных адресов сервера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b5c5a-125">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="b5c5a-126">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b5c5a-126">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="b5c5a-127">Задает параметры HTTP по умолчанию для использования в случае, если ни одно из правил, указанных в параметре *pathRules* , не совпадает.</span><span class="sxs-lookup"><span data-stu-id="b5c5a-127">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="b5c5a-128">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="b5c5a-128">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="b5c5a-129">Указывает идентификатор HTTP-параметров по умолчанию для внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="b5c5a-129">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="b5c5a-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5c5a-130">-DefaultProfile</span></span>
<span data-ttu-id="b5c5a-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b5c5a-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5c5a-132">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="b5c5a-132">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="b5c5a-133">RedirectConfiguration для шлюза приложений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b5c5a-133">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="b5c5a-134">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b5c5a-134">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="b5c5a-135">Идентификатор RedirectConfiguration шлюза приложения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b5c5a-135">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="b5c5a-136">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b5c5a-136">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="b5c5a-137">Наборы правил перезаписи по умолчанию для шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="b5c5a-137">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="b5c5a-138">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="b5c5a-138">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="b5c5a-139">Идентификатор набора правил перезаписи по умолчанию для шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="b5c5a-139">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="b5c5a-140">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b5c5a-140">-Name</span></span>
<span data-ttu-id="b5c5a-141">Указывает имя карты URL-пути, которое этот командлет добавляет в пул внутренних серверов.</span><span class="sxs-lookup"><span data-stu-id="b5c5a-141">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="b5c5a-142">-PathRules</span><span class="sxs-lookup"><span data-stu-id="b5c5a-142">-PathRules</span></span>
<span data-ttu-id="b5c5a-143">Задает список правил пути.</span><span class="sxs-lookup"><span data-stu-id="b5c5a-143">Specifies a list of path rules.</span></span>
<span data-ttu-id="b5c5a-144">Правила путей зависят от порядка, они применяются в порядке их указания.</span><span class="sxs-lookup"><span data-stu-id="b5c5a-144">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="b5c5a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5c5a-145">CommonParameters</span></span>
<span data-ttu-id="b5c5a-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b5c5a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5c5a-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5c5a-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5c5a-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b5c5a-148">INPUTS</span></span>

### <span data-ttu-id="b5c5a-149">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b5c5a-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b5c5a-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5c5a-150">OUTPUTS</span></span>

### <span data-ttu-id="b5c5a-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b5c5a-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b5c5a-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="b5c5a-152">NOTES</span></span>

## <span data-ttu-id="b5c5a-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5c5a-153">RELATED LINKS</span></span>

[<span data-ttu-id="b5c5a-154">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b5c5a-154">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="b5c5a-155">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b5c5a-155">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="b5c5a-156">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b5c5a-156">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="b5c5a-157">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b5c5a-157">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


