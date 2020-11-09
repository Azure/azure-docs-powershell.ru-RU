---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 8fc8f6785e9b6eda55615fb1e2ececbaf9ab0349
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244870"
---
# <span data-ttu-id="b7cd2-101">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b7cd2-101">New-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="b7cd2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b7cd2-102">SYNOPSIS</span></span>
<span data-ttu-id="b7cd2-103">Создание правила маршрутизации запросов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="b7cd2-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="b7cd2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b7cd2-104">SYNTAX</span></span>

### <span data-ttu-id="b7cd2-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b7cd2-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-BackendHttpSettingsId <String>]
 [-HttpListenerId <String>] [-BackendAddressPoolId <String>] [-UrlPathMapId <String>]
 [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b7cd2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b7cd2-106">SetByResource</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7cd2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7cd2-107">DESCRIPTION</span></span>
<span data-ttu-id="b7cd2-108">Командлет **Add-AzApplicationGatewayRequestRoutingRule** создает правило маршрутизации запросов для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="b7cd2-108">**The Add-AzApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="b7cd2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b7cd2-109">EXAMPLES</span></span>

### <span data-ttu-id="b7cd2-110">Пример 1: Создание правила маршрутизации запросов для шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="b7cd2-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="b7cd2-111">Эта команда создает базовое правило маршрутизации запросов с именем Rule01 и сохраняет результат в переменной с именем $Rule.</span><span class="sxs-lookup"><span data-stu-id="b7cd2-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="b7cd2-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b7cd2-112">PARAMETERS</span></span>

### <span data-ttu-id="b7cd2-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b7cd2-113">-BackendAddressPool</span></span>
<span data-ttu-id="b7cd2-114">Задает пул серверных адресов (объект) для создаваемого правила маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="b7cd2-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="b7cd2-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="b7cd2-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="b7cd2-116">Указывает идентификатор пула серверного адреса для правила маршрутизации запросов, которое нужно создать.</span><span class="sxs-lookup"><span data-stu-id="b7cd2-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="b7cd2-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b7cd2-117">-BackendHttpSettings</span></span>
<span data-ttu-id="b7cd2-118">Задает серверные параметры HTTP, как объект, для создаваемого правила маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="b7cd2-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="b7cd2-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="b7cd2-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="b7cd2-120">Указывает идентификатор HTTP-параметров для правила маршрутизации запросов, которое нужно создать.</span><span class="sxs-lookup"><span data-stu-id="b7cd2-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="b7cd2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7cd2-121">-DefaultProfile</span></span>
<span data-ttu-id="b7cd2-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b7cd2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7cd2-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="b7cd2-123">-HttpListener</span></span>
<span data-ttu-id="b7cd2-124">Задает прослушиватель HTTP для создаваемого правила маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="b7cd2-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="b7cd2-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="b7cd2-125">-HttpListenerId</span></span>
<span data-ttu-id="b7cd2-126">Задает идентификатор HTTP-прослушивателя для создаваемого правила маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="b7cd2-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="b7cd2-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b7cd2-127">-Name</span></span>
<span data-ttu-id="b7cd2-128">Указывает имя правила маршрутизации запросов, которое создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b7cd2-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b7cd2-129">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7cd2-129">-RedirectConfiguration</span></span>
<span data-ttu-id="b7cd2-130">RedirectConfiguration шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="b7cd2-130">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="b7cd2-131">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b7cd2-131">-RedirectConfigurationId</span></span>
<span data-ttu-id="b7cd2-132">Идентификатор RedirectConfiguration шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="b7cd2-132">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="b7cd2-133">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="b7cd2-133">-RewriteRuleSet</span></span>
<span data-ttu-id="b7cd2-134">RewriteRuleSet шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="b7cd2-134">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="b7cd2-135">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="b7cd2-135">-RewriteRuleSetId</span></span>
<span data-ttu-id="b7cd2-136">Идентификатор RewriteRuleSet шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="b7cd2-136">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="b7cd2-137">-RuleType</span><span class="sxs-lookup"><span data-stu-id="b7cd2-137">-RuleType</span></span>
<span data-ttu-id="b7cd2-138">Указывает тип правила маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="b7cd2-138">Specifies type of the request routing rule.</span></span>

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

### <span data-ttu-id="b7cd2-139">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="b7cd2-139">-UrlPathMap</span></span>
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

### <span data-ttu-id="b7cd2-140">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="b7cd2-140">-UrlPathMapId</span></span>
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

### <span data-ttu-id="b7cd2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7cd2-141">CommonParameters</span></span>
<span data-ttu-id="b7cd2-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b7cd2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7cd2-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7cd2-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7cd2-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b7cd2-144">INPUTS</span></span>

### <span data-ttu-id="b7cd2-145">Ничего</span><span class="sxs-lookup"><span data-stu-id="b7cd2-145">None</span></span>

## <span data-ttu-id="b7cd2-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7cd2-146">OUTPUTS</span></span>

### <span data-ttu-id="b7cd2-147">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b7cd2-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="b7cd2-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="b7cd2-148">NOTES</span></span>

## <span data-ttu-id="b7cd2-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7cd2-149">RELATED LINKS</span></span>

[<span data-ttu-id="b7cd2-150">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b7cd2-150">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="b7cd2-151">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b7cd2-151">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="b7cd2-152">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b7cd2-152">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="b7cd2-153">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="b7cd2-153">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)

