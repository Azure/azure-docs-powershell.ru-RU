---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 571739c72b42e07070a3882ef696388a4a923196
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568493"
---
# <span data-ttu-id="1a732-101">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1a732-101">Add-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="1a732-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1a732-102">SYNOPSIS</span></span>
<span data-ttu-id="1a732-103">Добавляет прослушиватель HTTP в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="1a732-103">Adds an HTTP listener to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a732-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1a732-104">SYNTAX</span></span>

### <span data-ttu-id="1a732-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1a732-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a732-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1a732-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a732-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a732-107">DESCRIPTION</span></span>
<span data-ttu-id="1a732-108">Командлет **Add-AzureRmApplicationGatewayHttpListener** добавляет прослушиватель HTTP в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="1a732-108">The **Add-AzureRmApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="1a732-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1a732-109">EXAMPLES</span></span>

### <span data-ttu-id="1a732-110">Пример 1: Добавление прослушивателя HTTP</span><span class="sxs-lookup"><span data-stu-id="1a732-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="1a732-111">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw. Вторая команда добавляет прослушиватель HTTP на шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="1a732-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="1a732-112">Пример 2: Добавление прослушивателя HTTPS с SSL</span><span class="sxs-lookup"><span data-stu-id="1a732-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="1a732-113">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="1a732-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="1a732-114">Вторая команда добавляет прослушиватель, использующий протокол HTTPS, к шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="1a732-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

## <span data-ttu-id="1a732-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1a732-115">PARAMETERS</span></span>

### <span data-ttu-id="1a732-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1a732-116">-ApplicationGateway</span></span>
<span data-ttu-id="1a732-117">Указывает шлюз приложений, к которому этот командлет добавляет прослушиватель HTTP.</span><span class="sxs-lookup"><span data-stu-id="1a732-117">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="1a732-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a732-118">-DefaultProfile</span></span>
<span data-ttu-id="1a732-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1a732-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a732-120">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1a732-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="1a732-121">Указывает внешний серверный IP-ресурс шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1a732-121">Specifies the application gateway front-end IP resource object.</span></span>

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

### <span data-ttu-id="1a732-122">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="1a732-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="1a732-123">Указывает серверный IP-идентификатор шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1a732-123">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="1a732-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="1a732-124">-FrontendPort</span></span>
<span data-ttu-id="1a732-125">Указывает объект внешнего порта шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1a732-125">Specifies the application gateway front-end port object.</span></span>

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

### <span data-ttu-id="1a732-126">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="1a732-126">-FrontendPortId</span></span>
<span data-ttu-id="1a732-127">Указывает идентификатор внешнего порта шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1a732-127">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="1a732-128">-HostName</span><span class="sxs-lookup"><span data-stu-id="1a732-128">-HostName</span></span>
<span data-ttu-id="1a732-129">Указывает имя узла, к которому этот командлет добавляет HTTP-прослушиватель.</span><span class="sxs-lookup"><span data-stu-id="1a732-129">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="1a732-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1a732-130">-Name</span></span>
<span data-ttu-id="1a732-131">Задает имя порта переднего плана, которое добавляет эта команда.</span><span class="sxs-lookup"><span data-stu-id="1a732-131">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="1a732-132">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="1a732-132">-Protocol</span></span>
<span data-ttu-id="1a732-133">Указывает протокол для HTTP-прослушивателя.</span><span class="sxs-lookup"><span data-stu-id="1a732-133">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="1a732-134">Поддерживаются протоколы HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="1a732-134">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="1a732-135">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="1a732-135">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="1a732-136">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="1a732-136">-SslCertificate</span></span>
<span data-ttu-id="1a732-137">Задает SSL-сертификат для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="1a732-137">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="1a732-138">Должен быть указан, если в качестве протокола прослушивателя выбран HTTPS.</span><span class="sxs-lookup"><span data-stu-id="1a732-138">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="1a732-139">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="1a732-139">-SslCertificateId</span></span>
<span data-ttu-id="1a732-140">Задает ИД SSL-сертификата для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="1a732-140">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="1a732-141">Должен быть указан, если в качестве протокола прослушивателя выбран HTTPS.</span><span class="sxs-lookup"><span data-stu-id="1a732-141">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="1a732-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a732-142">CommonParameters</span></span>
<span data-ttu-id="1a732-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1a732-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a732-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a732-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a732-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1a732-145">INPUTS</span></span>

### <span data-ttu-id="1a732-146">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1a732-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="1a732-147">Параметры: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1a732-147">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="1a732-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a732-148">OUTPUTS</span></span>

### <span data-ttu-id="1a732-149">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1a732-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1a732-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="1a732-150">NOTES</span></span>

## <span data-ttu-id="1a732-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a732-151">RELATED LINKS</span></span>

[<span data-ttu-id="1a732-152">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1a732-152">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="1a732-153">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1a732-153">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="1a732-154">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1a732-154">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="1a732-155">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1a732-155">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


