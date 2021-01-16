---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpacketcapturefilterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
ms.openlocfilehash: 194e3c71cc763aeb74091f912b37dd15e4dfe4aa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395055"
---
# <span data-ttu-id="8dc58-101">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8dc58-101">New-AzPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="8dc58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dc58-102">SYNOPSIS</span></span>
<span data-ttu-id="8dc58-103">Создание объекта фильтра пакетов.</span><span class="sxs-lookup"><span data-stu-id="8dc58-103">Creates a new packet capture filter object.</span></span>

## <span data-ttu-id="8dc58-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8dc58-104">SYNTAX</span></span>

```
New-AzPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>] [-LocalIPAddress <String>]
 [-LocalPort <String>] [-RemotePort <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8dc58-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dc58-105">DESCRIPTION</span></span>
<span data-ttu-id="8dc58-106">С New-AzPacketCaptureFilterConfig создается новый объект фильтра захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="8dc58-106">The New-AzPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="8dc58-107">Этот объект используется для ограничения типа пакетов, которые захватываются во время сеанса захвата пакетов, используя указанные условия.</span><span class="sxs-lookup"><span data-stu-id="8dc58-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="8dc58-108">С New-AzNetworkWatcherPacketCapture можно использовать несколько объектов фильтра, чтобы включить сеансы захвата с возможностью сносок.</span><span class="sxs-lookup"><span data-stu-id="8dc58-108">The New-AzNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="8dc58-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8dc58-109">EXAMPLES</span></span>

### <span data-ttu-id="8dc58-110">Пример 1. Создание пакета с несколькими фильтрами</span><span class="sxs-lookup"><span data-stu-id="8dc58-110">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="8dc58-111">В этом примере мы создали пакет PacketCaptureTest с несколькими фильтрами и ограничением по времени.</span><span class="sxs-lookup"><span data-stu-id="8dc58-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="8dc58-112">После завершения сеанса он будет сохранен в указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="8dc58-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="8dc58-113">Примечание. Для создания снимков пакетов на целевой виртуальной машине необходимо установить расширение Azure Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="8dc58-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="8dc58-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8dc58-114">PARAMETERS</span></span>

### <span data-ttu-id="8dc58-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dc58-115">-DefaultProfile</span></span>
<span data-ttu-id="8dc58-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8dc58-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8dc58-117">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="8dc58-117">-LocalIPAddress</span></span>
<span data-ttu-id="8dc58-118">Определяет локальный IP-адрес, по который нужно отфильтровать.</span><span class="sxs-lookup"><span data-stu-id="8dc58-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="8dc58-119">Пример входных данных: "127.0.0.1" для одной записи адреса.</span><span class="sxs-lookup"><span data-stu-id="8dc58-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="8dc58-120">"127.0.0.1-127.0.0.255" для диапазона.</span><span class="sxs-lookup"><span data-stu-id="8dc58-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="8dc58-121">"127.0.0.1:127.0.0.5;" для нескольких записей.</span><span class="sxs-lookup"><span data-stu-id="8dc58-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="8dc58-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="8dc58-122">-LocalPort</span></span>
<span data-ttu-id="8dc58-123">Определяет локальный IP-адрес, по который нужно отфильтровать.</span><span class="sxs-lookup"><span data-stu-id="8dc58-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="8dc58-124">Пример входных данных: "127.0.0.1" для одной записи адреса.</span><span class="sxs-lookup"><span data-stu-id="8dc58-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="8dc58-125">"127.0.0.1-127.0.0.255" для диапазона.</span><span class="sxs-lookup"><span data-stu-id="8dc58-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="8dc58-126">"127.0.0.1:127.0.0.5;" для нескольких записей.</span><span class="sxs-lookup"><span data-stu-id="8dc58-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="8dc58-127">-Protocol</span><span class="sxs-lookup"><span data-stu-id="8dc58-127">-Protocol</span></span>
<span data-ttu-id="8dc58-128">Протокол, по который нужно фильтровать.</span><span class="sxs-lookup"><span data-stu-id="8dc58-128">Specifies the Protocol to filter on.</span></span> <span data-ttu-id="8dc58-129">Допустимые значения :TCP,"UDP","Any"</span><span class="sxs-lookup"><span data-stu-id="8dc58-129">Acceptable values "TCP","UDP","Any"</span></span>

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

### <span data-ttu-id="8dc58-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="8dc58-130">-RemoteIPAddress</span></span>
<span data-ttu-id="8dc58-131">Определяет удаленный IP-адрес, по который нужно отфильтровать.</span><span class="sxs-lookup"><span data-stu-id="8dc58-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="8dc58-132">Пример входных данных: "127.0.0.1" для одной записи адреса.</span><span class="sxs-lookup"><span data-stu-id="8dc58-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="8dc58-133">"127.0.0.1-127.0.0.255" для диапазона.</span><span class="sxs-lookup"><span data-stu-id="8dc58-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="8dc58-134">"127.0.0.1:127.0.0.5;" для нескольких записей.</span><span class="sxs-lookup"><span data-stu-id="8dc58-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="8dc58-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="8dc58-135">-RemotePort</span></span>
<span data-ttu-id="8dc58-136">Определяет удаленный порт, по который нужно отфильтровать.</span><span class="sxs-lookup"><span data-stu-id="8dc58-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="8dc58-137">Пример удаленного порта: "80" для одной записи порта.</span><span class="sxs-lookup"><span data-stu-id="8dc58-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="8dc58-138">"80-85" для диапазона.</span><span class="sxs-lookup"><span data-stu-id="8dc58-138">"80-85" for range.</span></span>
<span data-ttu-id="8dc58-139">"80:443;" для нескольких записей.</span><span class="sxs-lookup"><span data-stu-id="8dc58-139">"80;443;" for multiple entries.</span></span>

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

### <span data-ttu-id="8dc58-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dc58-140">CommonParameters</span></span>
<span data-ttu-id="8dc58-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dc58-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dc58-142">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dc58-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dc58-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8dc58-143">INPUTS</span></span>

### <span data-ttu-id="8dc58-144">System.String</span><span class="sxs-lookup"><span data-stu-id="8dc58-144">System.String</span></span>

## <span data-ttu-id="8dc58-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8dc58-145">OUTPUTS</span></span>

### <span data-ttu-id="8dc58-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="8dc58-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="8dc58-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8dc58-147">NOTES</span></span>
<span data-ttu-id="8dc58-148">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span><span class="sxs-lookup"><span data-stu-id="8dc58-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="8dc58-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8dc58-149">RELATED LINKS</span></span>

[<span data-ttu-id="8dc58-150">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8dc58-150">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="8dc58-151">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8dc58-151">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="8dc58-152">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8dc58-152">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="8dc58-153">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8dc58-153">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="8dc58-154">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8dc58-154">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="8dc58-155">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8dc58-155">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="8dc58-156">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="8dc58-156">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="8dc58-157">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8dc58-157">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8dc58-158">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8dc58-158">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="8dc58-159">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8dc58-159">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8dc58-160">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8dc58-160">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8dc58-161">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8dc58-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8dc58-162">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="8dc58-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="8dc58-163">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8dc58-163">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="8dc58-164">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="8dc58-164">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="8dc58-165">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8dc58-165">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8dc58-166">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8dc58-166">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8dc58-167">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8dc58-167">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8dc58-168">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="8dc58-168">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="8dc58-169">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8dc58-169">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8dc58-170">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8dc58-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8dc58-171">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="8dc58-171">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="8dc58-172">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="8dc58-172">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="8dc58-173">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="8dc58-173">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="8dc58-174">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="8dc58-174">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="8dc58-175">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="8dc58-175">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="8dc58-176">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8dc58-176">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)