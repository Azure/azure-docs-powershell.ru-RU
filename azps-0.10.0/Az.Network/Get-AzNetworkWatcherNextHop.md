---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
ms.openlocfilehash: 02e24fd35fbe2e5aec5fc8b6ed73d3608d07c5b2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909914"
---
# <span data-ttu-id="2eb18-101">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2eb18-101">Get-AzNetworkWatcherNextHop</span></span>

## <span data-ttu-id="2eb18-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2eb18-102">SYNOPSIS</span></span>
<span data-ttu-id="2eb18-103">Получает следующий прыжок от виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2eb18-103">Gets the next hop from a VM.</span></span>

## <span data-ttu-id="2eb18-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2eb18-104">SYNTAX</span></span>

### <span data-ttu-id="2eb18-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2eb18-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2eb18-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="2eb18-106">SetByName</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2eb18-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2eb18-107">DESCRIPTION</span></span>
<span data-ttu-id="2eb18-108">Командлет Get-AzNetworkWatcherNextHop получает следующий прыжок от виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2eb18-108">The Get-AzNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="2eb18-109">Следующий прыжок позволяет просматривать тип ресурса Azure, соответствующий IP-адрес ресурса и правило таблицы маршрутизации, ответственное за маршрут.</span><span class="sxs-lookup"><span data-stu-id="2eb18-109">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="2eb18-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2eb18-110">EXAMPLES</span></span>

### <span data-ttu-id="2eb18-111">--Пример 1: получение следующего прыжка при общении с IP-адресом Интернет--</span><span class="sxs-lookup"><span data-stu-id="2eb18-111">-- Example 1: Get the Next Hop when communicating with an Internet IP --</span></span>
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

<span data-ttu-id="2eb18-112">Перейти к следующему прыжку для исходящей связи с основным сетевым интерфейсом на указанном виртуальном Vachineе в 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="2eb18-112">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="2eb18-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2eb18-113">PARAMETERS</span></span>

### <span data-ttu-id="2eb18-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2eb18-114">-AsJob</span></span>
<span data-ttu-id="2eb18-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2eb18-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb18-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eb18-116">-DefaultProfile</span></span>
<span data-ttu-id="2eb18-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2eb18-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb18-118">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="2eb18-118">-DestinationIPAddress</span></span>
<span data-ttu-id="2eb18-119">IP-адрес назначения.</span><span class="sxs-lookup"><span data-stu-id="2eb18-119">Destination IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb18-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2eb18-120">-NetworkWatcher</span></span>
<span data-ttu-id="2eb18-121">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="2eb18-121">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2eb18-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2eb18-122">-NetworkWatcherName</span></span>
<span data-ttu-id="2eb18-123">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="2eb18-123">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2eb18-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2eb18-124">-ResourceGroupName</span></span>
<span data-ttu-id="2eb18-125">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="2eb18-125">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2eb18-126">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="2eb18-126">-SourceIPAddress</span></span>
<span data-ttu-id="2eb18-127">IP-адрес источника.</span><span class="sxs-lookup"><span data-stu-id="2eb18-127">Source IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb18-128">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="2eb18-128">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="2eb18-129">Идентификатор целевого сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2eb18-129">Target network interface Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb18-130">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="2eb18-130">-TargetVirtualMachineId</span></span>
<span data-ttu-id="2eb18-131">Целевой ИД виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2eb18-131">The target virtual machine ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2eb18-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eb18-132">CommonParameters</span></span>
<span data-ttu-id="2eb18-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2eb18-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eb18-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2eb18-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eb18-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2eb18-135">INPUTS</span></span>

### <span data-ttu-id="2eb18-136">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2eb18-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="2eb18-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2eb18-137">System.String</span></span>

## <span data-ttu-id="2eb18-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2eb18-138">OUTPUTS</span></span>

### <span data-ttu-id="2eb18-139">Microsoft. Azure. Commands. Network. Models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="2eb18-139">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="2eb18-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="2eb18-140">NOTES</span></span>
<span data-ttu-id="2eb18-141">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, далее, прыжок</span><span class="sxs-lookup"><span data-stu-id="2eb18-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="2eb18-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2eb18-142">RELATED LINKS</span></span>

[<span data-ttu-id="2eb18-143">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2eb18-143">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="2eb18-144">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2eb18-144">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="2eb18-145">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2eb18-145">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="2eb18-146">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2eb18-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="2eb18-147">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2eb18-147">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2eb18-148">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2eb18-148">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="2eb18-149">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2eb18-149">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2eb18-150">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2eb18-150">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2eb18-151">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2eb18-151">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="2eb18-152">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2eb18-152">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2eb18-153">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2eb18-153">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2eb18-154">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2eb18-154">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

