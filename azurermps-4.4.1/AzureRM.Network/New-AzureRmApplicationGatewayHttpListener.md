---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: ea7a140d2dca2a590a8d3bc83e946d122fb8fd31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568040"
---
# <span data-ttu-id="36d68-101">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="36d68-101">New-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="36d68-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="36d68-102">SYNOPSIS</span></span>
<span data-ttu-id="36d68-103">Создает прослушиватель HTTP для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="36d68-103">Creates an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36d68-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="36d68-104">SYNTAX</span></span>

### <span data-ttu-id="36d68-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="36d68-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="36d68-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="36d68-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36d68-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36d68-107">DESCRIPTION</span></span>
<span data-ttu-id="36d68-108">Командлет **New-AzureRmApplicationGatewayHttpListener** создает прослушиватель HTTP для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="36d68-108">The **New-AzureRmApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="36d68-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="36d68-109">EXAMPLES</span></span>

### <span data-ttu-id="36d68-110">Пример 1: создание прослушивателя HTTP</span><span class="sxs-lookup"><span data-stu-id="36d68-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzureRmApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="36d68-111">Эта команда создает прослушиватель HTTP с именем Listener01 и сохраняет результат в переменной с именем $Listener.</span><span class="sxs-lookup"><span data-stu-id="36d68-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="36d68-112">Пример 2: создание прослушивателя HTTP с помощью SSL</span><span class="sxs-lookup"><span data-stu-id="36d68-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzureRmApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="36d68-113">Эта команда создает прослушиватель HTTP, использующий разгрузку SSL, и предоставляет сертификат SSL в переменной $SSLCert 01.</span><span class="sxs-lookup"><span data-stu-id="36d68-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="36d68-114">Команда сохраняет результат в переменной с именем $Listener.</span><span class="sxs-lookup"><span data-stu-id="36d68-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="36d68-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="36d68-115">PARAMETERS</span></span>

### <span data-ttu-id="36d68-116">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="36d68-116">-FrontendIPConfiguration</span></span>
<span data-ttu-id="36d68-117">Задает интерфейсный объект конфигурации IP для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="36d68-117">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="36d68-118">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="36d68-118">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="36d68-119">Указывает идентификатор IP-конфигурации переднего плана для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="36d68-119">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="36d68-120">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="36d68-120">-FrontendPort</span></span>
<span data-ttu-id="36d68-121">Задает интерфейсный порт для HTTP-прослушивателя.</span><span class="sxs-lookup"><span data-stu-id="36d68-121">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="36d68-122">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="36d68-122">-FrontendPortId</span></span>
<span data-ttu-id="36d68-123">Указывает идентификатор объекта переднего порта для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="36d68-123">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="36d68-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="36d68-124">-HostName</span></span>
<span data-ttu-id="36d68-125">Указывает имя узла для прослушивателя HTTP шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="36d68-125">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="36d68-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="36d68-126">-Name</span></span>
<span data-ttu-id="36d68-127">Указывает имя прослушивателя HTTP, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="36d68-127">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="36d68-128">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="36d68-128">-Protocol</span></span>
<span data-ttu-id="36d68-129">Указывает протокол, который использует прослушиватель HTTP.</span><span class="sxs-lookup"><span data-stu-id="36d68-129">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="36d68-130">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="36d68-130">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="36d68-131">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="36d68-131">-SslCertificate</span></span>
<span data-ttu-id="36d68-132">Указывает объект сертификата SSL для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="36d68-132">Specifies the SSL certificate object for  the HTTP listener.</span></span>

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

### <span data-ttu-id="36d68-133">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="36d68-133">-SslCertificateId</span></span>
<span data-ttu-id="36d68-134">Задает ИД SSL-сертификата для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="36d68-134">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="36d68-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36d68-135">-DefaultProfile</span></span>
<span data-ttu-id="36d68-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="36d68-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36d68-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36d68-137">CommonParameters</span></span>
<span data-ttu-id="36d68-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="36d68-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36d68-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36d68-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36d68-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="36d68-140">INPUTS</span></span>

### <span data-ttu-id="36d68-141">System. String</span><span class="sxs-lookup"><span data-stu-id="36d68-141">System.String</span></span>

## <span data-ttu-id="36d68-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="36d68-142">OUTPUTS</span></span>

### <span data-ttu-id="36d68-143">Microsoft. Azure. Commands. Network. Models. PSHttpListener</span><span class="sxs-lookup"><span data-stu-id="36d68-143">Microsoft.Azure.Commands.Network.Models.PSHttpListener</span></span>

## <span data-ttu-id="36d68-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="36d68-144">NOTES</span></span>

## <span data-ttu-id="36d68-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36d68-145">RELATED LINKS</span></span>

[<span data-ttu-id="36d68-146">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="36d68-146">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="36d68-147">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="36d68-147">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="36d68-148">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="36d68-148">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="36d68-149">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="36d68-149">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


