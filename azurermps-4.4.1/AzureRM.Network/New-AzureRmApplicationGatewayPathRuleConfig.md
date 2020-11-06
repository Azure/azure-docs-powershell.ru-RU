---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: bcb712e7bfe0cd619d63378cad89402828eb6d36
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568038"
---
# <span data-ttu-id="00130-101">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="00130-101">New-AzureRmApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="00130-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="00130-102">SYNOPSIS</span></span>
<span data-ttu-id="00130-103">Создает правило пути для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="00130-103">Creates an application gateway path rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00130-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="00130-104">SYNTAX</span></span>

### <span data-ttu-id="00130-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="00130-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00130-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="00130-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00130-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="00130-107">DESCRIPTION</span></span>
<span data-ttu-id="00130-108">Командлет **New-AzureRmApplicationGatewayPathRuleConfig** создает правило пути к шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="00130-108">The **New-AzureRmApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="00130-109">Правила, созданные этим командлетом, можно добавить в коллекцию параметров конфигурации карты URL-пути, а затем назначить шлюзу.</span><span class="sxs-lookup"><span data-stu-id="00130-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>

<span data-ttu-id="00130-110">Параметры конфигурации схемы пути используются в балансировке нагрузки для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="00130-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="00130-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="00130-111">EXAMPLES</span></span>

### <span data-ttu-id="00130-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="00130-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzureRmApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzureRmApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzureRmApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="00130-113">Эти команды создают новое правило для пути к шлюзу приложения, а затем используют командлет **Add-AzureRmApplicationGatewayUrlPathMapConfig** , чтобы назначить это правило для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="00130-113">These commands create a new application gateway path rule and then use the **Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="00130-114">Для этого первая команда создает ссылку на объект для шлюза ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="00130-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="00130-115">Эта ссылка на объект хранится в переменной с именем $Gateway.</span><span class="sxs-lookup"><span data-stu-id="00130-115">This object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="00130-116">Следующие две команды создают пул адресных ресурсов и объект параметров HTTP для внутренних баз данных. Эти объекты (хранящиеся в переменных $AddressPool и $HttpSettings) необходимы для создания объекта правила для пути.</span><span class="sxs-lookup"><span data-stu-id="00130-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>

<span data-ttu-id="00130-117">Четвертая команда создает объект правила пути и хранится в переменной с именем $PathRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="00130-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>

<span data-ttu-id="00130-118">Пятая команда использует **Add-AzureRmApplicationGatewayUrlPathMapConfig** , чтобы добавить параметры конфигурации и правило нового пути, содержащееся в этих параметрах, в ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="00130-118">The fifth command uses **Add-AzureRmApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="00130-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="00130-119">PARAMETERS</span></span>

### <span data-ttu-id="00130-120">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="00130-120">-BackendAddressPool</span></span>
<span data-ttu-id="00130-121">Задает ссылку на объект для коллекции параметров пула адресных данных, которые будут добавлены в параметры конфигурации правил для путей к шлюзу.</span><span class="sxs-lookup"><span data-stu-id="00130-121">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="00130-122">Вы можете создать ссылку на объект с помощью командлета New-AzureRmApplicationGatewayBackendAddressPool и синтаксиса, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="00130-122">You can create this object reference by using the New-AzureRmApplicationGatewayBackendAddressPool cmdlet and syntax similar to this:</span></span>

`$AddressPool = New-AzureRmApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`

<span data-ttu-id="00130-123">Предыдущая команда добавляет в пул адресов два IP-адреса (192.16.1.1 и 192.168.1.2).</span><span class="sxs-lookup"><span data-stu-id="00130-123">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="00130-124">Обратите внимание, что IP-адрес заключен в кавычки и отделен с помощью запятых.</span><span class="sxs-lookup"><span data-stu-id="00130-124">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>

<span data-ttu-id="00130-125">Конечную переменную, $AddressPool, можно использовать в качестве значения параметра для параметра *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="00130-125">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>

<span data-ttu-id="00130-126">Пул серверных адресов представляет IP-адреса на внутренних серверах.</span><span class="sxs-lookup"><span data-stu-id="00130-126">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="00130-127">Эти IP-адреса должны либо принадлежать к подсети виртуальной сети, либо быть общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="00130-127">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="00130-128">Если вы используете этот параметр, нельзя использовать параметр *DefaultBackendAddressPoolId* в той же команде.</span><span class="sxs-lookup"><span data-stu-id="00130-128">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

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

### <span data-ttu-id="00130-129">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="00130-129">-BackendAddressPoolId</span></span>
<span data-ttu-id="00130-130">Указывает идентификатор существующего пула серверных адресов, который можно добавить к параметрам конфигурации правила для пути шлюза.</span><span class="sxs-lookup"><span data-stu-id="00130-130">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="00130-131">Идентификаторы пула адресов можно вернуть с помощью командлета Get-AzureRmApplicationGatewayBackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="00130-131">Address pool IDs can be returned by using the Get-AzureRmApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="00130-132">После появления идентификатора вы можете использовать параметр *DefaultBackendAddressPoolId* вместо параметра *DefaultBackendAddressPool* .</span><span class="sxs-lookup"><span data-stu-id="00130-132">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="00130-133">Например:</span><span class="sxs-lookup"><span data-stu-id="00130-133">For instance:</span></span>

<span data-ttu-id="00130-134">-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"</span><span class="sxs-lookup"><span data-stu-id="00130-134">-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"</span></span>

<span data-ttu-id="00130-135">Пул серверных адресов представляет IP-адреса на внутренних серверах.</span><span class="sxs-lookup"><span data-stu-id="00130-135">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="00130-136">Эти IP-адреса должны либо принадлежать к подсети виртуальной сети, либо быть общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="00130-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="00130-137">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="00130-137">-BackendHttpSettings</span></span>
<span data-ttu-id="00130-138">Указывает ссылку на объект на коллекцию параметров внутренних HTTP-данных, которые должны быть добавлены в параметры конфигурации правила для пути к шлюзу.</span><span class="sxs-lookup"><span data-stu-id="00130-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="00130-139">Вы можете создать ссылку на объект с помощью командлета New-AzureRmApplicationGatewayBackendHttpSettings и синтаксиса, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="00130-139">You can create this object reference by using the New-AzureRmApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this:</span></span>

<span data-ttu-id="00130-140">$HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings-Name "ContosoHttpSetings"-Port 80-Protocol "http"-CookieBasedAffinity "Disabled"</span><span class="sxs-lookup"><span data-stu-id="00130-140">$HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"</span></span>

<span data-ttu-id="00130-141">Конечную переменную, $HttpSettings, можно использовать в качестве значения параметра для параметра *DefaultBackendAddressPool* :</span><span class="sxs-lookup"><span data-stu-id="00130-141">The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter:</span></span>

<span data-ttu-id="00130-142">-DefaultBackendHttpSettings $HttpSettings</span><span class="sxs-lookup"><span data-stu-id="00130-142">-DefaultBackendHttpSettings $HttpSettings</span></span>

<span data-ttu-id="00130-143">Внутренние параметры HTTP настраивают такие свойства, как порт, протокол и сходство на основе файлов cookie для пула баз данных.</span><span class="sxs-lookup"><span data-stu-id="00130-143">The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="00130-144">Если вы используете этот параметр, нельзя использовать параметр *DefaultBackendHttpSettingsId* в той же команде.</span><span class="sxs-lookup"><span data-stu-id="00130-144">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

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

### <span data-ttu-id="00130-145">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="00130-145">-BackendHttpSettingsId</span></span>
<span data-ttu-id="00130-146">Указывает идентификатор существующей коллекции параметров HTTP-сервера, которую можно добавить в параметры конфигурации правила для пути шлюза.</span><span class="sxs-lookup"><span data-stu-id="00130-146">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="00130-147">Идентификаторы параметра HTTP можно вернуть с помощью командлета Get-AzureRmApplicationGatewayBackendHttpSettings.</span><span class="sxs-lookup"><span data-stu-id="00130-147">HTTP setting IDs can be returned by using the Get-AzureRmApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="00130-148">После появления идентификатора вы можете использовать параметр *DefaultBackendHttpSettingsId* вместо параметра *DefaultBackendHttpSettings* .</span><span class="sxs-lookup"><span data-stu-id="00130-148">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="00130-149">Например:</span><span class="sxs-lookup"><span data-stu-id="00130-149">For instance:</span></span>

<span data-ttu-id="00130-150">-DefaultBackendSettings ID "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"</span><span class="sxs-lookup"><span data-stu-id="00130-150">-DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"</span></span>

<span data-ttu-id="00130-151">Внутренние параметры HTTP настраивают такие свойства, как порт, протокол и сходство на основе файлов cookie для пула баз данных.</span><span class="sxs-lookup"><span data-stu-id="00130-151">The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="00130-152">Если вы используете этот параметр, нельзя использовать параметр *DefaultBackendHttpSettings* в той же команде.</span><span class="sxs-lookup"><span data-stu-id="00130-152">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="00130-153">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="00130-153">-Name</span></span>
<span data-ttu-id="00130-154">Указывает имя конфигурации правила для пути, создаваемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="00130-154">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="00130-155">-Paths</span><span class="sxs-lookup"><span data-stu-id="00130-155">-Paths</span></span>
<span data-ttu-id="00130-156">Задает один или несколько правил пути к шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="00130-156">Specifies one or more application gateway path rules.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00130-157">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="00130-157">-RedirectConfiguration</span></span>
<span data-ttu-id="00130-158">RedirectConfiguration шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="00130-158">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="00130-159">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="00130-159">-RedirectConfigurationId</span></span>
<span data-ttu-id="00130-160">Идентификатор RedirectConfiguration шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="00130-160">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="00130-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00130-161">-DefaultProfile</span></span>
<span data-ttu-id="00130-162">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="00130-162">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00130-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00130-163">CommonParameters</span></span>
<span data-ttu-id="00130-164">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="00130-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00130-165">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00130-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00130-166">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="00130-166">INPUTS</span></span>

###  
<span data-ttu-id="00130-167">**New-AzureRmApplicationGatewayPathRuleConfig** не поддерживает конвейерные входные данные.</span><span class="sxs-lookup"><span data-stu-id="00130-167">**New-AzureRmApplicationGatewayPathRuleConfig** does not accept pipelined input.</span></span>

## <span data-ttu-id="00130-168">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="00130-168">OUTPUTS</span></span>

###  
<span data-ttu-id="00130-169">**New-AzureRmApplicationGatewayPathRuleConfig** создает новые экземпляры объекта **Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPathRule** .</span><span class="sxs-lookup"><span data-stu-id="00130-169">**New-AzureRmApplicationGatewayPathRuleConfig** creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule** object.</span></span>

## <span data-ttu-id="00130-170">Пуск</span><span class="sxs-lookup"><span data-stu-id="00130-170">NOTES</span></span>

## <span data-ttu-id="00130-171">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="00130-171">RELATED LINKS</span></span>

[<span data-ttu-id="00130-172">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="00130-172">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="00130-173">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="00130-173">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="00130-174">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="00130-174">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="00130-175">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="00130-175">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="00130-176">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="00130-176">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="00130-177">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="00130-177">New-AzureRmApplicationGatewayPathRuleConfig</span></span>](./New-AzureRmApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="00130-178">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="00130-178">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="00130-179">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="00130-179">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="00130-180">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="00130-180">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


