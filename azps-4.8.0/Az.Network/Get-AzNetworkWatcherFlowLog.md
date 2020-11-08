---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 5f4322ba81cdae5bdb0b33c2658a6d7934ed638d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235550"
---
# <span data-ttu-id="e42d5-101">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="e42d5-101">Get-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="e42d5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e42d5-102">SYNOPSIS</span></span>
<span data-ttu-id="e42d5-103">Получение ресурса журнала потока или списка ресурсов потока в указанной подписке и регионе.</span><span class="sxs-lookup"><span data-stu-id="e42d5-103">Gets a flow log resource or a list of flow log resources in the specified subscription and region.</span></span>

## <span data-ttu-id="e42d5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e42d5-104">SYNTAX</span></span>

### <span data-ttu-id="e42d5-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e42d5-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e42d5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="e42d5-106">SetByResource</span></span>
```
Get-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e42d5-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="e42d5-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherFlowLog -Location <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e42d5-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e42d5-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherFlowLog -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e42d5-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e42d5-109">DESCRIPTION</span></span>
<span data-ttu-id="e42d5-110">Получение ресурса журнала потока или списка ресурсов потока в указанной подписке и регионе.</span><span class="sxs-lookup"><span data-stu-id="e42d5-110">Gets a flow log resource or a list of flow log resources in the specified subscription and region.</span></span>

## <span data-ttu-id="e42d5-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e42d5-111">EXAMPLES</span></span>

### <span data-ttu-id="e42d5-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e42d5-112">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

<span data-ttu-id="e42d5-113">Name (имя): pstest ID:/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ERS/Microsoft. Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest ETag: W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState: успешное расположение: eastus TargetResourceId:/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide RS/Microsoft. Network/networkSecurityGroups/MyNSG StorageId:/subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft. Storage/storageAccounts/MySTorage Enabled: true RetentionPolicy: {"дн.: 5". true} Format: {"тип": "JSON", "Version": 2} FlowAnalyticsConfiguration: {"networkWatcherFlowAnalyticsConfiguration": {"Enabled": "BBBBBBBB-BBBB-BBBB-BBBB-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/Subscriptions/BBBBBBBB-BBBB-BBBB-BBBB-bbbbbbbbbbbb/resourcegr", oups, или providers/Microsoft. FlowLogsV2Demo/workspaces/OperationalInsights "," MyWorkspace ": 60}</span><span class="sxs-lookup"><span data-stu-id="e42d5-113">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : True RetentionPolicy            : { "Days": 5, "Enabled": true } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 }</span></span>

## <span data-ttu-id="e42d5-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e42d5-114">PARAMETERS</span></span>

### <span data-ttu-id="e42d5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e42d5-115">-DefaultProfile</span></span>
<span data-ttu-id="e42d5-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e42d5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e42d5-117">-Location</span><span class="sxs-lookup"><span data-stu-id="e42d5-117">-Location</span></span>
<span data-ttu-id="e42d5-118">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="e42d5-118">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e42d5-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e42d5-119">-Name</span></span>
<span data-ttu-id="e42d5-120">Имя журнала потока.</span><span class="sxs-lookup"><span data-stu-id="e42d5-120">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: FlowLogName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e42d5-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e42d5-121">-NetworkWatcher</span></span>
<span data-ttu-id="e42d5-122">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="e42d5-122">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e42d5-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e42d5-123">-NetworkWatcherName</span></span>
<span data-ttu-id="e42d5-124">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="e42d5-124">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e42d5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e42d5-125">-ResourceGroupName</span></span>
<span data-ttu-id="e42d5-126">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="e42d5-126">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e42d5-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e42d5-127">-ResourceId</span></span>
<span data-ttu-id="e42d5-128">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="e42d5-128">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e42d5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e42d5-129">CommonParameters</span></span>
<span data-ttu-id="e42d5-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e42d5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e42d5-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e42d5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e42d5-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e42d5-132">INPUTS</span></span>

### <span data-ttu-id="e42d5-133">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e42d5-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="e42d5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e42d5-134">System.String</span></span>

## <span data-ttu-id="e42d5-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e42d5-135">OUTPUTS</span></span>

### <span data-ttu-id="e42d5-136">Microsoft. Azure. Commands. Network. Models. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="e42d5-136">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="e42d5-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="e42d5-137">NOTES</span></span>

## <span data-ttu-id="e42d5-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e42d5-138">RELATED LINKS</span></span>

[<span data-ttu-id="e42d5-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e42d5-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="e42d5-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e42d5-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="e42d5-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e42d5-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="e42d5-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e42d5-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="e42d5-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e42d5-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e42d5-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e42d5-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="e42d5-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e42d5-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="e42d5-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e42d5-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e42d5-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e42d5-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="e42d5-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e42d5-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e42d5-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e42d5-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e42d5-150">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e42d5-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e42d5-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="e42d5-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="e42d5-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e42d5-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="e42d5-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="e42d5-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="e42d5-154">Остановить-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e42d5-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e42d5-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e42d5-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e42d5-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e42d5-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e42d5-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="e42d5-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="e42d5-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e42d5-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e42d5-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e42d5-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e42d5-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="e42d5-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="e42d5-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="e42d5-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="e42d5-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="e42d5-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="e42d5-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="e42d5-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="e42d5-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="e42d5-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="e42d5-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e42d5-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="e42d5-166">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="e42d5-166">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="e42d5-167">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="e42d5-167">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="e42d5-168">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="e42d5-168">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)
