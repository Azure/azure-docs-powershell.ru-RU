---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 325c4ca100bae93f88baaa9eb5c3fa6f2d3ecafe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730751"
---
# <span data-ttu-id="38f2b-101">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="38f2b-101">Add-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="38f2b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="38f2b-102">SYNOPSIS</span></span>
<span data-ttu-id="38f2b-103">Добавляет серверные параметры HTTP в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="38f2b-103">Adds back-end HTTP settings to an application gateway.</span></span>

## <span data-ttu-id="38f2b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="38f2b-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayBackendHttpSetting -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>] [-PickHostNameFromBackendAddress]
 [-HostName <String>] [-AffinityCookieName <String>] [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38f2b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="38f2b-105">DESCRIPTION</span></span>
<span data-ttu-id="38f2b-106">Командлет Add-AzApplicationGatewayBackendHttpSetting добавляет серверные параметры HTTP в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="38f2b-106">The Add-AzApplicationGatewayBackendHttpSetting cmdlet adds back-end HTTP settings to an application gateway.</span></span>
<span data-ttu-id="38f2b-107">Серверные параметры HTTP применяются ко всем внутренним серверам в пуле.</span><span class="sxs-lookup"><span data-stu-id="38f2b-107">Back-end HTTP settings are applied to all back-end servers in the pool.</span></span>

## <span data-ttu-id="38f2b-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="38f2b-108">EXAMPLES</span></span>

### <span data-ttu-id="38f2b-109">Пример 1: Добавление межсерверных параметров HTTP в шлюз приложений</span><span class="sxs-lookup"><span data-stu-id="38f2b-109">Example 1: Add back-end HTTP settings to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "HTTP" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="38f2b-110">Первая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw. Вторая команда добавляет параметры HTTP с внутренними параметрами на шлюз приложения, настроив порт 88 и протокол на HTTP и указав параметры Setting02.</span><span class="sxs-lookup"><span data-stu-id="38f2b-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.The second command adds back-end HTTP settings to the application gateway, setting the port to 88 and the protocol to HTTP and names the settings Setting02.</span></span>

## <span data-ttu-id="38f2b-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="38f2b-111">PARAMETERS</span></span>

### <span data-ttu-id="38f2b-112">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="38f2b-112">-AffinityCookieName</span></span>
<span data-ttu-id="38f2b-113">Имя cookie-файла, используемое для файла cookie схожести</span><span class="sxs-lookup"><span data-stu-id="38f2b-113">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="38f2b-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="38f2b-114">-ApplicationGateway</span></span>
<span data-ttu-id="38f2b-115">Указывает имя шлюза приложений, для которого нужно добавить параметры.</span><span class="sxs-lookup"><span data-stu-id="38f2b-115">Specifies the name of application gateway for which this cmdlet adds settings.</span></span>

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

### <span data-ttu-id="38f2b-116">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="38f2b-116">-AuthenticationCertificates</span></span>
<span data-ttu-id="38f2b-117">Определяет сертификаты проверки подлинности для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="38f2b-117">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38f2b-118">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="38f2b-118">-ConnectionDraining</span></span>
<span data-ttu-id="38f2b-119">Сток подключений для ресурса внутренних HTTP-параметров.</span><span class="sxs-lookup"><span data-stu-id="38f2b-119">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="38f2b-120">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="38f2b-120">-CookieBasedAffinity</span></span>
<span data-ttu-id="38f2b-121">Указывает, следует ли включать или отключать сходство на основе файлов cookie для пула серверов внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="38f2b-121">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="38f2b-122">Допустимые значения этого параметра: "отключено", "включено".</span><span class="sxs-lookup"><span data-stu-id="38f2b-122">The acceptable values for this parameter are: Disabled, Enabled.</span></span>

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

### <span data-ttu-id="38f2b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38f2b-123">-DefaultProfile</span></span>
<span data-ttu-id="38f2b-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="38f2b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38f2b-125">-HostName</span><span class="sxs-lookup"><span data-stu-id="38f2b-125">-HostName</span></span>
<span data-ttu-id="38f2b-126">Задает заголовок hosts, который будет отправляться внутренним серверам.</span><span class="sxs-lookup"><span data-stu-id="38f2b-126">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="38f2b-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="38f2b-127">-Name</span></span>
<span data-ttu-id="38f2b-128">Задает имена серверных параметров HTTP, которые добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="38f2b-128">Specifies the name of the back-end HTTP settings which this cmdlet adds.</span></span>

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

### <span data-ttu-id="38f2b-129">-Path</span><span class="sxs-lookup"><span data-stu-id="38f2b-129">-Path</span></span>
<span data-ttu-id="38f2b-130">Путь, который должен использоваться в качестве префикса для всех HTTP-запросов.</span><span class="sxs-lookup"><span data-stu-id="38f2b-130">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="38f2b-131">Если для этого параметра не задано значение, путь не будет иметь префикса.</span><span class="sxs-lookup"><span data-stu-id="38f2b-131">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="38f2b-132">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="38f2b-132">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="38f2b-133">Флаг, если заголовок узла должен быть выбран из имени узла внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="38f2b-133">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="38f2b-134">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="38f2b-134">-Port</span></span>
<span data-ttu-id="38f2b-135">Указывает порт пула серверов с внутренними интерфейсами.</span><span class="sxs-lookup"><span data-stu-id="38f2b-135">Specifies the port of the back-end server pool.</span></span>

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

### <span data-ttu-id="38f2b-136">-Зонд</span><span class="sxs-lookup"><span data-stu-id="38f2b-136">-Probe</span></span>
<span data-ttu-id="38f2b-137">Указывает зонд для связи с внутренним сервером.</span><span class="sxs-lookup"><span data-stu-id="38f2b-137">Specifies a probe to associate with a back-end server.</span></span>

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

### <span data-ttu-id="38f2b-138">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="38f2b-138">-ProbeId</span></span>
<span data-ttu-id="38f2b-139">Указывает идентификатор зонда, который нужно связать с внутренним сервером.</span><span class="sxs-lookup"><span data-stu-id="38f2b-139">Specifies the ID of the probe to associate with the back-end server.</span></span>

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

### <span data-ttu-id="38f2b-140">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="38f2b-140">-Protocol</span></span>
<span data-ttu-id="38f2b-141">Указывает протокол для обмена данными между шлюзом приложения и внутренними серверами.</span><span class="sxs-lookup"><span data-stu-id="38f2b-141">Specifies the protocol for communication between application gateway and back-end servers.</span></span>
<span data-ttu-id="38f2b-142">Допустимые значения этого параметра: HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="38f2b-142">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="38f2b-143">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="38f2b-143">-RequestTimeout</span></span>
<span data-ttu-id="38f2b-144">Указывает значение времени ожидания запроса.</span><span class="sxs-lookup"><span data-stu-id="38f2b-144">Specifies the request time-out value.</span></span>

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

### <span data-ttu-id="38f2b-145">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="38f2b-145">-TrustedRootCertificate</span></span>
<span data-ttu-id="38f2b-146">Доверенные корневые сертификаты шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="38f2b-146">Application gateway Trusted Root Certificates</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38f2b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38f2b-147">CommonParameters</span></span>
<span data-ttu-id="38f2b-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="38f2b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38f2b-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38f2b-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38f2b-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="38f2b-150">INPUTS</span></span>

### <span data-ttu-id="38f2b-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="38f2b-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="38f2b-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="38f2b-152">OUTPUTS</span></span>

### <span data-ttu-id="38f2b-153">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="38f2b-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="38f2b-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="38f2b-154">NOTES</span></span>

## <span data-ttu-id="38f2b-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="38f2b-155">RELATED LINKS</span></span>

[<span data-ttu-id="38f2b-156">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="38f2b-156">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="38f2b-157">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="38f2b-157">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="38f2b-158">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="38f2b-158">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="38f2b-159">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="38f2b-159">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

