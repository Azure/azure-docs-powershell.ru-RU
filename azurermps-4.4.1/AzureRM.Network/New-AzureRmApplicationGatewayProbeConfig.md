---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: a41daa12a126e768a4cc7842a72b031d4ca7a759
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568037"
---
# <span data-ttu-id="c34ea-101">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c34ea-101">New-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="c34ea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c34ea-102">SYNOPSIS</span></span>
<span data-ttu-id="c34ea-103">Создание проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="c34ea-103">Creates a health probe.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c34ea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c34ea-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c34ea-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c34ea-105">DESCRIPTION</span></span>
<span data-ttu-id="c34ea-106">Командлет New-AzureRmApplicationGatewayProbeConfig создает проверку работоспособности.</span><span class="sxs-lookup"><span data-stu-id="c34ea-106">The New-AzureRmApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="c34ea-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c34ea-107">EXAMPLES</span></span>

### <span data-ttu-id="c34ea-108">Example1: Создание проверки работоспособности</span><span class="sxs-lookup"><span data-stu-id="c34ea-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzureRmApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="c34ea-109">Эта команда создает проверку работоспособности с именем Probe03, с протоколом HTTP, 30-секундным интервалом, временем ожидания в 120 секунд и неработоспособным пороговым значением 8 повторных попыток.</span><span class="sxs-lookup"><span data-stu-id="c34ea-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="c34ea-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c34ea-110">PARAMETERS</span></span>

### <span data-ttu-id="c34ea-111">-HostName</span><span class="sxs-lookup"><span data-stu-id="c34ea-111">-HostName</span></span>
<span data-ttu-id="c34ea-112">Указывает имя узла, которое этот командлет отправляет зонда.</span><span class="sxs-lookup"><span data-stu-id="c34ea-112">Specifies the host name that this cmdlet sends the probe.</span></span>

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

### <span data-ttu-id="c34ea-113">-Interval (интервал)</span><span class="sxs-lookup"><span data-stu-id="c34ea-113">-Interval</span></span>
<span data-ttu-id="c34ea-114">Задает интервал проверки в секундах.</span><span class="sxs-lookup"><span data-stu-id="c34ea-114">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="c34ea-115">Это интервал времени между двумя последовательными зондами.</span><span class="sxs-lookup"><span data-stu-id="c34ea-115">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="c34ea-116">Это значение находится в диапазоне от 1 секунды до 86400 секунд.</span><span class="sxs-lookup"><span data-stu-id="c34ea-116">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="c34ea-117">-Match</span><span class="sxs-lookup"><span data-stu-id="c34ea-117">-Match</span></span>
<span data-ttu-id="c34ea-118">Текст, который должен содержаться в ответе работоспособности.</span><span class="sxs-lookup"><span data-stu-id="c34ea-118">Body that must be contained in the health response.</span></span>
<span data-ttu-id="c34ea-119">Пустое значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c34ea-119">Default value is empty</span></span>

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

### <span data-ttu-id="c34ea-120">-MinServers</span><span class="sxs-lookup"><span data-stu-id="c34ea-120">-MinServers</span></span>
<span data-ttu-id="c34ea-121">Минимальное количество серверов, которые всегда помечаются как работоспособные.</span><span class="sxs-lookup"><span data-stu-id="c34ea-121">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="c34ea-122">Значение по умолчанию: 0</span><span class="sxs-lookup"><span data-stu-id="c34ea-122">Default value is 0</span></span>

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

### <span data-ttu-id="c34ea-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c34ea-123">-Name</span></span>
<span data-ttu-id="c34ea-124">Указывает имя зонда.</span><span class="sxs-lookup"><span data-stu-id="c34ea-124">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="c34ea-125">-Path</span><span class="sxs-lookup"><span data-stu-id="c34ea-125">-Path</span></span>
<span data-ttu-id="c34ea-126">Указывает относительный путь к зонду.</span><span class="sxs-lookup"><span data-stu-id="c34ea-126">Specifies the relative path of probe.</span></span>
<span data-ttu-id="c34ea-127">Допустимый путь начинается с символа косой черты (/).</span><span class="sxs-lookup"><span data-stu-id="c34ea-127">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="c34ea-128">Пробный зонд отправляется в \<Protocol\> :// \<host\> : \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="c34ea-128">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="c34ea-129">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c34ea-129">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="c34ea-130">Следует ли выбирать заголовок узла из параметров внутреннего HTTP-сервера.</span><span class="sxs-lookup"><span data-stu-id="c34ea-130">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="c34ea-131">Значение по умолчанию: ложь</span><span class="sxs-lookup"><span data-stu-id="c34ea-131">Default value is false</span></span>

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

### <span data-ttu-id="c34ea-132">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="c34ea-132">-Protocol</span></span>
<span data-ttu-id="c34ea-133">Указывает протокол, используемый для отправки пробной проверки.</span><span class="sxs-lookup"><span data-stu-id="c34ea-133">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="c34ea-134">-Timeout</span><span class="sxs-lookup"><span data-stu-id="c34ea-134">-Timeout</span></span>
<span data-ttu-id="c34ea-135">Задает время ожидания пробы в секундах.</span><span class="sxs-lookup"><span data-stu-id="c34ea-135">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="c34ea-136">Этот командлет помечает пробу как сбой, если допустимый ответ не получен за этот период ожидания.</span><span class="sxs-lookup"><span data-stu-id="c34ea-136">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="c34ea-137">Допустимые значения: от 1 секунды до 86400 секунд.</span><span class="sxs-lookup"><span data-stu-id="c34ea-137">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="c34ea-138">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="c34ea-138">-UnhealthyThreshold</span></span>
<span data-ttu-id="c34ea-139">Указывает число повторных попыток проверки.</span><span class="sxs-lookup"><span data-stu-id="c34ea-139">Specifies the probe retry count.</span></span>
<span data-ttu-id="c34ea-140">Внутренний сервер помечается вниз после появления счетчика неудачных последовательностей проверки появления нерабочего порогового значения.</span><span class="sxs-lookup"><span data-stu-id="c34ea-140">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="c34ea-141">Допустимые значения находятся в диапазоне от 1 секунды до 20 секунд.</span><span class="sxs-lookup"><span data-stu-id="c34ea-141">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="c34ea-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c34ea-142">-DefaultProfile</span></span>
<span data-ttu-id="c34ea-143">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c34ea-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c34ea-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c34ea-144">CommonParameters</span></span>
<span data-ttu-id="c34ea-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c34ea-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c34ea-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c34ea-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c34ea-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c34ea-147">INPUTS</span></span>

## <span data-ttu-id="c34ea-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c34ea-148">OUTPUTS</span></span>

### <span data-ttu-id="c34ea-149">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="c34ea-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="c34ea-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="c34ea-150">NOTES</span></span>

## <span data-ttu-id="c34ea-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c34ea-151">RELATED LINKS</span></span>

[<span data-ttu-id="c34ea-152">Создание настраиваемого пробного для шлюза приложений с помощью PowerShell для диспетчера ресурсов Azure</span><span class="sxs-lookup"><span data-stu-id="c34ea-152">Create custom probe for Application Gateway using PowerShell for Azure Resource Manager</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[<span data-ttu-id="c34ea-153">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c34ea-153">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="c34ea-154">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c34ea-154">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="c34ea-155">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c34ea-155">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="c34ea-156">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c34ea-156">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

