---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 7808b663b53cc33309a3de5f705eca798c297acc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396540"
---
# <span data-ttu-id="a35ee-101">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a35ee-101">Add-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="a35ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a35ee-102">SYNOPSIS</span></span>
<span data-ttu-id="a35ee-103">Добавляет массив сопоставлений URL-путей в пул серверов серверов.</span><span class="sxs-lookup"><span data-stu-id="a35ee-103">Adds an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="a35ee-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a35ee-104">SYNTAX</span></span>

### <span data-ttu-id="a35ee-105">BackendSetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a35ee-105">BackendSetByResource (Default)</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a35ee-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a35ee-106">BackendSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a35ee-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="a35ee-107">RedirectSetByResource</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a35ee-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a35ee-108">RedirectSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a35ee-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a35ee-109">DESCRIPTION</span></span>
<span data-ttu-id="a35ee-110">**Cmdlet Add-AzApplicationGatewayUrlPathMapConfig** добавляет массив сопоставлений URL-путей в пул серверов.</span><span class="sxs-lookup"><span data-stu-id="a35ee-110">The **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="a35ee-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a35ee-111">EXAMPLES</span></span>

### <span data-ttu-id="a35ee-112">Пример 1. Добавление сопоставления URL-пути к шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="a35ee-112">Example 1: Add an URL path mapping to an application gateway.</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $pool = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $appgw -Name "pool01"
PS C:\> $poolSettings = Get-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $appgw -Name "poolSettings01"
PS C:\> $pathRule = New-AzApplicationGatewayPathRuleConfig -Name "rule01" -Paths "/path" -BackendAddressPool $pool -BackendHttpSettings $poolSettings
PS C:\> $appgw = Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "url01" -PathRules $pathRule -DefaultBackendAddressPool $pool -DefaultBackendHttpSettings $poolSettings
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="a35ee-113">Первая команда получает шлюз приложения appGwName и сохраняет его в $appgw переменной.</span><span class="sxs-lookup"><span data-stu-id="a35ee-113">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="a35ee-114">Вторая команда получает пул адресов для запасов и сохраняет его в $pool переменной.</span><span class="sxs-lookup"><span data-stu-id="a35ee-114">The second command gets backend address pool and stores it in $pool variable.</span></span>
<span data-ttu-id="a35ee-115">Третья команда возвращает параметры http и сохраняет его в переменной $poolSettings http.</span><span class="sxs-lookup"><span data-stu-id="a35ee-115">The third command gets backend http settings and stores it in $poolSettings variable.</span></span>
<span data-ttu-id="a35ee-116">Четвертая команда создает новую конфигурацию правила пути с именем "правило01" и сохраняет ее в $pathRule переменной.</span><span class="sxs-lookup"><span data-stu-id="a35ee-116">The fourth command create new path rule configuration named rule01 and stores it in $pathRule variable.</span></span>
<span data-ttu-id="a35ee-117">Пятая команда добавляет конфигурацию сопоставления url-пути с именем URL01 к шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="a35ee-117">The fifth command adds url path mapping configuration named url01 to the application gateway.</span></span>
<span data-ttu-id="a35ee-118">Шестая команда обновляет шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="a35ee-118">The sixth command updates the application gateway.</span></span>

## <span data-ttu-id="a35ee-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a35ee-119">PARAMETERS</span></span>

### <span data-ttu-id="a35ee-120">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a35ee-120">-ApplicationGateway</span></span>
<span data-ttu-id="a35ee-121">Указывает шлюз приложения, к которому этот cmdlet добавляет конфигурацию карты URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="a35ee-121">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="a35ee-122">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a35ee-122">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="a35ee-123">Определяет пул адресов для маршрутов по умолчанию на случай, если ни одно из правил, указанных в параметре *pathRules.*</span><span class="sxs-lookup"><span data-stu-id="a35ee-123">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="a35ee-124">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a35ee-124">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="a35ee-125">Определяет стандартный ИД пула адресов для backend.</span><span class="sxs-lookup"><span data-stu-id="a35ee-125">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="a35ee-126">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="a35ee-126">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="a35ee-127">Определяет параметры HTTP по умолчанию, которые будут применяться, если ни одно из правил, указанных в параметре *pathRules.*</span><span class="sxs-lookup"><span data-stu-id="a35ee-127">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="a35ee-128">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="a35ee-128">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="a35ee-129">Определяет стандартный ИД параметров HTTP по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a35ee-129">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="a35ee-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a35ee-130">-DefaultProfile</span></span>
<span data-ttu-id="a35ee-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a35ee-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a35ee-132">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="a35ee-132">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="a35ee-133">ПеренаправлениеConfiguration шлюза приложения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a35ee-133">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="a35ee-134">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a35ee-134">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="a35ee-135">ID of the application gateway default RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="a35ee-135">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="a35ee-136">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a35ee-136">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="a35ee-137">Набор правил переописи шлюза приложений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a35ee-137">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="a35ee-138">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="a35ee-138">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="a35ee-139">ID of the application gateway default rewrite rule set</span><span class="sxs-lookup"><span data-stu-id="a35ee-139">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="a35ee-140">-Name</span><span class="sxs-lookup"><span data-stu-id="a35ee-140">-Name</span></span>
<span data-ttu-id="a35ee-141">Указывает имя карты URL-адреса, которое этот cmdlet добавляет в пул серверов серверов.</span><span class="sxs-lookup"><span data-stu-id="a35ee-141">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="a35ee-142">-PathRules</span><span class="sxs-lookup"><span data-stu-id="a35ee-142">-PathRules</span></span>
<span data-ttu-id="a35ee-143">Определяет список правил пути.</span><span class="sxs-lookup"><span data-stu-id="a35ee-143">Specifies a list of path rules.</span></span>
<span data-ttu-id="a35ee-144">Правила пути должны порядок, они применяются в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="a35ee-144">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="a35ee-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a35ee-145">CommonParameters</span></span>
<span data-ttu-id="a35ee-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a35ee-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a35ee-147">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a35ee-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a35ee-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a35ee-148">INPUTS</span></span>

### <span data-ttu-id="a35ee-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a35ee-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a35ee-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a35ee-150">OUTPUTS</span></span>

### <span data-ttu-id="a35ee-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a35ee-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a35ee-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a35ee-152">NOTES</span></span>

## <span data-ttu-id="a35ee-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a35ee-153">RELATED LINKS</span></span>

[<span data-ttu-id="a35ee-154">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a35ee-154">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="a35ee-155">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a35ee-155">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="a35ee-156">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a35ee-156">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="a35ee-157">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a35ee-157">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


