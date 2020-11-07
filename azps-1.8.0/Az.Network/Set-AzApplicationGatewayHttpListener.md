---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 11a416e237ff4a12dc3aafbd161e1ae77faab732
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730054"
---
# <span data-ttu-id="9ffd0-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9ffd0-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="9ffd0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9ffd0-102">SYNOPSIS</span></span>
<span data-ttu-id="9ffd0-103">Изменяет прослушиватель HTTP для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="9ffd0-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="9ffd0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9ffd0-104">SYNTAX</span></span>

### <span data-ttu-id="9ffd0-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9ffd0-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ffd0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9ffd0-106">SetByResource</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ffd0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ffd0-107">DESCRIPTION</span></span>
<span data-ttu-id="9ffd0-108">Командлет **Set-AzApplicationGatewayHttpListener** изменяет прослушиватель HTTP для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="9ffd0-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="9ffd0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9ffd0-109">EXAMPLES</span></span>

### <span data-ttu-id="9ffd0-110">Пример 1: Настройка прослушивателя HTTP</span><span class="sxs-lookup"><span data-stu-id="9ffd0-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="9ffd0-111">Первая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="9ffd0-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="9ffd0-112">Вторая команда задает прослушивателю HTTP для шлюза для использования серверной конфигурации, хранящейся в $FIP 01, с помощью протокола HTTP для порта 80.</span><span class="sxs-lookup"><span data-stu-id="9ffd0-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="9ffd0-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9ffd0-113">PARAMETERS</span></span>

### <span data-ttu-id="9ffd0-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9ffd0-114">-ApplicationGateway</span></span>
<span data-ttu-id="9ffd0-115">Указывает шлюз приложений, с которым этот командлет связывает прослушиватель HTTP.</span><span class="sxs-lookup"><span data-stu-id="9ffd0-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="9ffd0-116">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="9ffd0-116">-CustomErrorConfiguration</span></span>
<span data-ttu-id="9ffd0-117">Ошибка клиента в шлюзе приложений</span><span class="sxs-lookup"><span data-stu-id="9ffd0-117">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="9ffd0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ffd0-118">-DefaultProfile</span></span>
<span data-ttu-id="9ffd0-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9ffd0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ffd0-120">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9ffd0-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="9ffd0-121">Задает интерфейсный IP-адрес шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="9ffd0-121">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="9ffd0-122">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9ffd0-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="9ffd0-123">Указывает идентификатор IP-адреса переднего плана для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="9ffd0-123">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="9ffd0-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="9ffd0-124">-FrontendPort</span></span>
<span data-ttu-id="9ffd0-125">Задает интерфейсный порт шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="9ffd0-125">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="9ffd0-126">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="9ffd0-126">-FrontendPortId</span></span>
<span data-ttu-id="9ffd0-127">Указывает идентификатор внешнего порта шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="9ffd0-127">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="9ffd0-128">-HostName</span><span class="sxs-lookup"><span data-stu-id="9ffd0-128">-HostName</span></span>
<span data-ttu-id="9ffd0-129">Указывает имя узла, которому командлет отправляет HTTP-прослушиватель.</span><span class="sxs-lookup"><span data-stu-id="9ffd0-129">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="9ffd0-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9ffd0-130">-Name</span></span>
<span data-ttu-id="9ffd0-131">Указывает имя прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="9ffd0-131">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="9ffd0-132">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="9ffd0-132">-Protocol</span></span>
<span data-ttu-id="9ffd0-133">Указывает протокол, который использует прослушиватель HTTP.</span><span class="sxs-lookup"><span data-stu-id="9ffd0-133">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="9ffd0-134">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9ffd0-134">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9ffd0-135">Через</span><span class="sxs-lookup"><span data-stu-id="9ffd0-135">Http</span></span>
- <span data-ttu-id="9ffd0-136">Протокол</span><span class="sxs-lookup"><span data-stu-id="9ffd0-136">Https</span></span>

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

### <span data-ttu-id="9ffd0-137">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="9ffd0-137">-RequireServerNameIndication</span></span>
<span data-ttu-id="9ffd0-138">Указывает, требуется ли для командлета указание имени сервера.</span><span class="sxs-lookup"><span data-stu-id="9ffd0-138">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="9ffd0-139">Допустимые значения этого параметра: истина или ложь.</span><span class="sxs-lookup"><span data-stu-id="9ffd0-139">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="9ffd0-140">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="9ffd0-140">-SslCertificate</span></span>
<span data-ttu-id="9ffd0-141">Задает SSL-сертификат для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="9ffd0-141">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="9ffd0-142">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="9ffd0-142">-SslCertificateId</span></span>
<span data-ttu-id="9ffd0-143">Задает ИД SSL-сертификата для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="9ffd0-143">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="9ffd0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ffd0-144">CommonParameters</span></span>
<span data-ttu-id="9ffd0-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9ffd0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ffd0-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ffd0-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ffd0-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9ffd0-147">INPUTS</span></span>

### <span data-ttu-id="9ffd0-148">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9ffd0-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9ffd0-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ffd0-149">OUTPUTS</span></span>

### <span data-ttu-id="9ffd0-150">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9ffd0-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9ffd0-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="9ffd0-151">NOTES</span></span>

## <span data-ttu-id="9ffd0-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ffd0-152">RELATED LINKS</span></span>

[<span data-ttu-id="9ffd0-153">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9ffd0-153">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="9ffd0-154">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9ffd0-154">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="9ffd0-155">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9ffd0-155">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="9ffd0-156">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9ffd0-156">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)


