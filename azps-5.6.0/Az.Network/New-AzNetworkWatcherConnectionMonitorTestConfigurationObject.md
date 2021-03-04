---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestconfigurationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
ms.openlocfilehash: 542a207e60e451d97ba5edcbdccc45b84b14f760
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958435"
---
# <span data-ttu-id="b7266-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="b7266-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="b7266-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7266-102">SYNOPSIS</span></span>
<span data-ttu-id="b7266-103">Создайте тестовую конфигурацию монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="b7266-103">Create a connection monitor test configuration.</span></span>

## <span data-ttu-id="b7266-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b7266-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name <String> -TestFrequencySec <Int32>
 -ProtocolConfiguration <PSNetworkWatcherConnectionMonitorProtocolConfiguration>
 [-SuccessThresholdChecksFailedPercent <Int32>] [-SuccessThresholdRoundTripTimeMs <Double>]
 [-PreferredIPVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7266-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7266-105">DESCRIPTION</span></span>
<span data-ttu-id="b7266-106">С New-AzNetworkWatcherConnectionMonitorTestConfigurationObject создается тестовая конфигурация монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="b7266-106">The New-AzNetworkWatcherConnectionMonitorTestConfigurationObject cmdlet creates a connection monitor test configuration.</span></span>

## <span data-ttu-id="b7266-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b7266-107">EXAMPLES</span></span>

### <span data-ttu-id="b7266-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b7266-108">Example 1</span></span>
```powershell
PS C:\>$httpProtocolConfiguration = New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -HttpProtocol -Port 443 -Method GET -RequestHeader @{"Allow" = "GET"} -ValidStatusCodeRange 2xx, 300-308 -PreferHTTPS
PS C:\>$httpTestConfiguration = New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name httpTC -TestFrequencySec 120 -ProtocolConfiguration $httpProtocolConfiguration -SuccessThresholdChecksFailedPercent 20 -SuccessThresholdRoundTripTimeMs 30
```

<span data-ttu-id="b7266-109">Name : httpTC TestFrequencySec : 120 PreferredIPVersion : ProtocolConfiguration : { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true } SuccessThreshold : { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 }</span><span class="sxs-lookup"><span data-stu-id="b7266-109">Name                  : httpTC TestFrequencySec      : 120 PreferredIPVersion    : ProtocolConfiguration : { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true } SuccessThreshold      : { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 }</span></span> 

## <span data-ttu-id="b7266-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7266-110">PARAMETERS</span></span>

### <span data-ttu-id="b7266-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7266-111">-DefaultProfile</span></span>
<span data-ttu-id="b7266-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b7266-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7266-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b7266-113">-Name</span></span>
<span data-ttu-id="b7266-114">Имя тестовой конфигурации монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="b7266-114">The name of the connection monitor test configuration.</span></span>

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

### <span data-ttu-id="b7266-115">-PreferredIPVersion</span><span class="sxs-lookup"><span data-stu-id="b7266-115">-PreferredIPVersion</span></span>
<span data-ttu-id="b7266-116">Предпочитаемая версия IP-адреса, используемая при тестовой оценке.</span><span class="sxs-lookup"><span data-stu-id="b7266-116">The preferred IP version to use in test evaluation.</span></span> <span data-ttu-id="b7266-117">Монитор подключения может использовать другую версию в зависимости от других параметров.</span><span class="sxs-lookup"><span data-stu-id="b7266-117">The connection monitor may choose to use a different version depending on other parameters.</span></span>

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

### <span data-ttu-id="b7266-118">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7266-118">-ProtocolConfiguration</span></span>
<span data-ttu-id="b7266-119">Параметры, используемые для проверки по протоколу.</span><span class="sxs-lookup"><span data-stu-id="b7266-119">The parameters used to perform test evaluation over some protocol.</span></span>

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

### <span data-ttu-id="b7266-120">-SuccessThresholdChecksFailedPercent</span><span class="sxs-lookup"><span data-stu-id="b7266-120">-SuccessThresholdChecksFailedPercent</span></span>
<span data-ttu-id="b7266-121">Максимальное количество сбойных проверок, разрешенных для проверки как успешное.</span><span class="sxs-lookup"><span data-stu-id="b7266-121">The maximum percentage of failed checks permitted for a test to evaluate as successful.</span></span>

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

### <span data-ttu-id="b7266-122">-SuccessThresholdRoundTripTimeMs</span><span class="sxs-lookup"><span data-stu-id="b7266-122">-SuccessThresholdRoundTripTimeMs</span></span>
<span data-ttu-id="b7266-123">Максимальное время кругового пути в миллисекундах, разрешенное для проверки как успешное.</span><span class="sxs-lookup"><span data-stu-id="b7266-123">The maximum round-trip time in milliseconds permitted for a test to evaluate as successful.</span></span>

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

### <span data-ttu-id="b7266-124">-TestFrequencySec</span><span class="sxs-lookup"><span data-stu-id="b7266-124">-TestFrequencySec</span></span>
<span data-ttu-id="b7266-125">Частота проверки в секундах.</span><span class="sxs-lookup"><span data-stu-id="b7266-125">The frequency of test evaluation, in seconds.</span></span>

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

### <span data-ttu-id="b7266-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7266-126">-Confirm</span></span>
<span data-ttu-id="b7266-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7266-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7266-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7266-128">-WhatIf</span></span>
<span data-ttu-id="b7266-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7266-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7266-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b7266-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7266-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7266-131">CommonParameters</span></span>
<span data-ttu-id="b7266-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7266-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7266-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7266-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7266-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7266-134">INPUTS</span></span>

### <span data-ttu-id="b7266-135">Нет</span><span class="sxs-lookup"><span data-stu-id="b7266-135">None</span></span>

## <span data-ttu-id="b7266-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b7266-136">OUTPUTS</span></span>

### <span data-ttu-id="b7266-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="b7266-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="b7266-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b7266-138">NOTES</span></span>

## <span data-ttu-id="b7266-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7266-139">RELATED LINKS</span></span>
