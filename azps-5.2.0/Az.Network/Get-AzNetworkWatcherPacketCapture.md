---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 1276a3c63ec4b9c4ec1c2c4c91ea792013cbacc9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415124"
---
# <span data-ttu-id="8e696-101">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8e696-101">Get-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="8e696-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e696-102">SYNOPSIS</span></span>
<span data-ttu-id="8e696-103">Возвращает сведения, свойства и состояние ресурса захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="8e696-103">Gets information and properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="8e696-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8e696-104">SYNTAX</span></span>

### <span data-ttu-id="8e696-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8e696-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e696-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="8e696-106">SetByName</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e696-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="8e696-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherPacketCapture -Location <String> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e696-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e696-108">DESCRIPTION</span></span>
<span data-ttu-id="8e696-109">Он Get-AzNetworkWatcherPacketCapture свойства и состояние ресурса захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="8e696-109">The Get-AzNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="8e696-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8e696-110">EXAMPLES</span></span>

### <span data-ttu-id="8e696-111">Пример 1. Создание пакета с несколькими фильтрами и извлечение состояния</span><span class="sxs-lookup"><span data-stu-id="8e696-111">Example 1: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="8e696-112">В этом примере мы создали пакет PacketCaptureTest с несколькими фильтрами и ограничением по времени.</span><span class="sxs-lookup"><span data-stu-id="8e696-112">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="8e696-113">После завершения сеанса он будет сохранен в указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="8e696-113">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="8e696-114">Затем мы звоним Get-AzNetworkWatcherPacketCapture, чтобы получить состояние сеанса захвата.</span><span class="sxs-lookup"><span data-stu-id="8e696-114">We then call Get-AzNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> <span data-ttu-id="8e696-115">Примечание. Для создания снимков пакетов на целевой виртуальной машине необходимо установить расширение Azure Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="8e696-115">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

>[!NOTE]
><span data-ttu-id="8e696-116">Если создать ссылку на захват пакета непосредственно с New-AzNetworkWatcherPacketCapture, свойства этого пакета будут иметь не все свойства.</span><span class="sxs-lookup"><span data-stu-id="8e696-116">If you create a reference to the packet capture directly from the New-AzNetworkWatcherPacketCapture command, it won't have all the properties.</span></span> <span data-ttu-id="8e696-117">Вы можете получить все свойства пакета, позвонив на Get-AzNetworkWatcherPacketCapture пакета.</span><span class="sxs-lookup"><span data-stu-id="8e696-117">You can get all of the properties of the packet capture by making a call to the Get-AzNetworkWatcherPacketCapture command.</span></span>

### <span data-ttu-id="8e696-118">Пример 2. Создание пакета с несколькими фильтрами и извлечение состояния</span><span class="sxs-lookup"><span data-stu-id="8e696-118">Example 2: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
Get-AzNetworkWatcherPacketCapture -ResourceGroupName rg1 -NetworkWatcherName nw1 -PacketCaptureName PacketCapture*
```

<span data-ttu-id="8e696-119">Этот cmdlet возвращает все PacketCaptures, которые начинаются с PacketCapture в NW1 Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="8e696-119">This cmdlet returns all PacketCaptures that start with "PacketCapture" in the nw1 Network Watcher.</span></span>

## <span data-ttu-id="8e696-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e696-120">PARAMETERS</span></span>

### <span data-ttu-id="8e696-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e696-121">-AsJob</span></span>
<span data-ttu-id="8e696-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8e696-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e696-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e696-123">-DefaultProfile</span></span>
<span data-ttu-id="8e696-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e696-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e696-125">-Location</span><span class="sxs-lookup"><span data-stu-id="8e696-125">-Location</span></span>
<span data-ttu-id="8e696-126">Расположение сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="8e696-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="8e696-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8e696-127">-NetworkWatcher</span></span>
<span data-ttu-id="8e696-128">Сетевой ресурс для просмотра.</span><span class="sxs-lookup"><span data-stu-id="8e696-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="8e696-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="8e696-129">-NetworkWatcherName</span></span>
<span data-ttu-id="8e696-130">Имя сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="8e696-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="8e696-131">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="8e696-131">-PacketCaptureName</span></span>
<span data-ttu-id="8e696-132">Имя захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="8e696-132">The packet capture name.</span></span>

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

### <span data-ttu-id="8e696-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e696-133">-ResourceGroupName</span></span>
<span data-ttu-id="8e696-134">Имя группы ресурсов сетевого watcher.</span><span class="sxs-lookup"><span data-stu-id="8e696-134">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="8e696-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e696-135">CommonParameters</span></span>
<span data-ttu-id="8e696-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e696-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e696-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e696-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e696-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e696-138">INPUTS</span></span>

### <span data-ttu-id="8e696-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8e696-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="8e696-140">System.String</span><span class="sxs-lookup"><span data-stu-id="8e696-140">System.String</span></span>

## <span data-ttu-id="8e696-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8e696-141">OUTPUTS</span></span>

### <span data-ttu-id="8e696-142">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="8e696-142">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="8e696-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8e696-143">NOTES</span></span>
<span data-ttu-id="8e696-144">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, network, networker, network watcher, packet, capture, traffic</span><span class="sxs-lookup"><span data-stu-id="8e696-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="8e696-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e696-145">RELATED LINKS</span></span>

[<span data-ttu-id="8e696-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8e696-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="8e696-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8e696-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="8e696-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8e696-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="8e696-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8e696-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="8e696-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8e696-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="8e696-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8e696-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="8e696-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="8e696-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="8e696-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8e696-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8e696-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8e696-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="8e696-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8e696-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8e696-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8e696-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8e696-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8e696-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8e696-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e696-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="8e696-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8e696-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="8e696-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="8e696-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="8e696-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8e696-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8e696-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8e696-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8e696-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8e696-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8e696-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="8e696-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="8e696-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8e696-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8e696-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8e696-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8e696-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="8e696-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="8e696-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="8e696-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="8e696-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="8e696-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="8e696-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="8e696-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="8e696-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="8e696-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="8e696-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8e696-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
