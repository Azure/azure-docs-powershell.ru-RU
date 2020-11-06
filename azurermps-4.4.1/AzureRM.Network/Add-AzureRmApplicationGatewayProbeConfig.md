---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 169a63248ebc499f577a635821131e0153e64433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567588"
---
# <span data-ttu-id="e130b-101">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e130b-101">Add-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="e130b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e130b-102">SYNOPSIS</span></span>
<span data-ttu-id="e130b-103">Добавляет зонда работоспособности к шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="e130b-103">Adds a health probe to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e130b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e130b-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e130b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e130b-105">DESCRIPTION</span></span>
<span data-ttu-id="e130b-106">Командлет Add-AzureRmApplicationGatewayProbeConfig добавляет в шлюз приложений зонд проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="e130b-106">The Add-AzureRmApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="e130b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e130b-107">EXAMPLES</span></span>

### <span data-ttu-id="e130b-108">Пример 1: Добавление проверки работоспособности в шлюз приложений</span><span class="sxs-lookup"><span data-stu-id="e130b-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="e130b-109">Эта команда добавляет проверку работоспособности с именем Probe01 для шлюза приложения с именем Gateway.</span><span class="sxs-lookup"><span data-stu-id="e130b-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="e130b-110">Кроме того, команда устанавливает для порога неработоспособности 8 повторных попыток и время ожидания после 120 секунд.</span><span class="sxs-lookup"><span data-stu-id="e130b-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="e130b-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e130b-111">PARAMETERS</span></span>

### <span data-ttu-id="e130b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e130b-112">-ApplicationGateway</span></span>
<span data-ttu-id="e130b-113">Указывает шлюз приложений, с которым этот командлет добавляет зонд.</span><span class="sxs-lookup"><span data-stu-id="e130b-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

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

### <span data-ttu-id="e130b-114">-HostName</span><span class="sxs-lookup"><span data-stu-id="e130b-114">-HostName</span></span>
<span data-ttu-id="e130b-115">Указывает имя хоста, на которое этот командлет отправляет зонд.</span><span class="sxs-lookup"><span data-stu-id="e130b-115">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="e130b-116">-Interval (интервал)</span><span class="sxs-lookup"><span data-stu-id="e130b-116">-Interval</span></span>
<span data-ttu-id="e130b-117">Задает интервал проверки в секундах.</span><span class="sxs-lookup"><span data-stu-id="e130b-117">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="e130b-118">Это интервал времени между двумя последовательными зондами.</span><span class="sxs-lookup"><span data-stu-id="e130b-118">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="e130b-119">Это значение находится в диапазоне от 1 секунды до 86400 секунд.</span><span class="sxs-lookup"><span data-stu-id="e130b-119">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="e130b-120">-Match</span><span class="sxs-lookup"><span data-stu-id="e130b-120">-Match</span></span>
<span data-ttu-id="e130b-121">Текст, который должен содержаться в ответе работоспособности.</span><span class="sxs-lookup"><span data-stu-id="e130b-121">Body that must be contained in the health response.</span></span>
<span data-ttu-id="e130b-122">Пустое значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e130b-122">Default value is empty</span></span>

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

### <span data-ttu-id="e130b-123">-MinServers</span><span class="sxs-lookup"><span data-stu-id="e130b-123">-MinServers</span></span>
<span data-ttu-id="e130b-124">Минимальное количество серверов, которые всегда помечаются как работоспособные.</span><span class="sxs-lookup"><span data-stu-id="e130b-124">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="e130b-125">Значение по умолчанию: 0</span><span class="sxs-lookup"><span data-stu-id="e130b-125">Default value is 0</span></span>

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

### <span data-ttu-id="e130b-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e130b-126">-Name</span></span>
<span data-ttu-id="e130b-127">Указывает имя зонда.</span><span class="sxs-lookup"><span data-stu-id="e130b-127">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="e130b-128">-Path</span><span class="sxs-lookup"><span data-stu-id="e130b-128">-Path</span></span>
<span data-ttu-id="e130b-129">Указывает относительный путь к зонду.</span><span class="sxs-lookup"><span data-stu-id="e130b-129">Specifies the relative path of probe.</span></span>
<span data-ttu-id="e130b-130">Допустимый путь начинается с символа косой черты (/).</span><span class="sxs-lookup"><span data-stu-id="e130b-130">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="e130b-131">Пробный зонд отправляется в \<Protocol\> :// \<host\> : \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="e130b-131">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="e130b-132">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e130b-132">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="e130b-133">Следует ли выбирать заголовок узла из параметров внутреннего HTTP-сервера.</span><span class="sxs-lookup"><span data-stu-id="e130b-133">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="e130b-134">Значение по умолчанию: ложь</span><span class="sxs-lookup"><span data-stu-id="e130b-134">Default value is false</span></span>

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

### <span data-ttu-id="e130b-135">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="e130b-135">-Protocol</span></span>
<span data-ttu-id="e130b-136">Указывает протокол, используемый для отправки пробной проверки.</span><span class="sxs-lookup"><span data-stu-id="e130b-136">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="e130b-137">Этот командлет поддерживает только HTTP.</span><span class="sxs-lookup"><span data-stu-id="e130b-137">This cmdlet supports HTTP only.</span></span>

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

### <span data-ttu-id="e130b-138">-Timeout</span><span class="sxs-lookup"><span data-stu-id="e130b-138">-Timeout</span></span>
<span data-ttu-id="e130b-139">Задает время ожидания пробы в секундах.</span><span class="sxs-lookup"><span data-stu-id="e130b-139">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="e130b-140">Этот командлет помечает пробу как сбой, если допустимый ответ не получен за этот период ожидания.</span><span class="sxs-lookup"><span data-stu-id="e130b-140">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="e130b-141">Допустимые значения: от 1 секунды до 86400 секунд.</span><span class="sxs-lookup"><span data-stu-id="e130b-141">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="e130b-142">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="e130b-142">-UnhealthyThreshold</span></span>
<span data-ttu-id="e130b-143">Указывает число повторных попыток проверки.</span><span class="sxs-lookup"><span data-stu-id="e130b-143">Specifies the probe retry count.</span></span>
<span data-ttu-id="e130b-144">Внутренний сервер помечается вниз после появления счетчика неудачных последовательностей проверки появления нерабочего порогового значения.</span><span class="sxs-lookup"><span data-stu-id="e130b-144">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="e130b-145">Допустимые значения находятся в диапазоне от 1 секунды до 20 секунд.</span><span class="sxs-lookup"><span data-stu-id="e130b-145">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="e130b-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e130b-146">-DefaultProfile</span></span>
<span data-ttu-id="e130b-147">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e130b-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e130b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e130b-148">CommonParameters</span></span>
<span data-ttu-id="e130b-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e130b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e130b-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e130b-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e130b-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e130b-151">INPUTS</span></span>

### <span data-ttu-id="e130b-152">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e130b-152">PSApplicationGateway</span></span>
<span data-ttu-id="e130b-153">Параметр "ApplicationGateway" принимает значение типа "PSApplicationGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e130b-153">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="e130b-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e130b-154">OUTPUTS</span></span>

### <span data-ttu-id="e130b-155">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e130b-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e130b-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="e130b-156">NOTES</span></span>

## <span data-ttu-id="e130b-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e130b-157">RELATED LINKS</span></span>

[<span data-ttu-id="e130b-158">Добавление зонда к существующему шлюзу приложений</span><span class="sxs-lookup"><span data-stu-id="e130b-158">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="e130b-159">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e130b-159">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="e130b-160">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e130b-160">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="e130b-161">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e130b-161">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="e130b-162">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e130b-162">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

