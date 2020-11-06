---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 00adf4abd887c56f4091761a4a2031bb6b033032
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568478"
---
# <span data-ttu-id="dd1c5-101">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dd1c5-101">Get-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="dd1c5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dd1c5-102">SYNOPSIS</span></span>
<span data-ttu-id="dd1c5-103">Возвращает сведения о ресурсе и его свойствах и состоянии.</span><span class="sxs-lookup"><span data-stu-id="dd1c5-103">Gets information and properties and status of a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd1c5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dd1c5-104">SYNTAX</span></span>

### <span data-ttu-id="dd1c5-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dd1c5-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd1c5-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="dd1c5-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd1c5-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="dd1c5-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -Location <String> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd1c5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd1c5-108">DESCRIPTION</span></span>
<span data-ttu-id="dd1c5-109">Get-AzureRmNetworkWatcherPacketCapture получает свойства и состояние ресурса захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="dd1c5-109">The Get-AzureRmNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="dd1c5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dd1c5-110">EXAMPLES</span></span>

### <span data-ttu-id="dd1c5-111">Пример 1: создание захвата пакетов с несколькими фильтрами и получение состояния</span><span class="sxs-lookup"><span data-stu-id="dd1c5-111">Example 1: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="dd1c5-112">В этом примере мы создаем запись пакета с именем "PacketCaptureTest" с несколькими фильтрами и ограничением по времени.</span><span class="sxs-lookup"><span data-stu-id="dd1c5-112">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="dd1c5-113">После завершения сеанса он будет сохранен в указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="dd1c5-113">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="dd1c5-114">Затем вызовите Get-AzureRmNetworkWatcherPacketCapture, чтобы получить состояние сеанса захвата.</span><span class="sxs-lookup"><span data-stu-id="dd1c5-114">We then call Get-AzureRmNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> <span data-ttu-id="dd1c5-115">Примечание: для создания захваченных пакетов на целевой виртуальной машине должно быть установлено расширение сетевого наблюдателя Azure.</span><span class="sxs-lookup"><span data-stu-id="dd1c5-115">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="dd1c5-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dd1c5-116">PARAMETERS</span></span>

### <span data-ttu-id="dd1c5-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd1c5-117">-AsJob</span></span>
<span data-ttu-id="dd1c5-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="dd1c5-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dd1c5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd1c5-119">-DefaultProfile</span></span>
<span data-ttu-id="dd1c5-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dd1c5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd1c5-121">-Location</span><span class="sxs-lookup"><span data-stu-id="dd1c5-121">-Location</span></span>
<span data-ttu-id="dd1c5-122">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="dd1c5-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="dd1c5-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dd1c5-123">-NetworkWatcher</span></span>
<span data-ttu-id="dd1c5-124">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="dd1c5-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="dd1c5-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="dd1c5-125">-NetworkWatcherName</span></span>
<span data-ttu-id="dd1c5-126">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="dd1c5-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="dd1c5-127">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="dd1c5-127">-PacketCaptureName</span></span>
<span data-ttu-id="dd1c5-128">Имя захвата пакета.</span><span class="sxs-lookup"><span data-stu-id="dd1c5-128">The packet capture name.</span></span>

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

### <span data-ttu-id="dd1c5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd1c5-129">-ResourceGroupName</span></span>
<span data-ttu-id="dd1c5-130">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="dd1c5-130">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="dd1c5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd1c5-131">CommonParameters</span></span>
<span data-ttu-id="dd1c5-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dd1c5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd1c5-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd1c5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd1c5-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dd1c5-134">INPUTS</span></span>

### <span data-ttu-id="dd1c5-135">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dd1c5-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="dd1c5-136">Параметры: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dd1c5-136">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="dd1c5-137">System. String</span><span class="sxs-lookup"><span data-stu-id="dd1c5-137">System.String</span></span>
<span data-ttu-id="dd1c5-138">Параметры: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dd1c5-138">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="dd1c5-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd1c5-139">OUTPUTS</span></span>

### <span data-ttu-id="dd1c5-140">Microsoft. Azure. Commands. Network. Models. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="dd1c5-140">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="dd1c5-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="dd1c5-141">NOTES</span></span>
<span data-ttu-id="dd1c5-142">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, пакет, захват, трафик</span><span class="sxs-lookup"><span data-stu-id="dd1c5-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="dd1c5-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd1c5-143">RELATED LINKS</span></span>

[<span data-ttu-id="dd1c5-144">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dd1c5-144">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="dd1c5-145">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dd1c5-145">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="dd1c5-146">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dd1c5-146">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="dd1c5-147">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="dd1c5-147">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="dd1c5-148">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="dd1c5-148">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="dd1c5-149">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="dd1c5-149">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="dd1c5-150">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="dd1c5-150">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="dd1c5-151">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dd1c5-151">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dd1c5-152">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="dd1c5-152">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="dd1c5-153">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dd1c5-153">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dd1c5-154">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dd1c5-154">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dd1c5-155">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dd1c5-155">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dd1c5-156">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd1c5-156">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="dd1c5-157">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="dd1c5-157">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="dd1c5-158">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="dd1c5-158">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="dd1c5-159">Остановить-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dd1c5-159">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dd1c5-160">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dd1c5-160">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dd1c5-161">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dd1c5-161">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dd1c5-162">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="dd1c5-162">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="dd1c5-163">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dd1c5-163">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dd1c5-164">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dd1c5-164">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dd1c5-165">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="dd1c5-165">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="dd1c5-166">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="dd1c5-166">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="dd1c5-167">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="dd1c5-167">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="dd1c5-168">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="dd1c5-168">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="dd1c5-169">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="dd1c5-169">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="dd1c5-170">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dd1c5-170">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)

