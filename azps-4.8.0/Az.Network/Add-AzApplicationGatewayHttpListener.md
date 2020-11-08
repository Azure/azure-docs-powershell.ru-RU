---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: d3434a650eb09391aa7505f288667aa130401e26
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077723"
---
# <span data-ttu-id="b4f3f-101">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b4f3f-101">Add-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="b4f3f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b4f3f-102">SYNOPSIS</span></span>
<span data-ttu-id="b4f3f-103">Добавляет прослушиватель HTTP в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="b4f3f-103">Adds an HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="b4f3f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b4f3f-104">SYNTAX</span></span>

### <span data-ttu-id="b4f3f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b4f3f-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4f3f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b4f3f-106">SetByResource</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b4f3f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4f3f-107">DESCRIPTION</span></span>
<span data-ttu-id="b4f3f-108">Командлет **Add-AzApplicationGatewayHttpListener** добавляет прослушиватель HTTP в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="b4f3f-108">The **Add-AzApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="b4f3f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b4f3f-109">EXAMPLES</span></span>

### <span data-ttu-id="b4f3f-110">Пример 1: Добавление прослушивателя HTTP</span><span class="sxs-lookup"><span data-stu-id="b4f3f-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="b4f3f-111">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw. Вторая команда добавляет прослушиватель HTTP на шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="b4f3f-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="b4f3f-112">Пример 2: Добавление прослушивателя HTTPS с SSL</span><span class="sxs-lookup"><span data-stu-id="b4f3f-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="b4f3f-113">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b4f3f-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b4f3f-114">Вторая команда добавляет прослушиватель, использующий протокол HTTPS, к шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="b4f3f-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

### <span data-ttu-id="b4f3f-115">Пример 3: Добавление прослушивателя HTTPS с SSL и HostName</span><span class="sxs-lookup"><span data-stu-id="b4f3f-115">Example 3: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="b4f3f-116">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b4f3f-116">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b4f3f-117">Вторая команда добавляет прослушиватель, использующий протокол HTTPS, с SSL-сертификатами и хост-именем для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="b4f3f-117">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="b4f3f-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b4f3f-118">PARAMETERS</span></span>

### <span data-ttu-id="b4f3f-119">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4f3f-119">-ApplicationGateway</span></span>
<span data-ttu-id="b4f3f-120">Указывает шлюз приложений, к которому этот командлет добавляет прослушиватель HTTP.</span><span class="sxs-lookup"><span data-stu-id="b4f3f-120">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="b4f3f-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4f3f-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="b4f3f-122">Ошибка клиента в шлюзе приложений</span><span class="sxs-lookup"><span data-stu-id="b4f3f-122">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="b4f3f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4f3f-123">-DefaultProfile</span></span>
<span data-ttu-id="b4f3f-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b4f3f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4f3f-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b4f3f-125">-FirewallPolicy</span></span>
<span data-ttu-id="b4f3f-126">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b4f3f-126">FirewallPolicy</span></span>

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

### <span data-ttu-id="b4f3f-127">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="b4f3f-127">-FirewallPolicyId</span></span>
<span data-ttu-id="b4f3f-128">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="b4f3f-128">FirewallPolicyId</span></span>

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

### <span data-ttu-id="b4f3f-129">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4f3f-129">-FrontendIPConfiguration</span></span>
<span data-ttu-id="b4f3f-130">Указывает внешний серверный IP-ресурс шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="b4f3f-130">Specifies the application gateway front-end IP resource object.</span></span>

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

### <span data-ttu-id="b4f3f-131">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b4f3f-131">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="b4f3f-132">Указывает серверный IP-идентификатор шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="b4f3f-132">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="b4f3f-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="b4f3f-133">-FrontendPort</span></span>
<span data-ttu-id="b4f3f-134">Указывает объект внешнего порта шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="b4f3f-134">Specifies the application gateway front-end port object.</span></span>

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

### <span data-ttu-id="b4f3f-135">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="b4f3f-135">-FrontendPortId</span></span>
<span data-ttu-id="b4f3f-136">Указывает идентификатор внешнего порта шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="b4f3f-136">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="b4f3f-137">-HostName</span><span class="sxs-lookup"><span data-stu-id="b4f3f-137">-HostName</span></span>
<span data-ttu-id="b4f3f-138">Указывает имя узла, к которому этот командлет добавляет HTTP-прослушиватель.</span><span class="sxs-lookup"><span data-stu-id="b4f3f-138">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="b4f3f-139">-HostName</span><span class="sxs-lookup"><span data-stu-id="b4f3f-139">-HostNames</span></span>
<span data-ttu-id="b4f3f-140">Имена узлов</span><span class="sxs-lookup"><span data-stu-id="b4f3f-140">Host names</span></span>

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

### <span data-ttu-id="b4f3f-141">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b4f3f-141">-Name</span></span>
<span data-ttu-id="b4f3f-142">Задает имя порта переднего плана, которое добавляет эта команда.</span><span class="sxs-lookup"><span data-stu-id="b4f3f-142">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="b4f3f-143">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="b4f3f-143">-Protocol</span></span>
<span data-ttu-id="b4f3f-144">Указывает протокол для HTTP-прослушивателя.</span><span class="sxs-lookup"><span data-stu-id="b4f3f-144">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="b4f3f-145">Поддерживаются протоколы HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b4f3f-145">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="b4f3f-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="b4f3f-146">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="b4f3f-147">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="b4f3f-147">-SslCertificate</span></span>
<span data-ttu-id="b4f3f-148">Задает SSL-сертификат для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="b4f3f-148">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="b4f3f-149">Должен быть указан, если в качестве протокола прослушивателя выбран HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b4f3f-149">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="b4f3f-150">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="b4f3f-150">-SslCertificateId</span></span>
<span data-ttu-id="b4f3f-151">Задает ИД SSL-сертификата для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="b4f3f-151">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="b4f3f-152">Должен быть указан, если в качестве протокола прослушивателя выбран HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b4f3f-152">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="b4f3f-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4f3f-153">CommonParameters</span></span>
<span data-ttu-id="b4f3f-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b4f3f-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4f3f-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4f3f-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4f3f-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b4f3f-156">INPUTS</span></span>

### <span data-ttu-id="b4f3f-157">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4f3f-157">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b4f3f-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4f3f-158">OUTPUTS</span></span>

### <span data-ttu-id="b4f3f-159">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b4f3f-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b4f3f-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="b4f3f-160">NOTES</span></span>

## <span data-ttu-id="b4f3f-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4f3f-161">RELATED LINKS</span></span>

[<span data-ttu-id="b4f3f-162">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b4f3f-162">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="b4f3f-163">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b4f3f-163">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="b4f3f-164">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b4f3f-164">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="b4f3f-165">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b4f3f-165">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)

