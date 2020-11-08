---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: c2da2b9173b3977a606699fd8e1def3dae2a68d9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073312"
---
# <span data-ttu-id="4e26b-101">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4e26b-101">Get-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="4e26b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e26b-102">SYNOPSIS</span></span>
<span data-ttu-id="4e26b-103">Возвращает монитор подключений с указанным именем или списком мониторов соединения.</span><span class="sxs-lookup"><span data-stu-id="4e26b-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

## <span data-ttu-id="4e26b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e26b-104">SYNTAX</span></span>

### <span data-ttu-id="4e26b-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e26b-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e26b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="4e26b-106">SetByResource</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e26b-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="4e26b-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e26b-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="4e26b-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e26b-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e26b-109">DESCRIPTION</span></span>
<span data-ttu-id="4e26b-110">Командлет Get-AzNetworkWatcherConnectionMonitor возвращает монитор подключений с указанным именем/resourceId или списком мониторов соединений, соответствующих указанному сетевому ресурсу или расположению.</span><span class="sxs-lookup"><span data-stu-id="4e26b-110">The Get-AzNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="4e26b-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e26b-111">EXAMPLES</span></span>

### <span data-ttu-id="4e26b-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4e26b-112">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="4e26b-113">Имя: ИД диспетчера подключений:/subscriptions/00000000-0000-0000-0000-000000000000/resourceGro UPS/NetworkWatcherRG/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/cm ETag: W/"40961b58-e379-4204-a47b-0c477739b095" ProvisioningState: успешно источник: {"ResourceId": "/Subscriptions/96e68903-0a56-4819-9987-8d08ad6 a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft. C ompute/virtualMachines/irinavm", "порт": 0} назначение: {"адрес": "google.com", "порт": 80} MonitoringIntervalInSeconds: 60 автозапуска:, время начала: 1/12/2018 7:19:28 PM MonitoringStatus: остановлено расположение: centraluseuap Type: Microsoft. Network/networkWatchers/connectionMonitors Теги: {"key1": "значение1"}</span><span class="sxs-lookup"><span data-stu-id="4e26b-113">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/cm Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6 a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C ompute/virtualMachines/irinavm", "Port": 0 } Destination                 : { "Address": "google.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:19:28 PM MonitoringStatus            : Stopped Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : { "key1": "value1" }</span></span>

## <span data-ttu-id="4e26b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e26b-114">PARAMETERS</span></span>

### <span data-ttu-id="4e26b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e26b-115">-DefaultProfile</span></span>
<span data-ttu-id="4e26b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e26b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e26b-117">-Location</span><span class="sxs-lookup"><span data-stu-id="4e26b-117">-Location</span></span>
<span data-ttu-id="4e26b-118">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="4e26b-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="4e26b-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4e26b-119">-Name</span></span>
<span data-ttu-id="4e26b-120">Имя монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="4e26b-120">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e26b-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4e26b-121">-NetworkWatcher</span></span>
<span data-ttu-id="4e26b-122">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="4e26b-122">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e26b-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4e26b-123">-NetworkWatcherName</span></span>
<span data-ttu-id="4e26b-124">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="4e26b-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="4e26b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e26b-125">-ResourceGroupName</span></span>
<span data-ttu-id="4e26b-126">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="4e26b-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="4e26b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e26b-127">-ResourceId</span></span>
<span data-ttu-id="4e26b-128">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="4e26b-128">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e26b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e26b-129">CommonParameters</span></span>
<span data-ttu-id="4e26b-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e26b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e26b-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e26b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e26b-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e26b-132">INPUTS</span></span>

### <span data-ttu-id="4e26b-133">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4e26b-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="4e26b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4e26b-134">System.String</span></span>

## <span data-ttu-id="4e26b-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e26b-135">OUTPUTS</span></span>

### <span data-ttu-id="4e26b-136">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="4e26b-136">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="4e26b-137">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="4e26b-137">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="4e26b-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e26b-138">NOTES</span></span>

## <span data-ttu-id="4e26b-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e26b-139">RELATED LINKS</span></span>
