---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 26cf3a0fb3ae118913130a754def47a257aac254
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734420"
---
# <span data-ttu-id="35c85-101">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="35c85-101">Set-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="35c85-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="35c85-102">SYNOPSIS</span></span>
<span data-ttu-id="35c85-103">Изменяет прослушиватель HTTP для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="35c85-103">Modifies an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35c85-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="35c85-104">SYNTAX</span></span>

### <span data-ttu-id="35c85-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="35c85-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35c85-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="35c85-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35c85-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35c85-107">DESCRIPTION</span></span>
<span data-ttu-id="35c85-108">Командлет **Set-AzureRmApplicationGatewayHttpListener** изменяет прослушиватель HTTP для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="35c85-108">The **Set-AzureRmApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="35c85-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="35c85-109">EXAMPLES</span></span>

### <span data-ttu-id="35c85-110">Пример 1: Настройка прослушивателя HTTP</span><span class="sxs-lookup"><span data-stu-id="35c85-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="35c85-111">Первая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="35c85-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="35c85-112">Вторая команда задает прослушивателю HTTP для шлюза для использования серверной конфигурации, хранящейся в $FIP 01, с помощью протокола HTTP для порта 80.</span><span class="sxs-lookup"><span data-stu-id="35c85-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="35c85-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="35c85-113">PARAMETERS</span></span>

### <span data-ttu-id="35c85-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="35c85-114">-ApplicationGateway</span></span>
<span data-ttu-id="35c85-115">Указывает шлюз приложений, с которым этот командлет связывает прослушиватель HTTP.</span><span class="sxs-lookup"><span data-stu-id="35c85-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="35c85-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35c85-116">-DefaultProfile</span></span>
<span data-ttu-id="35c85-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35c85-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35c85-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="35c85-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="35c85-119">Задает интерфейсный IP-адрес шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="35c85-119">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="35c85-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="35c85-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="35c85-121">Указывает идентификатор IP-адреса переднего плана для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="35c85-121">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="35c85-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="35c85-122">-FrontendPort</span></span>
<span data-ttu-id="35c85-123">Задает интерфейсный порт шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="35c85-123">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="35c85-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="35c85-124">-FrontendPortId</span></span>
<span data-ttu-id="35c85-125">Указывает идентификатор внешнего порта шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="35c85-125">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="35c85-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="35c85-126">-HostName</span></span>
<span data-ttu-id="35c85-127">Указывает имя узла, которому командлет отправляет HTTP-прослушиватель.</span><span class="sxs-lookup"><span data-stu-id="35c85-127">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="35c85-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="35c85-128">-Name</span></span>
<span data-ttu-id="35c85-129">Указывает имя прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="35c85-129">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="35c85-130">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="35c85-130">-Protocol</span></span>
<span data-ttu-id="35c85-131">Указывает протокол, который использует прослушиватель HTTP.</span><span class="sxs-lookup"><span data-stu-id="35c85-131">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="35c85-132">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="35c85-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="35c85-133">Через</span><span class="sxs-lookup"><span data-stu-id="35c85-133">Http</span></span>
- <span data-ttu-id="35c85-134">Протокол</span><span class="sxs-lookup"><span data-stu-id="35c85-134">Https</span></span>

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

### <span data-ttu-id="35c85-135">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="35c85-135">-RequireServerNameIndication</span></span>
<span data-ttu-id="35c85-136">Указывает, требуется ли для командлета указание имени сервера.</span><span class="sxs-lookup"><span data-stu-id="35c85-136">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="35c85-137">Допустимые значения этого параметра: истина или ложь.</span><span class="sxs-lookup"><span data-stu-id="35c85-137">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="35c85-138">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="35c85-138">-SslCertificate</span></span>
<span data-ttu-id="35c85-139">Задает SSL-сертификат для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="35c85-139">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="35c85-140">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="35c85-140">-SslCertificateId</span></span>
<span data-ttu-id="35c85-141">Задает ИД SSL-сертификата для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="35c85-141">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="35c85-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35c85-142">CommonParameters</span></span>
<span data-ttu-id="35c85-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="35c85-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35c85-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35c85-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35c85-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="35c85-145">INPUTS</span></span>

### <span data-ttu-id="35c85-146">System. String</span><span class="sxs-lookup"><span data-stu-id="35c85-146">System.String</span></span>

## <span data-ttu-id="35c85-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="35c85-147">OUTPUTS</span></span>

### <span data-ttu-id="35c85-148">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="35c85-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="35c85-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="35c85-149">NOTES</span></span>

## <span data-ttu-id="35c85-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35c85-150">RELATED LINKS</span></span>

[<span data-ttu-id="35c85-151">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="35c85-151">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="35c85-152">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="35c85-152">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="35c85-153">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="35c85-153">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="35c85-154">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="35c85-154">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)


