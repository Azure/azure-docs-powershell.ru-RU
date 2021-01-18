---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: cea6f92ba15e43d5977af03dfee1054240f5ecad
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506550"
---
# <span data-ttu-id="1bf91-101">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1bf91-101">Add-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="1bf91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bf91-102">SYNOPSIS</span></span>
<span data-ttu-id="1bf91-103">Добавляет к шлюзу приложения проверку здоровья.</span><span class="sxs-lookup"><span data-stu-id="1bf91-103">Adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="1bf91-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1bf91-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1bf91-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1bf91-105">DESCRIPTION</span></span>
<span data-ttu-id="1bf91-106">Этот Add-AzApplicationGatewayProbeConfig добавляет к шлюзу приложения керосо состояния.</span><span class="sxs-lookup"><span data-stu-id="1bf91-106">The Add-AzApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="1bf91-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1bf91-107">EXAMPLES</span></span>

### <span data-ttu-id="1bf91-108">Пример 1. Добавление области состояния на шлюз приложения</span><span class="sxs-lookup"><span data-stu-id="1bf91-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="1bf91-109">Эта команда добавляет Климову с именем "Проект01" для шлюза приложения "Шлюз".</span><span class="sxs-lookup"><span data-stu-id="1bf91-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="1bf91-110">Кроме того, для неработоспособного порога этой команды устанавливается 8 и время, необходимое для и после 120 секунд.</span><span class="sxs-lookup"><span data-stu-id="1bf91-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="1bf91-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1bf91-111">PARAMETERS</span></span>

### <span data-ttu-id="1bf91-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1bf91-112">-ApplicationGateway</span></span>
<span data-ttu-id="1bf91-113">Указывает шлюз приложения, к которому этот cmdlet добавляет замещает.</span><span class="sxs-lookup"><span data-stu-id="1bf91-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

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

### <span data-ttu-id="1bf91-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bf91-114">-DefaultProfile</span></span>
<span data-ttu-id="1bf91-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1bf91-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bf91-116">-HostName</span><span class="sxs-lookup"><span data-stu-id="1bf91-116">-HostName</span></span>
<span data-ttu-id="1bf91-117">Указывает имя хоста, в который этот cmdlet отправляет эту службу.</span><span class="sxs-lookup"><span data-stu-id="1bf91-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="1bf91-118">-Interval</span><span class="sxs-lookup"><span data-stu-id="1bf91-118">-Interval</span></span>
<span data-ttu-id="1bf91-119">Определяет интервал интервала интервала в секундах.</span><span class="sxs-lookup"><span data-stu-id="1bf91-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="1bf91-120">Это интервал времени между двумя последовательными интервалами.</span><span class="sxs-lookup"><span data-stu-id="1bf91-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="1bf91-121">Это значение находится от 1 секунды до 86400 секунд.</span><span class="sxs-lookup"><span data-stu-id="1bf91-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="1bf91-122">-Match</span><span class="sxs-lookup"><span data-stu-id="1bf91-122">-Match</span></span>
<span data-ttu-id="1bf91-123">Body that must be contained in the health response.</span><span class="sxs-lookup"><span data-stu-id="1bf91-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="1bf91-124">Значение по умолчанию пустое</span><span class="sxs-lookup"><span data-stu-id="1bf91-124">Default value is empty</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bf91-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="1bf91-125">-MinServers</span></span>
<span data-ttu-id="1bf91-126">Минимальное количество серверов, которые всегда отмечены как полезные.</span><span class="sxs-lookup"><span data-stu-id="1bf91-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="1bf91-127">Значение по умолчанию — 0</span><span class="sxs-lookup"><span data-stu-id="1bf91-127">Default value is 0</span></span>

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

### <span data-ttu-id="1bf91-128">-Name</span><span class="sxs-lookup"><span data-stu-id="1bf91-128">-Name</span></span>
<span data-ttu-id="1bf91-129">Указывает имя заме желтого.</span><span class="sxs-lookup"><span data-stu-id="1bf91-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="1bf91-130">-Path</span><span class="sxs-lookup"><span data-stu-id="1bf91-130">-Path</span></span>
<span data-ttu-id="1bf91-131">Указывает относительный путь к заданным данным.</span><span class="sxs-lookup"><span data-stu-id="1bf91-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="1bf91-132">Допустимый путь начинается с косой черты (/).</span><span class="sxs-lookup"><span data-stu-id="1bf91-132">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="1bf91-133">Письмо отправлено в \<Protocol\> адрес :// \<host\> : \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="1bf91-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="1bf91-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="1bf91-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="1bf91-135">Следует ли выбирать заме желтую ссылку в параметрах http-сайта.</span><span class="sxs-lookup"><span data-stu-id="1bf91-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="1bf91-136">Значение по умолчанию — false</span><span class="sxs-lookup"><span data-stu-id="1bf91-136">Default value is false</span></span>

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

### <span data-ttu-id="1bf91-137">-Protocol</span><span class="sxs-lookup"><span data-stu-id="1bf91-137">-Protocol</span></span>
<span data-ttu-id="1bf91-138">Протокол, используемый для отправки заме же.</span><span class="sxs-lookup"><span data-stu-id="1bf91-138">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="1bf91-139">Этот cmdlet поддерживает только HTTP.</span><span class="sxs-lookup"><span data-stu-id="1bf91-139">This cmdlet supports HTTP only.</span></span>

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

### <span data-ttu-id="1bf91-140">-Timeout</span><span class="sxs-lookup"><span data-stu-id="1bf91-140">-Timeout</span></span>
<span data-ttu-id="1bf91-141">Время и время времени висячих секунд.</span><span class="sxs-lookup"><span data-stu-id="1bf91-141">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="1bf91-142">Этот cmdlet помещает сообщение об сбойе, если в этот период времени ожидания не получен допустимый ответ.</span><span class="sxs-lookup"><span data-stu-id="1bf91-142">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="1bf91-143">Допустимые значения — от 1 секунды до 86400 секунд.</span><span class="sxs-lookup"><span data-stu-id="1bf91-143">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="1bf91-144">-НеработоспособныйThreshold</span><span class="sxs-lookup"><span data-stu-id="1bf91-144">-UnhealthyThreshold</span></span>
<span data-ttu-id="1bf91-145">Указывает, что посчитаются повторно.</span><span class="sxs-lookup"><span data-stu-id="1bf91-145">Specifies the probe retry count.</span></span>
<span data-ttu-id="1bf91-146">Сервер сервер серверов отмечен вниз, когда количество неудачных неудач подряд достигает неработоспособного порога.</span><span class="sxs-lookup"><span data-stu-id="1bf91-146">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="1bf91-147">Допустимые значения — от 1 секунды до 20 секунд.</span><span class="sxs-lookup"><span data-stu-id="1bf91-147">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="1bf91-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bf91-148">CommonParameters</span></span>
<span data-ttu-id="1bf91-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bf91-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bf91-150">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bf91-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bf91-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1bf91-151">INPUTS</span></span>

### <span data-ttu-id="1bf91-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1bf91-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1bf91-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1bf91-153">OUTPUTS</span></span>

### <span data-ttu-id="1bf91-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1bf91-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1bf91-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1bf91-155">NOTES</span></span>

## <span data-ttu-id="1bf91-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1bf91-156">RELATED LINKS</span></span>

[<span data-ttu-id="1bf91-157">Добавление астройки к существующему шлюзу приложения</span><span class="sxs-lookup"><span data-stu-id="1bf91-157">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="1bf91-158">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1bf91-158">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="1bf91-159">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1bf91-159">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="1bf91-160">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1bf91-160">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="1bf91-161">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1bf91-161">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

