---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpacketcapturefilterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
ms.openlocfilehash: c81eada89865585ae56af2ed629ee17e43d57aa8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066242"
---
# <span data-ttu-id="f5bc4-101">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f5bc4-101">New-AzPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="f5bc4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f5bc4-102">SYNOPSIS</span></span>
<span data-ttu-id="f5bc4-103">Создание нового объекта фильтра захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="f5bc4-103">Creates a new packet capture filter object.</span></span>

## <span data-ttu-id="f5bc4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f5bc4-104">SYNTAX</span></span>

```
New-AzPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>] [-LocalIPAddress <String>]
 [-LocalPort <String>] [-RemotePort <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5bc4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5bc4-105">DESCRIPTION</span></span>
<span data-ttu-id="f5bc4-106">Командлет New-AzPacketCaptureFilterConfig создает новый объект фильтра записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="f5bc4-106">The New-AzPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="f5bc4-107">Этот объект используется для ограничения типа пакетов, захваченных в течение сеанса захвата пакетов с использованием указанных условий.</span><span class="sxs-lookup"><span data-stu-id="f5bc4-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="f5bc4-108">Командлет New-AzNetworkWatcherPacketCapture может допускать несколько объектов фильтра для включения сеансов захвата для композиции.</span><span class="sxs-lookup"><span data-stu-id="f5bc4-108">The New-AzNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="f5bc4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f5bc4-109">EXAMPLES</span></span>

### <span data-ttu-id="f5bc4-110">Пример 1: создание захвата пакетов с несколькими фильтрами</span><span class="sxs-lookup"><span data-stu-id="f5bc4-110">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="f5bc4-111">В этом примере мы создаем запись пакета с именем "PacketCaptureTest" с несколькими фильтрами и ограничением по времени.</span><span class="sxs-lookup"><span data-stu-id="f5bc4-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="f5bc4-112">После завершения сеанса он будет сохранен в указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f5bc4-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="f5bc4-113">Примечание: для создания захваченных пакетов на целевой виртуальной машине должно быть установлено расширение сетевого наблюдателя Azure.</span><span class="sxs-lookup"><span data-stu-id="f5bc4-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="f5bc4-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f5bc4-114">PARAMETERS</span></span>

### <span data-ttu-id="f5bc4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5bc4-115">-DefaultProfile</span></span>
<span data-ttu-id="f5bc4-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f5bc4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5bc4-117">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="f5bc4-117">-LocalIPAddress</span></span>
<span data-ttu-id="f5bc4-118">Задает локальный IP-адрес, по которому нужно выполнить фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="f5bc4-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="f5bc4-119">Пример ввода: "127.0.0.1" для записи с одним адресом.</span><span class="sxs-lookup"><span data-stu-id="f5bc4-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="f5bc4-120">"127.0.0.1-127.0.0.255" для диапазона.</span><span class="sxs-lookup"><span data-stu-id="f5bc4-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="f5bc4-121">"127.0.0.1; 127.0.0.5;" для нескольких записей.</span><span class="sxs-lookup"><span data-stu-id="f5bc4-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5bc4-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="f5bc4-122">-LocalPort</span></span>
<span data-ttu-id="f5bc4-123">Задает локальный IP-адрес, по которому нужно выполнить фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="f5bc4-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="f5bc4-124">Пример ввода: "127.0.0.1" для записи с одним адресом.</span><span class="sxs-lookup"><span data-stu-id="f5bc4-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="f5bc4-125">"127.0.0.1-127.0.0.255" для диапазона.</span><span class="sxs-lookup"><span data-stu-id="f5bc4-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="f5bc4-126">"127.0.0.1; 127.0.0.5;" для нескольких записей.</span><span class="sxs-lookup"><span data-stu-id="f5bc4-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5bc4-127">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="f5bc4-127">-Protocol</span></span>
<span data-ttu-id="f5bc4-128">Задает протокол для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="f5bc4-128">Specifies the Protocol to filter on.</span></span> <span data-ttu-id="f5bc4-129">Допустимые значения "TCP", "UDP", "Any"</span><span class="sxs-lookup"><span data-stu-id="f5bc4-129">Acceptable values "TCP","UDP","Any"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5bc4-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="f5bc4-130">-RemoteIPAddress</span></span>
<span data-ttu-id="f5bc4-131">Задает удаленный IP-адрес, по которому нужно выполнить фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="f5bc4-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="f5bc4-132">Пример ввода: "127.0.0.1" для записи с одним адресом.</span><span class="sxs-lookup"><span data-stu-id="f5bc4-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="f5bc4-133">"127.0.0.1-127.0.0.255" для диапазона.</span><span class="sxs-lookup"><span data-stu-id="f5bc4-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="f5bc4-134">"127.0.0.1; 127.0.0.5;" для нескольких записей.</span><span class="sxs-lookup"><span data-stu-id="f5bc4-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5bc4-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="f5bc4-135">-RemotePort</span></span>
<span data-ttu-id="f5bc4-136">Указывает удаленный порт, по которому нужно выполнить фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="f5bc4-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="f5bc4-137">Пример удаленного порта входные данные: "80" для однопортового ввода.</span><span class="sxs-lookup"><span data-stu-id="f5bc4-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="f5bc4-138">"80-85" для диапазона.</span><span class="sxs-lookup"><span data-stu-id="f5bc4-138">"80-85" for range.</span></span>
<span data-ttu-id="f5bc4-139">"80; 443;" для нескольких записей.</span><span class="sxs-lookup"><span data-stu-id="f5bc4-139">"80;443;" for multiple entries.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5bc4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5bc4-140">CommonParameters</span></span>
<span data-ttu-id="f5bc4-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f5bc4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5bc4-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5bc4-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5bc4-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f5bc4-143">INPUTS</span></span>

### <span data-ttu-id="f5bc4-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f5bc4-144">System.String</span></span>

## <span data-ttu-id="f5bc4-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5bc4-145">OUTPUTS</span></span>

### <span data-ttu-id="f5bc4-146">Microsoft. Azure. Commands. Network. Models. PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="f5bc4-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="f5bc4-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="f5bc4-147">NOTES</span></span>
<span data-ttu-id="f5bc4-148">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель, пакет, захват, трафик, фильтр</span><span class="sxs-lookup"><span data-stu-id="f5bc4-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="f5bc4-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5bc4-149">RELATED LINKS</span></span>

[<span data-ttu-id="f5bc4-150">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f5bc4-150">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="f5bc4-151">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f5bc4-151">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="f5bc4-152">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f5bc4-152">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="f5bc4-153">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f5bc4-153">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="f5bc4-154">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f5bc4-154">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f5bc4-155">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f5bc4-155">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="f5bc4-156">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f5bc4-156">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f5bc4-157">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f5bc4-157">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f5bc4-158">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f5bc4-158">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="f5bc4-159">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f5bc4-159">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f5bc4-160">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f5bc4-160">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f5bc4-161">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f5bc4-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f5bc4-162">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5bc4-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="f5bc4-163">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f5bc4-163">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="f5bc4-164">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="f5bc4-164">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="f5bc4-165">Остановить-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f5bc4-165">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f5bc4-166">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f5bc4-166">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f5bc4-167">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f5bc4-167">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f5bc4-168">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="f5bc4-168">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="f5bc4-169">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f5bc4-169">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f5bc4-170">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f5bc4-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f5bc4-171">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="f5bc4-171">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="f5bc4-172">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="f5bc4-172">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="f5bc4-173">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="f5bc4-173">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="f5bc4-174">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="f5bc4-174">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="f5bc4-175">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="f5bc4-175">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="f5bc4-176">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f5bc4-176">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)