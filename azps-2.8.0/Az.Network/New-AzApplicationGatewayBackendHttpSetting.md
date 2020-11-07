---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 014309ceb54b1d16b2a55c97b03887deaf4ef281
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902794"
---
# <span data-ttu-id="2d36b-101">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="2d36b-101">New-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="2d36b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2d36b-102">SYNOPSIS</span></span>
<span data-ttu-id="2d36b-103">Создает для шлюза приложений серверный параметр HTTP "внутренний сервер".</span><span class="sxs-lookup"><span data-stu-id="2d36b-103">Creates back-end HTTP setting for an application gateway.</span></span>

## <span data-ttu-id="2d36b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2d36b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayBackendHttpSetting -Name <String> -Port <Int32> -Protocol <String>
 -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>] [-PickHostNameFromBackendAddress]
 [-HostName <String>] [-AffinityCookieName <String>] [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d36b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d36b-105">DESCRIPTION</span></span>
<span data-ttu-id="2d36b-106">Командлет New-AzApplicationGatewayBackendHttpSetting создает серверные параметры HTTP для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="2d36b-106">The New-AzApplicationGatewayBackendHttpSetting cmdlet creates back-end HTTP settings for an application gateway.</span></span>
<span data-ttu-id="2d36b-107">Серверные параметры HTTP применяются ко всем внутренним серверам в пуле.</span><span class="sxs-lookup"><span data-stu-id="2d36b-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="2d36b-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2d36b-108">EXAMPLES</span></span>

### <span data-ttu-id="2d36b-109">Пример 1: Создание HTTP-параметров для серверной части</span><span class="sxs-lookup"><span data-stu-id="2d36b-109">Example 1: Create back-end HTTP settings</span></span>
```
PS C:\>$Setting = New-AzApplicationGatewayBackendHttpSetting -Name "Setting01" -Port 80 -Protocol Http -CookieBasedAffinity Disabled
```

<span data-ttu-id="2d36b-110">Эта команда создает серверные параметры HTTP с именем Setting01 на порте 80, используя HTTP-протокол с отключенным сходством на основе файлов cookie.</span><span class="sxs-lookup"><span data-stu-id="2d36b-110">This command creates back-end HTTP settings named Setting01 on port 80, using the HTTP protocol, with cookie-based affinity disabled.</span></span>
<span data-ttu-id="2d36b-111">Параметры хранятся в переменной $Setting.</span><span class="sxs-lookup"><span data-stu-id="2d36b-111">The settings are stored in the $Setting variable.</span></span>

## <span data-ttu-id="2d36b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2d36b-112">PARAMETERS</span></span>

### <span data-ttu-id="2d36b-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="2d36b-113">-AffinityCookieName</span></span>
<span data-ttu-id="2d36b-114">Имя cookie-файла, используемое для файла cookie схожести</span><span class="sxs-lookup"><span data-stu-id="2d36b-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="2d36b-115">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="2d36b-115">-AuthenticationCertificates</span></span>
<span data-ttu-id="2d36b-116">Определяет сертификаты проверки подлинности для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2d36b-116">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="2d36b-117">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="2d36b-117">-ConnectionDraining</span></span>
<span data-ttu-id="2d36b-118">Сток подключений для ресурса внутренних HTTP-параметров.</span><span class="sxs-lookup"><span data-stu-id="2d36b-118">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="2d36b-119">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="2d36b-119">-CookieBasedAffinity</span></span>
<span data-ttu-id="2d36b-120">Указывает, следует ли включить или отключить сходство на основе файлов cookie для серверного пула.</span><span class="sxs-lookup"><span data-stu-id="2d36b-120">Specifies whether cookie-based affinity should be enabled or disabled for the back-end server pool.</span></span>

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

### <span data-ttu-id="2d36b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d36b-121">-DefaultProfile</span></span>
<span data-ttu-id="2d36b-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2d36b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d36b-123">-HostName</span><span class="sxs-lookup"><span data-stu-id="2d36b-123">-HostName</span></span>
<span data-ttu-id="2d36b-124">Задает заголовок hosts, который будет отправляться внутренним серверам.</span><span class="sxs-lookup"><span data-stu-id="2d36b-124">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="2d36b-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2d36b-125">-Name</span></span>
<span data-ttu-id="2d36b-126">Задает имена серверных параметров HTTP, создаваемых этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="2d36b-126">Specifies the name of the back-end HTTP settings that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2d36b-127">-Path</span><span class="sxs-lookup"><span data-stu-id="2d36b-127">-Path</span></span>
<span data-ttu-id="2d36b-128">Путь, который должен использоваться в качестве префикса для всех HTTP-запросов.</span><span class="sxs-lookup"><span data-stu-id="2d36b-128">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="2d36b-129">Если для этого параметра не задано значение, путь не будет иметь префикса.</span><span class="sxs-lookup"><span data-stu-id="2d36b-129">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="2d36b-130">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="2d36b-130">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="2d36b-131">Флаг, если заголовок узла должен быть выбран из имени узла внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="2d36b-131">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="2d36b-132">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="2d36b-132">-Port</span></span>
<span data-ttu-id="2d36b-133">Указывает порт пула серверов с внутренними интерфейсами.</span><span class="sxs-lookup"><span data-stu-id="2d36b-133">Specifies the port of the back-end server pool.</span></span>

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

### <span data-ttu-id="2d36b-134">-Зонд</span><span class="sxs-lookup"><span data-stu-id="2d36b-134">-Probe</span></span>
<span data-ttu-id="2d36b-135">Указывает зонд для связи с серверным пулом.</span><span class="sxs-lookup"><span data-stu-id="2d36b-135">Specifies a probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="2d36b-136">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="2d36b-136">-ProbeId</span></span>
<span data-ttu-id="2d36b-137">Указывает идентификатор зонда для связи с серверным пулом.</span><span class="sxs-lookup"><span data-stu-id="2d36b-137">Specifies the ID of the probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="2d36b-138">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="2d36b-138">-Protocol</span></span>
<span data-ttu-id="2d36b-139">Указывает протокол для обмена данными между шлюзом приложения и внутренними серверами.</span><span class="sxs-lookup"><span data-stu-id="2d36b-139">Specifies the protocol to use for communication between the application gateway and the back-end servers.</span></span>
<span data-ttu-id="2d36b-140">Допустимые значения этого параметра: HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="2d36b-140">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="2d36b-141">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="2d36b-141">-RequestTimeout</span></span>
<span data-ttu-id="2d36b-142">Указывает значение времени ожидания запроса.</span><span class="sxs-lookup"><span data-stu-id="2d36b-142">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="2d36b-143">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2d36b-143">-TrustedRootCertificate</span></span>
<span data-ttu-id="2d36b-144">Доверенные корневые сертификаты шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="2d36b-144">Application gateway Trusted Root Certificates</span></span>

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

### <span data-ttu-id="2d36b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d36b-145">CommonParameters</span></span>
<span data-ttu-id="2d36b-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2d36b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d36b-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d36b-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d36b-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2d36b-148">INPUTS</span></span>

### <span data-ttu-id="2d36b-149">Ничего</span><span class="sxs-lookup"><span data-stu-id="2d36b-149">None</span></span>

## <span data-ttu-id="2d36b-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d36b-150">OUTPUTS</span></span>

### <span data-ttu-id="2d36b-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="2d36b-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="2d36b-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="2d36b-152">NOTES</span></span>

## <span data-ttu-id="2d36b-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d36b-153">RELATED LINKS</span></span>

[<span data-ttu-id="2d36b-154">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="2d36b-154">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="2d36b-155">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="2d36b-155">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="2d36b-156">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="2d36b-156">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="2d36b-157">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="2d36b-157">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

