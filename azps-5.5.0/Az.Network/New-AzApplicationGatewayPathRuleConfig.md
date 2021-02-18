---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: c36cb832034535f13cbcb49805531c64ee906c60
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240909"
---
# <span data-ttu-id="555e0-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="555e0-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="555e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="555e0-102">SYNOPSIS</span></span>
<span data-ttu-id="555e0-103">Создает правило пути шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="555e0-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="555e0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="555e0-104">SYNTAX</span></span>

### <span data-ttu-id="555e0-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="555e0-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="555e0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="555e0-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="555e0-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="555e0-107">DESCRIPTION</span></span>
<span data-ttu-id="555e0-108">Для создания правила пути шлюза приложения создается **cmdlet New-AzApplicationGatewayPathRuleConfig.**</span><span class="sxs-lookup"><span data-stu-id="555e0-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="555e0-109">Правила, созданные этим cmdlet, можно добавить в коллекцию параметров конфигурации карты URL-адреса, а затем на назначенную шлюзу.</span><span class="sxs-lookup"><span data-stu-id="555e0-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="555e0-110">Параметры конфигурации карты пути используются для балансировки нагрузки шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="555e0-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="555e0-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="555e0-111">EXAMPLES</span></span>

### <span data-ttu-id="555e0-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="555e0-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="555e0-113">Эти команды создают новое правило пути шлюза приложения, а затем назначьте его шлюзу приложения с помощью командлета **Add-AzApplicationGatewayUrlPathConfig.**</span><span class="sxs-lookup"><span data-stu-id="555e0-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="555e0-114">Для этого первая команда создает ссылку на шлюз ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="555e0-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="555e0-115">Эта ссылка на объект хранится в переменной с именем $Gateway.</span><span class="sxs-lookup"><span data-stu-id="555e0-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="555e0-116">Следующие две команды создают пул адресов для дополнительных адресов и объект параметров HTTP. Эти объекты (которые хранятся в переменных $AddressPool и $HttpSettings) необходимы для создания объекта правила пути.</span><span class="sxs-lookup"><span data-stu-id="555e0-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="555e0-117">Четвертая команда создает объект правила пути и сохраняется в переменной с $PathRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="555e0-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="555e0-118">Пятая команда использует **Add-AzApplicationGatewayUrlPathMapConfig** для добавления параметров конфигурации и нового правила пути, содержаногося в этих параметрах, в ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="555e0-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

### <span data-ttu-id="555e0-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="555e0-119">Example 2</span></span>
```
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="555e0-120">Эта команда создает правило пути с именами "base", Paths as "/base", BackendAddressPool как $AddressPool, BackendHttpSettings как $HttpSettings и FirewallPolicy как $firewallPolicy.ngs и новым правилом пути, содержаменем ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="555e0-120">These command creates a path-rule with the Name as "base", Paths as "/base", BackendAddressPool as $AddressPool, BackendHttpSettings as $HttpSettings and FirewallPolicy as $firewallPolicy.ngs and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="555e0-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="555e0-121">PARAMETERS</span></span>

### <span data-ttu-id="555e0-122">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="555e0-122">-BackendAddressPool</span></span>
<span data-ttu-id="555e0-123">Указывает ссылку на коллекцию параметров пула адресов для дополнительных адресов, которые будут добавлены в параметры конфигурации правил путей шлюза.</span><span class="sxs-lookup"><span data-stu-id="555e0-123">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="555e0-124">Эту ссылку на объект можно создать с помощью New-AzApplicationGatewayBackendAddressPool и синтаксиса, аналогичных этой: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="555e0-124">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="555e0-125">При предыдущей команде в пул адресов добавляется два IP-адреса (192.16.1.1 и 192.168.1.2).</span><span class="sxs-lookup"><span data-stu-id="555e0-125">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="555e0-126">Обратите внимание, что IP-адрес заключен в кавычках и разделен запятой.</span><span class="sxs-lookup"><span data-stu-id="555e0-126">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="555e0-127">Итоговую переменную ($AddressPool) можно использовать в качестве значения параметра для параметра *DefaultBackendAddressPool.*</span><span class="sxs-lookup"><span data-stu-id="555e0-127">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="555e0-128">Пул серверных адресов представляет IP-адреса серверов.</span><span class="sxs-lookup"><span data-stu-id="555e0-128">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="555e0-129">Эти IP-адреса должны принадлежать виртуальной подсети сети или должны быть общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="555e0-129">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="555e0-130">Этот параметр нельзя использовать в одной команде с параметром *DefaultBackendAddressPoolId.*</span><span class="sxs-lookup"><span data-stu-id="555e0-130">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

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

### <span data-ttu-id="555e0-131">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="555e0-131">-BackendAddressPoolId</span></span>
<span data-ttu-id="555e0-132">Определяет ИД существующего пула адресов для дополнительных адресов, который можно добавить в параметры конфигурации пути шлюза.</span><span class="sxs-lookup"><span data-stu-id="555e0-132">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="555e0-133">Коды пула адресов можно вернуть с помощью Get-AzApplicationGatewayBackendAddressPool-адресов.</span><span class="sxs-lookup"><span data-stu-id="555e0-133">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="555e0-134">После этого можно использовать параметр *DefaultBackendAddressPoolId* вместо параметра *DefaultBackendAddressPool.*</span><span class="sxs-lookup"><span data-stu-id="555e0-134">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="555e0-135">Например: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups /appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" Пул адресов серверов представляет IP-адреса серверов.</span><span class="sxs-lookup"><span data-stu-id="555e0-135">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="555e0-136">Эти IP-адреса должны принадлежать виртуальной подсети сети или должны быть общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="555e0-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="555e0-137">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="555e0-137">-BackendHttpSettings</span></span>
<span data-ttu-id="555e0-138">Указывает ссылку на коллекцию дополнительных параметров HTTP, которые будут добавлены в параметры конфигурации пути шлюза.</span><span class="sxs-lookup"><span data-stu-id="555e0-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="555e0-139">Эту ссылку на объект можно создать с помощью New-AzApplicationGatewayBackendHttpSettings и синтаксиса $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings затем можно использовать в качестве значения параметра *DefaultBackendAddressPool:* -DefaultBackendHttpSettings $HttpSettings Параметры HTTP-файлов настраивают свойства, такие как порт, протокол и связь на основе cookie, для пула backend.</span><span class="sxs-lookup"><span data-stu-id="555e0-139">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="555e0-140">Если вы используете этот параметр, нельзя использовать параметр *DefaultBackendHttpSettingsId* в одной команде.</span><span class="sxs-lookup"><span data-stu-id="555e0-140">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

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

### <span data-ttu-id="555e0-141">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="555e0-141">-BackendHttpSettingsId</span></span>
<span data-ttu-id="555e0-142">Определяет ИД существующего коллекции параметров HTTP-адреса, который можно добавить в параметры конфигурации пути шлюза.</span><span class="sxs-lookup"><span data-stu-id="555e0-142">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="555e0-143">Коды параметров HTTP можно вернуть с помощью Get-AzApplicationGatewayBackendHttpSettings..</span><span class="sxs-lookup"><span data-stu-id="555e0-143">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="555e0-144">После этого можно использовать параметр *DefaultBackendHttpSettingsId* вместо *параметра DefaultBackendHttpSettings.*</span><span class="sxs-lookup"><span data-stu-id="555e0-144">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="555e0-145">Например: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, и бесконечность на основе файлов cookie для пула backend.</span><span class="sxs-lookup"><span data-stu-id="555e0-145">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="555e0-146">Если вы используете этот параметр, нельзя использовать параметр *DefaultBackendHttpSettings в* одной команде.</span><span class="sxs-lookup"><span data-stu-id="555e0-146">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="555e0-147">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="555e0-147">-FirewallPolicy</span></span>
<span data-ttu-id="555e0-148">Указывает ссылку на объект в политике брандмауэра верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="555e0-148">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="555e0-149">Ссылку на объект можно создать с помощью New-AzApplicationGatewayWebApplicationFirewallPolicy-управления.</span><span class="sxs-lookup"><span data-stu-id="555e0-149">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="555e0-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" Политика брандмауэра, созданная с помощью командлета выше, может быть передана на уровне пути.</span><span class="sxs-lookup"><span data-stu-id="555e0-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="555e0-151">Над командой, над командой, он создает параметры политики по умолчанию и управляемые правила.</span><span class="sxs-lookup"><span data-stu-id="555e0-151">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="555e0-152">Вместо стандартных значений пользователи могут указывать PolicySettings и ManagedRules New-AzApplicationGatewayFirewallPolicySettings и New-AzApplicationGatewayFirewallPolicyManagedRules соответственно.</span><span class="sxs-lookup"><span data-stu-id="555e0-152">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="555e0-153">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="555e0-153">-FirewallPolicyId</span></span>
<span data-ttu-id="555e0-154">Определяет ИД существующего ресурса брандмауэра веб-приложения верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="555e0-154">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="555e0-155">Коды политики брандмауэра можно вернуть с помощью Get-AzApplicationGatewayWebApplicationFirewallPolicy управления.</span><span class="sxs-lookup"><span data-stu-id="555e0-155">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="555e0-156">После того как у нас есть ИД, вы можете использовать параметр *FirewallPolicyId* вместо *параметра FirewallPolicy.*</span><span class="sxs-lookup"><span data-stu-id="555e0-156">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="555e0-157">Например: -FirewallPolicyId "/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName> "</span><span class="sxs-lookup"><span data-stu-id="555e0-157">For instance: -FirewallPolicyId  "/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>"</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="555e0-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="555e0-158">-DefaultProfile</span></span>
<span data-ttu-id="555e0-159">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="555e0-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="555e0-160">-Name</span><span class="sxs-lookup"><span data-stu-id="555e0-160">-Name</span></span>
<span data-ttu-id="555e0-161">Указывает имя конфигурации правила пути, которую создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="555e0-161">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="555e0-162">-Paths</span><span class="sxs-lookup"><span data-stu-id="555e0-162">-Paths</span></span>
<span data-ttu-id="555e0-163">Определяет одно или несколько правил пути шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="555e0-163">Specifies one or more application gateway path rules.</span></span>

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

### <span data-ttu-id="555e0-164">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="555e0-164">-RedirectConfiguration</span></span>
<span data-ttu-id="555e0-165">RedirectConfiguration шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="555e0-165">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="555e0-166">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="555e0-166">-RedirectConfigurationId</span></span>
<span data-ttu-id="555e0-167">ID of the application gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="555e0-167">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="555e0-168">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="555e0-168">-RewriteRuleSet</span></span>
<span data-ttu-id="555e0-169">RewriteRuleSet шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="555e0-169">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="555e0-170">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="555e0-170">-RewriteRuleSetId</span></span>
<span data-ttu-id="555e0-171">ИД шлюза приложения RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="555e0-171">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="555e0-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="555e0-172">CommonParameters</span></span>
<span data-ttu-id="555e0-173">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="555e0-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="555e0-174">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="555e0-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="555e0-175">INPUTS</span><span class="sxs-lookup"><span data-stu-id="555e0-175">INPUTS</span></span>

### <span data-ttu-id="555e0-176">Нет</span><span class="sxs-lookup"><span data-stu-id="555e0-176">None</span></span>

## <span data-ttu-id="555e0-177">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="555e0-177">OUTPUTS</span></span>

### <span data-ttu-id="555e0-178">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span><span class="sxs-lookup"><span data-stu-id="555e0-178">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="555e0-179">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="555e0-179">NOTES</span></span>

## <span data-ttu-id="555e0-180">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="555e0-180">RELATED LINKS</span></span>

[<span data-ttu-id="555e0-181">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="555e0-181">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="555e0-182">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="555e0-182">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="555e0-183">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="555e0-183">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="555e0-184">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="555e0-184">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="555e0-185">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="555e0-185">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="555e0-186">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="555e0-186">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="555e0-187">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="555e0-187">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="555e0-188">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="555e0-188">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="555e0-189">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="555e0-189">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


