---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 82f14ce9418566793572e2b5722d09460ab1e827
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902753"
---
# <span data-ttu-id="2288a-101">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2288a-101">New-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="2288a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2288a-102">SYNOPSIS</span></span>
<span data-ttu-id="2288a-103">Создание правила маршрутизации запросов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2288a-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="2288a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2288a-104">SYNTAX</span></span>

### <span data-ttu-id="2288a-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2288a-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-BackendHttpSettingsId <String>]
 [-HttpListenerId <String>] [-BackendAddressPoolId <String>] [-UrlPathMapId <String>]
 [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2288a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2288a-106">SetByResource</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2288a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2288a-107">DESCRIPTION</span></span>
<span data-ttu-id="2288a-108">Командлет **Add-AzApplicationGatewayRequestRoutingRule** создает правило маршрутизации запросов для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="2288a-108">**The Add-AzApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="2288a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2288a-109">EXAMPLES</span></span>

### <span data-ttu-id="2288a-110">Пример 1: Создание правила маршрутизации запросов для шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="2288a-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="2288a-111">Эта команда создает базовое правило маршрутизации запросов с именем Rule01 и сохраняет результат в переменной с именем $Rule.</span><span class="sxs-lookup"><span data-stu-id="2288a-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="2288a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2288a-112">PARAMETERS</span></span>

### <span data-ttu-id="2288a-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2288a-113">-BackendAddressPool</span></span>
<span data-ttu-id="2288a-114">Задает пул серверных адресов (объект) для создаваемого правила маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="2288a-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="2288a-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="2288a-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="2288a-116">Указывает идентификатор пула серверного адреса для правила маршрутизации запросов, которое нужно создать.</span><span class="sxs-lookup"><span data-stu-id="2288a-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="2288a-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2288a-117">-BackendHttpSettings</span></span>
<span data-ttu-id="2288a-118">Задает серверные параметры HTTP, как объект, для создаваемого правила маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="2288a-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="2288a-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="2288a-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="2288a-120">Указывает идентификатор HTTP-параметров для правила маршрутизации запросов, которое нужно создать.</span><span class="sxs-lookup"><span data-stu-id="2288a-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="2288a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2288a-121">-DefaultProfile</span></span>
<span data-ttu-id="2288a-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2288a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2288a-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="2288a-123">-HttpListener</span></span>
<span data-ttu-id="2288a-124">Задает прослушиватель HTTP для создаваемого правила маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="2288a-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="2288a-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="2288a-125">-HttpListenerId</span></span>
<span data-ttu-id="2288a-126">Задает идентификатор HTTP-прослушивателя для создаваемого правила маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="2288a-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="2288a-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2288a-127">-Name</span></span>
<span data-ttu-id="2288a-128">Указывает имя правила маршрутизации запросов, которое создает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2288a-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2288a-129">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2288a-129">-RedirectConfiguration</span></span>
<span data-ttu-id="2288a-130">RedirectConfiguration шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="2288a-130">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="2288a-131">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="2288a-131">-RedirectConfigurationId</span></span>
<span data-ttu-id="2288a-132">Идентификатор RedirectConfiguration шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="2288a-132">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="2288a-133">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2288a-133">-RewriteRuleSet</span></span>
<span data-ttu-id="2288a-134">RewriteRuleSet шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="2288a-134">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="2288a-135">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="2288a-135">-RewriteRuleSetId</span></span>
<span data-ttu-id="2288a-136">Идентификатор RewriteRuleSet шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="2288a-136">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="2288a-137">-RuleType</span><span class="sxs-lookup"><span data-stu-id="2288a-137">-RuleType</span></span>
<span data-ttu-id="2288a-138">Указывает тип правила маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="2288a-138">Specifies type of the request routing rule.</span></span>

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

### <span data-ttu-id="2288a-139">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="2288a-139">-UrlPathMap</span></span>
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

### <span data-ttu-id="2288a-140">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="2288a-140">-UrlPathMapId</span></span>
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

### <span data-ttu-id="2288a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2288a-141">CommonParameters</span></span>
<span data-ttu-id="2288a-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2288a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2288a-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2288a-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2288a-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2288a-144">INPUTS</span></span>

### <span data-ttu-id="2288a-145">Ничего</span><span class="sxs-lookup"><span data-stu-id="2288a-145">None</span></span>

## <span data-ttu-id="2288a-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2288a-146">OUTPUTS</span></span>

### <span data-ttu-id="2288a-147">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2288a-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="2288a-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="2288a-148">NOTES</span></span>

## <span data-ttu-id="2288a-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2288a-149">RELATED LINKS</span></span>

[<span data-ttu-id="2288a-150">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2288a-150">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="2288a-151">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2288a-151">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="2288a-152">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2288a-152">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="2288a-153">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2288a-153">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


