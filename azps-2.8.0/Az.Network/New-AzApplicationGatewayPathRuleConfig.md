---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: 82940003bbd40cfb15d1f109fbdd1b820d6bd647
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902765"
---
# <span data-ttu-id="2a906-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2a906-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="2a906-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2a906-102">SYNOPSIS</span></span>
<span data-ttu-id="2a906-103">Создает правило пути для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="2a906-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="2a906-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2a906-104">SYNTAX</span></span>

### <span data-ttu-id="2a906-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2a906-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a906-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2a906-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a906-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a906-107">DESCRIPTION</span></span>
<span data-ttu-id="2a906-108">Командлет **New-AzApplicationGatewayPathRuleConfig** создает правило пути к шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="2a906-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="2a906-109">Правила, созданные этим командлетом, можно добавить в коллекцию параметров конфигурации карты URL-пути, а затем назначить шлюзу.</span><span class="sxs-lookup"><span data-stu-id="2a906-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="2a906-110">Параметры конфигурации схемы пути используются в балансировке нагрузки для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2a906-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="2a906-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2a906-111">EXAMPLES</span></span>

### <span data-ttu-id="2a906-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2a906-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="2a906-113">Эти команды создают новое правило для пути к шлюзу приложения, а затем используют командлет **Add-AzApplicationGatewayUrlPathMapConfig** , чтобы назначить это правило для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2a906-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="2a906-114">Для этого первая команда создает ссылку на объект для шлюза ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="2a906-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="2a906-115">Эта ссылка на объект хранится в переменной с именем $Gateway.</span><span class="sxs-lookup"><span data-stu-id="2a906-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="2a906-116">Следующие две команды создают пул адресных ресурсов и объект параметров HTTP для внутренних баз данных. Эти объекты (хранящиеся в переменных $AddressPool и $HttpSettings) необходимы для создания объекта правила для пути.</span><span class="sxs-lookup"><span data-stu-id="2a906-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="2a906-117">Четвертая команда создает объект правила пути и хранится в переменной с именем $PathRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="2a906-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="2a906-118">Пятая команда использует **Add-AzApplicationGatewayUrlPathMapConfig** , чтобы добавить параметры конфигурации и правило нового пути, содержащееся в этих параметрах, в ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="2a906-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="2a906-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2a906-119">PARAMETERS</span></span>

### <span data-ttu-id="2a906-120">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2a906-120">-BackendAddressPool</span></span>
<span data-ttu-id="2a906-121">Задает ссылку на объект для коллекции параметров пула адресных данных, которые будут добавлены в параметры конфигурации правил для путей к шлюзу.</span><span class="sxs-lookup"><span data-stu-id="2a906-121">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="2a906-122">Вы можете создать ссылку на объект с помощью командлета New-AzApplicationGatewayBackendAddressPool и синтаксиса, как показано ниже. `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="2a906-122">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="2a906-123">Предыдущая команда добавляет в пул адресов два IP-адреса (192.16.1.1 и 192.168.1.2).</span><span class="sxs-lookup"><span data-stu-id="2a906-123">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="2a906-124">Обратите внимание, что IP-адрес заключен в кавычки и отделен с помощью запятых.</span><span class="sxs-lookup"><span data-stu-id="2a906-124">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="2a906-125">Конечную переменную, $AddressPool, можно использовать в качестве значения параметра для параметра *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="2a906-125">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="2a906-126">Пул серверных адресов представляет IP-адреса на внутренних серверах.</span><span class="sxs-lookup"><span data-stu-id="2a906-126">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="2a906-127">Эти IP-адреса должны либо принадлежать к подсети виртуальной сети, либо быть общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="2a906-127">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="2a906-128">Если вы используете этот параметр, нельзя использовать параметр *DefaultBackendAddressPoolId* в той же команде.</span><span class="sxs-lookup"><span data-stu-id="2a906-128">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

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

### <span data-ttu-id="2a906-129">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="2a906-129">-BackendAddressPoolId</span></span>
<span data-ttu-id="2a906-130">Указывает идентификатор существующего пула серверных адресов, который можно добавить к параметрам конфигурации правила для пути шлюза.</span><span class="sxs-lookup"><span data-stu-id="2a906-130">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="2a906-131">Идентификаторы пула адресов можно вернуть с помощью командлета Get-AzApplicationGatewayBackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="2a906-131">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="2a906-132">После появления идентификатора вы можете использовать параметр *DefaultBackendAddressPoolId* вместо параметра *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="2a906-132">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="2a906-133">Например:-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" серверный пул адресных адресов представляет IP-адреса на внутренних серверах.</span><span class="sxs-lookup"><span data-stu-id="2a906-133">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="2a906-134">Эти IP-адреса должны либо принадлежать к подсети виртуальной сети, либо быть общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="2a906-134">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="2a906-135">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2a906-135">-BackendHttpSettings</span></span>
<span data-ttu-id="2a906-136">Указывает ссылку на объект на коллекцию параметров внутренних HTTP-данных, которые должны быть добавлены в параметры конфигурации правила для пути к шлюзу.</span><span class="sxs-lookup"><span data-stu-id="2a906-136">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="2a906-137">Вы можете создать ссылку на объект с помощью командлета New-AzApplicationGatewayBackendHttpSettings и синтаксиса, как показано ниже. $HttpSettings = New-AzApplicationGatewayBackendHttpSettings-Name "ContosoHttpSettings"-Port 80-Protocol "http"-CookieBasedAffinity "Disabled", то есть переменная, $HttpSettings, может использоваться в качестве значения параметра для параметра *DefaultBackendAddressPool* :-DefaultBackendHttpSettings $HttpSettings ПАРАМЕТРах HTTP-сервера можно настроить свойства, такие как порт, протокол и сходство на основе файлов cookie для пула баз данных.</span><span class="sxs-lookup"><span data-stu-id="2a906-137">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="2a906-138">Если вы используете этот параметр, нельзя использовать параметр *DefaultBackendHttpSettingsId* в той же команде.</span><span class="sxs-lookup"><span data-stu-id="2a906-138">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

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

### <span data-ttu-id="2a906-139">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="2a906-139">-BackendHttpSettingsId</span></span>
<span data-ttu-id="2a906-140">Указывает идентификатор существующей коллекции параметров HTTP-сервера, которую можно добавить в параметры конфигурации правила для пути шлюза.</span><span class="sxs-lookup"><span data-stu-id="2a906-140">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="2a906-141">Идентификаторы параметра HTTP можно вернуть с помощью командлета Get-AzApplicationGatewayBackendHttpSettings.</span><span class="sxs-lookup"><span data-stu-id="2a906-141">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="2a906-142">После появления идентификатора вы можете использовать параметр *DefaultBackendHttpSettingsId* вместо параметра *DefaultBackendHttpSettings* .</span><span class="sxs-lookup"><span data-stu-id="2a906-142">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="2a906-143">Например:-DefaultBackendSettings ID "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" Параметры HTTP-базы данных настраивают такие свойства, как порт, протокол и сходство на основе файлов cookie для пула баз данных.</span><span class="sxs-lookup"><span data-stu-id="2a906-143">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="2a906-144">Если вы используете этот параметр, нельзя использовать параметр *DefaultBackendHttpSettings* в той же команде.</span><span class="sxs-lookup"><span data-stu-id="2a906-144">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="2a906-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a906-145">-DefaultProfile</span></span>
<span data-ttu-id="2a906-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a906-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a906-147">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2a906-147">-Name</span></span>
<span data-ttu-id="2a906-148">Указывает имя конфигурации правила для пути, создаваемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="2a906-148">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2a906-149">-Paths</span><span class="sxs-lookup"><span data-stu-id="2a906-149">-Paths</span></span>
<span data-ttu-id="2a906-150">Задает один или несколько правил пути к шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="2a906-150">Specifies one or more application gateway path rules.</span></span>

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

### <span data-ttu-id="2a906-151">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2a906-151">-RedirectConfiguration</span></span>
<span data-ttu-id="2a906-152">RedirectConfiguration шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="2a906-152">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="2a906-153">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="2a906-153">-RedirectConfigurationId</span></span>
<span data-ttu-id="2a906-154">Идентификатор RedirectConfiguration шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="2a906-154">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="2a906-155">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2a906-155">-RewriteRuleSet</span></span>
<span data-ttu-id="2a906-156">RewriteRuleSet шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="2a906-156">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="2a906-157">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="2a906-157">-RewriteRuleSetId</span></span>
<span data-ttu-id="2a906-158">Идентификатор RewriteRuleSet шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="2a906-158">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="2a906-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a906-159">CommonParameters</span></span>
<span data-ttu-id="2a906-160">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2a906-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a906-161">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a906-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a906-162">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2a906-162">INPUTS</span></span>

### <span data-ttu-id="2a906-163">Ничего</span><span class="sxs-lookup"><span data-stu-id="2a906-163">None</span></span>

## <span data-ttu-id="2a906-164">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a906-164">OUTPUTS</span></span>

### <span data-ttu-id="2a906-165">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPathRule</span><span class="sxs-lookup"><span data-stu-id="2a906-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="2a906-166">Пуск</span><span class="sxs-lookup"><span data-stu-id="2a906-166">NOTES</span></span>

## <span data-ttu-id="2a906-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a906-167">RELATED LINKS</span></span>

[<span data-ttu-id="2a906-168">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2a906-168">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2a906-169">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2a906-169">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="2a906-170">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2a906-170">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2a906-171">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2a906-171">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="2a906-172">New-AzApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2a906-172">New-AzApplicationGatewayBackendHttpSettings</span></span>](./New-AzApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="2a906-173">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2a906-173">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="2a906-174">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2a906-174">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2a906-175">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2a906-175">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2a906-176">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2a906-176">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


