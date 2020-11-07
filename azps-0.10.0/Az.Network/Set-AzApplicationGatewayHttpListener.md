---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: ea07f3b9f2dd1e79f59b3369f3f8d3a8c1434deb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911071"
---
# <span data-ttu-id="3c554-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3c554-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="3c554-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3c554-102">SYNOPSIS</span></span>
<span data-ttu-id="3c554-103">Изменяет прослушиватель HTTP для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="3c554-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="3c554-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3c554-104">SYNTAX</span></span>

### <span data-ttu-id="3c554-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3c554-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c554-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3c554-106">SetByResource</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c554-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c554-107">DESCRIPTION</span></span>
<span data-ttu-id="3c554-108">Командлет **Set-AzApplicationGatewayHttpListener** изменяет прослушиватель HTTP для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="3c554-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="3c554-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3c554-109">EXAMPLES</span></span>

### <span data-ttu-id="3c554-110">Пример 1: Настройка прослушивателя HTTP</span><span class="sxs-lookup"><span data-stu-id="3c554-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="3c554-111">Первая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3c554-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="3c554-112">Вторая команда задает прослушивателю HTTP для шлюза для использования серверной конфигурации, хранящейся в $FIP 01, с помощью протокола HTTP для порта 80.</span><span class="sxs-lookup"><span data-stu-id="3c554-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="3c554-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3c554-113">PARAMETERS</span></span>

### <span data-ttu-id="3c554-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3c554-114">-ApplicationGateway</span></span>
<span data-ttu-id="3c554-115">Указывает шлюз приложений, с которым этот командлет связывает прослушиватель HTTP.</span><span class="sxs-lookup"><span data-stu-id="3c554-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="3c554-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c554-116">-DefaultProfile</span></span>
<span data-ttu-id="3c554-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3c554-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c554-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c554-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="3c554-119">Задает интерфейсный IP-адрес шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="3c554-119">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="3c554-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="3c554-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="3c554-121">Указывает идентификатор IP-адреса переднего плана для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="3c554-121">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="3c554-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="3c554-122">-FrontendPort</span></span>
<span data-ttu-id="3c554-123">Задает интерфейсный порт шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="3c554-123">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="3c554-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="3c554-124">-FrontendPortId</span></span>
<span data-ttu-id="3c554-125">Указывает идентификатор внешнего порта шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="3c554-125">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="3c554-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="3c554-126">-HostName</span></span>
<span data-ttu-id="3c554-127">Указывает имя узла, которому командлет отправляет HTTP-прослушиватель.</span><span class="sxs-lookup"><span data-stu-id="3c554-127">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="3c554-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3c554-128">-Name</span></span>
<span data-ttu-id="3c554-129">Указывает имя прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="3c554-129">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="3c554-130">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="3c554-130">-Protocol</span></span>
<span data-ttu-id="3c554-131">Указывает протокол, который использует прослушиватель HTTP.</span><span class="sxs-lookup"><span data-stu-id="3c554-131">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="3c554-132">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3c554-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3c554-133">Через</span><span class="sxs-lookup"><span data-stu-id="3c554-133">Http</span></span>
- <span data-ttu-id="3c554-134">Протокол</span><span class="sxs-lookup"><span data-stu-id="3c554-134">Https</span></span>

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

### <span data-ttu-id="3c554-135">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="3c554-135">-RequireServerNameIndication</span></span>
<span data-ttu-id="3c554-136">Указывает, требуется ли для командлета указание имени сервера.</span><span class="sxs-lookup"><span data-stu-id="3c554-136">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="3c554-137">Допустимые значения этого параметра: истина или ложь.</span><span class="sxs-lookup"><span data-stu-id="3c554-137">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="3c554-138">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="3c554-138">-SslCertificate</span></span>
<span data-ttu-id="3c554-139">Задает SSL-сертификат для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="3c554-139">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="3c554-140">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="3c554-140">-SslCertificateId</span></span>
<span data-ttu-id="3c554-141">Задает ИД SSL-сертификата для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="3c554-141">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="3c554-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c554-142">CommonParameters</span></span>
<span data-ttu-id="3c554-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3c554-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c554-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c554-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c554-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3c554-145">INPUTS</span></span>

### <span data-ttu-id="3c554-146">System. String</span><span class="sxs-lookup"><span data-stu-id="3c554-146">System.String</span></span>

## <span data-ttu-id="3c554-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c554-147">OUTPUTS</span></span>

### <span data-ttu-id="3c554-148">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3c554-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3c554-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="3c554-149">NOTES</span></span>

## <span data-ttu-id="3c554-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c554-150">RELATED LINKS</span></span>

[<span data-ttu-id="3c554-151">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3c554-151">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="3c554-152">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3c554-152">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="3c554-153">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3c554-153">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="3c554-154">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3c554-154">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)


