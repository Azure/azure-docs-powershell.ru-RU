---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 3f380135cc6edde875c927dd9d640a10cdf14957
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733827"
---
# <span data-ttu-id="af16a-101">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="af16a-101">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="af16a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="af16a-102">SYNOPSIS</span></span>
<span data-ttu-id="af16a-103">Возвращает монитор подключений с указанным именем или списком мониторов соединения.</span><span class="sxs-lookup"><span data-stu-id="af16a-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af16a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="af16a-104">SYNTAX</span></span>

### <span data-ttu-id="af16a-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="af16a-105">SetByName (Default)</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af16a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="af16a-106">SetByResource</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af16a-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="af16a-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af16a-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="af16a-108">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="af16a-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af16a-109">DESCRIPTION</span></span>
<span data-ttu-id="af16a-110">Командлет Get-AzureRmNetworkWatcherConnectionMonitor возвращает монитор подключений с указанным именем/resourceId или списком мониторов соединений, соответствующих указанному сетевому ресурсу или расположению.</span><span class="sxs-lookup"><span data-stu-id="af16a-110">The Get-AzureRmNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="af16a-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="af16a-111">EXAMPLES</span></span>

### <span data-ttu-id="af16a-112">Пример 1: получение монитора подключений по имени в указанном расположении</span><span class="sxs-lookup"><span data-stu-id="af16a-112">Example 1: Get connection monitor by name in the specified location</span></span>
```
PS C:\> Get-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm


Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6
                              a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C
                              ompute/virtualMachines/irinavm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Stopped
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="af16a-113">В этом примере монитор соединения получается по имени в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="af16a-113">In this example we get connection monitor by name in the specified location.</span></span>

## <span data-ttu-id="af16a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="af16a-114">PARAMETERS</span></span>

### <span data-ttu-id="af16a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af16a-115">-DefaultProfile</span></span>
<span data-ttu-id="af16a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="af16a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af16a-117">-Location</span><span class="sxs-lookup"><span data-stu-id="af16a-117">-Location</span></span>
<span data-ttu-id="af16a-118">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="af16a-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="af16a-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="af16a-119">-Name</span></span>
<span data-ttu-id="af16a-120">Имя монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="af16a-120">The connection monitor name.</span></span>

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

### <span data-ttu-id="af16a-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="af16a-121">-NetworkWatcher</span></span>
<span data-ttu-id="af16a-122">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="af16a-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="af16a-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="af16a-123">-NetworkWatcherName</span></span>
<span data-ttu-id="af16a-124">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="af16a-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="af16a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af16a-125">-ResourceGroupName</span></span>
<span data-ttu-id="af16a-126">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="af16a-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="af16a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af16a-127">-ResourceId</span></span>
<span data-ttu-id="af16a-128">Идентификатор ресурса для монитора соединений.</span><span class="sxs-lookup"><span data-stu-id="af16a-128">Resource ID of the connection monitor.</span></span>

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

### <span data-ttu-id="af16a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af16a-129">CommonParameters</span></span>
<span data-ttu-id="af16a-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="af16a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af16a-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af16a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af16a-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="af16a-132">INPUTS</span></span>

### <span data-ttu-id="af16a-133">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="af16a-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="af16a-134">Параметры: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="af16a-134">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="af16a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="af16a-135">System.String</span></span>

## <span data-ttu-id="af16a-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="af16a-136">OUTPUTS</span></span>

### <span data-ttu-id="af16a-137">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="af16a-137">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="af16a-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="af16a-138">NOTES</span></span>
<span data-ttu-id="af16a-139">Ключевые слова: Azure, azurerm, ARM, Resource, подключение, управление, диспетчер, сеть, сеть, сетевое наблюдатель, монитор подключений</span><span class="sxs-lookup"><span data-stu-id="af16a-139">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="af16a-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af16a-140">RELATED LINKS</span></span>

[<span data-ttu-id="af16a-141">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="af16a-141">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="af16a-142">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="af16a-142">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="af16a-143">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="af16a-143">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="af16a-144">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="af16a-144">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="af16a-145">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="af16a-145">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="af16a-146">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="af16a-146">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="af16a-147">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="af16a-147">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="af16a-148">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="af16a-148">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="af16a-149">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="af16a-149">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="af16a-150">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="af16a-150">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="af16a-151">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="af16a-151">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="af16a-152">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="af16a-152">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="af16a-153">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="af16a-153">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="af16a-154">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="af16a-154">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="af16a-155">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="af16a-155">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="af16a-156">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="af16a-156">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="af16a-157">Остановить-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="af16a-157">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="af16a-158">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="af16a-158">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="af16a-159">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="af16a-159">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="af16a-160">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="af16a-160">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="af16a-161">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="af16a-161">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="af16a-162">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="af16a-162">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="af16a-163">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="af16a-163">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="af16a-164">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="af16a-164">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="af16a-165">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="af16a-165">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="af16a-166">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="af16a-166">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="af16a-167">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="af16a-167">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
