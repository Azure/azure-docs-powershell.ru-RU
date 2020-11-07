---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 104a5e022d89421ac960d699c7391db660c0dd6b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909758"
---
# <span data-ttu-id="ea294-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ea294-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="ea294-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ea294-102">SYNOPSIS</span></span>
<span data-ttu-id="ea294-103">Создает прослушиватель HTTP для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="ea294-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="ea294-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ea294-104">SYNTAX</span></span>

### <span data-ttu-id="ea294-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ea294-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ea294-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ea294-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea294-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea294-107">DESCRIPTION</span></span>
<span data-ttu-id="ea294-108">Командлет **New-AzApplicationGatewayHttpListener** создает прослушиватель HTTP для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="ea294-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="ea294-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ea294-109">EXAMPLES</span></span>

### <span data-ttu-id="ea294-110">Пример 1: создание прослушивателя HTTP</span><span class="sxs-lookup"><span data-stu-id="ea294-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="ea294-111">Эта команда создает прослушиватель HTTP с именем Listener01 и сохраняет результат в переменной с именем $Listener.</span><span class="sxs-lookup"><span data-stu-id="ea294-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="ea294-112">Пример 2: создание прослушивателя HTTP с помощью SSL</span><span class="sxs-lookup"><span data-stu-id="ea294-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="ea294-113">Эта команда создает прослушиватель HTTP, использующий разгрузку SSL, и предоставляет сертификат SSL в переменной $SSLCert 01.</span><span class="sxs-lookup"><span data-stu-id="ea294-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="ea294-114">Команда сохраняет результат в переменной с именем $Listener.</span><span class="sxs-lookup"><span data-stu-id="ea294-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="ea294-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ea294-115">PARAMETERS</span></span>

### <span data-ttu-id="ea294-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea294-116">-DefaultProfile</span></span>
<span data-ttu-id="ea294-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ea294-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea294-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea294-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="ea294-119">Задает интерфейсный объект конфигурации IP для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="ea294-119">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="ea294-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="ea294-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="ea294-121">Указывает идентификатор IP-конфигурации переднего плана для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="ea294-121">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="ea294-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="ea294-122">-FrontendPort</span></span>
<span data-ttu-id="ea294-123">Задает интерфейсный порт для HTTP-прослушивателя.</span><span class="sxs-lookup"><span data-stu-id="ea294-123">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="ea294-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="ea294-124">-FrontendPortId</span></span>
<span data-ttu-id="ea294-125">Указывает идентификатор объекта переднего порта для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="ea294-125">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="ea294-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="ea294-126">-HostName</span></span>
<span data-ttu-id="ea294-127">Указывает имя узла для прослушивателя HTTP шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="ea294-127">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="ea294-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ea294-128">-Name</span></span>
<span data-ttu-id="ea294-129">Указывает имя прослушивателя HTTP, создаваемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="ea294-129">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ea294-130">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="ea294-130">-Protocol</span></span>
<span data-ttu-id="ea294-131">Указывает протокол, который использует прослушиватель HTTP.</span><span class="sxs-lookup"><span data-stu-id="ea294-131">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="ea294-132">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="ea294-132">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="ea294-133">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="ea294-133">-SslCertificate</span></span>
<span data-ttu-id="ea294-134">Указывает объект сертификата SSL для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="ea294-134">Specifies the SSL certificate object for  the HTTP listener.</span></span>

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

### <span data-ttu-id="ea294-135">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="ea294-135">-SslCertificateId</span></span>
<span data-ttu-id="ea294-136">Задает ИД SSL-сертификата для прослушивателя HTTP.</span><span class="sxs-lookup"><span data-stu-id="ea294-136">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="ea294-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea294-137">CommonParameters</span></span>
<span data-ttu-id="ea294-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ea294-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea294-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea294-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea294-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ea294-140">INPUTS</span></span>

### <span data-ttu-id="ea294-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ea294-141">System.String</span></span>

## <span data-ttu-id="ea294-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea294-142">OUTPUTS</span></span>

### <span data-ttu-id="ea294-143">Microsoft. Azure. Commands. Network. Models. PSHttpListener</span><span class="sxs-lookup"><span data-stu-id="ea294-143">Microsoft.Azure.Commands.Network.Models.PSHttpListener</span></span>

## <span data-ttu-id="ea294-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="ea294-144">NOTES</span></span>

## <span data-ttu-id="ea294-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea294-145">RELATED LINKS</span></span>

[<span data-ttu-id="ea294-146">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ea294-146">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="ea294-147">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ea294-147">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="ea294-148">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ea294-148">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="ea294-149">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ea294-149">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


