---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: c36cb832034535f13cbcb49805531c64ee906c60
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244877"
---
# <span data-ttu-id="4bd4a-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4bd4a-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="4bd4a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4bd4a-102">SYNOPSIS</span></span>
<span data-ttu-id="4bd4a-103">Создает правило пути для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="4bd4a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4bd4a-104">SYNTAX</span></span>

### <span data-ttu-id="4bd4a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4bd4a-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bd4a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4bd4a-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bd4a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4bd4a-107">DESCRIPTION</span></span>
<span data-ttu-id="4bd4a-108">Командлет **New-AzApplicationGatewayPathRuleConfig** создает правило пути к шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="4bd4a-109">Правила, созданные этим командлетом, можно добавить в коллекцию параметров конфигурации карты URL-пути, а затем назначить шлюзу.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="4bd4a-110">Параметры конфигурации схемы пути используются в балансировке нагрузки для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="4bd4a-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4bd4a-111">EXAMPLES</span></span>

### <span data-ttu-id="4bd4a-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4bd4a-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="4bd4a-113">Эти команды создают новое правило для пути к шлюзу приложения, а затем используют командлет **Add-AzApplicationGatewayUrlPathMapConfig** , чтобы назначить это правило для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="4bd4a-114">Для этого первая команда создает ссылку на объект для шлюза ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="4bd4a-115">Эта ссылка на объект хранится в переменной с именем $Gateway.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="4bd4a-116">Следующие две команды создают пул адресных ресурсов и объект параметров HTTP для внутренних баз данных. Эти объекты (хранящиеся в переменных $AddressPool и $HttpSettings) необходимы для создания объекта правила для пути.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="4bd4a-117">Четвертая команда создает объект правила пути и хранится в переменной с именем $PathRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="4bd4a-118">Пятая команда использует **Add-AzApplicationGatewayUrlPathMapConfig** , чтобы добавить параметры конфигурации и правило нового пути, содержащееся в этих параметрах, в ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

### <span data-ttu-id="4bd4a-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4bd4a-119">Example 2</span></span>
```
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="4bd4a-120">Эти команды создают правило пути с именем как "Base", paths AS "/Base", BackendAddressPool как $AddressPool, $HttpSettings BackendHttpSettings и $firewallPolicy FirewallPolicy. NGS и новое правило для пути, содержащееся в этих параметрах, в ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-120">These command creates a path-rule with the Name as "base", Paths as "/base", BackendAddressPool as $AddressPool, BackendHttpSettings as $HttpSettings and FirewallPolicy as $firewallPolicy.ngs and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="4bd4a-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4bd4a-121">PARAMETERS</span></span>

### <span data-ttu-id="4bd4a-122">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4bd4a-122">-BackendAddressPool</span></span>
<span data-ttu-id="4bd4a-123">Задает ссылку на объект для коллекции параметров пула адресных данных, которые будут добавлены в параметры конфигурации правил для путей к шлюзу.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-123">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="4bd4a-124">Вы можете создать ссылку на объект с помощью командлета New-AzApplicationGatewayBackendAddressPool и синтаксиса, как показано ниже. `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="4bd4a-124">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="4bd4a-125">Предыдущая команда добавляет в пул адресов два IP-адреса (192.16.1.1 и 192.168.1.2).</span><span class="sxs-lookup"><span data-stu-id="4bd4a-125">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="4bd4a-126">Обратите внимание, что IP-адрес заключен в кавычки и отделен с помощью запятых.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-126">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="4bd4a-127">Конечную переменную, $AddressPool, можно использовать в качестве значения параметра для параметра *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="4bd4a-127">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="4bd4a-128">Пул серверных адресов представляет IP-адреса на внутренних серверах.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-128">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="4bd4a-129">Эти IP-адреса должны либо принадлежать к подсети виртуальной сети, либо быть общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-129">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="4bd4a-130">Если вы используете этот параметр, нельзя использовать параметр *DefaultBackendAddressPoolId* в той же команде.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-130">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

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

### <span data-ttu-id="4bd4a-131">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="4bd4a-131">-BackendAddressPoolId</span></span>
<span data-ttu-id="4bd4a-132">Указывает идентификатор существующего пула серверных адресов, который можно добавить к параметрам конфигурации правила для пути шлюза.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-132">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="4bd4a-133">Идентификаторы пула адресов можно вернуть с помощью командлета Get-AzApplicationGatewayBackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-133">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="4bd4a-134">После появления идентификатора вы можете использовать параметр *DefaultBackendAddressPoolId* вместо параметра *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="4bd4a-134">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="4bd4a-135">Например:-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" серверный пул адресных адресов представляет IP-адреса на внутренних серверах.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-135">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="4bd4a-136">Эти IP-адреса должны либо принадлежать к подсети виртуальной сети, либо быть общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="4bd4a-137">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4bd4a-137">-BackendHttpSettings</span></span>
<span data-ttu-id="4bd4a-138">Указывает ссылку на объект на коллекцию параметров внутренних HTTP-данных, которые должны быть добавлены в параметры конфигурации правила для пути к шлюзу.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="4bd4a-139">Вы можете создать ссылку на объект с помощью командлета New-AzApplicationGatewayBackendHttpSettings и синтаксиса, как показано ниже. $HttpSettings = New-AzApplicationGatewayBackendHttpSettings-Name "ContosoHttpSettings"-Port 80-Protocol "http"-CookieBasedAffinity "Disabled", то есть переменная, $HttpSettings, может использоваться в качестве значения параметра для параметра *DefaultBackendAddressPool* :-DefaultBackendHttpSettings $HttpSettings ПАРАМЕТРах HTTP-сервера можно настроить свойства, такие как порт, протокол и сходство на основе файлов cookie для пула баз данных.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-139">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="4bd4a-140">Если вы используете этот параметр, нельзя использовать параметр *DefaultBackendHttpSettingsId* в той же команде.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-140">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

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

### <span data-ttu-id="4bd4a-141">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="4bd4a-141">-BackendHttpSettingsId</span></span>
<span data-ttu-id="4bd4a-142">Указывает идентификатор существующей коллекции параметров HTTP-сервера, которую можно добавить в параметры конфигурации правила для пути шлюза.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-142">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="4bd4a-143">Идентификаторы параметра HTTP можно вернуть с помощью командлета Get-AzApplicationGatewayBackendHttpSettings.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-143">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="4bd4a-144">После появления идентификатора вы можете использовать параметр *DefaultBackendHttpSettingsId* вместо параметра *DefaultBackendHttpSettings* .</span><span class="sxs-lookup"><span data-stu-id="4bd4a-144">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="4bd4a-145">Например:-DefaultBackendSettings ID "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" Параметры HTTP-базы данных настраивают такие свойства, как порт, протокол и сходство на основе файлов cookie для пула баз данных.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-145">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="4bd4a-146">Если вы используете этот параметр, нельзя использовать параметр *DefaultBackendHttpSettings* в той же команде.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-146">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="4bd4a-147">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="4bd4a-147">-FirewallPolicy</span></span>
<span data-ttu-id="4bd4a-148">Указывает ссылку на объект для политики брандмауэра верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-148">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="4bd4a-149">Ссылку на объект можно создать с помощью New-AzApplicationGatewayWebApplicationFirewallPolicy командлета.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-149">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="4bd4a-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy-Name "wafPolicy1"-ResourceGroup "rgName" Политика брандмауэра, созданная с помощью приведенного выше unifiedgroup, может быть указана на уровне пути и правила.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="4bd4a-151">Команда "он больше" создаст параметры политики по умолчанию и управляемые правила.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-151">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="4bd4a-152">Вместо значений по умолчанию пользователи могут задать PolicySettings, ManagedRules с помощью New-AzApplicationGatewayFirewallPolicySettings и New-AzApplicationGatewayFirewallPolicyManagedRules соответственно.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-152">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd4a-153">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="4bd4a-153">-FirewallPolicyId</span></span>
<span data-ttu-id="4bd4a-154">Указывает идентификатор существующего ресурса межсетевого экрана веб-приложения верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-154">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="4bd4a-155">Идентификаторы политик брандмауэра можно вернуть с помощью командлета Get-AzApplicationGatewayWebApplicationFirewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-155">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="4bd4a-156">После того как у нас есть идентификатор, вы можете использовать параметр *FirewallPolicyId* вместо параметра *firewallpolicy* .</span><span class="sxs-lookup"><span data-stu-id="4bd4a-156">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="4bd4a-157">Для экземпляра:-FirewallPolicyId "/Subscriptions/<Subscription-ID>/resourceGroups/<ресурсов-ID>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName> "</span><span class="sxs-lookup"><span data-stu-id="4bd4a-157">For instance: -FirewallPolicyId  "/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>"</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd4a-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bd4a-158">-DefaultProfile</span></span>
<span data-ttu-id="4bd4a-159">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bd4a-160">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4bd4a-160">-Name</span></span>
<span data-ttu-id="4bd4a-161">Указывает имя конфигурации правила для пути, создаваемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-161">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="4bd4a-162">-Paths</span><span class="sxs-lookup"><span data-stu-id="4bd4a-162">-Paths</span></span>
<span data-ttu-id="4bd4a-163">Задает один или несколько правил пути к шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-163">Specifies one or more application gateway path rules.</span></span>

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

### <span data-ttu-id="4bd4a-164">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bd4a-164">-RedirectConfiguration</span></span>
<span data-ttu-id="4bd4a-165">RedirectConfiguration шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="4bd4a-165">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="4bd4a-166">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4bd4a-166">-RedirectConfigurationId</span></span>
<span data-ttu-id="4bd4a-167">Идентификатор RedirectConfiguration шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="4bd4a-167">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="4bd4a-168">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="4bd4a-168">-RewriteRuleSet</span></span>
<span data-ttu-id="4bd4a-169">RewriteRuleSet шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="4bd4a-169">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="4bd4a-170">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="4bd4a-170">-RewriteRuleSetId</span></span>
<span data-ttu-id="4bd4a-171">Идентификатор RewriteRuleSet шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="4bd4a-171">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="4bd4a-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bd4a-172">CommonParameters</span></span>
<span data-ttu-id="4bd4a-173">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4bd4a-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bd4a-174">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bd4a-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bd4a-175">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4bd4a-175">INPUTS</span></span>

### <span data-ttu-id="4bd4a-176">Ничего</span><span class="sxs-lookup"><span data-stu-id="4bd4a-176">None</span></span>

## <span data-ttu-id="4bd4a-177">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4bd4a-177">OUTPUTS</span></span>

### <span data-ttu-id="4bd4a-178">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPathRule</span><span class="sxs-lookup"><span data-stu-id="4bd4a-178">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="4bd4a-179">Пуск</span><span class="sxs-lookup"><span data-stu-id="4bd4a-179">NOTES</span></span>

## <span data-ttu-id="4bd4a-180">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4bd4a-180">RELATED LINKS</span></span>

[<span data-ttu-id="4bd4a-181">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4bd4a-181">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4bd4a-182">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4bd4a-182">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="4bd4a-183">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4bd4a-183">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4bd4a-184">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4bd4a-184">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4bd4a-185">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="4bd4a-185">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="4bd4a-186">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4bd4a-186">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="4bd4a-187">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4bd4a-187">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4bd4a-188">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4bd4a-188">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4bd4a-189">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4bd4a-189">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


