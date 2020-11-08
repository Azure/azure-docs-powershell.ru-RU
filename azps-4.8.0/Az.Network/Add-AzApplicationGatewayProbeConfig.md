---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: cea6f92ba15e43d5977af03dfee1054240f5ecad
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077714"
---
# <span data-ttu-id="ff5b1-101">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ff5b1-101">Add-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="ff5b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ff5b1-102">SYNOPSIS</span></span>
<span data-ttu-id="ff5b1-103">Добавляет зонда работоспособности к шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="ff5b1-103">Adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="ff5b1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ff5b1-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff5b1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff5b1-105">DESCRIPTION</span></span>
<span data-ttu-id="ff5b1-106">Командлет Add-AzApplicationGatewayProbeConfig добавляет в шлюз приложений зонд проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="ff5b1-106">The Add-AzApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="ff5b1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ff5b1-107">EXAMPLES</span></span>

### <span data-ttu-id="ff5b1-108">Пример 1: Добавление проверки работоспособности в шлюз приложений</span><span class="sxs-lookup"><span data-stu-id="ff5b1-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="ff5b1-109">Эта команда добавляет проверку работоспособности с именем Probe01 для шлюза приложения с именем Gateway.</span><span class="sxs-lookup"><span data-stu-id="ff5b1-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="ff5b1-110">Кроме того, команда устанавливает для порога неработоспособности 8 повторных попыток и время ожидания после 120 секунд.</span><span class="sxs-lookup"><span data-stu-id="ff5b1-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="ff5b1-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ff5b1-111">PARAMETERS</span></span>

### <span data-ttu-id="ff5b1-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ff5b1-112">-ApplicationGateway</span></span>
<span data-ttu-id="ff5b1-113">Указывает шлюз приложений, с которым этот командлет добавляет зонд.</span><span class="sxs-lookup"><span data-stu-id="ff5b1-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

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

### <span data-ttu-id="ff5b1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff5b1-114">-DefaultProfile</span></span>
<span data-ttu-id="ff5b1-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ff5b1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff5b1-116">-HostName</span><span class="sxs-lookup"><span data-stu-id="ff5b1-116">-HostName</span></span>
<span data-ttu-id="ff5b1-117">Указывает имя хоста, на которое этот командлет отправляет зонд.</span><span class="sxs-lookup"><span data-stu-id="ff5b1-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="ff5b1-118">-Interval (интервал)</span><span class="sxs-lookup"><span data-stu-id="ff5b1-118">-Interval</span></span>
<span data-ttu-id="ff5b1-119">Задает интервал проверки в секундах.</span><span class="sxs-lookup"><span data-stu-id="ff5b1-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="ff5b1-120">Это интервал времени между двумя последовательными зондами.</span><span class="sxs-lookup"><span data-stu-id="ff5b1-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="ff5b1-121">Это значение находится в диапазоне от 1 секунды до 86400 секунд.</span><span class="sxs-lookup"><span data-stu-id="ff5b1-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="ff5b1-122">-Match</span><span class="sxs-lookup"><span data-stu-id="ff5b1-122">-Match</span></span>
<span data-ttu-id="ff5b1-123">Текст, который должен содержаться в ответе работоспособности.</span><span class="sxs-lookup"><span data-stu-id="ff5b1-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="ff5b1-124">Пустое значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ff5b1-124">Default value is empty</span></span>

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

### <span data-ttu-id="ff5b1-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="ff5b1-125">-MinServers</span></span>
<span data-ttu-id="ff5b1-126">Минимальное количество серверов, которые всегда помечаются как работоспособные.</span><span class="sxs-lookup"><span data-stu-id="ff5b1-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="ff5b1-127">Значение по умолчанию: 0</span><span class="sxs-lookup"><span data-stu-id="ff5b1-127">Default value is 0</span></span>

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

### <span data-ttu-id="ff5b1-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ff5b1-128">-Name</span></span>
<span data-ttu-id="ff5b1-129">Указывает имя зонда.</span><span class="sxs-lookup"><span data-stu-id="ff5b1-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="ff5b1-130">-Path</span><span class="sxs-lookup"><span data-stu-id="ff5b1-130">-Path</span></span>
<span data-ttu-id="ff5b1-131">Указывает относительный путь к зонду.</span><span class="sxs-lookup"><span data-stu-id="ff5b1-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="ff5b1-132">Допустимый путь начинается с символа косой черты (/).</span><span class="sxs-lookup"><span data-stu-id="ff5b1-132">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="ff5b1-133">Пробный зонд отправляется в \<Protocol\> :// \<host\> : \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="ff5b1-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="ff5b1-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ff5b1-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="ff5b1-135">Следует ли выбирать заголовок узла из параметров внутреннего HTTP-сервера.</span><span class="sxs-lookup"><span data-stu-id="ff5b1-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="ff5b1-136">Значение по умолчанию: ложь</span><span class="sxs-lookup"><span data-stu-id="ff5b1-136">Default value is false</span></span>

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

### <span data-ttu-id="ff5b1-137">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="ff5b1-137">-Protocol</span></span>
<span data-ttu-id="ff5b1-138">Указывает протокол, используемый для отправки пробной проверки.</span><span class="sxs-lookup"><span data-stu-id="ff5b1-138">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="ff5b1-139">Этот командлет поддерживает только HTTP.</span><span class="sxs-lookup"><span data-stu-id="ff5b1-139">This cmdlet supports HTTP only.</span></span>

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

### <span data-ttu-id="ff5b1-140">-Timeout</span><span class="sxs-lookup"><span data-stu-id="ff5b1-140">-Timeout</span></span>
<span data-ttu-id="ff5b1-141">Задает время ожидания пробы в секундах.</span><span class="sxs-lookup"><span data-stu-id="ff5b1-141">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="ff5b1-142">Этот командлет помечает пробу как сбой, если допустимый ответ не получен за этот период ожидания.</span><span class="sxs-lookup"><span data-stu-id="ff5b1-142">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="ff5b1-143">Допустимые значения: от 1 секунды до 86400 секунд.</span><span class="sxs-lookup"><span data-stu-id="ff5b1-143">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="ff5b1-144">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="ff5b1-144">-UnhealthyThreshold</span></span>
<span data-ttu-id="ff5b1-145">Указывает число повторных попыток проверки.</span><span class="sxs-lookup"><span data-stu-id="ff5b1-145">Specifies the probe retry count.</span></span>
<span data-ttu-id="ff5b1-146">Внутренний сервер помечается вниз после появления счетчика неудачных последовательностей проверки появления нерабочего порогового значения.</span><span class="sxs-lookup"><span data-stu-id="ff5b1-146">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="ff5b1-147">Допустимые значения находятся в диапазоне от 1 секунды до 20 секунд.</span><span class="sxs-lookup"><span data-stu-id="ff5b1-147">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="ff5b1-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff5b1-148">CommonParameters</span></span>
<span data-ttu-id="ff5b1-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ff5b1-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff5b1-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff5b1-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff5b1-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ff5b1-151">INPUTS</span></span>

### <span data-ttu-id="ff5b1-152">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ff5b1-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ff5b1-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff5b1-153">OUTPUTS</span></span>

### <span data-ttu-id="ff5b1-154">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ff5b1-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ff5b1-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="ff5b1-155">NOTES</span></span>

## <span data-ttu-id="ff5b1-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff5b1-156">RELATED LINKS</span></span>

[<span data-ttu-id="ff5b1-157">Добавление зонда к существующему шлюзу приложений</span><span class="sxs-lookup"><span data-stu-id="ff5b1-157">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="ff5b1-158">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ff5b1-158">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="ff5b1-159">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ff5b1-159">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="ff5b1-160">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ff5b1-160">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="ff5b1-161">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ff5b1-161">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

