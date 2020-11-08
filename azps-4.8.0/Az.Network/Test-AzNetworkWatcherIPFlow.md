---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
ms.openlocfilehash: 75b8d976dc4c7be0544f2445ef991723c692edbf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235979"
---
# <span data-ttu-id="91c90-101">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="91c90-101">Test-AzNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="91c90-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="91c90-102">SYNOPSIS</span></span>
<span data-ttu-id="91c90-103">Возвращает значение, указывающее, разрешен или запрещен пакет в определенном месте.</span><span class="sxs-lookup"><span data-stu-id="91c90-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

## <span data-ttu-id="91c90-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="91c90-104">SYNTAX</span></span>

### <span data-ttu-id="91c90-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="91c90-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91c90-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="91c90-106">SetByName</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91c90-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="91c90-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherIPFlow -Location <String> -TargetVirtualMachineId <String> -Direction <String>
 -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91c90-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="91c90-108">DESCRIPTION</span></span>
<span data-ttu-id="91c90-109">Командлет Test-AzNetworkWatcherIPFlow, для определенного ресурса виртуальной машины и пакета в указанном направлении с использованием локальных и удаленных, IP-адресов и портов, возвращает сведения о том, является ли пакет разрешенным или нет.</span><span class="sxs-lookup"><span data-stu-id="91c90-109">The Test-AzNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="91c90-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="91c90-110">EXAMPLES</span></span>

### <span data-ttu-id="91c90-111">Пример 1: запуск Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="91c90-111">Example 1: Run Test-AzNetworkWatcherIPFlow</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzNetworkInterface | Where-Object { $vm.NetworkProfile.NetworkInterfaces.Id -contains $_.Id }

Test-AzNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="91c90-112">Возвращает наблюдатель сети в Западной Центральной США для этой подписки, затем получает виртуальную машину и связанные с ней сетевые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="91c90-112">Gets the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="91c90-113">Затем для первого сетевого интерфейса запускается Test-AzNetworkWatcherIPFlow с помощью первого IP-адреса из первого сетевого интерфейса для исходящего подключения к IP-адресу в Интернете.</span><span class="sxs-lookup"><span data-stu-id="91c90-113">Then for the first Network Interface, runs Test-AzNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="91c90-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="91c90-114">PARAMETERS</span></span>

### <span data-ttu-id="91c90-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91c90-115">-AsJob</span></span>
<span data-ttu-id="91c90-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="91c90-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91c90-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91c90-117">-DefaultProfile</span></span>
<span data-ttu-id="91c90-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="91c90-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91c90-119">-Направление</span><span class="sxs-lookup"><span data-stu-id="91c90-119">-Direction</span></span>
<span data-ttu-id="91c90-120">Бокс.</span><span class="sxs-lookup"><span data-stu-id="91c90-120">Direction.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91c90-121">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="91c90-121">-LocalIPAddress</span></span>
<span data-ttu-id="91c90-122">Локальный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="91c90-122">Local IP Address.</span></span>

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

### <span data-ttu-id="91c90-123">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="91c90-123">-LocalPort</span></span>
<span data-ttu-id="91c90-124">Локальный порт.</span><span class="sxs-lookup"><span data-stu-id="91c90-124">Local Port.</span></span>

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

### <span data-ttu-id="91c90-125">-Location</span><span class="sxs-lookup"><span data-stu-id="91c90-125">-Location</span></span>
<span data-ttu-id="91c90-126">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="91c90-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="91c90-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="91c90-127">-NetworkWatcher</span></span>
<span data-ttu-id="91c90-128">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="91c90-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="91c90-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="91c90-129">-NetworkWatcherName</span></span>
<span data-ttu-id="91c90-130">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="91c90-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="91c90-131">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="91c90-131">-Protocol</span></span>
<span data-ttu-id="91c90-132">NNTP.</span><span class="sxs-lookup"><span data-stu-id="91c90-132">Protocol.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91c90-133">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="91c90-133">-RemoteIPAddress</span></span>
<span data-ttu-id="91c90-134">Удаленный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="91c90-134">Remote IP Address.</span></span>

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

### <span data-ttu-id="91c90-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="91c90-135">-RemotePort</span></span>
<span data-ttu-id="91c90-136">Удаленный порт.</span><span class="sxs-lookup"><span data-stu-id="91c90-136">Remote port.</span></span>

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

### <span data-ttu-id="91c90-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91c90-137">-ResourceGroupName</span></span>
<span data-ttu-id="91c90-138">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="91c90-138">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="91c90-139">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="91c90-139">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="91c90-140">Идентификатор целевого сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="91c90-140">Target network interface Id.</span></span>

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

### <span data-ttu-id="91c90-141">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="91c90-141">-TargetVirtualMachineId</span></span>
<span data-ttu-id="91c90-142">Целевой ИД виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="91c90-142">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="91c90-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91c90-143">CommonParameters</span></span>
<span data-ttu-id="91c90-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="91c90-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91c90-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91c90-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91c90-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="91c90-146">INPUTS</span></span>

### <span data-ttu-id="91c90-147">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="91c90-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="91c90-148">System. String</span><span class="sxs-lookup"><span data-stu-id="91c90-148">System.String</span></span>

## <span data-ttu-id="91c90-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="91c90-149">OUTPUTS</span></span>

### <span data-ttu-id="91c90-150">Microsoft. Azure. Commands. Network. Models. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="91c90-150">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="91c90-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="91c90-151">NOTES</span></span>
<span data-ttu-id="91c90-152">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, поток, IP</span><span class="sxs-lookup"><span data-stu-id="91c90-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="91c90-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="91c90-153">RELATED LINKS</span></span>

[<span data-ttu-id="91c90-154">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="91c90-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="91c90-155">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="91c90-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="91c90-156">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="91c90-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="91c90-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="91c90-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="91c90-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="91c90-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="91c90-159">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="91c90-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="91c90-160">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="91c90-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="91c90-161">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="91c90-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="91c90-162">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="91c90-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="91c90-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="91c90-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="91c90-164">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="91c90-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="91c90-165">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="91c90-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="91c90-166">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="91c90-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="91c90-167">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="91c90-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="91c90-168">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="91c90-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="91c90-169">Остановить-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="91c90-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="91c90-170">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="91c90-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="91c90-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="91c90-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="91c90-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="91c90-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="91c90-173">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="91c90-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="91c90-174">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="91c90-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="91c90-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="91c90-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="91c90-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="91c90-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="91c90-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="91c90-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="91c90-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="91c90-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="91c90-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="91c90-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="91c90-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="91c90-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
