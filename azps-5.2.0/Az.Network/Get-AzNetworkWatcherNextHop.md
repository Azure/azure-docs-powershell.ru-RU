---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
ms.openlocfilehash: cf120e8e9ca9e0dad8f4d430c7f207d40fcfab3b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409927"
---
# <span data-ttu-id="55219-101">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="55219-101">Get-AzNetworkWatcherNextHop</span></span>

## <span data-ttu-id="55219-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55219-102">SYNOPSIS</span></span>
<span data-ttu-id="55219-103">Переход от VM к следующему переходу.</span><span class="sxs-lookup"><span data-stu-id="55219-103">Gets the next hop from a VM.</span></span>

## <span data-ttu-id="55219-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="55219-104">SYNTAX</span></span>

### <span data-ttu-id="55219-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="55219-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55219-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="55219-106">SetByName</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55219-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="55219-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherNextHop -Location <String> -TargetVirtualMachineId <String> -DestinationIPAddress <String>
 -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55219-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55219-108">DESCRIPTION</span></span>
<span data-ttu-id="55219-109">Следующий Get-AzNetworkWatcherNextHop-проектлет получает следующий переход от VM.</span><span class="sxs-lookup"><span data-stu-id="55219-109">The Get-AzNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="55219-110">Следующий переход позволяет просмотреть тип ресурса Azure, его IP-адрес и правило для таблицы маршрутов, за которое отвечает маршрут.</span><span class="sxs-lookup"><span data-stu-id="55219-110">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="55219-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="55219-111">EXAMPLES</span></span>

### <span data-ttu-id="55219-112">Пример 1. Переход на следующий переход при общении с IP-адресом в Интернете</span><span class="sxs-lookup"><span data-stu-id="55219-112">Example 1: Get the Next Hop when communicating with an Internet IP</span></span>
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

<span data-ttu-id="55219-113">Следующий переход для исходящие связи из основного сетевого интерфейса на указанной виртуальной машине до 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="55219-113">Gets the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Machine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="55219-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55219-114">PARAMETERS</span></span>

### <span data-ttu-id="55219-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55219-115">-AsJob</span></span>
<span data-ttu-id="55219-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="55219-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="55219-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55219-117">-DefaultProfile</span></span>
<span data-ttu-id="55219-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="55219-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55219-119">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="55219-119">-DestinationIPAddress</span></span>
<span data-ttu-id="55219-120">IP-адрес назначения.</span><span class="sxs-lookup"><span data-stu-id="55219-120">Destination IP address.</span></span>

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

### <span data-ttu-id="55219-121">-Location</span><span class="sxs-lookup"><span data-stu-id="55219-121">-Location</span></span>
<span data-ttu-id="55219-122">Расположение сетевого просмотра.</span><span class="sxs-lookup"><span data-stu-id="55219-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="55219-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="55219-123">-NetworkWatcher</span></span>
<span data-ttu-id="55219-124">Сетевой ресурс для просмотра.</span><span class="sxs-lookup"><span data-stu-id="55219-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="55219-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="55219-125">-NetworkWatcherName</span></span>
<span data-ttu-id="55219-126">Имя сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="55219-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="55219-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55219-127">-ResourceGroupName</span></span>
<span data-ttu-id="55219-128">Имя группы ресурсов сетевого watcher.</span><span class="sxs-lookup"><span data-stu-id="55219-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="55219-129">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="55219-129">-SourceIPAddress</span></span>
<span data-ttu-id="55219-130">IP-адрес источника.</span><span class="sxs-lookup"><span data-stu-id="55219-130">Source IP address.</span></span>

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

### <span data-ttu-id="55219-131">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="55219-131">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="55219-132">ИД целевого сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="55219-132">Target network interface Id.</span></span>

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

### <span data-ttu-id="55219-133">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="55219-133">-TargetVirtualMachineId</span></span>
<span data-ttu-id="55219-134">ИД целевой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="55219-134">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="55219-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55219-135">CommonParameters</span></span>
<span data-ttu-id="55219-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55219-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55219-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55219-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55219-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="55219-138">INPUTS</span></span>

### <span data-ttu-id="55219-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="55219-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="55219-140">System.String</span><span class="sxs-lookup"><span data-stu-id="55219-140">System.String</span></span>

## <span data-ttu-id="55219-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="55219-141">OUTPUTS</span></span>

### <span data-ttu-id="55219-142">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="55219-142">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="55219-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="55219-143">NOTES</span></span>
<span data-ttu-id="55219-144">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, network, networking, network watcher, next, hop</span><span class="sxs-lookup"><span data-stu-id="55219-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="55219-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55219-145">RELATED LINKS</span></span>

[<span data-ttu-id="55219-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="55219-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="55219-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="55219-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="55219-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="55219-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="55219-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="55219-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="55219-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="55219-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="55219-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="55219-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="55219-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="55219-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="55219-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="55219-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="55219-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="55219-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="55219-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="55219-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="55219-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="55219-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="55219-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="55219-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="55219-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="55219-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="55219-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="55219-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="55219-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="55219-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="55219-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="55219-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="55219-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="55219-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="55219-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="55219-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="55219-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="55219-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="55219-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="55219-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="55219-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="55219-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="55219-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="55219-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="55219-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="55219-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="55219-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="55219-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="55219-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="55219-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="55219-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="55219-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="55219-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="55219-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
