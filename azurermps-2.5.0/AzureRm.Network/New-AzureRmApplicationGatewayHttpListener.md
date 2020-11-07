---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayhttplistener
schema: 2.0.0
ms.openlocfilehash: f6b8e2a869ba6c59011241c5ebb7b1fe46ac2bc7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913445"
---
# <span data-ttu-id="edeb3-101">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="edeb3-101">New-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="edeb3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="edeb3-102">SYNOPSIS</span></span>
<span data-ttu-id="edeb3-103">Создает прослушиватель HTTP для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="edeb3-103">Creates an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="edeb3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="edeb3-104">SYNTAX</span></span>

### <span data-ttu-id="edeb3-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="edeb3-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="edeb3-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="edeb3-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edeb3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="edeb3-107">DESCRIPTION</span></span>
<span data-ttu-id="edeb3-108">Командлет **New-AzureRmApplicationGatewayHttpListener** создает прослушиватель HTTP для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="edeb3-108">The **New-AzureRmApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="edeb3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="edeb3-109">EXAMPLES</span></span>

### <span data-ttu-id="edeb3-110">Пример 1: создание прослушивателя HTTP</span><span class="sxs-lookup"><span data-stu-id="edeb3-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzureRmApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="edeb3-111">Эта команда создает прослушиватель HTTP с именем Listener01 и сохраняет результат в переменной с именем $Listener.</span><span class="sxs-lookup"><span data-stu-id="edeb3-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="edeb3-112">Пример 2: создание прослушивателя HTTP с помощью SSL</span><span class="sxs-lookup"><span data-stu-id="edeb3-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzureRmApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="edeb3-113">Эта команда создает прослушиватель HTTP, использующий разгрузку SSL, и предоставляет сертификат SSL в переменной $SSLCert 01.</span><span class="sxs-lookup"><span data-stu-id="edeb3-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="edeb3-114">Команда сохраняет результат в переменной с именем $Listener.</span><span class="sxs-lookup"><span data-stu-id="edeb3-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="edeb3-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="edeb3-115">PARAMETERS</span></span>

### <span data-ttu-id="edeb3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edeb3-116">-DefaultProfile</span></span>
<span data-ttu-id="edeb3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="edeb3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edeb3-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="edeb3-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="edeb3-119">Задает интерфейсный объект конфигурации IP для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="edeb3-119">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="edeb3-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="edeb3-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="edeb3-121">Указывает идентификатор IP-конфигурации переднего плана для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="edeb3-121">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="edeb3-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="edeb3-122">-FrontendPort</span></span>
<span data-ttu-id="edeb3-123">Задает интерфейсный порт для HTTP-прослушивателя.</span><span class="sxs-lookup"><span data-stu-id="edeb3-123">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="edeb3-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="edeb3-124">-FrontendPortId</span></span>
<span data-ttu-id="edeb3-125">Указывает идентификатор объекта переднего порта для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="edeb3-125">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="edeb3-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="edeb3-126">-HostName</span></span>
<span data-ttu-id="edeb3-127">Указывает имя узла для прослушивателя HTTP шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="edeb3-127">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="edeb3-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="edeb3-128">-Name</span></span>
<span data-ttu-id="edeb3-129">Указывает имя прослушивателя HTTP, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="edeb3-129">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="edeb3-130">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="edeb3-130">-Protocol</span></span>
<span data-ttu-id="edeb3-131">Указывает протокол, который использует прослушиватель HTTP.</span><span class="sxs-lookup"><span data-stu-id="edeb3-131">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="edeb3-132">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="edeb3-132">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="edeb3-133">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="edeb3-133">-SslCertificate</span></span>
<span data-ttu-id="edeb3-134">Указывает объект сертификата SSL для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="edeb3-134">Specifies the SSL certificate object for  the HTTP listener.</span></span>

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

### <span data-ttu-id="edeb3-135">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="edeb3-135">-SslCertificateId</span></span>
<span data-ttu-id="edeb3-136">Задает ИД SSL-сертификата для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="edeb3-136">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="edeb3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edeb3-137">CommonParameters</span></span>
<span data-ttu-id="edeb3-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="edeb3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edeb3-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edeb3-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edeb3-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="edeb3-140">INPUTS</span></span>

### <span data-ttu-id="edeb3-141">System. String</span><span class="sxs-lookup"><span data-stu-id="edeb3-141">System.String</span></span>

## <span data-ttu-id="edeb3-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="edeb3-142">OUTPUTS</span></span>

### <span data-ttu-id="edeb3-143">Microsoft. Azure. Commands. Network. Models. PSHttpListener</span><span class="sxs-lookup"><span data-stu-id="edeb3-143">Microsoft.Azure.Commands.Network.Models.PSHttpListener</span></span>

## <span data-ttu-id="edeb3-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="edeb3-144">NOTES</span></span>

## <span data-ttu-id="edeb3-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="edeb3-145">RELATED LINKS</span></span>

[<span data-ttu-id="edeb3-146">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="edeb3-146">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="edeb3-147">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="edeb3-147">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="edeb3-148">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="edeb3-148">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="edeb3-149">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="edeb3-149">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


