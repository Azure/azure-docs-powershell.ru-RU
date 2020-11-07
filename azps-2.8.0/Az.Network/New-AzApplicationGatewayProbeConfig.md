---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 61afe67e06316dc94948be00e4778394594468cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902222"
---
# <span data-ttu-id="8cc67-101">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8cc67-101">New-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="8cc67-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8cc67-102">SYNOPSIS</span></span>
<span data-ttu-id="8cc67-103">Создание проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="8cc67-103">Creates a health probe.</span></span>

## <span data-ttu-id="8cc67-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8cc67-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>] [-Port <Int32>]
```

## <span data-ttu-id="8cc67-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8cc67-105">DESCRIPTION</span></span>
<span data-ttu-id="8cc67-106">Командлет New-AzApplicationGatewayProbeConfig создает проверку работоспособности.</span><span class="sxs-lookup"><span data-stu-id="8cc67-106">The New-AzApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="8cc67-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8cc67-107">EXAMPLES</span></span>

### <span data-ttu-id="8cc67-108">Example1: Создание проверки работоспособности</span><span class="sxs-lookup"><span data-stu-id="8cc67-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="8cc67-109">Эта команда создает проверку работоспособности с именем Probe03, с протоколом HTTP, 30-секундным интервалом, временем ожидания в 120 секунд и неработоспособным пороговым значением 8 повторных попыток.</span><span class="sxs-lookup"><span data-stu-id="8cc67-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="8cc67-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8cc67-110">PARAMETERS</span></span>

### <span data-ttu-id="8cc67-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cc67-111">-DefaultProfile</span></span>
<span data-ttu-id="8cc67-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc67-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cc67-113">-HostName</span><span class="sxs-lookup"><span data-stu-id="8cc67-113">-HostName</span></span>
<span data-ttu-id="8cc67-114">Указывает имя узла, которое этот командлет отправляет зонда.</span><span class="sxs-lookup"><span data-stu-id="8cc67-114">Specifies the host name that this cmdlet sends the probe.</span></span>

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

### <span data-ttu-id="8cc67-115">-Interval (интервал)</span><span class="sxs-lookup"><span data-stu-id="8cc67-115">-Interval</span></span>
<span data-ttu-id="8cc67-116">Задает интервал проверки в секундах.</span><span class="sxs-lookup"><span data-stu-id="8cc67-116">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="8cc67-117">Это интервал времени между двумя последовательными зондами.</span><span class="sxs-lookup"><span data-stu-id="8cc67-117">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="8cc67-118">Это значение находится в диапазоне от 1 секунды до 86400 секунд.</span><span class="sxs-lookup"><span data-stu-id="8cc67-118">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="8cc67-119">-Match</span><span class="sxs-lookup"><span data-stu-id="8cc67-119">-Match</span></span>
<span data-ttu-id="8cc67-120">Текст, который должен содержаться в ответе работоспособности.</span><span class="sxs-lookup"><span data-stu-id="8cc67-120">Body that must be contained in the health response.</span></span>
<span data-ttu-id="8cc67-121">Пустое значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8cc67-121">Default value is empty</span></span>

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

### <span data-ttu-id="8cc67-122">-MinServers</span><span class="sxs-lookup"><span data-stu-id="8cc67-122">-MinServers</span></span>
<span data-ttu-id="8cc67-123">Минимальное количество серверов, которые всегда помечаются как работоспособные.</span><span class="sxs-lookup"><span data-stu-id="8cc67-123">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="8cc67-124">Значение по умолчанию: 0</span><span class="sxs-lookup"><span data-stu-id="8cc67-124">Default value is 0</span></span>

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

### <span data-ttu-id="8cc67-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8cc67-125">-Name</span></span>
<span data-ttu-id="8cc67-126">Указывает имя зонда.</span><span class="sxs-lookup"><span data-stu-id="8cc67-126">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="8cc67-127">-Path</span><span class="sxs-lookup"><span data-stu-id="8cc67-127">-Path</span></span>
<span data-ttu-id="8cc67-128">Указывает относительный путь к зонду.</span><span class="sxs-lookup"><span data-stu-id="8cc67-128">Specifies the relative path of probe.</span></span>
<span data-ttu-id="8cc67-129">Допустимый путь начинается с символа косой черты (/).</span><span class="sxs-lookup"><span data-stu-id="8cc67-129">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="8cc67-130">Зонд отправляется \< протоколу \> :// \< host \> : \< \> \< путь к порту \> .</span><span class="sxs-lookup"><span data-stu-id="8cc67-130">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="8cc67-131">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="8cc67-131">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="8cc67-132">Следует ли выбирать заголовок узла из параметров внутреннего HTTP-сервера.</span><span class="sxs-lookup"><span data-stu-id="8cc67-132">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="8cc67-133">Значение по умолчанию: ложь</span><span class="sxs-lookup"><span data-stu-id="8cc67-133">Default value is false</span></span>

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

### <span data-ttu-id="8cc67-134">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="8cc67-134">-Protocol</span></span>
<span data-ttu-id="8cc67-135">Указывает протокол, используемый для отправки пробной проверки.</span><span class="sxs-lookup"><span data-stu-id="8cc67-135">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="8cc67-136">-Timeout</span><span class="sxs-lookup"><span data-stu-id="8cc67-136">-Timeout</span></span>
<span data-ttu-id="8cc67-137">Задает время ожидания пробы в секундах.</span><span class="sxs-lookup"><span data-stu-id="8cc67-137">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="8cc67-138">Этот командлет помечает пробу как сбой, если допустимый ответ не получен за этот период ожидания.</span><span class="sxs-lookup"><span data-stu-id="8cc67-138">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="8cc67-139">Допустимые значения: от 1 секунды до 86400 секунд.</span><span class="sxs-lookup"><span data-stu-id="8cc67-139">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="8cc67-140">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="8cc67-140">-UnhealthyThreshold</span></span>
<span data-ttu-id="8cc67-141">Указывает число повторных попыток проверки.</span><span class="sxs-lookup"><span data-stu-id="8cc67-141">Specifies the probe retry count.</span></span>
<span data-ttu-id="8cc67-142">Внутренний сервер помечается вниз после появления счетчика неудачных последовательностей проверки появления нерабочего порогового значения.</span><span class="sxs-lookup"><span data-stu-id="8cc67-142">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="8cc67-143">Допустимые значения находятся в диапазоне от 1 секунды до 20 секунд.</span><span class="sxs-lookup"><span data-stu-id="8cc67-143">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="8cc67-144">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="8cc67-144">-Port</span></span>
<span data-ttu-id="8cc67-145">Указывает порт, используемый для зондирования внутренних серверов.</span><span class="sxs-lookup"><span data-stu-id="8cc67-145">Specifies the port used for probing backend servers.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe

## NOTES

## RELATED LINKS

[Create custom probe for Application Gateway using PowerShell for Azure Resource Manager](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[Add-AzApplicationGatewayProbeConfig](./Add-AzApplicationGatewayProbeConfig.md)

[Get-AzApplicationGatewayProbeConfig](./Get-AzApplicationGatewayProbeConfig.md)

[Remove-AzApplicationGatewayProbeConfig](./Remove-AzApplicationGatewayProbeConfig.md)

[Set-AzApplicationGatewayProbeConfig](./Set-AzApplicationGatewayProbeConfig.md)

