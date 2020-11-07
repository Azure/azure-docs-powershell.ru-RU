---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: eaae79c09f6ee609d7a7bf645c2312007a78ad59
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910161"
---
# <span data-ttu-id="1ab8e-101">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1ab8e-101">Add-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="1ab8e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1ab8e-102">SYNOPSIS</span></span>
<span data-ttu-id="1ab8e-103">Добавляет прослушиватель HTTP в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="1ab8e-103">Adds an HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="1ab8e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1ab8e-104">SYNTAX</span></span>

### <span data-ttu-id="1ab8e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1ab8e-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ab8e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1ab8e-106">SetByResource</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ab8e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ab8e-107">DESCRIPTION</span></span>
<span data-ttu-id="1ab8e-108">Командлет **Add-AzApplicationGatewayHttpListener** добавляет прослушиватель HTTP в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="1ab8e-108">The **Add-AzApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="1ab8e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1ab8e-109">EXAMPLES</span></span>

### <span data-ttu-id="1ab8e-110">Пример 1: Добавление прослушивателя HTTP</span><span class="sxs-lookup"><span data-stu-id="1ab8e-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="1ab8e-111">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw. Вторая команда добавляет прослушиватель HTTP на шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="1ab8e-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="1ab8e-112">Пример 2: Добавление прослушивателя HTTPS с SSL</span><span class="sxs-lookup"><span data-stu-id="1ab8e-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="1ab8e-113">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="1ab8e-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="1ab8e-114">Вторая команда добавляет прослушиватель, использующий протокол HTTPS, к шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="1ab8e-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

## <span data-ttu-id="1ab8e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1ab8e-115">PARAMETERS</span></span>

### <span data-ttu-id="1ab8e-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1ab8e-116">-ApplicationGateway</span></span>
<span data-ttu-id="1ab8e-117">Указывает шлюз приложений, к которому этот командлет добавляет прослушиватель HTTP.</span><span class="sxs-lookup"><span data-stu-id="1ab8e-117">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="1ab8e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ab8e-118">-DefaultProfile</span></span>
<span data-ttu-id="1ab8e-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1ab8e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ab8e-120">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ab8e-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="1ab8e-121">Указывает внешний серверный IP-ресурс шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1ab8e-121">Specifies the application gateway front-end IP resource object.</span></span>

```yaml
Type: PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ab8e-122">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="1ab8e-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="1ab8e-123">Указывает серверный IP-идентификатор шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1ab8e-123">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="1ab8e-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="1ab8e-124">-FrontendPort</span></span>
<span data-ttu-id="1ab8e-125">Указывает объект внешнего порта шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1ab8e-125">Specifies the application gateway front-end port object.</span></span>

```yaml
Type: PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ab8e-126">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="1ab8e-126">-FrontendPortId</span></span>
<span data-ttu-id="1ab8e-127">Указывает идентификатор внешнего порта шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1ab8e-127">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="1ab8e-128">-HostName</span><span class="sxs-lookup"><span data-stu-id="1ab8e-128">-HostName</span></span>
<span data-ttu-id="1ab8e-129">Указывает имя узла, к которому этот командлет добавляет HTTP-прослушиватель.</span><span class="sxs-lookup"><span data-stu-id="1ab8e-129">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ab8e-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1ab8e-130">-Name</span></span>
<span data-ttu-id="1ab8e-131">Задает имя порта переднего плана, которое добавляет эта команда.</span><span class="sxs-lookup"><span data-stu-id="1ab8e-131">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="1ab8e-132">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="1ab8e-132">-Protocol</span></span>
<span data-ttu-id="1ab8e-133">Указывает протокол для HTTP-прослушивателя.</span><span class="sxs-lookup"><span data-stu-id="1ab8e-133">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="1ab8e-134">Поддерживаются протоколы HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="1ab8e-134">Both HTTP and HTTPS are supported.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ab8e-135">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="1ab8e-135">-RequireServerNameIndication</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: true, false

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ab8e-136">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="1ab8e-136">-SslCertificate</span></span>
<span data-ttu-id="1ab8e-137">Задает SSL-сертификат для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="1ab8e-137">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="1ab8e-138">Должен быть указан, если в качестве протокола прослушивателя выбран HTTPS.</span><span class="sxs-lookup"><span data-stu-id="1ab8e-138">Must be specified if HTTPS is chosen as listener protocol.</span></span>

```yaml
Type: PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ab8e-139">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="1ab8e-139">-SslCertificateId</span></span>
<span data-ttu-id="1ab8e-140">Задает ИД SSL-сертификата для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="1ab8e-140">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="1ab8e-141">Должен быть указан, если в качестве протокола прослушивателя выбран HTTPS.</span><span class="sxs-lookup"><span data-stu-id="1ab8e-141">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="1ab8e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ab8e-142">CommonParameters</span></span>
<span data-ttu-id="1ab8e-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1ab8e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ab8e-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ab8e-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ab8e-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1ab8e-145">INPUTS</span></span>

### <span data-ttu-id="1ab8e-146">System. String</span><span class="sxs-lookup"><span data-stu-id="1ab8e-146">System.String</span></span>

## <span data-ttu-id="1ab8e-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ab8e-147">OUTPUTS</span></span>

### <span data-ttu-id="1ab8e-148">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1ab8e-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1ab8e-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="1ab8e-149">NOTES</span></span>

## <span data-ttu-id="1ab8e-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ab8e-150">RELATED LINKS</span></span>

[<span data-ttu-id="1ab8e-151">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1ab8e-151">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="1ab8e-152">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1ab8e-152">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="1ab8e-153">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1ab8e-153">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="1ab8e-154">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1ab8e-154">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


