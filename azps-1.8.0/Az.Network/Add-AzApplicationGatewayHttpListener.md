---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 5648bb1cb7497517afb5ff461674294e426c0131
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730745"
---
# <span data-ttu-id="51e31-101">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="51e31-101">Add-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="51e31-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="51e31-102">SYNOPSIS</span></span>
<span data-ttu-id="51e31-103">Добавляет прослушиватель HTTP в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="51e31-103">Adds an HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="51e31-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="51e31-104">SYNTAX</span></span>

### <span data-ttu-id="51e31-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="51e31-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="51e31-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="51e31-106">SetByResource</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="51e31-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="51e31-107">DESCRIPTION</span></span>
<span data-ttu-id="51e31-108">Командлет **Add-AzApplicationGatewayHttpListener** добавляет прослушиватель HTTP в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="51e31-108">The **Add-AzApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="51e31-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="51e31-109">EXAMPLES</span></span>

### <span data-ttu-id="51e31-110">Пример 1: Добавление прослушивателя HTTP</span><span class="sxs-lookup"><span data-stu-id="51e31-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="51e31-111">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw. Вторая команда добавляет прослушиватель HTTP на шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="51e31-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="51e31-112">Пример 2: Добавление прослушивателя HTTPS с SSL</span><span class="sxs-lookup"><span data-stu-id="51e31-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="51e31-113">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="51e31-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="51e31-114">Вторая команда добавляет прослушиватель, использующий протокол HTTPS, к шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="51e31-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

## <span data-ttu-id="51e31-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="51e31-115">PARAMETERS</span></span>

### <span data-ttu-id="51e31-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="51e31-116">-ApplicationGateway</span></span>
<span data-ttu-id="51e31-117">Указывает шлюз приложений, к которому этот командлет добавляет прослушиватель HTTP.</span><span class="sxs-lookup"><span data-stu-id="51e31-117">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="51e31-118">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="51e31-118">-CustomErrorConfiguration</span></span>
<span data-ttu-id="51e31-119">Ошибка клиента в шлюзе приложений</span><span class="sxs-lookup"><span data-stu-id="51e31-119">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="51e31-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51e31-120">-DefaultProfile</span></span>
<span data-ttu-id="51e31-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="51e31-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51e31-122">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="51e31-122">-FrontendIPConfiguration</span></span>
<span data-ttu-id="51e31-123">Указывает внешний серверный IP-ресурс шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="51e31-123">Specifies the application gateway front-end IP resource object.</span></span>

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

### <span data-ttu-id="51e31-124">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="51e31-124">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="51e31-125">Указывает серверный IP-идентификатор шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="51e31-125">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="51e31-126">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="51e31-126">-FrontendPort</span></span>
<span data-ttu-id="51e31-127">Указывает объект внешнего порта шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="51e31-127">Specifies the application gateway front-end port object.</span></span>

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

### <span data-ttu-id="51e31-128">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="51e31-128">-FrontendPortId</span></span>
<span data-ttu-id="51e31-129">Указывает идентификатор внешнего порта шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="51e31-129">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="51e31-130">-HostName</span><span class="sxs-lookup"><span data-stu-id="51e31-130">-HostName</span></span>
<span data-ttu-id="51e31-131">Указывает имя узла, к которому этот командлет добавляет HTTP-прослушиватель.</span><span class="sxs-lookup"><span data-stu-id="51e31-131">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="51e31-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="51e31-132">-Name</span></span>
<span data-ttu-id="51e31-133">Задает имя порта переднего плана, которое добавляет эта команда.</span><span class="sxs-lookup"><span data-stu-id="51e31-133">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="51e31-134">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="51e31-134">-Protocol</span></span>
<span data-ttu-id="51e31-135">Указывает протокол для HTTP-прослушивателя.</span><span class="sxs-lookup"><span data-stu-id="51e31-135">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="51e31-136">Поддерживаются протоколы HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="51e31-136">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="51e31-137">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="51e31-137">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="51e31-138">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="51e31-138">-SslCertificate</span></span>
<span data-ttu-id="51e31-139">Задает SSL-сертификат для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="51e31-139">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="51e31-140">Должен быть указан, если в качестве протокола прослушивателя выбран HTTPS.</span><span class="sxs-lookup"><span data-stu-id="51e31-140">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="51e31-141">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="51e31-141">-SslCertificateId</span></span>
<span data-ttu-id="51e31-142">Задает ИД SSL-сертификата для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="51e31-142">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="51e31-143">Должен быть указан, если в качестве протокола прослушивателя выбран HTTPS.</span><span class="sxs-lookup"><span data-stu-id="51e31-143">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="51e31-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51e31-144">CommonParameters</span></span>
<span data-ttu-id="51e31-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="51e31-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51e31-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51e31-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51e31-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="51e31-147">INPUTS</span></span>

### <span data-ttu-id="51e31-148">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="51e31-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="51e31-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="51e31-149">OUTPUTS</span></span>

### <span data-ttu-id="51e31-150">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="51e31-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="51e31-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="51e31-151">NOTES</span></span>

## <span data-ttu-id="51e31-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="51e31-152">RELATED LINKS</span></span>

[<span data-ttu-id="51e31-153">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="51e31-153">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="51e31-154">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="51e31-154">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="51e31-155">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="51e31-155">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="51e31-156">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="51e31-156">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


