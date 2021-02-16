---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherprotocolconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherProtocolConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherProtocolConfiguration.md
ms.openlocfilehash: 435345992759c85edc4a66c1493ed64e6d440605
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400150"
---
# <span data-ttu-id="0b3b0-101">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b3b0-101">New-AzNetworkWatcherProtocolConfiguration</span></span>

## <span data-ttu-id="0b3b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b3b0-102">SYNOPSIS</span></span>
<span data-ttu-id="0b3b0-103">Создает объект конфигурации протокола.</span><span class="sxs-lookup"><span data-stu-id="0b3b0-103">Creates a new protocol configuration object.</span></span>

## <span data-ttu-id="0b3b0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0b3b0-104">SYNTAX</span></span>

```
New-AzNetworkWatcherProtocolConfiguration -Protocol <String> [-Method <String>] [-Header <IDictionary>]
 [-ValidStatusCode <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b3b0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b3b0-105">DESCRIPTION</span></span>
<span data-ttu-id="0b3b0-106">С New-AzNetworkWatcherProtocolConfiguration создается новый объект конфигурации протокола.</span><span class="sxs-lookup"><span data-stu-id="0b3b0-106">The New-AzNetworkWatcherProtocolConfiguration cmdlet creates a new protocol configuration object.</span></span> <span data-ttu-id="0b3b0-107">Этот объект используется для ограничения соответствия протокола во время сеанса проверки одновременности с использованием указанных критериев.</span><span class="sxs-lookup"><span data-stu-id="0b3b0-107">This object is used to restrict the protocol confiuration during a connecitivity check session using the specified criteria.</span></span> 

## <span data-ttu-id="0b3b0-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0b3b0-108">EXAMPLES</span></span>

### <span data-ttu-id="0b3b0-109">Пример 1. Проверка подключения сетевого средства просмотра с помощью VM-оборудования к веб-сайту с конфигурацией протокола</span><span class="sxs-lookup"><span data-stu-id="0b3b0-109">Example 1: Test Network Watcher Connectivity from a VM to a website with protocol configuration</span></span>
```
$config = New-AzNetworkWatcherProtocolConfiguration -Protocol Http -Method Get -Headers @{"accept"="application/json"} -ValidStatusCodes @(200,202,204)

Test-AzNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80 -ProtocolConfiguration $config


ConnectionStatus : Reachable
AvgLatencyInMs   : 4
MinLatencyInMs   : 2
MaxLatencyInMs   : 15
ProbesSent       : 15
ProbesFailed     : 0
Hops             : [
                     {
                       "Type": "Source",
                       "Id": "f8cff464-e13f-457f-a09e-4dcd53d38a85",
                       "Address": "10.1.1.4",
                       "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/provi                   iders/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                       "NextHopIds": [
                         "1034b1bf-0b1b-4f0a-93b2-900477f45485"
                       ],
                       "Issues": []
                     },
                     {
                       "Type": "Internet",
                       "Id": "1034b1bf-0b1b-4f0a-93b2-900477f45485",
                       "Address": "13.107.21.200",
                       "ResourceId": "Internet",
                       "NextHopIds": [],
                       "Issues": []
                     }
                   ]
```

<span data-ttu-id="0b3b0-110">В этом примере мы протестировали подключение из VM-службы Azure к www.bing.com.</span><span class="sxs-lookup"><span data-stu-id="0b3b0-110">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="0b3b0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b3b0-111">PARAMETERS</span></span>

### <span data-ttu-id="0b3b0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b3b0-112">-DefaultProfile</span></span>
<span data-ttu-id="0b3b0-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0b3b0-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b3b0-114">-Header</span><span class="sxs-lookup"><span data-stu-id="0b3b0-114">-Header</span></span>
<span data-ttu-id="0b3b0-115">Список http-заглавных оглавителей</span><span class="sxs-lookup"><span data-stu-id="0b3b0-115">list of HTTP headers</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b3b0-116">-Method</span><span class="sxs-lookup"><span data-stu-id="0b3b0-116">-Method</span></span>
<span data-ttu-id="0b3b0-117">Метод HTTP</span><span class="sxs-lookup"><span data-stu-id="0b3b0-117">HTTP method</span></span>

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

### <span data-ttu-id="0b3b0-118">-Protocol</span><span class="sxs-lookup"><span data-stu-id="0b3b0-118">-Protocol</span></span>
<span data-ttu-id="0b3b0-119">Тип procotol</span><span class="sxs-lookup"><span data-stu-id="0b3b0-119">Procotol type</span></span>

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

### <span data-ttu-id="0b3b0-120">-ValidStatusCode</span><span class="sxs-lookup"><span data-stu-id="0b3b0-120">-ValidStatusCode</span></span>
<span data-ttu-id="0b3b0-121">действительные коды состояния</span><span class="sxs-lookup"><span data-stu-id="0b3b0-121">valid status codes</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b3b0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b3b0-122">CommonParameters</span></span>
<span data-ttu-id="0b3b0-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b3b0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b3b0-124">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b3b0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b3b0-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0b3b0-125">INPUTS</span></span>

### <span data-ttu-id="0b3b0-126">Нет</span><span class="sxs-lookup"><span data-stu-id="0b3b0-126">None</span></span>

## <span data-ttu-id="0b3b0-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0b3b0-127">OUTPUTS</span></span>

### <span data-ttu-id="0b3b0-128">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b3b0-128">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherProtocolConfiguration</span></span>

## <span data-ttu-id="0b3b0-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0b3b0-129">NOTES</span></span>
<span data-ttu-id="0b3b0-130">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span><span class="sxs-lookup"><span data-stu-id="0b3b0-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span>

## <span data-ttu-id="0b3b0-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0b3b0-131">RELATED LINKS</span></span>

[<span data-ttu-id="0b3b0-132">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0b3b0-132">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="0b3b0-133">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0b3b0-133">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="0b3b0-134">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0b3b0-134">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="0b3b0-135">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0b3b0-135">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="0b3b0-136">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0b3b0-136">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0b3b0-137">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0b3b0-137">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="0b3b0-138">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0b3b0-138">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="0b3b0-139">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0b3b0-139">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0b3b0-140">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0b3b0-140">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="0b3b0-141">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0b3b0-141">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0b3b0-142">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0b3b0-142">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0b3b0-143">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0b3b0-143">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0b3b0-144">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b3b0-144">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="0b3b0-145">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0b3b0-145">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="0b3b0-146">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="0b3b0-146">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="0b3b0-147">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0b3b0-147">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0b3b0-148">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0b3b0-148">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0b3b0-149">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0b3b0-149">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0b3b0-150">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="0b3b0-150">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="0b3b0-151">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0b3b0-151">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0b3b0-152">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0b3b0-152">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0b3b0-153">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="0b3b0-153">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="0b3b0-154">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="0b3b0-154">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="0b3b0-155">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="0b3b0-155">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="0b3b0-156">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="0b3b0-156">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="0b3b0-157">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="0b3b0-157">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="0b3b0-158">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0b3b0-158">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
