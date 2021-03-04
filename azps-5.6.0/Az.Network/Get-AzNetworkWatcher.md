---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
ms.openlocfilehash: 93534530c84898f3c4243ad85c75de5bc72e23c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954467"
---
# <span data-ttu-id="c5ffa-101">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c5ffa-101">Get-AzNetworkWatcher</span></span>

## <span data-ttu-id="c5ffa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5ffa-102">SYNOPSIS</span></span>
<span data-ttu-id="c5ffa-103">Свойства сетевого watcher</span><span class="sxs-lookup"><span data-stu-id="c5ffa-103">Gets the properties of a Network Watcher</span></span>

## <span data-ttu-id="c5ffa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c5ffa-104">SYNTAX</span></span>

### <span data-ttu-id="c5ffa-105">Список</span><span class="sxs-lookup"><span data-stu-id="c5ffa-105">List</span></span>
```
Get-AzNetworkWatcher [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c5ffa-106">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c5ffa-106">SetByLocation</span></span>
```
Get-AzNetworkWatcher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5ffa-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5ffa-107">DESCRIPTION</span></span>
<span data-ttu-id="c5ffa-108">Этот Get-AzNetworkWatcher получает один или несколько ресурсов azure Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="c5ffa-108">The Get-AzNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="c5ffa-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c5ffa-109">EXAMPLES</span></span>

### <span data-ttu-id="c5ffa-110">Пример 1. Получить Network Watcher</span><span class="sxs-lookup"><span data-stu-id="c5ffa-110">Example 1: Get a Network Watcher</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="c5ffa-111">Получает network Watcher NetworkWatcher_westcentralus в группе ресурсов NetworkWatcherRG.</span><span class="sxs-lookup"><span data-stu-id="c5ffa-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

### <span data-ttu-id="c5ffa-112">Пример 2. Список сетевых watchers с использованием фильтрации</span><span class="sxs-lookup"><span data-stu-id="c5ffa-112">Example 2: List Network Watchers using filtering</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher*

Name              : NetworkWatcher_westcentralus1
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus1
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded

Name              : NetworkWatcher_westcentralus2
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus2
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="c5ffa-113">Получает network Watchers, которые начинаются с "NetworkWatcher"</span><span class="sxs-lookup"><span data-stu-id="c5ffa-113">Gets the Network Watchers that start with "NetworkWatcher"</span></span>

## <span data-ttu-id="c5ffa-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5ffa-114">PARAMETERS</span></span>

### <span data-ttu-id="c5ffa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5ffa-115">-DefaultProfile</span></span>
<span data-ttu-id="c5ffa-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c5ffa-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5ffa-117">-Location</span><span class="sxs-lookup"><span data-stu-id="c5ffa-117">-Location</span></span>
<span data-ttu-id="c5ffa-118">Расположение сетевого просмотра.</span><span class="sxs-lookup"><span data-stu-id="c5ffa-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="c5ffa-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c5ffa-119">-Name</span></span>
<span data-ttu-id="c5ffa-120">Имя сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="c5ffa-120">The network watcher name.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="c5ffa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5ffa-121">-ResourceGroupName</span></span>
<span data-ttu-id="c5ffa-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c5ffa-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="c5ffa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5ffa-123">CommonParameters</span></span>
<span data-ttu-id="c5ffa-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5ffa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5ffa-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5ffa-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5ffa-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5ffa-126">INPUTS</span></span>

### <span data-ttu-id="c5ffa-127">Нет</span><span class="sxs-lookup"><span data-stu-id="c5ffa-127">None</span></span>

## <span data-ttu-id="c5ffa-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c5ffa-128">OUTPUTS</span></span>

### <span data-ttu-id="c5ffa-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c5ffa-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="c5ffa-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c5ffa-130">NOTES</span></span>
<span data-ttu-id="c5ffa-131">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span><span class="sxs-lookup"><span data-stu-id="c5ffa-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="c5ffa-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5ffa-132">RELATED LINKS</span></span>

[<span data-ttu-id="c5ffa-133">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c5ffa-133">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="c5ffa-134">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c5ffa-134">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="c5ffa-135">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c5ffa-135">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="c5ffa-136">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c5ffa-136">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="c5ffa-137">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c5ffa-137">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c5ffa-138">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c5ffa-138">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="c5ffa-139">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c5ffa-139">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c5ffa-140">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c5ffa-140">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c5ffa-141">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c5ffa-141">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="c5ffa-142">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c5ffa-142">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c5ffa-143">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c5ffa-143">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c5ffa-144">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c5ffa-144">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c5ffa-145">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c5ffa-145">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c5ffa-146">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c5ffa-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="c5ffa-147">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c5ffa-147">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="c5ffa-148">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c5ffa-148">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c5ffa-149">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c5ffa-149">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c5ffa-150">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c5ffa-150">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c5ffa-151">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c5ffa-151">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c5ffa-152">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c5ffa-152">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c5ffa-153">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c5ffa-153">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c5ffa-154">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c5ffa-154">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c5ffa-155">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c5ffa-155">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c5ffa-156">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c5ffa-156">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c5ffa-157">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c5ffa-157">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="c5ffa-158">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c5ffa-158">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="c5ffa-159">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c5ffa-159">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
