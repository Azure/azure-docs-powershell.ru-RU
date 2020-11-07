---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcher.md
ms.openlocfilehash: c1ea29572bb42bea0c7e64c3ec818fe2f2d0ed0f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912197"
---
# <span data-ttu-id="40d30-101">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="40d30-101">Get-AzNetworkWatcher</span></span>

## <span data-ttu-id="40d30-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="40d30-102">SYNOPSIS</span></span>
<span data-ttu-id="40d30-103">Возвращает свойства наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="40d30-103">Gets the properties of a Network Watcher</span></span>

## <span data-ttu-id="40d30-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="40d30-104">SYNTAX</span></span>

### <span data-ttu-id="40d30-105">Список</span><span class="sxs-lookup"><span data-stu-id="40d30-105">List</span></span>
```
Get-AzNetworkWatcher [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="40d30-106">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="40d30-106">SetByLocation</span></span>
```
Get-AzNetworkWatcher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40d30-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40d30-107">DESCRIPTION</span></span>
<span data-ttu-id="40d30-108">Командлет Get-AzNetworkWatcher получает один или несколько ресурсов сетевого наблюдателя Azure.</span><span class="sxs-lookup"><span data-stu-id="40d30-108">The Get-AzNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="40d30-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="40d30-109">EXAMPLES</span></span>

### <span data-ttu-id="40d30-110">Пример 1: получение сетевого наблюдателя</span><span class="sxs-lookup"><span data-stu-id="40d30-110">Example 1: Get a Network Watcher</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="40d30-111">Возвращает наблюдатель сети с именем NetworkWatcher_westcentralus в группе NetworkWatcherRG ресурсов.</span><span class="sxs-lookup"><span data-stu-id="40d30-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

### <span data-ttu-id="40d30-112">Пример 2: Просмотр списка наблюдателей сети с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="40d30-112">Example 2: List Network Watchers using filtering</span></span>
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

<span data-ttu-id="40d30-113">Возвращает наблюдатели сети, которые начинаются с "NetworkWatcher".</span><span class="sxs-lookup"><span data-stu-id="40d30-113">Gets the Network Watchers that start with "NetworkWatcher"</span></span>

## <span data-ttu-id="40d30-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="40d30-114">PARAMETERS</span></span>

### <span data-ttu-id="40d30-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40d30-115">-DefaultProfile</span></span>
<span data-ttu-id="40d30-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40d30-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40d30-117">-Location</span><span class="sxs-lookup"><span data-stu-id="40d30-117">-Location</span></span>
<span data-ttu-id="40d30-118">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="40d30-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="40d30-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="40d30-119">-Name</span></span>
<span data-ttu-id="40d30-120">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="40d30-120">The network watcher name.</span></span>

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

### <span data-ttu-id="40d30-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40d30-121">-ResourceGroupName</span></span>
<span data-ttu-id="40d30-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="40d30-122">The resource group name.</span></span>

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

### <span data-ttu-id="40d30-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40d30-123">CommonParameters</span></span>
<span data-ttu-id="40d30-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="40d30-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40d30-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40d30-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40d30-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="40d30-126">INPUTS</span></span>

### <span data-ttu-id="40d30-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="40d30-127">None</span></span>

## <span data-ttu-id="40d30-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="40d30-128">OUTPUTS</span></span>

### <span data-ttu-id="40d30-129">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="40d30-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="40d30-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="40d30-130">NOTES</span></span>
<span data-ttu-id="40d30-131">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети</span><span class="sxs-lookup"><span data-stu-id="40d30-131">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="40d30-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40d30-132">RELATED LINKS</span></span>

[<span data-ttu-id="40d30-133">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="40d30-133">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="40d30-134">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="40d30-134">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="40d30-135">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="40d30-135">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="40d30-136">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="40d30-136">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="40d30-137">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="40d30-137">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="40d30-138">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="40d30-138">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="40d30-139">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="40d30-139">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="40d30-140">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="40d30-140">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="40d30-141">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="40d30-141">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="40d30-142">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="40d30-142">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="40d30-143">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="40d30-143">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="40d30-144">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="40d30-144">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="40d30-145">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="40d30-145">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="40d30-146">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="40d30-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="40d30-147">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="40d30-147">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="40d30-148">Остановить-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="40d30-148">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="40d30-149">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="40d30-149">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="40d30-150">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="40d30-150">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="40d30-151">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="40d30-151">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="40d30-152">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="40d30-152">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="40d30-153">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="40d30-153">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="40d30-154">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="40d30-154">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="40d30-155">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="40d30-155">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="40d30-156">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="40d30-156">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="40d30-157">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="40d30-157">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="40d30-158">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="40d30-158">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="40d30-159">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="40d30-159">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
