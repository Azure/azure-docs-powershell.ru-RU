---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
ms.openlocfilehash: b16b405162a87c54c25f47b7e2a977a8e0022df5
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100416181"
---
# <span data-ttu-id="8e1b7-101">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8e1b7-101">Test-AzNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="8e1b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e1b7-102">SYNOPSIS</span></span>
<span data-ttu-id="8e1b7-103">Возвращает, разрешено ли использовать пакет в определенном месте или из него.</span><span class="sxs-lookup"><span data-stu-id="8e1b7-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

## <span data-ttu-id="8e1b7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8e1b7-104">SYNTAX</span></span>

### <span data-ttu-id="8e1b7-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8e1b7-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e1b7-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="8e1b7-106">SetByName</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e1b7-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="8e1b7-107">SetByLocation</span></span>
```
Test-AzNetworkWatcherIPFlow -Location <String> -TargetVirtualMachineId <String> -Direction <String>
 -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e1b7-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e1b7-108">DESCRIPTION</span></span>
<span data-ttu-id="8e1b7-109">С помощью Test-AzNetworkWatcherIPFlow ИТ-адреса и портов для указанного ресурса VM и пакета с указанным направлением с использованием локальных и удаленных IP-адресов и портов возвращается, разрешен ли пакет.</span><span class="sxs-lookup"><span data-stu-id="8e1b7-109">The Test-AzNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="8e1b7-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8e1b7-110">EXAMPLES</span></span>

### <span data-ttu-id="8e1b7-111">Пример 1. Запуск Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8e1b7-111">Example 1: Run Test-AzNetworkWatcherIPFlow</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzNetworkInterface | Where-Object { $vm.NetworkProfile.NetworkInterfaces.Id -contains $_.Id }

Test-AzNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="8e1b7-112">Получает Network Watcher в Западной центральной части США для этой подписки, а затем получает VM и связанные с ним сетевые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="8e1b7-112">Gets the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="8e1b7-113">Затем для первого сетевого интерфейса выполняется Test-AzNetworkWatcherIPFlow с первым IP-адресом из первого сетевого интерфейса для исходящие подключения к IP-адресу в Интернете.</span><span class="sxs-lookup"><span data-stu-id="8e1b7-113">Then for the first Network Interface, runs Test-AzNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="8e1b7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e1b7-114">PARAMETERS</span></span>

### <span data-ttu-id="8e1b7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e1b7-115">-AsJob</span></span>
<span data-ttu-id="8e1b7-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8e1b7-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e1b7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e1b7-117">-DefaultProfile</span></span>
<span data-ttu-id="8e1b7-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e1b7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e1b7-119">-Direction</span><span class="sxs-lookup"><span data-stu-id="8e1b7-119">-Direction</span></span>
<span data-ttu-id="8e1b7-120">Направление.</span><span class="sxs-lookup"><span data-stu-id="8e1b7-120">Direction.</span></span>

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

### <span data-ttu-id="8e1b7-121">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="8e1b7-121">-LocalIPAddress</span></span>
<span data-ttu-id="8e1b7-122">Локальный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="8e1b7-122">Local IP Address.</span></span>

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

### <span data-ttu-id="8e1b7-123">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="8e1b7-123">-LocalPort</span></span>
<span data-ttu-id="8e1b7-124">Локальный порт.</span><span class="sxs-lookup"><span data-stu-id="8e1b7-124">Local Port.</span></span>

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

### <span data-ttu-id="8e1b7-125">-Location</span><span class="sxs-lookup"><span data-stu-id="8e1b7-125">-Location</span></span>
<span data-ttu-id="8e1b7-126">Расположение сетевого просмотра.</span><span class="sxs-lookup"><span data-stu-id="8e1b7-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="8e1b7-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8e1b7-127">-NetworkWatcher</span></span>
<span data-ttu-id="8e1b7-128">Сетевой ресурс для просмотра.</span><span class="sxs-lookup"><span data-stu-id="8e1b7-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="8e1b7-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="8e1b7-129">-NetworkWatcherName</span></span>
<span data-ttu-id="8e1b7-130">Имя сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="8e1b7-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="8e1b7-131">-Protocol</span><span class="sxs-lookup"><span data-stu-id="8e1b7-131">-Protocol</span></span>
<span data-ttu-id="8e1b7-132">Протокол.</span><span class="sxs-lookup"><span data-stu-id="8e1b7-132">Protocol.</span></span>

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

### <span data-ttu-id="8e1b7-133">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="8e1b7-133">-RemoteIPAddress</span></span>
<span data-ttu-id="8e1b7-134">Удаленный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="8e1b7-134">Remote IP Address.</span></span>

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

### <span data-ttu-id="8e1b7-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="8e1b7-135">-RemotePort</span></span>
<span data-ttu-id="8e1b7-136">Удаленный порт.</span><span class="sxs-lookup"><span data-stu-id="8e1b7-136">Remote port.</span></span>

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

### <span data-ttu-id="8e1b7-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e1b7-137">-ResourceGroupName</span></span>
<span data-ttu-id="8e1b7-138">Имя группы ресурсов сетевого watcher.</span><span class="sxs-lookup"><span data-stu-id="8e1b7-138">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="8e1b7-139">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="8e1b7-139">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="8e1b7-140">ИД целевого сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8e1b7-140">Target network interface Id.</span></span>

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

### <span data-ttu-id="8e1b7-141">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="8e1b7-141">-TargetVirtualMachineId</span></span>
<span data-ttu-id="8e1b7-142">ИД целевой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8e1b7-142">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="8e1b7-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e1b7-143">CommonParameters</span></span>
<span data-ttu-id="8e1b7-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e1b7-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e1b7-145">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e1b7-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e1b7-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e1b7-146">INPUTS</span></span>

### <span data-ttu-id="8e1b7-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8e1b7-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="8e1b7-148">System.String</span><span class="sxs-lookup"><span data-stu-id="8e1b7-148">System.String</span></span>

## <span data-ttu-id="8e1b7-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8e1b7-149">OUTPUTS</span></span>

### <span data-ttu-id="8e1b7-150">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="8e1b7-150">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="8e1b7-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8e1b7-151">NOTES</span></span>
<span data-ttu-id="8e1b7-152">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span><span class="sxs-lookup"><span data-stu-id="8e1b7-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="8e1b7-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e1b7-153">RELATED LINKS</span></span>

[<span data-ttu-id="8e1b7-154">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8e1b7-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="8e1b7-155">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8e1b7-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="8e1b7-156">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8e1b7-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="8e1b7-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8e1b7-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="8e1b7-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8e1b7-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="8e1b7-159">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8e1b7-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="8e1b7-160">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="8e1b7-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="8e1b7-161">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8e1b7-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8e1b7-162">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8e1b7-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="8e1b7-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8e1b7-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8e1b7-164">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8e1b7-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8e1b7-165">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8e1b7-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8e1b7-166">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e1b7-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="8e1b7-167">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8e1b7-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="8e1b7-168">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="8e1b7-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="8e1b7-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8e1b7-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8e1b7-170">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8e1b7-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8e1b7-171">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8e1b7-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8e1b7-172">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="8e1b7-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="8e1b7-173">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8e1b7-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8e1b7-174">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8e1b7-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8e1b7-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="8e1b7-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="8e1b7-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="8e1b7-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="8e1b7-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="8e1b7-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="8e1b7-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="8e1b7-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="8e1b7-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="8e1b7-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="8e1b7-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8e1b7-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
