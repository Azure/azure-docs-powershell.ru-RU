---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorObject.md
ms.openlocfilehash: 06c20432821336b57764d70b5747759b7517801f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316636"
---
# <span data-ttu-id="4fdb7-101">New-AzNetworkWatcherConnectionMonitorObject</span><span class="sxs-lookup"><span data-stu-id="4fdb7-101">New-AzNetworkWatcherConnectionMonitorObject</span></span>

## <span data-ttu-id="4fdb7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4fdb7-102">SYNOPSIS</span></span>
<span data-ttu-id="4fdb7-103">Создайте объект монитора подключений v2.</span><span class="sxs-lookup"><span data-stu-id="4fdb7-103">Create a connection monitor V2 object.</span></span>

## <span data-ttu-id="4fdb7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4fdb7-104">SYNTAX</span></span>

### <span data-ttu-id="4fdb7-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4fdb7-105">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitorObject -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fdb7-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="4fdb7-106">SetByName</span></span>
```
New-AzNetworkWatcherConnectionMonitorObject -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fdb7-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="4fdb7-107">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitorObject -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fdb7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4fdb7-108">DESCRIPTION</span></span>
<span data-ttu-id="4fdb7-109">Командлет New-AzNetworkWatcherConnectionMonitorObject создает объект монитора соединения v2.</span><span class="sxs-lookup"><span data-stu-id="4fdb7-109">The New-AzNetworkWatcherConnectionMonitorObject cmdlet creates a connection monitor V2 object.</span></span>

## <span data-ttu-id="4fdb7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4fdb7-110">EXAMPLES</span></span>

### <span data-ttu-id="4fdb7-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4fdb7-111">Example 1</span></span>
```powershell
PS> $cmtest = New-AzNetworkWatcherConnectionMonitorObject -Location westcentralus -Name cmV2test -TestGroup $testGroup1, $testGroup2 -Tag @{"name" = "value"}
PS> $cmtest
```

<span data-ttu-id="4fdb7-112">NetworkWatcherName : NetworkWatcher_westcentralus ResourceGroupName : NetworkWatcherRG Name : cmV2test TestGroups : [ { "Name": "testGroup1", "Disable": false, "TestConfigurations": [ { "Name": "tcpTC", "TestFrequencySec": 60, "ProtocolConfiguration": { "Port": 80, "DisableTraceRoute": false }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 5 } }, { "Name": "icmpTC", "TestFrequencySec": 30, "PreferredIPVersion": "IPv4", "ProtocolConfiguration": { "DisableTraceRoute": true } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/RGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" }, { "Name": "NPM-CommonEUS(er-lab)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/er-lab/p roviders/Microsoft.OperationalInsights/workspaces/NPM-CommonEUS", "Filter": { "Type": "Include", "Items": [ { "Type": "AgentAddress", "Address": "SEA-Cust50-VM01" }, { "Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B" } ] } } ], "Destinations": [ { "Name": "bingEndpoint", "Address": "bing.com" }, { "Name": "googleEndpoint", "Address": "google.com" } ] }, { "Name": "testGroup2", "Disable": false, "TestConfigurations": [ { "Name": "httpTC", "TestFrequencySec": 120, "ProtocolConfiguration": { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/IrinaRGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" } ], "Destinations": [ { "Name": "googleEndpoint", "Address": "google.com" } ] } ] Outputs : null Notes : Tags : { "name": "value" }</span><span class="sxs-lookup"><span data-stu-id="4fdb7-112">NetworkWatcherName : NetworkWatcher_westcentralus ResourceGroupName  : NetworkWatcherRG Name               : cmV2test TestGroups         : [ { "Name": "testGroup1", "Disable": false, "TestConfigurations": [ { "Name": "tcpTC", "TestFrequencySec": 60, "ProtocolConfiguration": { "Port": 80, "DisableTraceRoute": false }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 5 } }, { "Name": "icmpTC", "TestFrequencySec": 30, "PreferredIPVersion": "IPv4", "ProtocolConfiguration": { "DisableTraceRoute": true } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/RGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" }, { "Name": "NPM-CommonEUS(er-lab)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/er-lab/p roviders/Microsoft.OperationalInsights/workspaces/NPM-CommonEUS", "Filter": { "Type": "Include", "Items": [ { "Type": "AgentAddress", "Address": "SEA-Cust50-VM01" }, { "Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B" } ] } } ], "Destinations": [ { "Name": "bingEndpoint", "Address": "bing.com" }, { "Name": "googleEndpoint", "Address": "google.com" } ] }, { "Name": "testGroup2", "Disable": false, "TestConfigurations": [ { "Name": "httpTC", "TestFrequencySec": 120, "ProtocolConfiguration": { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true }, "SuccessThreshold": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 } } ], "Sources": [ { "Name": "MultiTierApp0(IrinaRGWestcentralus)", "ResourceId": "/subscriptions/00000000-0000-0000-0000-00000000/resourceGroups/IrinaRGW estcentralus/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" } ], "Destinations": [ { "Name": "googleEndpoint", "Address": "google.com" } ] } ] Outputs            : null Notes              : Tags               : { "name": "value" }</span></span>
        
   

## <span data-ttu-id="4fdb7-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4fdb7-113">PARAMETERS</span></span>

### <span data-ttu-id="4fdb7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fdb7-114">-DefaultProfile</span></span>
<span data-ttu-id="4fdb7-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4fdb7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fdb7-116">-Location</span><span class="sxs-lookup"><span data-stu-id="4fdb7-116">-Location</span></span>
<span data-ttu-id="4fdb7-117">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="4fdb7-117">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fdb7-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4fdb7-118">-Name</span></span>
<span data-ttu-id="4fdb7-119">Имя монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="4fdb7-119">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fdb7-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4fdb7-120">-NetworkWatcher</span></span>
<span data-ttu-id="4fdb7-121">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="4fdb7-121">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fdb7-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4fdb7-122">-NetworkWatcherName</span></span>
<span data-ttu-id="4fdb7-123">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="4fdb7-123">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fdb7-124">-Примечание</span><span class="sxs-lookup"><span data-stu-id="4fdb7-124">-Note</span></span>
<span data-ttu-id="4fdb7-125">Заметки, связанные с монитором подключений.</span><span class="sxs-lookup"><span data-stu-id="4fdb7-125">Notes associated with connection monitor.</span></span>

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

### <span data-ttu-id="4fdb7-126">-Output</span><span class="sxs-lookup"><span data-stu-id="4fdb7-126">-Output</span></span>
<span data-ttu-id="4fdb7-127">Описание пунктов назначения выходных данных монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="4fdb7-127">Describes a connection monitor output destinations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fdb7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fdb7-128">-ResourceGroupName</span></span>
<span data-ttu-id="4fdb7-129">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="4fdb7-129">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fdb7-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="4fdb7-130">-Tag</span></span>
<span data-ttu-id="4fdb7-131">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4fdb7-131">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fdb7-132">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="4fdb7-132">-TestGroup</span></span>
<span data-ttu-id="4fdb7-133">Список групп тестов.</span><span class="sxs-lookup"><span data-stu-id="4fdb7-133">The list of test groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fdb7-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4fdb7-134">-Confirm</span></span>
<span data-ttu-id="4fdb7-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4fdb7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fdb7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fdb7-136">-WhatIf</span></span>
<span data-ttu-id="4fdb7-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4fdb7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fdb7-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4fdb7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fdb7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fdb7-139">CommonParameters</span></span>
<span data-ttu-id="4fdb7-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4fdb7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fdb7-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4fdb7-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fdb7-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4fdb7-142">INPUTS</span></span>

### <span data-ttu-id="4fdb7-143">Ничего</span><span class="sxs-lookup"><span data-stu-id="4fdb7-143">None</span></span>

## <span data-ttu-id="4fdb7-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4fdb7-144">OUTPUTS</span></span>

### <span data-ttu-id="4fdb7-145">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorObject</span><span class="sxs-lookup"><span data-stu-id="4fdb7-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorObject</span></span>

## <span data-ttu-id="4fdb7-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="4fdb7-146">NOTES</span></span>

## <span data-ttu-id="4fdb7-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4fdb7-147">RELATED LINKS</span></span>
