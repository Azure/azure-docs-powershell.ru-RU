---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 35742a6dc65bd84359d08f4e30533a0a49488053
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506835"
---
# <span data-ttu-id="a95a8-101">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a95a8-101">Set-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="a95a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a95a8-102">SYNOPSIS</span></span>
<span data-ttu-id="a95a8-103">Обновление back-end HTTP-параметров шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="a95a8-103">Updates back-end HTTP settings for an application gateway.</span></span>

## <span data-ttu-id="a95a8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a95a8-104">SYNTAX</span></span>

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

## <span data-ttu-id="a95a8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a95a8-105">DESCRIPTION</span></span>
<span data-ttu-id="a95a8-106">Этот Set-AzApplicationGatewayBackendHttpSetting обновляет параметры протокола HTTP для шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="a95a8-106">The Set-AzApplicationGatewayBackendHttpSetting cmdlet updates the back-end Hypertext Transfer Protocol (HTTP) settings for an Azure application gateway.</span></span>
<span data-ttu-id="a95a8-107">Серверные параметры HTTP применяются на всех серверах в пуле.</span><span class="sxs-lookup"><span data-stu-id="a95a8-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="a95a8-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a95a8-108">EXAMPLES</span></span>

### <span data-ttu-id="a95a8-109">Пример 1. Обновление back-end HTTP-параметров шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="a95a8-109">Example 1: Update the back-end HTTP settings for an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "Http" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="a95a8-110">Первая команда получает шлюз приложения ApplicationGateway01, который принадлежит к группе ресурсов ResourceGroup01, и сохраняет его в переменной $AppGw ресурса.</span><span class="sxs-lookup"><span data-stu-id="a95a8-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a95a8-111">Вторая команда обновляет параметры HTTP шлюза приложения в переменной $AppGw, чтобы использовать порт 88 (HTTP- и включает сходство с файлами cookie).</span><span class="sxs-lookup"><span data-stu-id="a95a8-111">The second command updates the HTTP settings of the application gateway in the $AppGw variable to use port 88, the HTTP protocol and enables cookie-based affinity.</span></span>

## <span data-ttu-id="a95a8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a95a8-112">PARAMETERS</span></span>

### <span data-ttu-id="a95a8-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="a95a8-113">-AffinityCookieName</span></span>
<span data-ttu-id="a95a8-114">Имя файла cookie, используемое для файлов cookie бесконечности</span><span class="sxs-lookup"><span data-stu-id="a95a8-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="a95a8-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a95a8-115">-ApplicationGateway</span></span>
<span data-ttu-id="a95a8-116">Определяет объект шлюза приложения, с которым этот cmdlet связывает back-end HTTP-параметры.</span><span class="sxs-lookup"><span data-stu-id="a95a8-116">Specifies an application gateway object with which this cmdlet associates back-end HTTP settings.</span></span>

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

### <span data-ttu-id="a95a8-117">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="a95a8-117">-AuthenticationCertificates</span></span>
<span data-ttu-id="a95a8-118">Определяет сертификаты проверки подлинности для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="a95a8-118">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="a95a8-119">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="a95a8-119">-ConnectionDraining</span></span>
<span data-ttu-id="a95a8-120">Разрядка подключения к ресурсу параметров backend http.</span><span class="sxs-lookup"><span data-stu-id="a95a8-120">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="a95a8-121">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="a95a8-121">-CookieBasedAffinity</span></span>
<span data-ttu-id="a95a8-122">Указывает, должно ли быть включено или отключено бесконечность на основе файлов cookie для пула серверов серверов.</span><span class="sxs-lookup"><span data-stu-id="a95a8-122">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="a95a8-123">Допустимыми значениями для этого параметра являются отключенные или включенные.</span><span class="sxs-lookup"><span data-stu-id="a95a8-123">The acceptable values for this parameter are: Disabled or Enabled.</span></span>

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

### <span data-ttu-id="a95a8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a95a8-124">-DefaultProfile</span></span>
<span data-ttu-id="a95a8-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a95a8-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a95a8-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="a95a8-126">-HostName</span></span>
<span data-ttu-id="a95a8-127">Задает заме желтую серверную серверу.</span><span class="sxs-lookup"><span data-stu-id="a95a8-127">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="a95a8-128">-Name</span><span class="sxs-lookup"><span data-stu-id="a95a8-128">-Name</span></span>
<span data-ttu-id="a95a8-129">Указывает имя объекта, который является объектом параметров HTTP.</span><span class="sxs-lookup"><span data-stu-id="a95a8-129">Specifies the name of the back-end HTTP settings object.</span></span>

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

### <span data-ttu-id="a95a8-130">-Path</span><span class="sxs-lookup"><span data-stu-id="a95a8-130">-Path</span></span>
<span data-ttu-id="a95a8-131">Путь, который должен использоваться в качестве префикса для всех HTTP-запросов.</span><span class="sxs-lookup"><span data-stu-id="a95a8-131">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="a95a8-132">Если значение для этого параметра не задано, путь не будет добавлен.</span><span class="sxs-lookup"><span data-stu-id="a95a8-132">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="a95a8-133">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="a95a8-133">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="a95a8-134">Пометить этот флажок, если в имени сервера серверов следует выбрать заме же.</span><span class="sxs-lookup"><span data-stu-id="a95a8-134">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="a95a8-135">-Port</span><span class="sxs-lookup"><span data-stu-id="a95a8-135">-Port</span></span>
<span data-ttu-id="a95a8-136">Порт, который будет использовать для каждого сервера в серверном пуле серверов.</span><span class="sxs-lookup"><span data-stu-id="a95a8-136">Specifies the port to use for each server in the back-end server pool.</span></span>

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

### <span data-ttu-id="a95a8-137">-Разротные</span><span class="sxs-lookup"><span data-stu-id="a95a8-137">-Probe</span></span>
<span data-ttu-id="a95a8-138">Этот параметр определяет, к какову будет связываться с конечными http-настройками.</span><span class="sxs-lookup"><span data-stu-id="a95a8-138">Specifies a probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="a95a8-139">-Вадим-ИД</span><span class="sxs-lookup"><span data-stu-id="a95a8-139">-ProbeId</span></span>
<span data-ttu-id="a95a8-140">Определяет ИД протокола, который нужно связать с конечными http-настройками.</span><span class="sxs-lookup"><span data-stu-id="a95a8-140">Specifies the ID of the probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="a95a8-141">-Protocol</span><span class="sxs-lookup"><span data-stu-id="a95a8-141">-Protocol</span></span>
<span data-ttu-id="a95a8-142">Протокол, который будет применяться для связи между шлюзом приложения и серверами серверов.</span><span class="sxs-lookup"><span data-stu-id="a95a8-142">Specifies the protocol to use for communication between the application gateway and back-end servers.</span></span>
<span data-ttu-id="a95a8-143">Допустимыми значениями для этого параметра являются http и https.</span><span class="sxs-lookup"><span data-stu-id="a95a8-143">The acceptable values for this parameter are: Http and Https.</span></span>
<span data-ttu-id="a95a8-144">Этот параметр внося в него с чувствительный к делу.</span><span class="sxs-lookup"><span data-stu-id="a95a8-144">This parameter is case-sensitive.</span></span>

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

### <span data-ttu-id="a95a8-145">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="a95a8-145">-RequestTimeout</span></span>
<span data-ttu-id="a95a8-146">Указывает значение времени и времени, заданное для запроса.</span><span class="sxs-lookup"><span data-stu-id="a95a8-146">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="a95a8-147">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a95a8-147">-TrustedRootCertificate</span></span>
<span data-ttu-id="a95a8-148">Доверенные корневые сертификаты шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="a95a8-148">Application gateway Trusted Root Certificates</span></span>

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

### <span data-ttu-id="a95a8-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a95a8-149">CommonParameters</span></span>
<span data-ttu-id="a95a8-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a95a8-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a95a8-151">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a95a8-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a95a8-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a95a8-152">INPUTS</span></span>

### <span data-ttu-id="a95a8-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a95a8-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a95a8-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a95a8-154">OUTPUTS</span></span>

### <span data-ttu-id="a95a8-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a95a8-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a95a8-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a95a8-156">NOTES</span></span>

## <span data-ttu-id="a95a8-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a95a8-157">RELATED LINKS</span></span>

[<span data-ttu-id="a95a8-158">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a95a8-158">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="a95a8-159">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a95a8-159">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="a95a8-160">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a95a8-160">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="a95a8-161">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="a95a8-161">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)
