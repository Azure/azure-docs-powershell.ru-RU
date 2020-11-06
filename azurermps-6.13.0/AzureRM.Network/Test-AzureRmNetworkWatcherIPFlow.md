---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermnetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
ms.openlocfilehash: 6fc406d0af3ed451fbbf2f14c9ca8943256df744
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569752"
---
# <span data-ttu-id="07ea9-101">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="07ea9-101">Test-AzureRmNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="07ea9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="07ea9-102">SYNOPSIS</span></span>
<span data-ttu-id="07ea9-103">Возвращает значение, указывающее, разрешен или запрещен пакет в определенном месте.</span><span class="sxs-lookup"><span data-stu-id="07ea9-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07ea9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="07ea9-104">SYNTAX</span></span>

### <span data-ttu-id="07ea9-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="07ea9-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07ea9-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="07ea9-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07ea9-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="07ea9-107">SetByLocation</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -Location <String> -TargetVirtualMachineId <String> -Direction <String>
 -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07ea9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07ea9-108">DESCRIPTION</span></span>
<span data-ttu-id="07ea9-109">Командлет Test-AzureRmNetworkWatcherIPFlow, для определенного ресурса виртуальной машины и пакета в указанном направлении с использованием локальных и удаленных, IP-адресов и портов, возвращает сведения о том, является ли пакет разрешенным или нет.</span><span class="sxs-lookup"><span data-stu-id="07ea9-109">The Test-AzureRmNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="07ea9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="07ea9-110">EXAMPLES</span></span>

### <span data-ttu-id="07ea9-111">Пример 1: запуск Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="07ea9-111">Example 1: Run Test-AzureRmNetworkWatcherIPFlow</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="07ea9-112">Получить доступ к сетевому ресурсу в области "Западная Центральная часть США" для этой подписки, а затем получает виртуальную машину и связанные с ней сетевые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="07ea9-112">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="07ea9-113">Затем для первого сетевого интерфейса запускается Test-AzureRmNetworkWatcherIPFlow с помощью первого IP-адреса из первого сетевого интерфейса для исходящего подключения к IP-адресу в Интернете.</span><span class="sxs-lookup"><span data-stu-id="07ea9-113">Then for the first Network Interface, runs Test-AzureRmNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="07ea9-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="07ea9-114">PARAMETERS</span></span>

### <span data-ttu-id="07ea9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07ea9-115">-AsJob</span></span>
<span data-ttu-id="07ea9-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="07ea9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="07ea9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07ea9-117">-DefaultProfile</span></span>
<span data-ttu-id="07ea9-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="07ea9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07ea9-119">-Направление</span><span class="sxs-lookup"><span data-stu-id="07ea9-119">-Direction</span></span>
<span data-ttu-id="07ea9-120">Бокс.</span><span class="sxs-lookup"><span data-stu-id="07ea9-120">Direction.</span></span>

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

### <span data-ttu-id="07ea9-121">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="07ea9-121">-LocalIPAddress</span></span>
<span data-ttu-id="07ea9-122">Локальный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="07ea9-122">Local IP Address.</span></span>

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

### <span data-ttu-id="07ea9-123">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="07ea9-123">-LocalPort</span></span>
<span data-ttu-id="07ea9-124">Локальный порт.</span><span class="sxs-lookup"><span data-stu-id="07ea9-124">Local Port.</span></span>

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

### <span data-ttu-id="07ea9-125">-Location</span><span class="sxs-lookup"><span data-stu-id="07ea9-125">-Location</span></span>
<span data-ttu-id="07ea9-126">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="07ea9-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="07ea9-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="07ea9-127">-NetworkWatcher</span></span>
<span data-ttu-id="07ea9-128">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="07ea9-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="07ea9-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="07ea9-129">-NetworkWatcherName</span></span>
<span data-ttu-id="07ea9-130">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="07ea9-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="07ea9-131">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="07ea9-131">-Protocol</span></span>
<span data-ttu-id="07ea9-132">NNTP.</span><span class="sxs-lookup"><span data-stu-id="07ea9-132">Protocol.</span></span>

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

### <span data-ttu-id="07ea9-133">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="07ea9-133">-RemoteIPAddress</span></span>
<span data-ttu-id="07ea9-134">Удаленный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="07ea9-134">Remote IP Address.</span></span>

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

### <span data-ttu-id="07ea9-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="07ea9-135">-RemotePort</span></span>
<span data-ttu-id="07ea9-136">Удаленный порт.</span><span class="sxs-lookup"><span data-stu-id="07ea9-136">Remote port.</span></span>

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

### <span data-ttu-id="07ea9-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07ea9-137">-ResourceGroupName</span></span>
<span data-ttu-id="07ea9-138">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="07ea9-138">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="07ea9-139">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="07ea9-139">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="07ea9-140">Идентификатор целевого сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="07ea9-140">Target network interface Id.</span></span>

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

### <span data-ttu-id="07ea9-141">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="07ea9-141">-TargetVirtualMachineId</span></span>
<span data-ttu-id="07ea9-142">Целевой ИД виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="07ea9-142">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="07ea9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07ea9-143">CommonParameters</span></span>
<span data-ttu-id="07ea9-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="07ea9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07ea9-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07ea9-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07ea9-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="07ea9-146">INPUTS</span></span>

### <span data-ttu-id="07ea9-147">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="07ea9-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="07ea9-148">Параметры: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="07ea9-148">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="07ea9-149">System. String</span><span class="sxs-lookup"><span data-stu-id="07ea9-149">System.String</span></span>
<span data-ttu-id="07ea9-150">Параметры: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="07ea9-150">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="07ea9-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="07ea9-151">OUTPUTS</span></span>

### <span data-ttu-id="07ea9-152">Microsoft. Azure. Commands. Network. Models. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="07ea9-152">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="07ea9-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="07ea9-153">NOTES</span></span>
<span data-ttu-id="07ea9-154">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, поток, IP</span><span class="sxs-lookup"><span data-stu-id="07ea9-154">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="07ea9-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07ea9-155">RELATED LINKS</span></span>

[<span data-ttu-id="07ea9-156">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="07ea9-156">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="07ea9-157">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="07ea9-157">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="07ea9-158">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="07ea9-158">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="07ea9-159">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="07ea9-159">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="07ea9-160">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="07ea9-160">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="07ea9-161">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="07ea9-161">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="07ea9-162">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="07ea9-162">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="07ea9-163">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="07ea9-163">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="07ea9-164">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="07ea9-164">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="07ea9-165">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="07ea9-165">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="07ea9-166">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="07ea9-166">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="07ea9-167">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="07ea9-167">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="07ea9-168">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="07ea9-168">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="07ea9-169">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="07ea9-169">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="07ea9-170">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="07ea9-170">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="07ea9-171">Остановить-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="07ea9-171">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="07ea9-172">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="07ea9-172">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="07ea9-173">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="07ea9-173">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="07ea9-174">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="07ea9-174">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="07ea9-175">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="07ea9-175">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="07ea9-176">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="07ea9-176">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="07ea9-177">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="07ea9-177">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="07ea9-178">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="07ea9-178">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="07ea9-179">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="07ea9-179">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="07ea9-180">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="07ea9-180">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="07ea9-181">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="07ea9-181">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="07ea9-182">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="07ea9-182">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
