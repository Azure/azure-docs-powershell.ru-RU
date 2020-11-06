---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
ms.openlocfilehash: 4c6a1e179cf0c6086035488d092232e85c570637
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562964"
---
# <span data-ttu-id="86a5f-101">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="86a5f-101">Get-AzureRmNetworkWatcherNextHop</span></span>

## <span data-ttu-id="86a5f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="86a5f-102">SYNOPSIS</span></span>
<span data-ttu-id="86a5f-103">Получает следующий прыжок от виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="86a5f-103">Gets the next hop from a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86a5f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="86a5f-104">SYNTAX</span></span>

### <span data-ttu-id="86a5f-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="86a5f-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86a5f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="86a5f-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86a5f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="86a5f-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherNextHop -Location <String> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86a5f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86a5f-108">DESCRIPTION</span></span>
<span data-ttu-id="86a5f-109">Командлет Get-AzureRmNetworkWatcherNextHop получает следующий прыжок от виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="86a5f-109">The Get-AzureRmNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="86a5f-110">Следующий прыжок позволяет просматривать тип ресурса Azure, соответствующий IP-адрес ресурса и правило таблицы маршрутизации, ответственное за маршрут.</span><span class="sxs-lookup"><span data-stu-id="86a5f-110">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="86a5f-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="86a5f-111">EXAMPLES</span></span>

### <span data-ttu-id="86a5f-112">Пример 1: получение следующего прыжка при общении с IP-адресом в Интернете</span><span class="sxs-lookup"><span data-stu-id="86a5f-112">Example 1: Get the Next Hop when communicating with an Internet IP</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -SourceIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress  -DestinationIPAddress 204.79.197.200


NextHopIpAddress NextHopType RouteTableId
---------------- ----------- ------------
                 Internet    System Route
```

<span data-ttu-id="86a5f-113">Перейти к следующему прыжку для исходящей связи с основным сетевым интерфейсом на указанном виртуальном Vachineе в 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="86a5f-113">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="86a5f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="86a5f-114">PARAMETERS</span></span>

### <span data-ttu-id="86a5f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86a5f-115">-AsJob</span></span>
<span data-ttu-id="86a5f-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="86a5f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86a5f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86a5f-117">-DefaultProfile</span></span>
<span data-ttu-id="86a5f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="86a5f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86a5f-119">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="86a5f-119">-DestinationIPAddress</span></span>
<span data-ttu-id="86a5f-120">IP-адрес назначения.</span><span class="sxs-lookup"><span data-stu-id="86a5f-120">Destination IP address.</span></span>

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

### <span data-ttu-id="86a5f-121">-Location</span><span class="sxs-lookup"><span data-stu-id="86a5f-121">-Location</span></span>
<span data-ttu-id="86a5f-122">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="86a5f-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="86a5f-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86a5f-123">-NetworkWatcher</span></span>
<span data-ttu-id="86a5f-124">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="86a5f-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="86a5f-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="86a5f-125">-NetworkWatcherName</span></span>
<span data-ttu-id="86a5f-126">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="86a5f-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="86a5f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86a5f-127">-ResourceGroupName</span></span>
<span data-ttu-id="86a5f-128">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="86a5f-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="86a5f-129">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="86a5f-129">-SourceIPAddress</span></span>
<span data-ttu-id="86a5f-130">IP-адрес источника.</span><span class="sxs-lookup"><span data-stu-id="86a5f-130">Source IP address.</span></span>

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

### <span data-ttu-id="86a5f-131">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="86a5f-131">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="86a5f-132">Идентификатор целевого сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="86a5f-132">Target network interface Id.</span></span>

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

### <span data-ttu-id="86a5f-133">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="86a5f-133">-TargetVirtualMachineId</span></span>
<span data-ttu-id="86a5f-134">Целевой ИД виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="86a5f-134">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="86a5f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86a5f-135">CommonParameters</span></span>
<span data-ttu-id="86a5f-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="86a5f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86a5f-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86a5f-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86a5f-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="86a5f-138">INPUTS</span></span>

### <span data-ttu-id="86a5f-139">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86a5f-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="86a5f-140">Параметры: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="86a5f-140">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="86a5f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="86a5f-141">System.String</span></span>
<span data-ttu-id="86a5f-142">Параметры: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="86a5f-142">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="86a5f-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="86a5f-143">OUTPUTS</span></span>

### <span data-ttu-id="86a5f-144">Microsoft. Azure. Commands. Network. Models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="86a5f-144">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="86a5f-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="86a5f-145">NOTES</span></span>
<span data-ttu-id="86a5f-146">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, далее, прыжок</span><span class="sxs-lookup"><span data-stu-id="86a5f-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="86a5f-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86a5f-147">RELATED LINKS</span></span>

[<span data-ttu-id="86a5f-148">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86a5f-148">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="86a5f-149">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86a5f-149">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="86a5f-150">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="86a5f-150">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="86a5f-151">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="86a5f-151">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="86a5f-152">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="86a5f-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="86a5f-153">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="86a5f-153">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="86a5f-154">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="86a5f-154">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="86a5f-155">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86a5f-155">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="86a5f-156">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="86a5f-156">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="86a5f-157">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86a5f-157">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="86a5f-158">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86a5f-158">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="86a5f-159">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="86a5f-159">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="86a5f-160">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="86a5f-160">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="86a5f-161">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="86a5f-161">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="86a5f-162">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="86a5f-162">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="86a5f-163">Остановить-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86a5f-163">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="86a5f-164">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86a5f-164">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="86a5f-165">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86a5f-165">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="86a5f-166">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="86a5f-166">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="86a5f-167">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86a5f-167">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="86a5f-168">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86a5f-168">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="86a5f-169">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="86a5f-169">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="86a5f-170">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="86a5f-170">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="86a5f-171">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="86a5f-171">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="86a5f-172">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="86a5f-172">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="86a5f-173">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="86a5f-173">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="86a5f-174">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="86a5f-174">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
