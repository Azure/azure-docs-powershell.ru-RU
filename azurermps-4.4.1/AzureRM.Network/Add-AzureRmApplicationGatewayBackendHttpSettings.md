---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: add18f52e46f39c639c87526d948c750bb22fa93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568741"
---
# <span data-ttu-id="c2531-101">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c2531-101">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="c2531-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c2531-102">SYNOPSIS</span></span>
<span data-ttu-id="c2531-103">Добавляет серверные параметры HTTP в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="c2531-103">Adds back-end HTTP settings to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2531-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c2531-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2531-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2531-105">DESCRIPTION</span></span>
<span data-ttu-id="c2531-106">Командлет Add-AzureRmApplicationGatewayBackendHttpSettings добавляет серверные параметры HTTP в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="c2531-106">The Add-AzureRmApplicationGatewayBackendHttpSettings cmdlet adds back-end HTTP settings to an application gateway.</span></span>

<span data-ttu-id="c2531-107">Серверные параметры HTTP применяются ко всем внутренним серверам в пуле.</span><span class="sxs-lookup"><span data-stu-id="c2531-107">Back-end HTTP settings are applied to all back-end servers in the pool.</span></span>

## <span data-ttu-id="c2531-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c2531-108">EXAMPLES</span></span>

### <span data-ttu-id="c2531-109">Пример 1: Добавление межсерверных параметров HTTP в шлюз приложений</span><span class="sxs-lookup"><span data-stu-id="c2531-109">Example 1: Add back-end HTTP settings to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "HTTP" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="c2531-110">Первая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw. Вторая команда добавляет параметры HTTP с внутренними параметрами на шлюз приложения, настроив порт 88 и протокол на HTTP и указав параметры Setting02.</span><span class="sxs-lookup"><span data-stu-id="c2531-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.The second command adds back-end HTTP settings to the application gateway, setting the port to 88 and the protocol to HTTP and names the settings Setting02.</span></span>

## <span data-ttu-id="c2531-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c2531-111">PARAMETERS</span></span>

### <span data-ttu-id="c2531-112">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="c2531-112">-AffinityCookieName</span></span>
<span data-ttu-id="c2531-113">Имя cookie-файла, используемое для файла cookie схожести</span><span class="sxs-lookup"><span data-stu-id="c2531-113">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="c2531-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c2531-114">-ApplicationGateway</span></span>
<span data-ttu-id="c2531-115">Указывает имя шлюза приложений, для которого нужно добавить параметры.</span><span class="sxs-lookup"><span data-stu-id="c2531-115">Specifies the name of application gateway for which this cmdlet adds settings.</span></span>

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

### <span data-ttu-id="c2531-116">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="c2531-116">-AuthenticationCertificates</span></span>
<span data-ttu-id="c2531-117">Определяет сертификаты проверки подлинности для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="c2531-117">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="c2531-118">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c2531-118">-ConnectionDraining</span></span>
<span data-ttu-id="c2531-119">Сток подключений для ресурса внутренних HTTP-параметров.</span><span class="sxs-lookup"><span data-stu-id="c2531-119">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="c2531-120">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="c2531-120">-CookieBasedAffinity</span></span>
<span data-ttu-id="c2531-121">Указывает, следует ли включать или отключать сходство на основе файлов cookie для пула серверов внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="c2531-121">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="c2531-122">Допустимые значения этого параметра: "отключено", "включено".</span><span class="sxs-lookup"><span data-stu-id="c2531-122">The acceptable values for this parameter are: Disabled, Enabled.</span></span>

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

### <span data-ttu-id="c2531-123">-HostName</span><span class="sxs-lookup"><span data-stu-id="c2531-123">-HostName</span></span>
<span data-ttu-id="c2531-124">Задает заголовок hosts, который будет отправляться внутренним серверам.</span><span class="sxs-lookup"><span data-stu-id="c2531-124">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="c2531-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c2531-125">-Name</span></span>
<span data-ttu-id="c2531-126">Задает имена серверных параметров HTTP, которые добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c2531-126">Specifies the name of the back-end HTTP settings which this cmdlet adds.</span></span>

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

### <span data-ttu-id="c2531-127">-Path</span><span class="sxs-lookup"><span data-stu-id="c2531-127">-Path</span></span>
<span data-ttu-id="c2531-128">Путь, который должен использоваться в качестве префикса для всех HTTP-запросов.</span><span class="sxs-lookup"><span data-stu-id="c2531-128">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="c2531-129">Если для этого параметра не задано значение, путь не будет иметь префикса.</span><span class="sxs-lookup"><span data-stu-id="c2531-129">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="c2531-130">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="c2531-130">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="c2531-131">Флаг, если заголовок узла должен быть выбран из имени узла внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="c2531-131">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="c2531-132">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="c2531-132">-Port</span></span>
<span data-ttu-id="c2531-133">Указывает порт пула серверов с внутренними интерфейсами.</span><span class="sxs-lookup"><span data-stu-id="c2531-133">Specifies the port of the back-end server pool.</span></span>

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

### <span data-ttu-id="c2531-134">-Зонд</span><span class="sxs-lookup"><span data-stu-id="c2531-134">-Probe</span></span>
<span data-ttu-id="c2531-135">Указывает зонд для связи с внутренним сервером.</span><span class="sxs-lookup"><span data-stu-id="c2531-135">Specifies a probe to associate with a back-end server.</span></span>

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

### <span data-ttu-id="c2531-136">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="c2531-136">-ProbeEnabled</span></span>
<span data-ttu-id="c2531-137">Флажок, если зонд должен быть включен.</span><span class="sxs-lookup"><span data-stu-id="c2531-137">Flag if probe should be enabled.</span></span>

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

### <span data-ttu-id="c2531-138">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="c2531-138">-ProbeId</span></span>
<span data-ttu-id="c2531-139">Указывает идентификатор зонда, который нужно связать с внутренним сервером.</span><span class="sxs-lookup"><span data-stu-id="c2531-139">Specifies the ID of the probe to associate with the back-end server.</span></span>

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

### <span data-ttu-id="c2531-140">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="c2531-140">-Protocol</span></span>
<span data-ttu-id="c2531-141">Указывает протокол для обмена данными между шлюзом приложения и внутренними серверами.</span><span class="sxs-lookup"><span data-stu-id="c2531-141">Specifies the protocol for communication between application gateway and back-end servers.</span></span>
<span data-ttu-id="c2531-142">Допустимые значения этого параметра: HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c2531-142">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="c2531-143">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="c2531-143">-RequestTimeout</span></span>
<span data-ttu-id="c2531-144">Указывает значение времени ожидания запроса.</span><span class="sxs-lookup"><span data-stu-id="c2531-144">Specifies the request time-out value.</span></span>

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

### <span data-ttu-id="c2531-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2531-145">-DefaultProfile</span></span>
<span data-ttu-id="c2531-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2531-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2531-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2531-147">CommonParameters</span></span>
<span data-ttu-id="c2531-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c2531-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2531-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2531-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2531-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c2531-150">INPUTS</span></span>

### <span data-ttu-id="c2531-151">System. String</span><span class="sxs-lookup"><span data-stu-id="c2531-151">System.String</span></span>

## <span data-ttu-id="c2531-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2531-152">OUTPUTS</span></span>

### <span data-ttu-id="c2531-153">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c2531-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c2531-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="c2531-154">NOTES</span></span>

## <span data-ttu-id="c2531-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2531-155">RELATED LINKS</span></span>

[<span data-ttu-id="c2531-156">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c2531-156">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="c2531-157">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c2531-157">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="c2531-158">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c2531-158">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="c2531-159">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c2531-159">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

