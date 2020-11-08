---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 3cc9af0865ca47099f5617cc1e94f3232ed9bdb7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065820"
---
# <span data-ttu-id="8e5e1-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="8e5e1-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="8e5e1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8e5e1-102">SYNOPSIS</span></span>
<span data-ttu-id="8e5e1-103">Изменяет прослушиватель HTTP для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="8e5e1-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="8e5e1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8e5e1-104">SYNTAX</span></span>

### <span data-ttu-id="8e5e1-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8e5e1-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8e5e1-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8e5e1-106">SetByResource</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e5e1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e5e1-107">DESCRIPTION</span></span>
<span data-ttu-id="8e5e1-108">Командлет **Set-AzApplicationGatewayHttpListener** изменяет прослушиватель HTTP для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="8e5e1-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="8e5e1-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8e5e1-109">EXAMPLES</span></span>

### <span data-ttu-id="8e5e1-110">Пример 1: Настройка прослушивателя HTTP</span><span class="sxs-lookup"><span data-stu-id="8e5e1-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="8e5e1-111">Первая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="8e5e1-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="8e5e1-112">Вторая команда задает прослушивателю HTTP для шлюза для использования серверной конфигурации, хранящейся в $FIP 01, с помощью протокола HTTP для порта 80.</span><span class="sxs-lookup"><span data-stu-id="8e5e1-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

### <span data-ttu-id="8e5e1-113">Пример 2: Добавление прослушивателя HTTPS с SSL и HostName</span><span class="sxs-lookup"><span data-stu-id="8e5e1-113">Example 2: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="8e5e1-114">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="8e5e1-114">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="8e5e1-115">Вторая команда добавляет прослушиватель, использующий протокол HTTPS, с SSL-сертификатами и хост-именем для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="8e5e1-115">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="8e5e1-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8e5e1-116">PARAMETERS</span></span>

### <span data-ttu-id="8e5e1-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e5e1-117">-ApplicationGateway</span></span>
<span data-ttu-id="8e5e1-118">Указывает шлюз приложений, с которым этот командлет связывает прослушиватель HTTP.</span><span class="sxs-lookup"><span data-stu-id="8e5e1-118">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="8e5e1-119">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e5e1-119">-CustomErrorConfiguration</span></span>
<span data-ttu-id="8e5e1-120">Ошибка клиента в шлюзе приложений</span><span class="sxs-lookup"><span data-stu-id="8e5e1-120">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="8e5e1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e5e1-121">-DefaultProfile</span></span>
<span data-ttu-id="8e5e1-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e5e1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e5e1-123">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="8e5e1-123">-FirewallPolicy</span></span>
<span data-ttu-id="8e5e1-124">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="8e5e1-124">FirewallPolicy</span></span>

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

### <span data-ttu-id="8e5e1-125">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="8e5e1-125">-FirewallPolicyId</span></span>
<span data-ttu-id="8e5e1-126">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="8e5e1-126">FirewallPolicyId</span></span>

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

### <span data-ttu-id="8e5e1-127">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e5e1-127">-FrontendIPConfiguration</span></span>
<span data-ttu-id="8e5e1-128">Задает интерфейсный IP-адрес шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="8e5e1-128">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="8e5e1-129">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="8e5e1-129">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="8e5e1-130">Указывает идентификатор IP-адреса переднего плана для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="8e5e1-130">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="8e5e1-131">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="8e5e1-131">-FrontendPort</span></span>
<span data-ttu-id="8e5e1-132">Задает интерфейсный порт шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="8e5e1-132">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="8e5e1-133">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="8e5e1-133">-FrontendPortId</span></span>
<span data-ttu-id="8e5e1-134">Указывает идентификатор внешнего порта шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="8e5e1-134">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="8e5e1-135">-HostName</span><span class="sxs-lookup"><span data-stu-id="8e5e1-135">-HostName</span></span>
<span data-ttu-id="8e5e1-136">Указывает имя узла, которому командлет отправляет HTTP-прослушиватель.</span><span class="sxs-lookup"><span data-stu-id="8e5e1-136">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="8e5e1-137">-HostName</span><span class="sxs-lookup"><span data-stu-id="8e5e1-137">-HostNames</span></span>
<span data-ttu-id="8e5e1-138">Имена узлов</span><span class="sxs-lookup"><span data-stu-id="8e5e1-138">Host names</span></span>

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

### <span data-ttu-id="8e5e1-139">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8e5e1-139">-Name</span></span>
<span data-ttu-id="8e5e1-140">Указывает имя прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="8e5e1-140">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="8e5e1-141">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="8e5e1-141">-Protocol</span></span>
<span data-ttu-id="8e5e1-142">Указывает протокол, который использует прослушиватель HTTP.</span><span class="sxs-lookup"><span data-stu-id="8e5e1-142">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="8e5e1-143">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8e5e1-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8e5e1-144">Через</span><span class="sxs-lookup"><span data-stu-id="8e5e1-144">Http</span></span>
- <span data-ttu-id="8e5e1-145">Протокол</span><span class="sxs-lookup"><span data-stu-id="8e5e1-145">Https</span></span>

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

### <span data-ttu-id="8e5e1-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="8e5e1-146">-RequireServerNameIndication</span></span>
<span data-ttu-id="8e5e1-147">Указывает, требуется ли для командлета указание имени сервера.</span><span class="sxs-lookup"><span data-stu-id="8e5e1-147">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="8e5e1-148">Допустимые значения этого параметра: истина или ложь.</span><span class="sxs-lookup"><span data-stu-id="8e5e1-148">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="8e5e1-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="8e5e1-149">-SslCertificate</span></span>
<span data-ttu-id="8e5e1-150">Задает SSL-сертификат для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="8e5e1-150">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="8e5e1-151">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="8e5e1-151">-SslCertificateId</span></span>
<span data-ttu-id="8e5e1-152">Задает ИД SSL-сертификата для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="8e5e1-152">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="8e5e1-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e5e1-153">CommonParameters</span></span>
<span data-ttu-id="8e5e1-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8e5e1-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e5e1-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e5e1-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e5e1-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8e5e1-156">INPUTS</span></span>

### <span data-ttu-id="8e5e1-157">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e5e1-157">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8e5e1-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e5e1-158">OUTPUTS</span></span>

### <span data-ttu-id="8e5e1-159">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8e5e1-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8e5e1-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="8e5e1-160">NOTES</span></span>

## <span data-ttu-id="8e5e1-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e5e1-161">RELATED LINKS</span></span>

[<span data-ttu-id="8e5e1-162">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="8e5e1-162">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="8e5e1-163">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="8e5e1-163">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="8e5e1-164">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="8e5e1-164">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="8e5e1-165">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="8e5e1-165">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)


