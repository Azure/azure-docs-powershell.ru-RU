---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: f769eb91d524bc9115199127833471246f6fdd1f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224073"
---
# <span data-ttu-id="e20f0-101">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="e20f0-101">Add-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="e20f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e20f0-102">SYNOPSIS</span></span>
<span data-ttu-id="e20f0-103">Добавляет http-прослушивание к шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="e20f0-103">Adds an HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="e20f0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e20f0-104">SYNTAX</span></span>

### <span data-ttu-id="e20f0-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e20f0-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-SslProfileId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e20f0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e20f0-106">SetByResource</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-SslProfile <PSApplicationGatewaySslProfile>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e20f0-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e20f0-107">DESCRIPTION</span></span>
<span data-ttu-id="e20f0-108">С **помощью cmdlet Add-AzApplicationGatewayHttpListener** можно добавить http-прослушивание к шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="e20f0-108">The **Add-AzApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="e20f0-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e20f0-109">EXAMPLES</span></span>

### <span data-ttu-id="e20f0-110">Пример 1. Добавление http-прослушивание</span><span class="sxs-lookup"><span data-stu-id="e20f0-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="e20f0-111">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw. Вторая команда добавляет http-прослушивание к шлюзу приложения.</span><span class="sxs-lookup"><span data-stu-id="e20f0-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="e20f0-112">Пример 2. Добавление прослушивание HTTPS с помощью SSL</span><span class="sxs-lookup"><span data-stu-id="e20f0-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="e20f0-113">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e20f0-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e20f0-114">Вторая команда добавляет в шлюз приложения слушателя, который использует протокол HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e20f0-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

### <span data-ttu-id="e20f0-115">Пример 3. Добавление прослушки HTTPS с помощью SSL и HostNames</span><span class="sxs-lookup"><span data-stu-id="e20f0-115">Example 3: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com","www.microsoft.com"
```

<span data-ttu-id="e20f0-116">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e20f0-116">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e20f0-117">Вторая команда добавляет в шлюз приложения пользователя, который использует протокол HTTPS с SSL-сертификатами и именами хост-кодов.</span><span class="sxs-lookup"><span data-stu-id="e20f0-117">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="e20f0-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e20f0-118">PARAMETERS</span></span>

### <span data-ttu-id="e20f0-119">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e20f0-119">-ApplicationGateway</span></span>
<span data-ttu-id="e20f0-120">Указывает шлюз приложения, к которому этот cmdlet добавляет http-прослушивание.</span><span class="sxs-lookup"><span data-stu-id="e20f0-120">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="e20f0-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="e20f0-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="e20f0-122">Ошибка клиента шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="e20f0-122">Customer error of an application gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e20f0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e20f0-123">-DefaultProfile</span></span>
<span data-ttu-id="e20f0-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e20f0-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e20f0-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="e20f0-125">-FirewallPolicy</span></span>
<span data-ttu-id="e20f0-126">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="e20f0-126">FirewallPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e20f0-127">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="e20f0-127">-FirewallPolicyId</span></span>
<span data-ttu-id="e20f0-128">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="e20f0-128">FirewallPolicyId</span></span>

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

### <span data-ttu-id="e20f0-129">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e20f0-129">-FrontendIPConfiguration</span></span>
<span data-ttu-id="e20f0-130">Определяет объект переднего IP-ресурса шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="e20f0-130">Specifies the application gateway front-end IP resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e20f0-131">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e20f0-131">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="e20f0-132">Указывает IP-адрес переднего IP-адреса шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="e20f0-132">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="e20f0-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="e20f0-133">-FrontendPort</span></span>
<span data-ttu-id="e20f0-134">Определяет объект переднего порта шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="e20f0-134">Specifies the application gateway front-end port object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e20f0-135">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="e20f0-135">-FrontendPortId</span></span>
<span data-ttu-id="e20f0-136">Определяет стойкий порт шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="e20f0-136">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="e20f0-137">-HostName</span><span class="sxs-lookup"><span data-stu-id="e20f0-137">-HostName</span></span>
<span data-ttu-id="e20f0-138">Указывает имя хоста, к имени которого этот cmdlet добавляет http-прослушивание.</span><span class="sxs-lookup"><span data-stu-id="e20f0-138">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e20f0-139">-HostNames</span><span class="sxs-lookup"><span data-stu-id="e20f0-139">-HostNames</span></span>
<span data-ttu-id="e20f0-140">Host names (Имена хостов)</span><span class="sxs-lookup"><span data-stu-id="e20f0-140">Host names</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e20f0-141">-Name</span><span class="sxs-lookup"><span data-stu-id="e20f0-141">-Name</span></span>
<span data-ttu-id="e20f0-142">Указывает имя переднего порта, который добавляет эта команда.</span><span class="sxs-lookup"><span data-stu-id="e20f0-142">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="e20f0-143">-Protocol</span><span class="sxs-lookup"><span data-stu-id="e20f0-143">-Protocol</span></span>
<span data-ttu-id="e20f0-144">Определяет протокол http-прослушивание.</span><span class="sxs-lookup"><span data-stu-id="e20f0-144">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="e20f0-145">Поддерживаются протоколы HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e20f0-145">Both HTTP and HTTPS are supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e20f0-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="e20f0-146">-RequireServerNameIndication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e20f0-147">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="e20f0-147">-SslCertificate</span></span>
<span data-ttu-id="e20f0-148">Указывает SSL-сертификат для http-прослушивание.</span><span class="sxs-lookup"><span data-stu-id="e20f0-148">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="e20f0-149">Должен быть указан, является ли ПРОТОКОЛ HTTPS протоколом прослушиванием.</span><span class="sxs-lookup"><span data-stu-id="e20f0-149">Must be specified if HTTPS is chosen as listener protocol.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e20f0-150">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="e20f0-150">-SslCertificateId</span></span>
<span data-ttu-id="e20f0-151">Определяет ИД SSL-сертификата для прослушки HTTP- или SSL-сертификата.</span><span class="sxs-lookup"><span data-stu-id="e20f0-151">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="e20f0-152">Должен быть указан, является ли ПРОТОКОЛ HTTPS протоколом прослушиванием.</span><span class="sxs-lookup"><span data-stu-id="e20f0-152">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="e20f0-153">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="e20f0-153">-SslProfile</span></span>
<span data-ttu-id="e20f0-154">SslProfile</span><span class="sxs-lookup"><span data-stu-id="e20f0-154">SslProfile</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e20f0-155">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="e20f0-155">-SslProfileId</span></span>
<span data-ttu-id="e20f0-156">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="e20f0-156">SslProfileId</span></span>

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

### <span data-ttu-id="e20f0-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e20f0-157">CommonParameters</span></span>
<span data-ttu-id="e20f0-158">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e20f0-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e20f0-159">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e20f0-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e20f0-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e20f0-160">INPUTS</span></span>

### <span data-ttu-id="e20f0-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e20f0-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e20f0-162">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e20f0-162">OUTPUTS</span></span>

### <span data-ttu-id="e20f0-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e20f0-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e20f0-164">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e20f0-164">NOTES</span></span>

## <span data-ttu-id="e20f0-165">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e20f0-165">RELATED LINKS</span></span>

[<span data-ttu-id="e20f0-166">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="e20f0-166">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="e20f0-167">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="e20f0-167">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="e20f0-168">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="e20f0-168">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="e20f0-169">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="e20f0-169">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


