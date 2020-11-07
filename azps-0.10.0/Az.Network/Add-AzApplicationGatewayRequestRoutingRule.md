---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 32695204a153d04643063f4d991b577e619edcea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910153"
---
# <span data-ttu-id="0fe4b-101">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0fe4b-101">Add-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="0fe4b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0fe4b-102">SYNOPSIS</span></span>
<span data-ttu-id="0fe4b-103">Добавляет правило маршрутизации запросов в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="0fe4b-103">Adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="0fe4b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0fe4b-104">SYNTAX</span></span>

### <span data-ttu-id="0fe4b-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0fe4b-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0fe4b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0fe4b-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0fe4b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fe4b-107">DESCRIPTION</span></span>
<span data-ttu-id="0fe4b-108">Командлет **Add-AzApplicationGatewayRequestRoutingRule** добавляет правило маршрутизации запросов в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="0fe4b-108">The **Add-AzApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="0fe4b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0fe4b-109">EXAMPLES</span></span>

### <span data-ttu-id="0fe4b-110">Пример 1: Добавление правила маршрутизации запросов к шлюзу приложений</span><span class="sxs-lookup"><span data-stu-id="0fe4b-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzureApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="0fe4b-111">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="0fe4b-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="0fe4b-112">Вторая команда добавляет правило маршрутизации запросов к шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="0fe4b-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="0fe4b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0fe4b-113">PARAMETERS</span></span>

### <span data-ttu-id="0fe4b-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0fe4b-114">-ApplicationGateway</span></span>
<span data-ttu-id="0fe4b-115">Указывает шлюз приложений, к которому этот командлет добавляет правило маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="0fe4b-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0fe4b-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0fe4b-116">-BackendAddressPool</span></span>
<span data-ttu-id="0fe4b-117">Указывает объект пула для серверного конечного адреса шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="0fe4b-117">Specifies an application gateway back-end address pool object.</span></span>

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fe4b-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="0fe4b-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="0fe4b-119">Задает серверный идентификатор пула конечных адресов для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="0fe4b-119">Specifies an application gateway back-end address pool ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fe4b-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0fe4b-120">-BackendHttpSettings</span></span>
<span data-ttu-id="0fe4b-121">Указывает объект параметров HTTP для веб-части для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="0fe4b-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fe4b-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="0fe4b-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="0fe4b-123">Указывает идентификатор HTTP-параметров для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="0fe4b-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fe4b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fe4b-124">-DefaultProfile</span></span>
<span data-ttu-id="0fe4b-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0fe4b-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fe4b-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="0fe4b-126">-HttpListener</span></span>
<span data-ttu-id="0fe4b-127">Указывает объект прослушивателя HTTP для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="0fe4b-127">Specifies application gateway HTTP listener object.</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fe4b-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="0fe4b-128">-HttpListenerId</span></span>
<span data-ttu-id="0fe4b-129">Указывает идентификатор прослушивателя HTTP для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="0fe4b-129">Specifies application gateway HTTP listener ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fe4b-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0fe4b-130">-Name</span></span>
<span data-ttu-id="0fe4b-131">Указывает имя правила маршрутизации запросов, которое добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0fe4b-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fe4b-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="0fe4b-132">-RedirectConfiguration</span></span>
<span data-ttu-id="0fe4b-133">RedirectConfiguration шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="0fe4b-133">Application gateway RedirectConfiguration</span></span>

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fe4b-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="0fe4b-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="0fe4b-135">Идентификатор RedirectConfiguration шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="0fe4b-135">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fe4b-136">-RuleType</span><span class="sxs-lookup"><span data-stu-id="0fe4b-136">-RuleType</span></span>
<span data-ttu-id="0fe4b-137">Указывает тип правила маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="0fe4b-137">Specifies the type of request routing rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fe4b-138">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="0fe4b-138">-UrlPathMap</span></span>
```yaml
Type: PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fe4b-139">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="0fe4b-139">-UrlPathMapId</span></span>
<span data-ttu-id="0fe4b-140">Указывает идентификатор URL-пути для правила маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="0fe4b-140">Specifies the URL path map ID for the routing rule.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fe4b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fe4b-141">CommonParameters</span></span>
<span data-ttu-id="0fe4b-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0fe4b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fe4b-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fe4b-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fe4b-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0fe4b-144">INPUTS</span></span>

### <span data-ttu-id="0fe4b-145">System. String</span><span class="sxs-lookup"><span data-stu-id="0fe4b-145">System.String</span></span>

## <span data-ttu-id="0fe4b-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fe4b-146">OUTPUTS</span></span>

### <span data-ttu-id="0fe4b-147">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0fe4b-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0fe4b-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="0fe4b-148">NOTES</span></span>

## <span data-ttu-id="0fe4b-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0fe4b-149">RELATED LINKS</span></span>

[<span data-ttu-id="0fe4b-150">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0fe4b-150">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="0fe4b-151">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0fe4b-151">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="0fe4b-152">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0fe4b-152">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="0fe4b-153">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0fe4b-153">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


