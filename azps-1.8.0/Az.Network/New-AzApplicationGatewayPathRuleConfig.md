---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: 94fbc1e9a4ae8b7befe6961a9648174770458583
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400218"
---
# <span data-ttu-id="da4fd-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="da4fd-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="da4fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da4fd-102">SYNOPSIS</span></span>
<span data-ttu-id="da4fd-103">Создает правило пути шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="da4fd-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="da4fd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="da4fd-104">SYNTAX</span></span>

### <span data-ttu-id="da4fd-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="da4fd-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da4fd-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="da4fd-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da4fd-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da4fd-107">DESCRIPTION</span></span>
<span data-ttu-id="da4fd-108">Для создания правила пути шлюза приложения создается **cmdlet New-AzApplicationGatewayPathRuleConfig.**</span><span class="sxs-lookup"><span data-stu-id="da4fd-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="da4fd-109">Правила, созданные этим cmdlet, можно добавить в коллекцию параметров конфигурации карты URL-адреса, а затем на назначенную шлюзу.</span><span class="sxs-lookup"><span data-stu-id="da4fd-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="da4fd-110">Параметры конфигурации карты пути используются для балансировки нагрузки шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="da4fd-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="da4fd-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="da4fd-111">EXAMPLES</span></span>

### <span data-ttu-id="da4fd-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="da4fd-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="da4fd-113">Эти команды создают новое правило пути шлюза приложения, а затем назначьте его шлюзу приложения с помощью командлета **Add-AzApplicationGatewayUrlPathConfig.**</span><span class="sxs-lookup"><span data-stu-id="da4fd-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="da4fd-114">Для этого первая команда создает ссылку на шлюз ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="da4fd-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="da4fd-115">Эта ссылка на объект хранится в переменной с именем $Gateway.</span><span class="sxs-lookup"><span data-stu-id="da4fd-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="da4fd-116">Следующие две команды создают пул адресов для дополнительных адресов и объект параметров HTTP. Эти объекты (которые хранятся в переменных $AddressPool и $HttpSettings) необходимы для создания объекта правила пути.</span><span class="sxs-lookup"><span data-stu-id="da4fd-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="da4fd-117">Четвертая команда создает объект правила пути и сохраняется в переменной с $PathRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="da4fd-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="da4fd-118">Пятая команда использует **Add-AzApplicationGatewayUrlPathMapConfig** для добавления параметров конфигурации и нового правила пути, содержаногося в этих параметрах, в ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="da4fd-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="da4fd-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da4fd-119">PARAMETERS</span></span>

### <span data-ttu-id="da4fd-120">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="da4fd-120">-BackendAddressPool</span></span>
<span data-ttu-id="da4fd-121">Указывает ссылку на коллекцию параметров пула адресов для дополнительных адресов, которые будут добавлены в параметры конфигурации правил путей шлюза.</span><span class="sxs-lookup"><span data-stu-id="da4fd-121">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="da4fd-122">Эту ссылку на объект можно создать с помощью New-AzApplicationGatewayBackendAddressPool и синтаксиса, аналогичных этой: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="da4fd-122">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="da4fd-123">При предыдущей команде в пул адресов добавляется два IP-адреса (192.16.1.1 и 192.168.1.2).</span><span class="sxs-lookup"><span data-stu-id="da4fd-123">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="da4fd-124">Обратите внимание, что IP-адрес заключен в кавычках и разделен запятой.</span><span class="sxs-lookup"><span data-stu-id="da4fd-124">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="da4fd-125">Итоговую переменную ($AddressPool) можно использовать в качестве значения параметра для параметра *DefaultBackendAddressPool.*</span><span class="sxs-lookup"><span data-stu-id="da4fd-125">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="da4fd-126">Пул серверных адресов представляет IP-адреса серверов.</span><span class="sxs-lookup"><span data-stu-id="da4fd-126">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="da4fd-127">Эти IP-адреса должны принадлежать виртуальной подсети сети или должны быть общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="da4fd-127">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="da4fd-128">Этот параметр нельзя использовать в одной команде с параметром *DefaultBackendAddressPoolId.*</span><span class="sxs-lookup"><span data-stu-id="da4fd-128">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da4fd-129">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="da4fd-129">-BackendAddressPoolId</span></span>
<span data-ttu-id="da4fd-130">Определяет ИД существующего пула адресов для дополнительных адресов, который можно добавить в параметры конфигурации пути шлюза.</span><span class="sxs-lookup"><span data-stu-id="da4fd-130">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="da4fd-131">Коды пула адресов можно вернуть с помощью Get-AzApplicationGatewayBackendAddressPool-адресов.</span><span class="sxs-lookup"><span data-stu-id="da4fd-131">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="da4fd-132">После этого можно использовать параметр *DefaultBackendAddressPoolId* вместо параметра *DefaultBackendAddressPool.*</span><span class="sxs-lookup"><span data-stu-id="da4fd-132">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="da4fd-133">Например: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups /appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" Пул адресов серверов представляет IP-адреса серверов.</span><span class="sxs-lookup"><span data-stu-id="da4fd-133">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="da4fd-134">Эти IP-адреса должны принадлежать виртуальной подсети сети или должны быть общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="da4fd-134">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da4fd-135">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="da4fd-135">-BackendHttpSettings</span></span>
<span data-ttu-id="da4fd-136">Указывает ссылку на коллекцию дополнительных параметров HTTP, которые будут добавлены в параметры конфигурации пути шлюза.</span><span class="sxs-lookup"><span data-stu-id="da4fd-136">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="da4fd-137">Эту ссылку на объект можно создать с помощью New-AzApplicationGatewayBackendHttpSettings и синтаксиса, аналогичных этой: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, можно использовать параметр DefaultBackendAddressPool в качестве значения параметра *DefaultBackendAddressPool:* -DefaultBackendHttpSettings $HttpSettings Параметры HTTP-файлов настраивают свойства, такие как порт, протокол и на основе cookie, для пула backend.</span><span class="sxs-lookup"><span data-stu-id="da4fd-137">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="da4fd-138">Если вы используете этот параметр, нельзя использовать параметр *DefaultBackendHttpSettingsId* в одной команде.</span><span class="sxs-lookup"><span data-stu-id="da4fd-138">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da4fd-139">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="da4fd-139">-BackendHttpSettingsId</span></span>
<span data-ttu-id="da4fd-140">Определяет ИД существующего коллекции параметров HTTP-адреса, который можно добавить в параметры конфигурации пути шлюза.</span><span class="sxs-lookup"><span data-stu-id="da4fd-140">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="da4fd-141">Коды параметров HTTP можно вернуть с помощью Get-AzApplicationGatewayBackendHttpSettings..</span><span class="sxs-lookup"><span data-stu-id="da4fd-141">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="da4fd-142">После этого можно использовать параметр *DefaultBackendHttpSettingsId* вместо *параметра DefaultBackendHttpSettings.*</span><span class="sxs-lookup"><span data-stu-id="da4fd-142">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="da4fd-143">Например: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, и бесконечность на основе файлов cookie для пула backend.</span><span class="sxs-lookup"><span data-stu-id="da4fd-143">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="da4fd-144">Если вы используете этот параметр, нельзя использовать параметр *DefaultBackendHttpSettings в* одной команде.</span><span class="sxs-lookup"><span data-stu-id="da4fd-144">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da4fd-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da4fd-145">-DefaultProfile</span></span>
<span data-ttu-id="da4fd-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="da4fd-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da4fd-147">-Name</span><span class="sxs-lookup"><span data-stu-id="da4fd-147">-Name</span></span>
<span data-ttu-id="da4fd-148">Указывает имя конфигурации правила пути, которую создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da4fd-148">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="da4fd-149">-Paths</span><span class="sxs-lookup"><span data-stu-id="da4fd-149">-Paths</span></span>
<span data-ttu-id="da4fd-150">Определяет одно или несколько правил пути шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="da4fd-150">Specifies one or more application gateway path rules.</span></span>

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

### <span data-ttu-id="da4fd-151">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="da4fd-151">-RedirectConfiguration</span></span>
<span data-ttu-id="da4fd-152">RedirectConfiguration шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="da4fd-152">Application gateway RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da4fd-153">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="da4fd-153">-RedirectConfigurationId</span></span>
<span data-ttu-id="da4fd-154">ID of the application gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="da4fd-154">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da4fd-155">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="da4fd-155">-RewriteRuleSet</span></span>
<span data-ttu-id="da4fd-156">RewriteRuleSet шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="da4fd-156">Application gateway RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da4fd-157">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="da4fd-157">-RewriteRuleSetId</span></span>
<span data-ttu-id="da4fd-158">ИД шлюза приложения RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="da4fd-158">ID of the application gateway RewriteRuleSet</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da4fd-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da4fd-159">CommonParameters</span></span>
<span data-ttu-id="da4fd-160">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da4fd-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da4fd-161">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da4fd-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da4fd-162">INPUTS</span><span class="sxs-lookup"><span data-stu-id="da4fd-162">INPUTS</span></span>

### <span data-ttu-id="da4fd-163">Нет</span><span class="sxs-lookup"><span data-stu-id="da4fd-163">None</span></span>

## <span data-ttu-id="da4fd-164">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="da4fd-164">OUTPUTS</span></span>

### <span data-ttu-id="da4fd-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span><span class="sxs-lookup"><span data-stu-id="da4fd-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="da4fd-166">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="da4fd-166">NOTES</span></span>

## <span data-ttu-id="da4fd-167">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da4fd-167">RELATED LINKS</span></span>

[<span data-ttu-id="da4fd-168">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="da4fd-168">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="da4fd-169">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="da4fd-169">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="da4fd-170">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="da4fd-170">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="da4fd-171">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="da4fd-171">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)


[<span data-ttu-id="da4fd-172">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="da4fd-172">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="da4fd-173">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="da4fd-173">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="da4fd-174">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="da4fd-174">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="da4fd-175">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="da4fd-175">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


