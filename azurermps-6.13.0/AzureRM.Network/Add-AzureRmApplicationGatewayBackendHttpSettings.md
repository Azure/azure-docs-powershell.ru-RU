---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: 07820860f1a6a43f51f8436fa3ba28d6238de087
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567729"
---
# <span data-ttu-id="40d53-101">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="40d53-101">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="40d53-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="40d53-102">SYNOPSIS</span></span>
<span data-ttu-id="40d53-103">Добавляет серверные параметры HTTP в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="40d53-103">Adds back-end HTTP settings to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40d53-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="40d53-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-TrustedRootCertificate <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40d53-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40d53-105">DESCRIPTION</span></span>
<span data-ttu-id="40d53-106">Командлет Add-AzureRmApplicationGatewayBackendHttpSettings добавляет серверные параметры HTTP в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="40d53-106">The Add-AzureRmApplicationGatewayBackendHttpSettings cmdlet adds back-end HTTP settings to an application gateway.</span></span>
<span data-ttu-id="40d53-107">Серверные параметры HTTP применяются ко всем внутренним серверам в пуле.</span><span class="sxs-lookup"><span data-stu-id="40d53-107">Back-end HTTP settings are applied to all back-end servers in the pool.</span></span>

## <span data-ttu-id="40d53-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="40d53-108">EXAMPLES</span></span>

### <span data-ttu-id="40d53-109">Пример 1: Добавление межсерверных параметров HTTP в шлюз приложений</span><span class="sxs-lookup"><span data-stu-id="40d53-109">Example 1: Add back-end HTTP settings to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "HTTP" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="40d53-110">Первая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw. Вторая команда добавляет параметры HTTP с внутренними параметрами на шлюз приложения, настроив порт 88 и протокол на HTTP и указав параметры Setting02.</span><span class="sxs-lookup"><span data-stu-id="40d53-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.The second command adds back-end HTTP settings to the application gateway, setting the port to 88 and the protocol to HTTP and names the settings Setting02.</span></span>

## <span data-ttu-id="40d53-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="40d53-111">PARAMETERS</span></span>

### <span data-ttu-id="40d53-112">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="40d53-112">-AffinityCookieName</span></span>
<span data-ttu-id="40d53-113">Имя cookie-файла, используемое для файла cookie схожести</span><span class="sxs-lookup"><span data-stu-id="40d53-113">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="40d53-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="40d53-114">-ApplicationGateway</span></span>
<span data-ttu-id="40d53-115">Указывает имя шлюза приложений, для которого нужно добавить параметры.</span><span class="sxs-lookup"><span data-stu-id="40d53-115">Specifies the name of application gateway for which this cmdlet adds settings.</span></span>

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

### <span data-ttu-id="40d53-116">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="40d53-116">-AuthenticationCertificates</span></span>
<span data-ttu-id="40d53-117">Определяет сертификаты проверки подлинности для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="40d53-117">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40d53-118">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="40d53-118">-ConnectionDraining</span></span>
<span data-ttu-id="40d53-119">Сток подключений для ресурса внутренних HTTP-параметров.</span><span class="sxs-lookup"><span data-stu-id="40d53-119">Connection draining of the backend http settings resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40d53-120">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="40d53-120">-CookieBasedAffinity</span></span>
<span data-ttu-id="40d53-121">Указывает, следует ли включать или отключать сходство на основе файлов cookie для пула серверов внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="40d53-121">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="40d53-122">Допустимые значения этого параметра: "отключено", "включено".</span><span class="sxs-lookup"><span data-stu-id="40d53-122">The acceptable values for this parameter are: Disabled, Enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40d53-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40d53-123">-DefaultProfile</span></span>
<span data-ttu-id="40d53-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40d53-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40d53-125">-HostName</span><span class="sxs-lookup"><span data-stu-id="40d53-125">-HostName</span></span>
<span data-ttu-id="40d53-126">Задает заголовок hosts, который будет отправляться внутренним серверам.</span><span class="sxs-lookup"><span data-stu-id="40d53-126">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="40d53-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="40d53-127">-Name</span></span>
<span data-ttu-id="40d53-128">Задает имена серверных параметров HTTP, которые добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="40d53-128">Specifies the name of the back-end HTTP settings which this cmdlet adds.</span></span>

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

### <span data-ttu-id="40d53-129">-Path</span><span class="sxs-lookup"><span data-stu-id="40d53-129">-Path</span></span>
<span data-ttu-id="40d53-130">Путь, который должен использоваться в качестве префикса для всех HTTP-запросов.</span><span class="sxs-lookup"><span data-stu-id="40d53-130">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="40d53-131">Если для этого параметра не задано значение, путь не будет иметь префикса.</span><span class="sxs-lookup"><span data-stu-id="40d53-131">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="40d53-132">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="40d53-132">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="40d53-133">Флаг, если заголовок узла должен быть выбран из имени узла внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="40d53-133">Flag if host header should be picked from the host name of the backend server.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40d53-134">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="40d53-134">-Port</span></span>
<span data-ttu-id="40d53-135">Указывает порт пула серверов с внутренними интерфейсами.</span><span class="sxs-lookup"><span data-stu-id="40d53-135">Specifies the port of the back-end server pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40d53-136">-Зонд</span><span class="sxs-lookup"><span data-stu-id="40d53-136">-Probe</span></span>
<span data-ttu-id="40d53-137">Указывает зонд для связи с внутренним сервером.</span><span class="sxs-lookup"><span data-stu-id="40d53-137">Specifies a probe to associate with a back-end server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40d53-138">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="40d53-138">-ProbeId</span></span>
<span data-ttu-id="40d53-139">Указывает идентификатор зонда, который нужно связать с внутренним сервером.</span><span class="sxs-lookup"><span data-stu-id="40d53-139">Specifies the ID of the probe to associate with the back-end server.</span></span>

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

### <span data-ttu-id="40d53-140">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="40d53-140">-Protocol</span></span>
<span data-ttu-id="40d53-141">Указывает протокол для обмена данными между шлюзом приложения и внутренними серверами.</span><span class="sxs-lookup"><span data-stu-id="40d53-141">Specifies the protocol for communication between application gateway and back-end servers.</span></span>
<span data-ttu-id="40d53-142">Допустимые значения этого параметра: HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="40d53-142">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="40d53-143">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="40d53-143">-RequestTimeout</span></span>
<span data-ttu-id="40d53-144">Указывает значение времени ожидания запроса.</span><span class="sxs-lookup"><span data-stu-id="40d53-144">Specifies the request time-out value.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40d53-145">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="40d53-145">-TrustedRootCertificate</span></span>
<span data-ttu-id="40d53-146">Доверенные корневые сертификаты шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="40d53-146">Application gateway Trusted Root Certificates</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40d53-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40d53-147">CommonParameters</span></span>
<span data-ttu-id="40d53-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="40d53-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40d53-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40d53-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40d53-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="40d53-150">INPUTS</span></span>

### <span data-ttu-id="40d53-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="40d53-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="40d53-152">Параметры: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="40d53-152">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="40d53-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="40d53-153">OUTPUTS</span></span>

### <span data-ttu-id="40d53-154">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="40d53-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="40d53-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="40d53-155">NOTES</span></span>

## <span data-ttu-id="40d53-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40d53-156">RELATED LINKS</span></span>

[<span data-ttu-id="40d53-157">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="40d53-157">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="40d53-158">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="40d53-158">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="40d53-159">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="40d53-159">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="40d53-160">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="40d53-160">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

