---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 1276a3c63ec4b9c4ec1c2c4c91ea792013cbacc9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235029"
---
# <span data-ttu-id="6769f-101">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6769f-101">Get-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="6769f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6769f-102">SYNOPSIS</span></span>
<span data-ttu-id="6769f-103">Возвращает сведения о ресурсе и его свойствах и состоянии.</span><span class="sxs-lookup"><span data-stu-id="6769f-103">Gets information and properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="6769f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6769f-104">SYNTAX</span></span>

### <span data-ttu-id="6769f-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6769f-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6769f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="6769f-106">SetByName</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6769f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="6769f-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherPacketCapture -Location <String> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6769f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6769f-108">DESCRIPTION</span></span>
<span data-ttu-id="6769f-109">Get-AzNetworkWatcherPacketCapture получает свойства и состояние ресурса захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="6769f-109">The Get-AzNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="6769f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6769f-110">EXAMPLES</span></span>

### <span data-ttu-id="6769f-111">Пример 1: создание захвата пакетов с несколькими фильтрами и получение состояния</span><span class="sxs-lookup"><span data-stu-id="6769f-111">Example 1: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="6769f-112">В этом примере мы создаем запись пакета с именем "PacketCaptureTest" с несколькими фильтрами и ограничением по времени.</span><span class="sxs-lookup"><span data-stu-id="6769f-112">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="6769f-113">После завершения сеанса он будет сохранен в указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6769f-113">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="6769f-114">Затем вызовите Get-AzNetworkWatcherPacketCapture, чтобы получить состояние сеанса захвата.</span><span class="sxs-lookup"><span data-stu-id="6769f-114">We then call Get-AzNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> <span data-ttu-id="6769f-115">Примечание: для создания захваченных пакетов на целевой виртуальной машине должно быть установлено расширение сетевого наблюдателя Azure.</span><span class="sxs-lookup"><span data-stu-id="6769f-115">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

>[!NOTE]
><span data-ttu-id="6769f-116">Если вы создаете ссылку на захват пакета непосредственно из команды New-AzNetworkWatcherPacketCapture, у нее не будут все свойства.</span><span class="sxs-lookup"><span data-stu-id="6769f-116">If you create a reference to the packet capture directly from the New-AzNetworkWatcherPacketCapture command, it won't have all the properties.</span></span> <span data-ttu-id="6769f-117">Вы можете получить все свойства захвата пакета, вызвав команду "Get-AzNetworkWatcherPacketCapture".</span><span class="sxs-lookup"><span data-stu-id="6769f-117">You can get all of the properties of the packet capture by making a call to the Get-AzNetworkWatcherPacketCapture command.</span></span>

### <span data-ttu-id="6769f-118">Пример 2: создание захвата пакетов с несколькими фильтрами и получение их состояния</span><span class="sxs-lookup"><span data-stu-id="6769f-118">Example 2: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
Get-AzNetworkWatcherPacketCapture -ResourceGroupName rg1 -NetworkWatcherName nw1 -PacketCaptureName PacketCapture*
```

<span data-ttu-id="6769f-119">Этот командлет возвращает все PacketCaptures, которые начинаются с "PacketCapture" в окне сетевого наблюдателя NW1.</span><span class="sxs-lookup"><span data-stu-id="6769f-119">This cmdlet returns all PacketCaptures that start with "PacketCapture" in the nw1 Network Watcher.</span></span>

## <span data-ttu-id="6769f-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6769f-120">PARAMETERS</span></span>

### <span data-ttu-id="6769f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6769f-121">-AsJob</span></span>
<span data-ttu-id="6769f-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6769f-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6769f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6769f-123">-DefaultProfile</span></span>
<span data-ttu-id="6769f-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6769f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6769f-125">-Location</span><span class="sxs-lookup"><span data-stu-id="6769f-125">-Location</span></span>
<span data-ttu-id="6769f-126">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="6769f-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="6769f-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6769f-127">-NetworkWatcher</span></span>
<span data-ttu-id="6769f-128">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="6769f-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="6769f-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="6769f-129">-NetworkWatcherName</span></span>
<span data-ttu-id="6769f-130">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="6769f-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="6769f-131">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="6769f-131">-PacketCaptureName</span></span>
<span data-ttu-id="6769f-132">Имя захвата пакета.</span><span class="sxs-lookup"><span data-stu-id="6769f-132">The packet capture name.</span></span>

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

### <span data-ttu-id="6769f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6769f-133">-ResourceGroupName</span></span>
<span data-ttu-id="6769f-134">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="6769f-134">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="6769f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6769f-135">CommonParameters</span></span>
<span data-ttu-id="6769f-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6769f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6769f-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6769f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6769f-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6769f-138">INPUTS</span></span>

### <span data-ttu-id="6769f-139">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6769f-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="6769f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6769f-140">System.String</span></span>

## <span data-ttu-id="6769f-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6769f-141">OUTPUTS</span></span>

### <span data-ttu-id="6769f-142">Microsoft. Azure. Commands. Network. Models. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="6769f-142">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="6769f-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="6769f-143">NOTES</span></span>
<span data-ttu-id="6769f-144">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, пакет, захват, трафик</span><span class="sxs-lookup"><span data-stu-id="6769f-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="6769f-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6769f-145">RELATED LINKS</span></span>

[<span data-ttu-id="6769f-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6769f-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="6769f-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6769f-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="6769f-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6769f-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="6769f-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="6769f-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="6769f-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="6769f-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="6769f-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="6769f-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="6769f-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="6769f-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="6769f-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6769f-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6769f-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="6769f-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="6769f-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6769f-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6769f-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6769f-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6769f-157">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6769f-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6769f-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="6769f-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="6769f-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="6769f-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="6769f-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="6769f-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="6769f-161">Остановить-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6769f-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6769f-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6769f-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6769f-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6769f-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6769f-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="6769f-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="6769f-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6769f-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6769f-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6769f-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6769f-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="6769f-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="6769f-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="6769f-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="6769f-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="6769f-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="6769f-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="6769f-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="6769f-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="6769f-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="6769f-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6769f-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

