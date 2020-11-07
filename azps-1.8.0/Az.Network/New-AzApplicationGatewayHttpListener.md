---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: e5593ae97692813cc36f14942edb21768517f317
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730407"
---
# <span data-ttu-id="9761f-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9761f-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="9761f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9761f-102">SYNOPSIS</span></span>
<span data-ttu-id="9761f-103">Создает прослушиватель HTTP для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="9761f-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="9761f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9761f-104">SYNTAX</span></span>

### <span data-ttu-id="9761f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9761f-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9761f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9761f-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9761f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9761f-107">DESCRIPTION</span></span>
<span data-ttu-id="9761f-108">Командлет **New-AzApplicationGatewayHttpListener** создает прослушиватель HTTP для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="9761f-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="9761f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9761f-109">EXAMPLES</span></span>

### <span data-ttu-id="9761f-110">Пример 1: создание прослушивателя HTTP</span><span class="sxs-lookup"><span data-stu-id="9761f-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="9761f-111">Эта команда создает прослушиватель HTTP с именем Listener01 и сохраняет результат в переменной с именем $Listener.</span><span class="sxs-lookup"><span data-stu-id="9761f-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="9761f-112">Пример 2: создание прослушивателя HTTP с помощью SSL</span><span class="sxs-lookup"><span data-stu-id="9761f-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="9761f-113">Эта команда создает прослушиватель HTTP, использующий разгрузку SSL, и предоставляет сертификат SSL в переменной $SSLCert 01.</span><span class="sxs-lookup"><span data-stu-id="9761f-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="9761f-114">Команда сохраняет результат в переменной с именем $Listener.</span><span class="sxs-lookup"><span data-stu-id="9761f-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="9761f-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9761f-115">PARAMETERS</span></span>

### <span data-ttu-id="9761f-116">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="9761f-116">-CustomErrorConfiguration</span></span>
<span data-ttu-id="9761f-117">Ошибка клиента в шлюзе приложений</span><span class="sxs-lookup"><span data-stu-id="9761f-117">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="9761f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9761f-118">-DefaultProfile</span></span>
<span data-ttu-id="9761f-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9761f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9761f-120">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="9761f-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="9761f-121">Задает интерфейсный объект конфигурации IP для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="9761f-121">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="9761f-122">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9761f-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="9761f-123">Указывает идентификатор IP-конфигурации переднего плана для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="9761f-123">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="9761f-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="9761f-124">-FrontendPort</span></span>
<span data-ttu-id="9761f-125">Задает интерфейсный порт для HTTP-прослушивателя.</span><span class="sxs-lookup"><span data-stu-id="9761f-125">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="9761f-126">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="9761f-126">-FrontendPortId</span></span>
<span data-ttu-id="9761f-127">Указывает идентификатор объекта переднего порта для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="9761f-127">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="9761f-128">-HostName</span><span class="sxs-lookup"><span data-stu-id="9761f-128">-HostName</span></span>
<span data-ttu-id="9761f-129">Указывает имя узла для прослушивателя HTTP шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="9761f-129">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="9761f-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9761f-130">-Name</span></span>
<span data-ttu-id="9761f-131">Указывает имя прослушивателя HTTP, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="9761f-131">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9761f-132">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="9761f-132">-Protocol</span></span>
<span data-ttu-id="9761f-133">Указывает протокол, который использует прослушиватель HTTP.</span><span class="sxs-lookup"><span data-stu-id="9761f-133">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="9761f-134">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="9761f-134">-RequireServerNameIndication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: true
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9761f-135">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="9761f-135">-SslCertificate</span></span>
<span data-ttu-id="9761f-136">Указывает объект сертификата SSL для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="9761f-136">Specifies the SSL certificate object for the HTTP listener.</span></span>

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

### <span data-ttu-id="9761f-137">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="9761f-137">-SslCertificateId</span></span>
<span data-ttu-id="9761f-138">Задает ИД SSL-сертификата для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="9761f-138">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="9761f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9761f-139">CommonParameters</span></span>
<span data-ttu-id="9761f-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9761f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9761f-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9761f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9761f-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9761f-142">INPUTS</span></span>

### <span data-ttu-id="9761f-143">Ничего</span><span class="sxs-lookup"><span data-stu-id="9761f-143">None</span></span>

## <span data-ttu-id="9761f-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9761f-144">OUTPUTS</span></span>

### <span data-ttu-id="9761f-145">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9761f-145">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="9761f-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="9761f-146">NOTES</span></span>

## <span data-ttu-id="9761f-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9761f-147">RELATED LINKS</span></span>

[<span data-ttu-id="9761f-148">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9761f-148">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="9761f-149">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9761f-149">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="9761f-150">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9761f-150">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="9761f-151">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9761f-151">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


