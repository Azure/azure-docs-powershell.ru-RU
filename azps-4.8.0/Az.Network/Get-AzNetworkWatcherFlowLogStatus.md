---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: a45a6ad4ee85dfabb28bef07400a0b6ebe115d7c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399181"
---
# <span data-ttu-id="08c3d-101">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="08c3d-101">Get-AzNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="08c3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08c3d-102">SYNOPSIS</span></span>
<span data-ttu-id="08c3d-103">Возвращает состояние ведения журнала потока для ресурса.</span><span class="sxs-lookup"><span data-stu-id="08c3d-103">Gets the status of flow logging on a resource.</span></span>

## <span data-ttu-id="08c3d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="08c3d-104">SYNTAX</span></span>

### <span data-ttu-id="08c3d-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="08c3d-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08c3d-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="08c3d-106">SetByName</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08c3d-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="08c3d-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -Location <String> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08c3d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="08c3d-108">DESCRIPTION</span></span>
<span data-ttu-id="08c3d-109">Этот Get-AzNetworkWatcherFlowLogStatus возвращает состояние ведения журнала потока для ресурса.</span><span class="sxs-lookup"><span data-stu-id="08c3d-109">The Get-AzNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="08c3d-110">Состояние включает в себя, включено ли ведение журнала потоков для предоставленного ресурса, настроенная учетная запись хранения для отправки журналов и политика хранения журналов.</span><span class="sxs-lookup"><span data-stu-id="08c3d-110">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="08c3d-111">В настоящее время сетевые группы безопасности поддерживают ведение журнала потоков.</span><span class="sxs-lookup"><span data-stu-id="08c3d-111">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="08c3d-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="08c3d-112">EXAMPLES</span></span>

### <span data-ttu-id="08c3d-113">Пример 1. Просмотр состояния ведения журнала потока для указанного NSG</span><span class="sxs-lookup"><span data-stu-id="08c3d-113">Example 1: Get the Flow Logging Status for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
Properties       : {
                     "Enabled": true,
                     "RetentionPolicy": {
                       "Days": 0,
                       "Enabled": false
                     },
                     "StorageId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
                     "Format"         : {
                       "Type ": "Json",
                       "Version": 1
                     }
                   }
```

<span data-ttu-id="08c3d-114">В этом примере мы получаем состояние ведения журнала потока для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="08c3d-114">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="08c3d-115">В указанной NSG включено ведение журнала потоков, формат по умолчанию, а политика хранения не настроена.</span><span class="sxs-lookup"><span data-stu-id="08c3d-115">The specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="08c3d-116">Пример 2. Просмотр состояния журнала потока и аналитики трафика для указанного NSG</span><span class="sxs-lookup"><span data-stu-id="08c3d-116">Example 2: Get the Flow Logging and Traffic Analytics Status for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
FlowAnalyticsConfiguration : {
            "networkWatcherFlowAnalyticsConfiguration": {
              "enabled": true,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName",
              "TrafficAnalyticsInterval": 60
            }
          }
```

<span data-ttu-id="08c3d-117">В этом примере мы получаем данные о состоянии ведения журнала потоков и аналитики трафика для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="08c3d-117">In this example we get the flow logging and Traffic Analytics status for a Network Security Group.</span></span> <span data-ttu-id="08c3d-118">В указанном формате NSG включено ведение журнала потоков и включена аналитика трафика, формат по умолчанию, а политика хранения не настроена.</span><span class="sxs-lookup"><span data-stu-id="08c3d-118">The specified NSG has flow logging and Traffic Analytics enabled, default format and no retention policy set.</span></span>

## <span data-ttu-id="08c3d-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08c3d-119">PARAMETERS</span></span>

### <span data-ttu-id="08c3d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08c3d-120">-AsJob</span></span>
<span data-ttu-id="08c3d-121">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="08c3d-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="08c3d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08c3d-122">-DefaultProfile</span></span>
<span data-ttu-id="08c3d-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="08c3d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08c3d-124">-Location</span><span class="sxs-lookup"><span data-stu-id="08c3d-124">-Location</span></span>
<span data-ttu-id="08c3d-125">Расположение сетевого просмотра.</span><span class="sxs-lookup"><span data-stu-id="08c3d-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="08c3d-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="08c3d-126">-NetworkWatcher</span></span>
<span data-ttu-id="08c3d-127">Сетевой ресурс для просмотра.</span><span class="sxs-lookup"><span data-stu-id="08c3d-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="08c3d-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="08c3d-128">-NetworkWatcherName</span></span>
<span data-ttu-id="08c3d-129">Имя сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="08c3d-129">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08c3d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08c3d-130">-ResourceGroupName</span></span>
<span data-ttu-id="08c3d-131">Имя группы ресурсов сетевого watcher.</span><span class="sxs-lookup"><span data-stu-id="08c3d-131">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08c3d-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="08c3d-132">-TargetResourceId</span></span>
<span data-ttu-id="08c3d-133">ИД целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="08c3d-133">The target resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08c3d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08c3d-134">CommonParameters</span></span>
<span data-ttu-id="08c3d-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08c3d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08c3d-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="08c3d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08c3d-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="08c3d-137">INPUTS</span></span>

### <span data-ttu-id="08c3d-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="08c3d-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="08c3d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="08c3d-139">System.String</span></span>

## <span data-ttu-id="08c3d-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="08c3d-140">OUTPUTS</span></span>

### <span data-ttu-id="08c3d-141">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="08c3d-141">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="08c3d-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="08c3d-142">NOTES</span></span>
<span data-ttu-id="08c3d-143">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking, networking, watcher, flow, logs, flowlog, logging</span><span class="sxs-lookup"><span data-stu-id="08c3d-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="08c3d-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="08c3d-144">RELATED LINKS</span></span>

[<span data-ttu-id="08c3d-145">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="08c3d-145">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="08c3d-146">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="08c3d-146">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="08c3d-147">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="08c3d-147">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="08c3d-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="08c3d-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="08c3d-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="08c3d-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="08c3d-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="08c3d-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="08c3d-151">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="08c3d-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="08c3d-152">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="08c3d-152">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="08c3d-153">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="08c3d-153">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="08c3d-154">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="08c3d-154">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="08c3d-155">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="08c3d-155">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="08c3d-156">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="08c3d-156">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="08c3d-157">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="08c3d-157">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="08c3d-158">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="08c3d-158">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="08c3d-159">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="08c3d-159">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="08c3d-160">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="08c3d-160">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="08c3d-161">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="08c3d-161">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="08c3d-162">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="08c3d-162">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="08c3d-163">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="08c3d-163">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="08c3d-164">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="08c3d-164">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="08c3d-165">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="08c3d-165">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="08c3d-166">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="08c3d-166">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="08c3d-167">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="08c3d-167">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="08c3d-168">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="08c3d-168">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="08c3d-169">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="08c3d-169">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="08c3d-170">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="08c3d-170">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="08c3d-171">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="08c3d-171">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
