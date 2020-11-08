---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestconfigurationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
ms.openlocfilehash: d46cba5a939a2054bc8cc40975647a198808ca09
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242990"
---
# <span data-ttu-id="084fe-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="084fe-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="084fe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="084fe-102">SYNOPSIS</span></span>
<span data-ttu-id="084fe-103">Создание конфигурации теста монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="084fe-103">Create a connection monitor test configuration.</span></span>

## <span data-ttu-id="084fe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="084fe-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name <String> -TestFrequencySec <Int32>
 -ProtocolConfiguration <PSNetworkWatcherConnectionMonitorProtocolConfiguration>
 [-SuccessThresholdChecksFailedPercent <Int32>] [-SuccessThresholdRoundTripTimeMs <Double>]
 [-PreferredIPVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="084fe-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="084fe-105">DESCRIPTION</span></span>
<span data-ttu-id="084fe-106">Командлет New-AzNetworkWatcherConnectionMonitorTestConfigurationObject создает конфигурацию теста монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="084fe-106">The New-AzNetworkWatcherConnectionMonitorTestConfigurationObject cmdlet creates a connection monitor test configuration.</span></span>

## <span data-ttu-id="084fe-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="084fe-107">EXAMPLES</span></span>

### <span data-ttu-id="084fe-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="084fe-108">Example 1</span></span>
```powershell
PS C:\>$httpProtocolConfiguration = New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -HttpProtocol -Port 443 -Method GET -RequestHeader @{"Allow" = "GET"} -ValidStatusCodeRange 2xx, 300-308 -PreferHTTPS
PS C:\>$httpTestConfiguration = New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name httpTC -TestFrequencySec 120 -ProtocolConfiguration $httpProtocolConfiguration -SuccessThresholdChecksFailedPercent 20 -SuccessThresholdRoundTripTimeMs 30
```

<span data-ttu-id="084fe-109">Name (имя): httpTC TestFrequencySec: 120 PreferredIPVersion: ProtocolConfiguration: {"порт": 443; "метод": "GET", "RequestHeaders": [{"имя": "разрешить", "значение"), "ValidStatusCodeRanges": ["2xx", "300-308"], "PreferHTTPS": true} SuccessThreshold: {"ChecksFailedPercent": = = 20, "RoundTripTimeMs": 30}</span><span class="sxs-lookup"><span data-stu-id="084fe-109">Name                  : httpTC TestFrequencySec      : 120 PreferredIPVersion    : ProtocolConfiguration : { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true } SuccessThreshold      : { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 }</span></span> 

## <span data-ttu-id="084fe-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="084fe-110">PARAMETERS</span></span>

### <span data-ttu-id="084fe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="084fe-111">-DefaultProfile</span></span>
<span data-ttu-id="084fe-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="084fe-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="084fe-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="084fe-113">-Name</span></span>
<span data-ttu-id="084fe-114">Имя конфигурации теста монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="084fe-114">The name of the connection monitor test configuration.</span></span>

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

### <span data-ttu-id="084fe-115">-PreferredIPVersion</span><span class="sxs-lookup"><span data-stu-id="084fe-115">-PreferredIPVersion</span></span>
<span data-ttu-id="084fe-116">Предпочитаемая IP-версия, используемая при оценке тестов.</span><span class="sxs-lookup"><span data-stu-id="084fe-116">The preferred IP version to use in test evaluation.</span></span> <span data-ttu-id="084fe-117">В зависимости от других параметров монитор подключений может использовать другую версию.</span><span class="sxs-lookup"><span data-stu-id="084fe-117">The connection monitor may choose to use a different version depending on other parameters.</span></span>

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

### <span data-ttu-id="084fe-118">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="084fe-118">-ProtocolConfiguration</span></span>
<span data-ttu-id="084fe-119">Параметры, используемые для выполнения оценки теста по некоторым протоколам.</span><span class="sxs-lookup"><span data-stu-id="084fe-119">The parameters used to perform test evaluation over some protocol.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorProtocolConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="084fe-120">-SuccessThresholdChecksFailedPercent</span><span class="sxs-lookup"><span data-stu-id="084fe-120">-SuccessThresholdChecksFailedPercent</span></span>
<span data-ttu-id="084fe-121">Максимальный процент от числа неудачных проверок, разрешенных для проверки как успешных.</span><span class="sxs-lookup"><span data-stu-id="084fe-121">The maximum percentage of failed checks permitted for a test to evaluate as successful.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="084fe-122">-SuccessThresholdRoundTripTimeMs</span><span class="sxs-lookup"><span data-stu-id="084fe-122">-SuccessThresholdRoundTripTimeMs</span></span>
<span data-ttu-id="084fe-123">Максимальное время кругового приема в миллисекундах, в течение которого может выполняться проверка как успешно.</span><span class="sxs-lookup"><span data-stu-id="084fe-123">The maximum round-trip time in milliseconds permitted for a test to evaluate as successful.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="084fe-124">-TestFrequencySec</span><span class="sxs-lookup"><span data-stu-id="084fe-124">-TestFrequencySec</span></span>
<span data-ttu-id="084fe-125">Частота вычисления теста в секундах.</span><span class="sxs-lookup"><span data-stu-id="084fe-125">The frequency of test evaluation, in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: TestFrequency

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="084fe-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="084fe-126">-Confirm</span></span>
<span data-ttu-id="084fe-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="084fe-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="084fe-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="084fe-128">-WhatIf</span></span>
<span data-ttu-id="084fe-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="084fe-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="084fe-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="084fe-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="084fe-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="084fe-131">CommonParameters</span></span>
<span data-ttu-id="084fe-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="084fe-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="084fe-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="084fe-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="084fe-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="084fe-134">INPUTS</span></span>

### <span data-ttu-id="084fe-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="084fe-135">None</span></span>

## <span data-ttu-id="084fe-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="084fe-136">OUTPUTS</span></span>

### <span data-ttu-id="084fe-137">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="084fe-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="084fe-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="084fe-138">NOTES</span></span>

## <span data-ttu-id="084fe-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="084fe-139">RELATED LINKS</span></span>