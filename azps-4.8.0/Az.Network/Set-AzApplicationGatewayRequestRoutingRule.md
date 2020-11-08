---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 2e323170bac22950b9a6ca479e8470630741c2bc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244074"
---
# <span data-ttu-id="0c082-101">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0c082-101">Set-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="0c082-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0c082-102">SYNOPSIS</span></span>
<span data-ttu-id="0c082-103">Изменяет правило маршрутизации запросов для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="0c082-103">Modifies a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="0c082-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0c082-104">SYNTAX</span></span>

### <span data-ttu-id="0c082-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0c082-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c082-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0c082-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c082-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c082-107">DESCRIPTION</span></span>
<span data-ttu-id="0c082-108">Командлет **Set-AzApplicationGatewayRequestRoutingRule** изменяет правило маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="0c082-108">The **Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="0c082-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0c082-109">EXAMPLES</span></span>

### <span data-ttu-id="0c082-110">Пример 1: обновление правила маршрутизации запросов</span><span class="sxs-lookup"><span data-stu-id="0c082-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="0c082-111">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="0c082-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="0c082-112">Вторая команда изменяет правило маршрутизации запросов для шлюза приложений на использование серверных настроек HTTP, заданных в переменной $Setting, HTTP-прослушивателя, заданного в переменной $Listener, и пула серверных адресов, указанный в переменной $Pool.</span><span class="sxs-lookup"><span data-stu-id="0c082-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="0c082-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0c082-113">PARAMETERS</span></span>

### <span data-ttu-id="0c082-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0c082-114">-ApplicationGateway</span></span>
<span data-ttu-id="0c082-115">Указывает объект шлюза приложения, с которым этот командлет связывает правило маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="0c082-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="0c082-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0c082-116">-BackendAddressPool</span></span>
<span data-ttu-id="0c082-117">Указывает пул задних серверных адресов для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="0c082-117">Specifies the application gateway back-end address pool.</span></span>

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

### <span data-ttu-id="0c082-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="0c082-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="0c082-119">Указывает идентификатор пула для серверного конечного адреса шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="0c082-119">Specifies the application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="0c082-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0c082-120">-BackendHttpSettings</span></span>
<span data-ttu-id="0c082-121">Задает серверные параметры HTTP для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="0c082-121">Specifies the application gateway backend HTTP settings.</span></span>

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

### <span data-ttu-id="0c082-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="0c082-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="0c082-123">Указывает идентификатор серверных параметров HTTP шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="0c082-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

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

### <span data-ttu-id="0c082-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c082-124">-DefaultProfile</span></span>
<span data-ttu-id="0c082-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0c082-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c082-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="0c082-126">-HttpListener</span></span>
<span data-ttu-id="0c082-127">Указывает прослушиватель HTTP шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="0c082-127">Specifies the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="0c082-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="0c082-128">-HttpListenerId</span></span>
<span data-ttu-id="0c082-129">Указывает идентификатор прослушивателя HTTP для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="0c082-129">Specifies the application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="0c082-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0c082-130">-Name</span></span>
<span data-ttu-id="0c082-131">Указывает имя правила маршрутизации запросов, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0c082-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0c082-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="0c082-132">-RedirectConfiguration</span></span>
<span data-ttu-id="0c082-133">RedirectConfiguration шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="0c082-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="0c082-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="0c082-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="0c082-135">Идентификатор RedirectConfiguration шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="0c082-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="0c082-136">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0c082-136">-RewriteRuleSet</span></span>
<span data-ttu-id="0c082-137">RewriteRuleSet шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="0c082-137">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="0c082-138">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="0c082-138">-RewriteRuleSetId</span></span>
<span data-ttu-id="0c082-139">Идентификатор RewriteRuleSet шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="0c082-139">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="0c082-140">-RuleType</span><span class="sxs-lookup"><span data-stu-id="0c082-140">-RuleType</span></span>
<span data-ttu-id="0c082-141">Указывает тип правила маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="0c082-141">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="0c082-142">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="0c082-142">-UrlPathMap</span></span>
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

### <span data-ttu-id="0c082-143">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="0c082-143">-UrlPathMapId</span></span>
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

### <span data-ttu-id="0c082-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c082-144">CommonParameters</span></span>
<span data-ttu-id="0c082-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0c082-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c082-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c082-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c082-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0c082-147">INPUTS</span></span>

### <span data-ttu-id="0c082-148">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0c082-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0c082-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c082-149">OUTPUTS</span></span>

### <span data-ttu-id="0c082-150">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0c082-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0c082-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="0c082-151">NOTES</span></span>

## <span data-ttu-id="0c082-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c082-152">RELATED LINKS</span></span>

[<span data-ttu-id="0c082-153">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0c082-153">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="0c082-154">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0c082-154">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="0c082-155">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0c082-155">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="0c082-156">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0c082-156">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)


