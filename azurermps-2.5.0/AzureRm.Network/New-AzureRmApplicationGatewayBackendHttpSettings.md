---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
ms.openlocfilehash: f4c4ccdce719b3593968f0429d5e02936d052cc4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914066"
---
# <span data-ttu-id="e339a-101">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e339a-101">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="e339a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e339a-102">SYNOPSIS</span></span>
<span data-ttu-id="e339a-103">Создает серверные параметры HTTP для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="e339a-103">Creates back-end HTTP settings for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e339a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e339a-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayBackendHttpSettings -Name <String> -Port <Int32> -Protocol <String>
 -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e339a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e339a-105">DESCRIPTION</span></span>
<span data-ttu-id="e339a-106">Командлет New-AzureRmApplicationGatewayBackendHttpSettings создает серверные параметры HTTP для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="e339a-106">The New-AzureRmApplicationGatewayBackendHttpSettings cmdlet creates back-end HTTP settings for an application gateway.</span></span>
<span data-ttu-id="e339a-107">Серверные параметры HTTP применяются ко всем внутренним серверам в пуле.</span><span class="sxs-lookup"><span data-stu-id="e339a-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="e339a-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e339a-108">EXAMPLES</span></span>

### <span data-ttu-id="e339a-109">Пример 1: Создание HTTP-параметров для серверной части</span><span class="sxs-lookup"><span data-stu-id="e339a-109">Example 1: Create back-end HTTP settings</span></span>
```
PS C:\>$Setting = New-AzureRmApplicationGatewayBackendHttpSettings -Name "Setting01" -Port 80 -Protocol Http -CookieBasedAffinity Disabled
```

<span data-ttu-id="e339a-110">Эта команда создает серверные параметры HTTP с именем Setting01 на порте 80, используя HTTP-протокол с отключенным сходством на основе файлов cookie.</span><span class="sxs-lookup"><span data-stu-id="e339a-110">This command creates back-end HTTP settings named Setting01 on port 80, using the HTTP protocol, with cookie-based affinity disabled.</span></span>
<span data-ttu-id="e339a-111">Параметры хранятся в переменной $Setting.</span><span class="sxs-lookup"><span data-stu-id="e339a-111">The settings are stored in the $Setting variable.</span></span>

## <span data-ttu-id="e339a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e339a-112">PARAMETERS</span></span>

### <span data-ttu-id="e339a-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="e339a-113">-AffinityCookieName</span></span>
<span data-ttu-id="e339a-114">Имя cookie-файла, используемое для файла cookie схожести</span><span class="sxs-lookup"><span data-stu-id="e339a-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="e339a-115">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="e339a-115">-AuthenticationCertificates</span></span>
<span data-ttu-id="e339a-116">Определяет сертификаты проверки подлинности для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="e339a-116">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="e339a-117">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="e339a-117">-ConnectionDraining</span></span>
<span data-ttu-id="e339a-118">Сток подключений для ресурса внутренних HTTP-параметров.</span><span class="sxs-lookup"><span data-stu-id="e339a-118">Connection draining of the backend http settings resource.</span></span>

```yaml
Type: PSApplicationGatewayConnectionDraining
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e339a-119">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="e339a-119">-CookieBasedAffinity</span></span>
<span data-ttu-id="e339a-120">Указывает, следует ли включить или отключить сходство на основе файлов cookie для серверного пула.</span><span class="sxs-lookup"><span data-stu-id="e339a-120">Specifies whether cookie-based affinity should be enabled or disabled for the back-end server pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e339a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e339a-121">-DefaultProfile</span></span>
<span data-ttu-id="e339a-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e339a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e339a-123">-HostName</span><span class="sxs-lookup"><span data-stu-id="e339a-123">-HostName</span></span>
<span data-ttu-id="e339a-124">Задает заголовок hosts, который будет отправляться внутренним серверам.</span><span class="sxs-lookup"><span data-stu-id="e339a-124">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="e339a-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e339a-125">-Name</span></span>
<span data-ttu-id="e339a-126">Задает имена серверных параметров HTTP, создаваемых этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="e339a-126">Specifies the name of the back-end HTTP settings that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e339a-127">-Path</span><span class="sxs-lookup"><span data-stu-id="e339a-127">-Path</span></span>
<span data-ttu-id="e339a-128">Путь, который должен использоваться в качестве префикса для всех HTTP-запросов.</span><span class="sxs-lookup"><span data-stu-id="e339a-128">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="e339a-129">Если для этого параметра не задано значение, путь не будет иметь префикса.</span><span class="sxs-lookup"><span data-stu-id="e339a-129">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="e339a-130">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="e339a-130">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="e339a-131">Флаг, если заголовок узла должен быть выбран из имени узла внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="e339a-131">Flag if host header should be picked from the host name of the backend server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e339a-132">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="e339a-132">-Port</span></span>
<span data-ttu-id="e339a-133">Указывает порт пула серверов с внутренними интерфейсами.</span><span class="sxs-lookup"><span data-stu-id="e339a-133">Specifies the port of the back-end server pool.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e339a-134">-Зонд</span><span class="sxs-lookup"><span data-stu-id="e339a-134">-Probe</span></span>
<span data-ttu-id="e339a-135">Указывает зонд для связи с серверным пулом.</span><span class="sxs-lookup"><span data-stu-id="e339a-135">Specifies a probe to associate with the back-end server pool.</span></span>

```yaml
Type: PSApplicationGatewayProbe
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e339a-136">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="e339a-136">-ProbeEnabled</span></span>
<span data-ttu-id="e339a-137">Флажок, если зонд должен быть включен.</span><span class="sxs-lookup"><span data-stu-id="e339a-137">Flag if probe should be enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e339a-138">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="e339a-138">-ProbeId</span></span>
<span data-ttu-id="e339a-139">Указывает идентификатор зонда для связи с серверным пулом.</span><span class="sxs-lookup"><span data-stu-id="e339a-139">Specifies the ID of the probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="e339a-140">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="e339a-140">-Protocol</span></span>
<span data-ttu-id="e339a-141">Указывает протокол для обмена данными между шлюзом приложения и внутренними серверами.</span><span class="sxs-lookup"><span data-stu-id="e339a-141">Specifies the protocol to use for communication between the application gateway and the back-end servers.</span></span>
<span data-ttu-id="e339a-142">Допустимые значения этого параметра: HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e339a-142">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="e339a-143">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="e339a-143">-RequestTimeout</span></span>
<span data-ttu-id="e339a-144">Указывает значение времени ожидания запроса.</span><span class="sxs-lookup"><span data-stu-id="e339a-144">Specifies a request time-out value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e339a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e339a-145">CommonParameters</span></span>
<span data-ttu-id="e339a-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e339a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e339a-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e339a-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e339a-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e339a-148">INPUTS</span></span>

### <span data-ttu-id="e339a-149">System. String</span><span class="sxs-lookup"><span data-stu-id="e339a-149">System.String</span></span>

## <span data-ttu-id="e339a-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e339a-150">OUTPUTS</span></span>

### <span data-ttu-id="e339a-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e339a-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="e339a-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="e339a-152">NOTES</span></span>

## <span data-ttu-id="e339a-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e339a-153">RELATED LINKS</span></span>

[<span data-ttu-id="e339a-154">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e339a-154">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="e339a-155">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e339a-155">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="e339a-156">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e339a-156">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="e339a-157">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e339a-157">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

