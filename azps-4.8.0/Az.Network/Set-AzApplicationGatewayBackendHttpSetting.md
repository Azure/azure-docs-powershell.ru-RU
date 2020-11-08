---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 35742a6dc65bd84359d08f4e30533a0a49488053
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235993"
---
# <span data-ttu-id="a045a-101">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a045a-101">Set-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="a045a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a045a-102">SYNOPSIS</span></span>
<span data-ttu-id="a045a-103">Обновляет параметры HTTP для шлюза приложения на сервер.</span><span class="sxs-lookup"><span data-stu-id="a045a-103">Updates back-end HTTP settings for an application gateway.</span></span>

## <span data-ttu-id="a045a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a045a-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>] [-PickHostNameFromBackendAddress]
 [-HostName <String>] [-AffinityCookieName <String>] [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a045a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a045a-105">DESCRIPTION</span></span>
<span data-ttu-id="a045a-106">Командлет Set-AzApplicationGatewayBackendHttpSetting обновляет параметры HTTP-протокола для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="a045a-106">The Set-AzApplicationGatewayBackendHttpSetting cmdlet updates the back-end Hypertext Transfer Protocol (HTTP) settings for an Azure application gateway.</span></span>
<span data-ttu-id="a045a-107">Серверные параметры HTTP применяются ко всем внутренним серверам в пуле.</span><span class="sxs-lookup"><span data-stu-id="a045a-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="a045a-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a045a-108">EXAMPLES</span></span>

### <span data-ttu-id="a045a-109">Пример 1: Обновление параметров HTTP для шлюза приложения на сервер</span><span class="sxs-lookup"><span data-stu-id="a045a-109">Example 1: Update the back-end HTTP settings for an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "Http" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="a045a-110">Первая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="a045a-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a045a-111">Вторая команда обновляет параметры HTTP для шлюза приложений в переменной $AppGw, чтобы использовать порт 88, протокол HTTP и допускает сходство на основе файлов cookie.</span><span class="sxs-lookup"><span data-stu-id="a045a-111">The second command updates the HTTP settings of the application gateway in the $AppGw variable to use port 88, the HTTP protocol and enables cookie-based affinity.</span></span>

## <span data-ttu-id="a045a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a045a-112">PARAMETERS</span></span>

### <span data-ttu-id="a045a-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="a045a-113">-AffinityCookieName</span></span>
<span data-ttu-id="a045a-114">Имя cookie-файла, используемое для файла cookie схожести</span><span class="sxs-lookup"><span data-stu-id="a045a-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="a045a-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a045a-115">-ApplicationGateway</span></span>
<span data-ttu-id="a045a-116">Указывает объект шлюза приложения, с которым этот командлет связывает серверные параметры HTTP.</span><span class="sxs-lookup"><span data-stu-id="a045a-116">Specifies an application gateway object with which this cmdlet associates back-end HTTP settings.</span></span>

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

### <span data-ttu-id="a045a-117">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="a045a-117">-AuthenticationCertificates</span></span>
<span data-ttu-id="a045a-118">Определяет сертификаты проверки подлинности для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="a045a-118">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="a045a-119">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="a045a-119">-ConnectionDraining</span></span>
<span data-ttu-id="a045a-120">Сток подключений для ресурса внутренних HTTP-параметров.</span><span class="sxs-lookup"><span data-stu-id="a045a-120">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="a045a-121">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="a045a-121">-CookieBasedAffinity</span></span>
<span data-ttu-id="a045a-122">Указывает, следует ли включать или отключать сходство на основе файлов cookie для пула серверов внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="a045a-122">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="a045a-123">Допустимые значения этого параметра: "отключено" и "включено".</span><span class="sxs-lookup"><span data-stu-id="a045a-123">The acceptable values for this parameter are: Disabled or Enabled.</span></span>

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

### <span data-ttu-id="a045a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a045a-124">-DefaultProfile</span></span>
<span data-ttu-id="a045a-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a045a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a045a-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="a045a-126">-HostName</span></span>
<span data-ttu-id="a045a-127">Задает заголовок hosts, который будет отправляться внутренним серверам.</span><span class="sxs-lookup"><span data-stu-id="a045a-127">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="a045a-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a045a-128">-Name</span></span>
<span data-ttu-id="a045a-129">Указывает имя объекта параметров HTTP для серверного элемента.</span><span class="sxs-lookup"><span data-stu-id="a045a-129">Specifies the name of the back-end HTTP settings object.</span></span>

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

### <span data-ttu-id="a045a-130">-Path</span><span class="sxs-lookup"><span data-stu-id="a045a-130">-Path</span></span>
<span data-ttu-id="a045a-131">Путь, который должен использоваться в качестве префикса для всех HTTP-запросов.</span><span class="sxs-lookup"><span data-stu-id="a045a-131">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="a045a-132">Если для этого параметра не задано значение, путь не будет иметь префикса.</span><span class="sxs-lookup"><span data-stu-id="a045a-132">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="a045a-133">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="a045a-133">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="a045a-134">Флаг, если заголовок узла должен быть выбран из имени узла внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="a045a-134">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="a045a-135">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="a045a-135">-Port</span></span>
<span data-ttu-id="a045a-136">Указывает порт, который будет использоваться для каждого сервера в пуле на внутреннем сервере.</span><span class="sxs-lookup"><span data-stu-id="a045a-136">Specifies the port to use for each server in the back-end server pool.</span></span>

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

### <span data-ttu-id="a045a-137">-Зонд</span><span class="sxs-lookup"><span data-stu-id="a045a-137">-Probe</span></span>
<span data-ttu-id="a045a-138">Указывает зонд для связи с параметрами HTTP для веб-части.</span><span class="sxs-lookup"><span data-stu-id="a045a-138">Specifies a probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="a045a-139">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="a045a-139">-ProbeId</span></span>
<span data-ttu-id="a045a-140">Указывает идентификатор зонда, который нужно связать с параметрами HTTP для серверного элемента.</span><span class="sxs-lookup"><span data-stu-id="a045a-140">Specifies the ID of the probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="a045a-141">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="a045a-141">-Protocol</span></span>
<span data-ttu-id="a045a-142">Указывает протокол для обмена данными между шлюзом приложения и внутренними серверами.</span><span class="sxs-lookup"><span data-stu-id="a045a-142">Specifies the protocol to use for communication between the application gateway and back-end servers.</span></span>
<span data-ttu-id="a045a-143">Допустимые значения этого параметра: HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="a045a-143">The acceptable values for this parameter are: Http and Https.</span></span>
<span data-ttu-id="a045a-144">Этот параметр учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="a045a-144">This parameter is case-sensitive.</span></span>

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

### <span data-ttu-id="a045a-145">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="a045a-145">-RequestTimeout</span></span>
<span data-ttu-id="a045a-146">Указывает значение времени ожидания запроса.</span><span class="sxs-lookup"><span data-stu-id="a045a-146">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="a045a-147">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a045a-147">-TrustedRootCertificate</span></span>
<span data-ttu-id="a045a-148">Доверенные корневые сертификаты шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="a045a-148">Application gateway Trusted Root Certificates</span></span>

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

### <span data-ttu-id="a045a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a045a-149">CommonParameters</span></span>
<span data-ttu-id="a045a-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a045a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a045a-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a045a-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a045a-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a045a-152">INPUTS</span></span>

### <span data-ttu-id="a045a-153">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a045a-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a045a-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a045a-154">OUTPUTS</span></span>

### <span data-ttu-id="a045a-155">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a045a-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a045a-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="a045a-156">NOTES</span></span>

## <span data-ttu-id="a045a-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a045a-157">RELATED LINKS</span></span>

[<span data-ttu-id="a045a-158">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a045a-158">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="a045a-159">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a045a-159">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="a045a-160">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a045a-160">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="a045a-161">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a045a-161">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

