---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 30ab203f50df9e712792e216a1b4ecf1c5378b2e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954435"
---
# <span data-ttu-id="bedc2-101">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bedc2-101">Get-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="bedc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bedc2-102">SYNOPSIS</span></span>
<span data-ttu-id="bedc2-103">Возвращает монитор подключения с указанным именем или список мониторов подключения.</span><span class="sxs-lookup"><span data-stu-id="bedc2-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

## <span data-ttu-id="bedc2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bedc2-104">SYNTAX</span></span>

### <span data-ttu-id="bedc2-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bedc2-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bedc2-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="bedc2-106">SetByResource</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bedc2-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="bedc2-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bedc2-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bedc2-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bedc2-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bedc2-109">DESCRIPTION</span></span>
<span data-ttu-id="bedc2-110">Этот Get-AzNetworkWatcherConnectionMonitor возвращает монитор подключения с указанным именем или именем ресурса или список мониторов подключения, соответствующих указанному сетевому монитору или расположению.</span><span class="sxs-lookup"><span data-stu-id="bedc2-110">The Get-AzNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="bedc2-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bedc2-111">EXAMPLES</span></span>

### <span data-ttu-id="bedc2-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bedc2-112">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="bedc2-113">Name : cm Id : /subscriptions/00000000-0000-0000-0000-00000000000/resourceGro ups/NetworkWatcherRG/provider Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/cm Etag : W/"40961b58-e379-4204-a47b-0c477739b095" ProvisioningState : Succeeded Source : { "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6 a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C ompute/virtualMachines/irinavm", "Port": 0 } Destination : { "Address": "google.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart : True StartTime : 12.01.2018 19:28 MonitoringStatus : Stopped Location : centraluseuap Type : Microsoft.Network/networkWatchers/connectionMonitors Tags: { "key1": "value1" }</span><span class="sxs-lookup"><span data-stu-id="bedc2-113">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/cm Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6 a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C ompute/virtualMachines/irinavm", "Port": 0 } Destination                 : { "Address": "google.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:19:28 PM MonitoringStatus            : Stopped Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : { "key1": "value1" }</span></span>

## <span data-ttu-id="bedc2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bedc2-114">PARAMETERS</span></span>

### <span data-ttu-id="bedc2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bedc2-115">-DefaultProfile</span></span>
<span data-ttu-id="bedc2-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bedc2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bedc2-117">-Location</span><span class="sxs-lookup"><span data-stu-id="bedc2-117">-Location</span></span>
<span data-ttu-id="bedc2-118">Расположение сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="bedc2-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="bedc2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="bedc2-119">-Name</span></span>
<span data-ttu-id="bedc2-120">Имя монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="bedc2-120">The connection monitor name.</span></span>

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

### <span data-ttu-id="bedc2-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bedc2-121">-NetworkWatcher</span></span>
<span data-ttu-id="bedc2-122">Сетевой ресурс для просмотра.</span><span class="sxs-lookup"><span data-stu-id="bedc2-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="bedc2-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="bedc2-123">-NetworkWatcherName</span></span>
<span data-ttu-id="bedc2-124">Имя сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="bedc2-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="bedc2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bedc2-125">-ResourceGroupName</span></span>
<span data-ttu-id="bedc2-126">Имя группы ресурсов сетевого watcher.</span><span class="sxs-lookup"><span data-stu-id="bedc2-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="bedc2-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bedc2-127">-ResourceId</span></span>
<span data-ttu-id="bedc2-128">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="bedc2-128">Resource ID.</span></span>

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

### <span data-ttu-id="bedc2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bedc2-129">CommonParameters</span></span>
<span data-ttu-id="bedc2-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bedc2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bedc2-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bedc2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bedc2-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bedc2-132">INPUTS</span></span>

### <span data-ttu-id="bedc2-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bedc2-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="bedc2-134">System.String</span><span class="sxs-lookup"><span data-stu-id="bedc2-134">System.String</span></span>

## <span data-ttu-id="bedc2-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bedc2-135">OUTPUTS</span></span>

### <span data-ttu-id="bedc2-136">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="bedc2-136">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="bedc2-137">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="bedc2-137">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="bedc2-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bedc2-138">NOTES</span></span>

## <span data-ttu-id="bedc2-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bedc2-139">RELATED LINKS</span></span>
