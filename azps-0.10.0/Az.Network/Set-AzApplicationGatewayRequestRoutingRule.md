---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: c2c212d3cf80044ce7c81d9d4ebd318f6a1e93ad
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911065"
---
# <span data-ttu-id="e9bcd-101">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e9bcd-101">Set-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="e9bcd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e9bcd-102">SYNOPSIS</span></span>
<span data-ttu-id="e9bcd-103">Изменяет правило маршрутизации запросов для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="e9bcd-103">Modifies a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="e9bcd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e9bcd-104">SYNTAX</span></span>

### <span data-ttu-id="e9bcd-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e9bcd-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9bcd-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e9bcd-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9bcd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9bcd-107">DESCRIPTION</span></span>
<span data-ttu-id="e9bcd-108">Командлет **Set-AzApplicationGatewayRequestRoutingRule** изменяет правило маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="e9bcd-108">The **Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="e9bcd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e9bcd-109">EXAMPLES</span></span>

### <span data-ttu-id="e9bcd-110">Пример 1: обновление правила маршрутизации запросов</span><span class="sxs-lookup"><span data-stu-id="e9bcd-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="e9bcd-111">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e9bcd-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="e9bcd-112">Вторая команда изменяет правило маршрутизации запросов для шлюза приложений на использование серверных настроек HTTP, заданных в переменной $Setting, HTTP-прослушивателя, заданного в переменной $Listener, и пула серверных адресов, указанный в переменной $Pool.</span><span class="sxs-lookup"><span data-stu-id="e9bcd-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="e9bcd-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e9bcd-113">PARAMETERS</span></span>

### <span data-ttu-id="e9bcd-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e9bcd-114">-ApplicationGateway</span></span>
<span data-ttu-id="e9bcd-115">Указывает объект шлюза приложения, с которым этот командлет связывает правило маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="e9bcd-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="e9bcd-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e9bcd-116">-BackendAddressPool</span></span>
<span data-ttu-id="e9bcd-117">Указывает пул задних серверных адресов для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="e9bcd-117">Specifies the application gateway back-end address pool.</span></span>

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

### <span data-ttu-id="e9bcd-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="e9bcd-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="e9bcd-119">Указывает идентификатор пула для серверного конечного адреса шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="e9bcd-119">Specifies the application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="e9bcd-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e9bcd-120">-BackendHttpSettings</span></span>
<span data-ttu-id="e9bcd-121">Задает серверные параметры HTTP для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="e9bcd-121">Specifies the application gateway backend HTTP settings.</span></span>

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

### <span data-ttu-id="e9bcd-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="e9bcd-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="e9bcd-123">Указывает идентификатор серверных параметров HTTP шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="e9bcd-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

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

### <span data-ttu-id="e9bcd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9bcd-124">-DefaultProfile</span></span>
<span data-ttu-id="e9bcd-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e9bcd-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9bcd-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="e9bcd-126">-HttpListener</span></span>
<span data-ttu-id="e9bcd-127">Указывает прослушиватель HTTP шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="e9bcd-127">Specifies the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="e9bcd-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="e9bcd-128">-HttpListenerId</span></span>
<span data-ttu-id="e9bcd-129">Указывает идентификатор прослушивателя HTTP для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="e9bcd-129">Specifies the application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="e9bcd-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e9bcd-130">-Name</span></span>
<span data-ttu-id="e9bcd-131">Указывает имя правила маршрутизации запросов, которое изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e9bcd-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e9bcd-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9bcd-132">-RedirectConfiguration</span></span>
<span data-ttu-id="e9bcd-133">RedirectConfiguration шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="e9bcd-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="e9bcd-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e9bcd-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="e9bcd-135">Идентификатор RedirectConfiguration шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="e9bcd-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="e9bcd-136">-RuleType</span><span class="sxs-lookup"><span data-stu-id="e9bcd-136">-RuleType</span></span>
<span data-ttu-id="e9bcd-137">Указывает тип правила маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="e9bcd-137">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="e9bcd-138">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="e9bcd-138">-UrlPathMap</span></span>
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

### <span data-ttu-id="e9bcd-139">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="e9bcd-139">-UrlPathMapId</span></span>
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

### <span data-ttu-id="e9bcd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9bcd-140">CommonParameters</span></span>
<span data-ttu-id="e9bcd-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e9bcd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9bcd-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9bcd-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9bcd-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e9bcd-143">INPUTS</span></span>

### <span data-ttu-id="e9bcd-144">System. String</span><span class="sxs-lookup"><span data-stu-id="e9bcd-144">System.String</span></span>

## <span data-ttu-id="e9bcd-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9bcd-145">OUTPUTS</span></span>

### <span data-ttu-id="e9bcd-146">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e9bcd-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e9bcd-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="e9bcd-147">NOTES</span></span>

## <span data-ttu-id="e9bcd-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e9bcd-148">RELATED LINKS</span></span>

[<span data-ttu-id="e9bcd-149">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e9bcd-149">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e9bcd-150">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e9bcd-150">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e9bcd-151">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e9bcd-151">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="e9bcd-152">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="e9bcd-152">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)


