---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 6805eaa6f1d710c607a7911b628d3642d48ece29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733097"
---
# <span data-ttu-id="b6b78-101">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b6b78-101">Set-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="b6b78-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b6b78-102">SYNOPSIS</span></span>
<span data-ttu-id="b6b78-103">Изменяет прослушиватель HTTP для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="b6b78-103">Modifies an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6b78-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b6b78-104">SYNTAX</span></span>

### <span data-ttu-id="b6b78-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b6b78-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6b78-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b6b78-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6b78-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6b78-107">DESCRIPTION</span></span>
<span data-ttu-id="b6b78-108">Командлет **Set-AzureRmApplicationGatewayHttpListener** изменяет прослушиватель HTTP для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="b6b78-108">The **Set-AzureRmApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="b6b78-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b6b78-109">EXAMPLES</span></span>

### <span data-ttu-id="b6b78-110">Пример 1: Настройка прослушивателя HTTP</span><span class="sxs-lookup"><span data-stu-id="b6b78-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="b6b78-111">Первая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b6b78-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="b6b78-112">Вторая команда задает прослушивателю HTTP для шлюза для использования серверной конфигурации, хранящейся в $FIP 01, с помощью протокола HTTP для порта 80.</span><span class="sxs-lookup"><span data-stu-id="b6b78-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="b6b78-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b6b78-113">PARAMETERS</span></span>

### <span data-ttu-id="b6b78-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b6b78-114">-ApplicationGateway</span></span>
<span data-ttu-id="b6b78-115">Указывает шлюз приложений, с которым этот командлет связывает прослушиватель HTTP.</span><span class="sxs-lookup"><span data-stu-id="b6b78-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="b6b78-116">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6b78-116">-FrontendIPConfiguration</span></span>
<span data-ttu-id="b6b78-117">Задает интерфейсный IP-адрес шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="b6b78-117">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="b6b78-118">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b6b78-118">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="b6b78-119">Указывает идентификатор IP-адреса переднего плана для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="b6b78-119">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="b6b78-120">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="b6b78-120">-FrontendPort</span></span>
<span data-ttu-id="b6b78-121">Задает интерфейсный порт шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="b6b78-121">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="b6b78-122">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="b6b78-122">-FrontendPortId</span></span>
<span data-ttu-id="b6b78-123">Указывает идентификатор внешнего порта шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="b6b78-123">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="b6b78-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="b6b78-124">-HostName</span></span>
<span data-ttu-id="b6b78-125">Указывает имя узла, которому командлет отправляет HTTP-прослушиватель.</span><span class="sxs-lookup"><span data-stu-id="b6b78-125">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="b6b78-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b6b78-126">-Name</span></span>
<span data-ttu-id="b6b78-127">Указывает имя прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="b6b78-127">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="b6b78-128">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="b6b78-128">-Protocol</span></span>
<span data-ttu-id="b6b78-129">Указывает протокол, который использует прослушиватель HTTP.</span><span class="sxs-lookup"><span data-stu-id="b6b78-129">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="b6b78-130">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b6b78-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b6b78-131">Через</span><span class="sxs-lookup"><span data-stu-id="b6b78-131">Http</span></span>
- <span data-ttu-id="b6b78-132">Протокол</span><span class="sxs-lookup"><span data-stu-id="b6b78-132">Https</span></span>

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

### <span data-ttu-id="b6b78-133">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="b6b78-133">-RequireServerNameIndication</span></span>
<span data-ttu-id="b6b78-134">Указывает, требуется ли для командлета указание имени сервера.</span><span class="sxs-lookup"><span data-stu-id="b6b78-134">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="b6b78-135">Допустимые значения этого параметра: истина или ложь.</span><span class="sxs-lookup"><span data-stu-id="b6b78-135">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="b6b78-136">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="b6b78-136">-SslCertificate</span></span>
<span data-ttu-id="b6b78-137">Задает SSL-сертификат для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="b6b78-137">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="b6b78-138">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="b6b78-138">-SslCertificateId</span></span>
<span data-ttu-id="b6b78-139">Задает ИД SSL-сертификата для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="b6b78-139">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="b6b78-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6b78-140">-DefaultProfile</span></span>
<span data-ttu-id="b6b78-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b6b78-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6b78-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6b78-142">CommonParameters</span></span>
<span data-ttu-id="b6b78-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b6b78-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6b78-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6b78-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6b78-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b6b78-145">INPUTS</span></span>

### <span data-ttu-id="b6b78-146">System. String</span><span class="sxs-lookup"><span data-stu-id="b6b78-146">System.String</span></span>

## <span data-ttu-id="b6b78-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6b78-147">OUTPUTS</span></span>

### <span data-ttu-id="b6b78-148">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b6b78-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b6b78-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="b6b78-149">NOTES</span></span>

## <span data-ttu-id="b6b78-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6b78-150">RELATED LINKS</span></span>

[<span data-ttu-id="b6b78-151">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b6b78-151">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="b6b78-152">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b6b78-152">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="b6b78-153">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b6b78-153">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="b6b78-154">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b6b78-154">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)


