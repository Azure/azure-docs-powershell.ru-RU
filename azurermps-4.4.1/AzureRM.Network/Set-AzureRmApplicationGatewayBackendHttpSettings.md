---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: 87d875881ce6086f033353dd4b37ba8a8098a96c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735143"
---
# <span data-ttu-id="fd302-101">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="fd302-101">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="fd302-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fd302-102">SYNOPSIS</span></span>
<span data-ttu-id="fd302-103">Обновляет параметры HTTP для шлюза приложения на сервер.</span><span class="sxs-lookup"><span data-stu-id="fd302-103">Updates back-end HTTP settings for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd302-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fd302-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd302-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd302-105">DESCRIPTION</span></span>
<span data-ttu-id="fd302-106">Командлет Set-AzureRmApplicationGatewayBackendHttpSettings обновляет параметры HTTP-протокола для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="fd302-106">The Set-AzureRmApplicationGatewayBackendHttpSettings cmdlet updates the back-end Hypertext Transfer Protocol (HTTP) settings for an Azure application gateway.</span></span>
<span data-ttu-id="fd302-107">Серверные параметры HTTP применяются ко всем внутренним серверам в пуле.</span><span class="sxs-lookup"><span data-stu-id="fd302-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="fd302-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fd302-108">EXAMPLES</span></span>

### <span data-ttu-id="fd302-109">Пример 1: Обновление параметров HTTP для шлюза приложения на сервер</span><span class="sxs-lookup"><span data-stu-id="fd302-109">Example 1: Update the back-end HTTP settings for an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "Http" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="fd302-110">Первая команда получает шлюз приложения с именем ApplicationGateway01, который принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="fd302-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="fd302-111">Вторая команда обновляет параметры HTTP для шлюза приложений в переменной $AppGw, чтобы использовать порт 88, протокол HTTP и допускает сходство на основе файлов cookie.</span><span class="sxs-lookup"><span data-stu-id="fd302-111">The second command updates the HTTP settings of the application gateway in the $AppGw variable to use port 88, the HTTP protocol and enables cookie-based affinity.</span></span>

## <span data-ttu-id="fd302-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fd302-112">PARAMETERS</span></span>

### <span data-ttu-id="fd302-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="fd302-113">-AffinityCookieName</span></span>
<span data-ttu-id="fd302-114">Имя cookie-файла, используемое для файла cookie схожести</span><span class="sxs-lookup"><span data-stu-id="fd302-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="fd302-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fd302-115">-ApplicationGateway</span></span>
<span data-ttu-id="fd302-116">Указывает объект шлюза приложения, с которым этот командлет связывает серверные параметры HTTP.</span><span class="sxs-lookup"><span data-stu-id="fd302-116">Specifies an application gateway object with which this cmdlet associates back-end HTTP settings.</span></span>

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

### <span data-ttu-id="fd302-117">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="fd302-117">-AuthenticationCertificates</span></span>
<span data-ttu-id="fd302-118">Определяет сертификаты проверки подлинности для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="fd302-118">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="fd302-119">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="fd302-119">-ConnectionDraining</span></span>
<span data-ttu-id="fd302-120">Сток подключений для ресурса внутренних HTTP-параметров.</span><span class="sxs-lookup"><span data-stu-id="fd302-120">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="fd302-121">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="fd302-121">-CookieBasedAffinity</span></span>
<span data-ttu-id="fd302-122">Указывает, следует ли включать или отключать сходство на основе файлов cookie для пула серверов внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="fd302-122">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="fd302-123">Допустимые значения этого параметра: "отключено" и "включено".</span><span class="sxs-lookup"><span data-stu-id="fd302-123">The acceptable values for this parameter are: Disabled or Enabled.</span></span>

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

### <span data-ttu-id="fd302-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="fd302-124">-HostName</span></span>
<span data-ttu-id="fd302-125">Задает заголовок hosts, который будет отправляться внутренним серверам.</span><span class="sxs-lookup"><span data-stu-id="fd302-125">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="fd302-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fd302-126">-Name</span></span>
<span data-ttu-id="fd302-127">Указывает имя объекта параметров HTTP для серверного элемента.</span><span class="sxs-lookup"><span data-stu-id="fd302-127">Specifies the name of the back-end HTTP settings object.</span></span>

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

### <span data-ttu-id="fd302-128">-Path</span><span class="sxs-lookup"><span data-stu-id="fd302-128">-Path</span></span>
<span data-ttu-id="fd302-129">Путь, который должен использоваться в качестве префикса для всех HTTP-запросов.</span><span class="sxs-lookup"><span data-stu-id="fd302-129">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="fd302-130">Если для этого параметра не задано значение, путь не будет иметь префикса.</span><span class="sxs-lookup"><span data-stu-id="fd302-130">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="fd302-131">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="fd302-131">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="fd302-132">Флаг, если заголовок узла должен быть выбран из имени узла внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="fd302-132">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="fd302-133">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="fd302-133">-Port</span></span>
<span data-ttu-id="fd302-134">Указывает порт, который будет использоваться для каждого сервера в пуле на внутреннем сервере.</span><span class="sxs-lookup"><span data-stu-id="fd302-134">Specifies the port to use for each server in the back-end server pool.</span></span>

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

### <span data-ttu-id="fd302-135">-Зонд</span><span class="sxs-lookup"><span data-stu-id="fd302-135">-Probe</span></span>
<span data-ttu-id="fd302-136">Указывает зонд для связи с параметрами HTTP для веб-части.</span><span class="sxs-lookup"><span data-stu-id="fd302-136">Specifies a probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="fd302-137">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="fd302-137">-ProbeEnabled</span></span>
<span data-ttu-id="fd302-138">Флажок, если зонд должен быть включен.</span><span class="sxs-lookup"><span data-stu-id="fd302-138">Flag if probe should be enabled.</span></span>

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

### <span data-ttu-id="fd302-139">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="fd302-139">-ProbeId</span></span>
<span data-ttu-id="fd302-140">Указывает идентификатор зонда, который нужно связать с параметрами HTTP для серверного элемента.</span><span class="sxs-lookup"><span data-stu-id="fd302-140">Specifies the ID of the probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="fd302-141">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="fd302-141">-Protocol</span></span>
<span data-ttu-id="fd302-142">Указывает протокол для обмена данными между шлюзом приложения и внутренними серверами.</span><span class="sxs-lookup"><span data-stu-id="fd302-142">Specifies the protocol to use for communication between the application gateway and back-end servers.</span></span>
<span data-ttu-id="fd302-143">Допустимые значения этого параметра: HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="fd302-143">The acceptable values for this parameter are: Http and Https.</span></span>
<span data-ttu-id="fd302-144">Этот параметр учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="fd302-144">This parameter is case-sensitive.</span></span>

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

### <span data-ttu-id="fd302-145">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="fd302-145">-RequestTimeout</span></span>
<span data-ttu-id="fd302-146">Указывает значение времени ожидания запроса.</span><span class="sxs-lookup"><span data-stu-id="fd302-146">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="fd302-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd302-147">-DefaultProfile</span></span>
<span data-ttu-id="fd302-148">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fd302-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd302-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd302-149">CommonParameters</span></span>
<span data-ttu-id="fd302-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fd302-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd302-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd302-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd302-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fd302-152">INPUTS</span></span>

### <span data-ttu-id="fd302-153">System. String</span><span class="sxs-lookup"><span data-stu-id="fd302-153">System.String</span></span>

## <span data-ttu-id="fd302-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd302-154">OUTPUTS</span></span>

### <span data-ttu-id="fd302-155">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fd302-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fd302-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="fd302-156">NOTES</span></span>

## <span data-ttu-id="fd302-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd302-157">RELATED LINKS</span></span>

[<span data-ttu-id="fd302-158">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="fd302-158">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="fd302-159">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="fd302-159">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="fd302-160">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="fd302-160">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="fd302-161">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="fd302-161">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

