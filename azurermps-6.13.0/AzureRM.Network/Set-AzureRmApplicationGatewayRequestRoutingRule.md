---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 95e46bfc1f90f4e9760077b11f52d8020cb7f409
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568436"
---
# <span data-ttu-id="58e00-101">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="58e00-101">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="58e00-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="58e00-102">SYNOPSIS</span></span>
<span data-ttu-id="58e00-103">Изменяет правило маршрутизации запросов для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="58e00-103">Modifies a request routing rule for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58e00-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="58e00-104">SYNTAX</span></span>

### <span data-ttu-id="58e00-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="58e00-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58e00-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="58e00-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58e00-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="58e00-107">DESCRIPTION</span></span>
<span data-ttu-id="58e00-108">Командлет **Set-AzureRmApplicationGatewayRequestRoutingRule** изменяет правило маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="58e00-108">The **Set-AzureRmApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="58e00-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="58e00-109">EXAMPLES</span></span>

### <span data-ttu-id="58e00-110">Пример 1: обновление правила маршрутизации запросов</span><span class="sxs-lookup"><span data-stu-id="58e00-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="58e00-111">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="58e00-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="58e00-112">Вторая команда изменяет правило маршрутизации запросов для шлюза приложений на использование серверных настроек HTTP, заданных в переменной $Setting, HTTP-прослушивателя, заданного в переменной $Listener, и пула серверных адресов, указанный в переменной $Pool.</span><span class="sxs-lookup"><span data-stu-id="58e00-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="58e00-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="58e00-113">PARAMETERS</span></span>

### <span data-ttu-id="58e00-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="58e00-114">-ApplicationGateway</span></span>
<span data-ttu-id="58e00-115">Указывает объект шлюза приложения, с которым этот командлет связывает правило маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="58e00-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="58e00-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="58e00-116">-BackendAddressPool</span></span>
<span data-ttu-id="58e00-117">Указывает пул задних серверных адресов для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="58e00-117">Specifies the application gateway back-end address pool.</span></span>

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

### <span data-ttu-id="58e00-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="58e00-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="58e00-119">Указывает идентификатор пула для серверного конечного адреса шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="58e00-119">Specifies the application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="58e00-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="58e00-120">-BackendHttpSettings</span></span>
<span data-ttu-id="58e00-121">Задает серверные параметры HTTP для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="58e00-121">Specifies the application gateway backend HTTP settings.</span></span>

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

### <span data-ttu-id="58e00-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="58e00-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="58e00-123">Указывает идентификатор серверных параметров HTTP шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="58e00-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

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

### <span data-ttu-id="58e00-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58e00-124">-DefaultProfile</span></span>
<span data-ttu-id="58e00-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="58e00-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58e00-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="58e00-126">-HttpListener</span></span>
<span data-ttu-id="58e00-127">Указывает прослушиватель HTTP шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="58e00-127">Specifies the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="58e00-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="58e00-128">-HttpListenerId</span></span>
<span data-ttu-id="58e00-129">Указывает идентификатор прослушивателя HTTP для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="58e00-129">Specifies the application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="58e00-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="58e00-130">-Name</span></span>
<span data-ttu-id="58e00-131">Указывает имя правила маршрутизации запросов, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="58e00-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="58e00-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="58e00-132">-RedirectConfiguration</span></span>
<span data-ttu-id="58e00-133">RedirectConfiguration шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="58e00-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="58e00-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="58e00-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="58e00-135">Идентификатор RedirectConfiguration шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="58e00-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="58e00-136">-RuleType</span><span class="sxs-lookup"><span data-stu-id="58e00-136">-RuleType</span></span>
<span data-ttu-id="58e00-137">Указывает тип правила маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="58e00-137">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="58e00-138">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="58e00-138">-UrlPathMap</span></span>
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

### <span data-ttu-id="58e00-139">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="58e00-139">-UrlPathMapId</span></span>
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

### <span data-ttu-id="58e00-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58e00-140">CommonParameters</span></span>
<span data-ttu-id="58e00-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="58e00-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58e00-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58e00-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58e00-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="58e00-143">INPUTS</span></span>

### <span data-ttu-id="58e00-144">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="58e00-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="58e00-145">Параметры: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="58e00-145">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="58e00-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="58e00-146">OUTPUTS</span></span>

### <span data-ttu-id="58e00-147">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="58e00-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="58e00-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="58e00-148">NOTES</span></span>

## <span data-ttu-id="58e00-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="58e00-149">RELATED LINKS</span></span>

[<span data-ttu-id="58e00-150">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="58e00-150">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="58e00-151">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="58e00-151">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="58e00-152">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="58e00-152">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="58e00-153">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="58e00-153">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)


