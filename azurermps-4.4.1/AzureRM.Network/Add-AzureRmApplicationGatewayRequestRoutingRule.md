---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: f72fb4eb80475b421ca4a893a598d8686dde64c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567587"
---
# <span data-ttu-id="ec94a-101">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ec94a-101">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="ec94a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ec94a-102">SYNOPSIS</span></span>
<span data-ttu-id="ec94a-103">Добавляет правило маршрутизации запросов в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="ec94a-103">Adds a request routing rule to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec94a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ec94a-104">SYNTAX</span></span>

### <span data-ttu-id="ec94a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ec94a-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec94a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ec94a-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec94a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec94a-107">DESCRIPTION</span></span>
<span data-ttu-id="ec94a-108">Командлет **Add-AzureRmApplicationGatewayRequestRoutingRule** добавляет правило маршрутизации запросов в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="ec94a-108">The **Add-AzureRmApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="ec94a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ec94a-109">EXAMPLES</span></span>

### <span data-ttu-id="ec94a-110">Пример 1: Добавление правила маршрутизации запросов к шлюзу приложений</span><span class="sxs-lookup"><span data-stu-id="ec94a-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzureApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="ec94a-111">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ec94a-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ec94a-112">Вторая команда добавляет правило маршрутизации запросов к шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="ec94a-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="ec94a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ec94a-113">PARAMETERS</span></span>

### <span data-ttu-id="ec94a-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ec94a-114">-ApplicationGateway</span></span>
<span data-ttu-id="ec94a-115">Указывает шлюз приложений, к которому этот командлет добавляет правило маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="ec94a-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

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

### <span data-ttu-id="ec94a-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="ec94a-116">-BackendAddressPool</span></span>
<span data-ttu-id="ec94a-117">Указывает объект пула для серверного конечного адреса шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="ec94a-117">Specifies an application gateway back-end address pool object.</span></span>

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

### <span data-ttu-id="ec94a-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="ec94a-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="ec94a-119">Задает серверный идентификатор пула конечных адресов для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="ec94a-119">Specifies an application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="ec94a-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ec94a-120">-BackendHttpSettings</span></span>
<span data-ttu-id="ec94a-121">Указывает объект параметров HTTP для веб-части для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="ec94a-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

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

### <span data-ttu-id="ec94a-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="ec94a-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="ec94a-123">Указывает идентификатор HTTP-параметров для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="ec94a-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

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

### <span data-ttu-id="ec94a-124">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="ec94a-124">-HttpListener</span></span>
<span data-ttu-id="ec94a-125">Указывает объект прослушивателя HTTP для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="ec94a-125">Specifies application gateway HTTP listener object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec94a-126">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="ec94a-126">-HttpListenerId</span></span>
<span data-ttu-id="ec94a-127">Указывает идентификатор прослушивателя HTTP для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="ec94a-127">Specifies application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="ec94a-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ec94a-128">-Name</span></span>
<span data-ttu-id="ec94a-129">Указывает имя правила маршрутизации запросов, которое добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ec94a-129">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="ec94a-130">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="ec94a-130">-RedirectConfiguration</span></span>
<span data-ttu-id="ec94a-131">RedirectConfiguration шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="ec94a-131">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="ec94a-132">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ec94a-132">-RedirectConfigurationId</span></span>
<span data-ttu-id="ec94a-133">Идентификатор RedirectConfiguration шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="ec94a-133">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="ec94a-134">-RuleType</span><span class="sxs-lookup"><span data-stu-id="ec94a-134">-RuleType</span></span>
<span data-ttu-id="ec94a-135">Указывает тип правила маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="ec94a-135">Specifies the type of request routing rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec94a-136">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="ec94a-136">-UrlPathMap</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec94a-137">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="ec94a-137">-UrlPathMapId</span></span>
<span data-ttu-id="ec94a-138">Указывает идентификатор URL-пути для правила маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="ec94a-138">Specifies the URL path map ID for the routing rule.</span></span>

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

### <span data-ttu-id="ec94a-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec94a-139">-DefaultProfile</span></span>
<span data-ttu-id="ec94a-140">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ec94a-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec94a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec94a-141">CommonParameters</span></span>
<span data-ttu-id="ec94a-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ec94a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec94a-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec94a-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec94a-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ec94a-144">INPUTS</span></span>

### <span data-ttu-id="ec94a-145">System. String</span><span class="sxs-lookup"><span data-stu-id="ec94a-145">System.String</span></span>

## <span data-ttu-id="ec94a-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec94a-146">OUTPUTS</span></span>

### <span data-ttu-id="ec94a-147">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ec94a-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ec94a-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="ec94a-148">NOTES</span></span>

## <span data-ttu-id="ec94a-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ec94a-149">RELATED LINKS</span></span>

[<span data-ttu-id="ec94a-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ec94a-150">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="ec94a-151">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ec94a-151">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="ec94a-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ec94a-152">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="ec94a-153">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ec94a-153">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


