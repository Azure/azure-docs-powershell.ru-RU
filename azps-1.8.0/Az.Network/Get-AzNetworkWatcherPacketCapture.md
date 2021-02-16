---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: b98ebe6bfe1bbae1f88c49799f875f56cee52698
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400337"
---
# <span data-ttu-id="22fd9-101">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="22fd9-101">Get-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="22fd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22fd9-102">SYNOPSIS</span></span>
<span data-ttu-id="22fd9-103">Возвращает сведения, свойства и состояние ресурса захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="22fd9-103">Gets information and properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="22fd9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="22fd9-104">SYNTAX</span></span>

### <span data-ttu-id="22fd9-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="22fd9-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22fd9-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="22fd9-106">SetByName</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22fd9-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="22fd9-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherPacketCapture -Location <String> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22fd9-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="22fd9-108">DESCRIPTION</span></span>
<span data-ttu-id="22fd9-109">Он Get-AzNetworkWatcherPacketCapture свойства и состояние ресурса захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="22fd9-109">The Get-AzNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="22fd9-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="22fd9-110">EXAMPLES</span></span>

### <span data-ttu-id="22fd9-111">Пример 1. Создание пакета с несколькими фильтрами и извлечение его состояния</span><span class="sxs-lookup"><span data-stu-id="22fd9-111">Example 1: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="22fd9-112">В этом примере мы создали пакет PacketCaptureTest с несколькими фильтрами и ограничением по времени.</span><span class="sxs-lookup"><span data-stu-id="22fd9-112">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="22fd9-113">После завершения сеанса он будет сохранен в указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="22fd9-113">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="22fd9-114">Затем мы звоним Get-AzNetworkWatcherPacketCapture, чтобы получить состояние сеанса захвата.</span><span class="sxs-lookup"><span data-stu-id="22fd9-114">We then call Get-AzNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> <span data-ttu-id="22fd9-115">Примечание. Для создания снимков пакетов на целевой виртуальной машине необходимо установить расширение Azure Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="22fd9-115">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

### <span data-ttu-id="22fd9-116">Пример 2. Создание пакета с несколькими фильтрами и извлечение состояния</span><span class="sxs-lookup"><span data-stu-id="22fd9-116">Example 2: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
Get-AzNetworkWatcherPacketCapture -ResourceGroupName rg1 -NetworkWatcherName nw1 -PacketCaptureName PacketCapture*
```

<span data-ttu-id="22fd9-117">Этот cmdlet возвращает все PacketCaptures, которые начинаются с PacketCapture в NW1 Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="22fd9-117">This cmdlet returns all PacketCaptures that start with "PacketCapture" in the nw1 Network Watcher.</span></span>

## <span data-ttu-id="22fd9-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22fd9-118">PARAMETERS</span></span>

### <span data-ttu-id="22fd9-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22fd9-119">-AsJob</span></span>
<span data-ttu-id="22fd9-120">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="22fd9-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22fd9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22fd9-121">-DefaultProfile</span></span>
<span data-ttu-id="22fd9-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="22fd9-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22fd9-123">-Location</span><span class="sxs-lookup"><span data-stu-id="22fd9-123">-Location</span></span>
<span data-ttu-id="22fd9-124">Расположение сетевого просмотра.</span><span class="sxs-lookup"><span data-stu-id="22fd9-124">Location of the network watcher.</span></span>

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

### <span data-ttu-id="22fd9-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="22fd9-125">-NetworkWatcher</span></span>
<span data-ttu-id="22fd9-126">Сетевой ресурс для просмотра.</span><span class="sxs-lookup"><span data-stu-id="22fd9-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="22fd9-127">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="22fd9-127">-NetworkWatcherName</span></span>
<span data-ttu-id="22fd9-128">Имя сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="22fd9-128">The name of network watcher.</span></span>

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

### <span data-ttu-id="22fd9-129">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="22fd9-129">-PacketCaptureName</span></span>
<span data-ttu-id="22fd9-130">Имя захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="22fd9-130">The packet capture name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="22fd9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22fd9-131">-ResourceGroupName</span></span>
<span data-ttu-id="22fd9-132">Имя группы ресурсов сетевого watcher.</span><span class="sxs-lookup"><span data-stu-id="22fd9-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="22fd9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22fd9-133">CommonParameters</span></span>
<span data-ttu-id="22fd9-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22fd9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22fd9-135">Дополнительные сведения см. [в about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22fd9-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22fd9-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="22fd9-136">INPUTS</span></span>

### <span data-ttu-id="22fd9-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="22fd9-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="22fd9-138">System.String</span><span class="sxs-lookup"><span data-stu-id="22fd9-138">System.String</span></span>

## <span data-ttu-id="22fd9-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="22fd9-139">OUTPUTS</span></span>

### <span data-ttu-id="22fd9-140">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="22fd9-140">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="22fd9-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="22fd9-141">NOTES</span></span>
<span data-ttu-id="22fd9-142">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, network, networking, network watcher, packet, capture, traffic</span><span class="sxs-lookup"><span data-stu-id="22fd9-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="22fd9-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="22fd9-143">RELATED LINKS</span></span>

[<span data-ttu-id="22fd9-144">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="22fd9-144">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="22fd9-145">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="22fd9-145">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="22fd9-146">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="22fd9-146">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="22fd9-147">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="22fd9-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="22fd9-148">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="22fd9-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="22fd9-149">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="22fd9-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="22fd9-150">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="22fd9-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="22fd9-151">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="22fd9-151">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="22fd9-152">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="22fd9-152">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="22fd9-153">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="22fd9-153">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="22fd9-154">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="22fd9-154">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="22fd9-155">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="22fd9-155">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="22fd9-156">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="22fd9-156">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="22fd9-157">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="22fd9-157">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="22fd9-158">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="22fd9-158">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="22fd9-159">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="22fd9-159">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="22fd9-160">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="22fd9-160">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="22fd9-161">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="22fd9-161">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="22fd9-162">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="22fd9-162">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="22fd9-163">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="22fd9-163">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="22fd9-164">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="22fd9-164">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="22fd9-165">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="22fd9-165">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="22fd9-166">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="22fd9-166">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="22fd9-167">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="22fd9-167">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="22fd9-168">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="22fd9-168">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="22fd9-169">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="22fd9-169">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="22fd9-170">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="22fd9-170">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

