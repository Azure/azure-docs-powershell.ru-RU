---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 8ce5d01d78b8b434e062b0f33ee41a4cbbce20ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223620"
---
# <span data-ttu-id="ebe8b-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ebe8b-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="ebe8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebe8b-102">SYNOPSIS</span></span>
<span data-ttu-id="ebe8b-103">Изменяет http-прослушивание для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="ebe8b-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="ebe8b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ebe8b-104">SYNTAX</span></span>

### <span data-ttu-id="ebe8b-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ebe8b-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-SslProfileId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ebe8b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ebe8b-106">SetByResource</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-SslProfile <PSApplicationGatewaySslProfile>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ebe8b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebe8b-107">DESCRIPTION</span></span>
<span data-ttu-id="ebe8b-108">**Cmdlet Set-AzApplicationGatewayHttpListener изменяет http-прослушивание** для шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="ebe8b-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="ebe8b-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ebe8b-109">EXAMPLES</span></span>

### <span data-ttu-id="ebe8b-110">Пример 1. Настройка http-прослушивание</span><span class="sxs-lookup"><span data-stu-id="ebe8b-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="ebe8b-111">Первая команда получает шлюз приложения ApplicationGateway01, который принадлежит к группе ресурсов ResourceGroup01, и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="ebe8b-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ebe8b-112">Вторая команда задает для HTTP-компоновщика использование передней конфигурации, хранимой в $FIP 01, с протоколом HTTP в порте 80.</span><span class="sxs-lookup"><span data-stu-id="ebe8b-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

### <span data-ttu-id="ebe8b-113">Пример 2. Добавление прослушки HTTPS с помощью SSL и HostNames</span><span class="sxs-lookup"><span data-stu-id="ebe8b-113">Example 2: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="ebe8b-114">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="ebe8b-114">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="ebe8b-115">Вторая команда добавляет в шлюз приложения пользователя, который использует протокол HTTPS с SSL-сертификатами и именами хост-кодов.</span><span class="sxs-lookup"><span data-stu-id="ebe8b-115">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="ebe8b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ebe8b-116">PARAMETERS</span></span>

### <span data-ttu-id="ebe8b-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ebe8b-117">-ApplicationGateway</span></span>
<span data-ttu-id="ebe8b-118">Указывает шлюз приложения, с которым этот cmdlet связывает http-прослушивание.</span><span class="sxs-lookup"><span data-stu-id="ebe8b-118">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="ebe8b-119">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="ebe8b-119">-CustomErrorConfiguration</span></span>
<span data-ttu-id="ebe8b-120">Ошибка клиента шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="ebe8b-120">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="ebe8b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebe8b-121">-DefaultProfile</span></span>
<span data-ttu-id="ebe8b-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ebe8b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebe8b-123">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="ebe8b-123">-FirewallPolicy</span></span>
<span data-ttu-id="ebe8b-124">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="ebe8b-124">FirewallPolicy</span></span>

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

### <span data-ttu-id="ebe8b-125">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="ebe8b-125">-FirewallPolicyId</span></span>
<span data-ttu-id="ebe8b-126">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="ebe8b-126">FirewallPolicyId</span></span>

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

### <span data-ttu-id="ebe8b-127">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ebe8b-127">-FrontendIPConfiguration</span></span>
<span data-ttu-id="ebe8b-128">Указывает IP-адрес переднего IP-адреса шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="ebe8b-128">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="ebe8b-129">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ebe8b-129">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="ebe8b-130">Определяет IP-адрес переднего IP-адреса шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="ebe8b-130">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="ebe8b-131">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="ebe8b-131">-FrontendPort</span></span>
<span data-ttu-id="ebe8b-132">Определяет стойкий порт шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="ebe8b-132">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="ebe8b-133">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="ebe8b-133">-FrontendPortId</span></span>
<span data-ttu-id="ebe8b-134">Определяет стойкий порт шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="ebe8b-134">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="ebe8b-135">-HostName</span><span class="sxs-lookup"><span data-stu-id="ebe8b-135">-HostName</span></span>
<span data-ttu-id="ebe8b-136">Указывает имя хоста, для которого этот cmdlet отправляет http-прослушивание.</span><span class="sxs-lookup"><span data-stu-id="ebe8b-136">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="ebe8b-137">-HostNames</span><span class="sxs-lookup"><span data-stu-id="ebe8b-137">-HostNames</span></span>
<span data-ttu-id="ebe8b-138">Host names (Имена хостов)</span><span class="sxs-lookup"><span data-stu-id="ebe8b-138">Host names</span></span>

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

### <span data-ttu-id="ebe8b-139">-Name</span><span class="sxs-lookup"><span data-stu-id="ebe8b-139">-Name</span></span>
<span data-ttu-id="ebe8b-140">Указывает имя http-слушателя.</span><span class="sxs-lookup"><span data-stu-id="ebe8b-140">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="ebe8b-141">-Protocol</span><span class="sxs-lookup"><span data-stu-id="ebe8b-141">-Protocol</span></span>
<span data-ttu-id="ebe8b-142">Протокол, который использует http-прослушивание.</span><span class="sxs-lookup"><span data-stu-id="ebe8b-142">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="ebe8b-143">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="ebe8b-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ebe8b-144">Http</span><span class="sxs-lookup"><span data-stu-id="ebe8b-144">Http</span></span>
- <span data-ttu-id="ebe8b-145">Https</span><span class="sxs-lookup"><span data-stu-id="ebe8b-145">Https</span></span>

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

### <span data-ttu-id="ebe8b-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="ebe8b-146">-RequireServerNameIndication</span></span>
<span data-ttu-id="ebe8b-147">Указывает, требуется ли для cmdlet указание имени сервера.</span><span class="sxs-lookup"><span data-stu-id="ebe8b-147">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="ebe8b-148">Допустимые значения этого параметра: TRUE или False.</span><span class="sxs-lookup"><span data-stu-id="ebe8b-148">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="ebe8b-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="ebe8b-149">-SslCertificate</span></span>
<span data-ttu-id="ebe8b-150">Указывает SSL-сертификат для http-прослушивание.</span><span class="sxs-lookup"><span data-stu-id="ebe8b-150">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="ebe8b-151">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="ebe8b-151">-SslCertificateId</span></span>
<span data-ttu-id="ebe8b-152">Определяет ИД SSL-сертификата http-прослушивание.</span><span class="sxs-lookup"><span data-stu-id="ebe8b-152">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="ebe8b-153">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="ebe8b-153">-SslProfile</span></span>
<span data-ttu-id="ebe8b-154">SslProfile</span><span class="sxs-lookup"><span data-stu-id="ebe8b-154">SslProfile</span></span>

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

### <span data-ttu-id="ebe8b-155">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="ebe8b-155">-SslProfileId</span></span>
<span data-ttu-id="ebe8b-156">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="ebe8b-156">SslProfileId</span></span>

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

### <span data-ttu-id="ebe8b-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebe8b-157">CommonParameters</span></span>
<span data-ttu-id="ebe8b-158">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebe8b-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebe8b-159">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ebe8b-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebe8b-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ebe8b-160">INPUTS</span></span>

### <span data-ttu-id="ebe8b-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ebe8b-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ebe8b-162">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ebe8b-162">OUTPUTS</span></span>

### <span data-ttu-id="ebe8b-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ebe8b-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ebe8b-164">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ebe8b-164">NOTES</span></span>

## <span data-ttu-id="ebe8b-165">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ebe8b-165">RELATED LINKS</span></span>

[<span data-ttu-id="ebe8b-166">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ebe8b-166">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="ebe8b-167">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ebe8b-167">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="ebe8b-168">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ebe8b-168">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="ebe8b-169">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ebe8b-169">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)


