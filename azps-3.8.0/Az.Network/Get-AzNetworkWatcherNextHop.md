---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
ms.openlocfilehash: 7fe316bda1cc6385babad2b5a7cb03d44a6fc128
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912192"
---
# <span data-ttu-id="1a0f9-101">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="1a0f9-101">Get-AzNetworkWatcherNextHop</span></span>

## <span data-ttu-id="1a0f9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1a0f9-102">SYNOPSIS</span></span>
<span data-ttu-id="1a0f9-103">Получает следующий прыжок от виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1a0f9-103">Gets the next hop from a VM.</span></span>

## <span data-ttu-id="1a0f9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1a0f9-104">SYNTAX</span></span>

### <span data-ttu-id="1a0f9-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1a0f9-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a0f9-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="1a0f9-106">SetByName</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a0f9-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="1a0f9-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherNextHop -Location <String> -TargetVirtualMachineId <String> -DestinationIPAddress <String>
 -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a0f9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a0f9-108">DESCRIPTION</span></span>
<span data-ttu-id="1a0f9-109">Командлет Get-AzNetworkWatcherNextHop получает следующий прыжок от виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1a0f9-109">The Get-AzNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="1a0f9-110">Следующий прыжок позволяет просматривать тип ресурса Azure, соответствующий IP-адрес ресурса и правило таблицы маршрутизации, ответственное за маршрут.</span><span class="sxs-lookup"><span data-stu-id="1a0f9-110">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="1a0f9-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1a0f9-111">EXAMPLES</span></span>

### <span data-ttu-id="1a0f9-112">Пример 1: получение следующего прыжка при общении с IP-адресом в Интернете</span><span class="sxs-lookup"><span data-stu-id="1a0f9-112">Example 1: Get the Next Hop when communicating with an Internet IP</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0
$Nics = Get-AzNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}
Get-AzNetworkWatcherNextHop -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -SourceIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress  -DestinationIPAddress 204.79.197.200


NextHopIpAddress NextHopType RouteTableId
---------------- ----------- ------------
                 Internet    System Route
```

<span data-ttu-id="1a0f9-113">Возвращает следующий прыжок для исходящей связи от основного сетевого интерфейса на указанной виртуальной машине в 204.79.197.200 (www.bing.com).</span><span class="sxs-lookup"><span data-stu-id="1a0f9-113">Gets the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Machine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="1a0f9-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1a0f9-114">PARAMETERS</span></span>

### <span data-ttu-id="1a0f9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a0f9-115">-AsJob</span></span>
<span data-ttu-id="1a0f9-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1a0f9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a0f9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a0f9-117">-DefaultProfile</span></span>
<span data-ttu-id="1a0f9-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1a0f9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a0f9-119">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="1a0f9-119">-DestinationIPAddress</span></span>
<span data-ttu-id="1a0f9-120">IP-адрес назначения.</span><span class="sxs-lookup"><span data-stu-id="1a0f9-120">Destination IP address.</span></span>

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

### <span data-ttu-id="1a0f9-121">-Location</span><span class="sxs-lookup"><span data-stu-id="1a0f9-121">-Location</span></span>
<span data-ttu-id="1a0f9-122">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="1a0f9-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="1a0f9-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1a0f9-123">-NetworkWatcher</span></span>
<span data-ttu-id="1a0f9-124">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="1a0f9-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="1a0f9-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1a0f9-125">-NetworkWatcherName</span></span>
<span data-ttu-id="1a0f9-126">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="1a0f9-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="1a0f9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a0f9-127">-ResourceGroupName</span></span>
<span data-ttu-id="1a0f9-128">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="1a0f9-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="1a0f9-129">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="1a0f9-129">-SourceIPAddress</span></span>
<span data-ttu-id="1a0f9-130">IP-адрес источника.</span><span class="sxs-lookup"><span data-stu-id="1a0f9-130">Source IP address.</span></span>

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

### <span data-ttu-id="1a0f9-131">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="1a0f9-131">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="1a0f9-132">Идентификатор целевого сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="1a0f9-132">Target network interface Id.</span></span>

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

### <span data-ttu-id="1a0f9-133">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="1a0f9-133">-TargetVirtualMachineId</span></span>
<span data-ttu-id="1a0f9-134">Целевой ИД виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1a0f9-134">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="1a0f9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a0f9-135">CommonParameters</span></span>
<span data-ttu-id="1a0f9-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1a0f9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a0f9-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a0f9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a0f9-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1a0f9-138">INPUTS</span></span>

### <span data-ttu-id="1a0f9-139">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1a0f9-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="1a0f9-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1a0f9-140">System.String</span></span>

## <span data-ttu-id="1a0f9-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a0f9-141">OUTPUTS</span></span>

### <span data-ttu-id="1a0f9-142">Microsoft. Azure. Commands. Network. Models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="1a0f9-142">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="1a0f9-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="1a0f9-143">NOTES</span></span>
<span data-ttu-id="1a0f9-144">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, далее, прыжок</span><span class="sxs-lookup"><span data-stu-id="1a0f9-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="1a0f9-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a0f9-145">RELATED LINKS</span></span>

[<span data-ttu-id="1a0f9-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1a0f9-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="1a0f9-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1a0f9-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="1a0f9-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1a0f9-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="1a0f9-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="1a0f9-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="1a0f9-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1a0f9-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="1a0f9-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="1a0f9-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="1a0f9-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="1a0f9-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="1a0f9-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1a0f9-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1a0f9-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="1a0f9-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="1a0f9-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1a0f9-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1a0f9-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1a0f9-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1a0f9-157">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1a0f9-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1a0f9-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="1a0f9-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="1a0f9-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1a0f9-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="1a0f9-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="1a0f9-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="1a0f9-161">Остановить-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1a0f9-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1a0f9-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1a0f9-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1a0f9-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1a0f9-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1a0f9-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="1a0f9-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="1a0f9-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1a0f9-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1a0f9-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1a0f9-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1a0f9-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="1a0f9-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="1a0f9-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="1a0f9-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="1a0f9-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="1a0f9-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="1a0f9-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="1a0f9-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="1a0f9-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="1a0f9-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="1a0f9-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1a0f9-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
