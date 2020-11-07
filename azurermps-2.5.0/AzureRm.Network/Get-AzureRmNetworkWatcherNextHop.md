---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchernexthop
schema: 2.0.0
ms.openlocfilehash: 41c76d78ad27ff889f2dc3e7be254bcc88668023
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914870"
---
# <span data-ttu-id="e01f0-101">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e01f0-101">Get-AzureRmNetworkWatcherNextHop</span></span>

## <span data-ttu-id="e01f0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e01f0-102">SYNOPSIS</span></span>
<span data-ttu-id="e01f0-103">Получает следующий прыжок от виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e01f0-103">Gets the next hop from a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e01f0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e01f0-104">SYNTAX</span></span>

### <span data-ttu-id="e01f0-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e01f0-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e01f0-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="e01f0-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e01f0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e01f0-107">DESCRIPTION</span></span>
<span data-ttu-id="e01f0-108">Командлет Get-AzureRmNetworkWatcherNextHop получает следующий прыжок от виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e01f0-108">The Get-AzureRmNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="e01f0-109">Следующий прыжок позволяет просматривать тип ресурса Azure, соответствующий IP-адрес ресурса и правило таблицы маршрутизации, ответственное за маршрут.</span><span class="sxs-lookup"><span data-stu-id="e01f0-109">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="e01f0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e01f0-110">EXAMPLES</span></span>

### <span data-ttu-id="e01f0-111">--Пример 1: получение следующего прыжка при общении с IP-адресом Интернет--</span><span class="sxs-lookup"><span data-stu-id="e01f0-111">-- Example 1: Get the Next Hop when communicating with an Internet IP --</span></span>
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

<span data-ttu-id="e01f0-112">Перейти к следующему прыжку для исходящей связи с основным сетевым интерфейсом на указанном виртуальном Vachineе в 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="e01f0-112">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="e01f0-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e01f0-113">PARAMETERS</span></span>

### <span data-ttu-id="e01f0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e01f0-114">-AsJob</span></span>
<span data-ttu-id="e01f0-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e01f0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e01f0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e01f0-116">-DefaultProfile</span></span>
<span data-ttu-id="e01f0-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e01f0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e01f0-118">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="e01f0-118">-DestinationIPAddress</span></span>
<span data-ttu-id="e01f0-119">IP-адрес назначения.</span><span class="sxs-lookup"><span data-stu-id="e01f0-119">Destination IP address.</span></span>

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

### <span data-ttu-id="e01f0-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e01f0-120">-NetworkWatcher</span></span>
<span data-ttu-id="e01f0-121">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="e01f0-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="e01f0-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e01f0-122">-NetworkWatcherName</span></span>
<span data-ttu-id="e01f0-123">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="e01f0-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="e01f0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e01f0-124">-ResourceGroupName</span></span>
<span data-ttu-id="e01f0-125">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="e01f0-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="e01f0-126">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="e01f0-126">-SourceIPAddress</span></span>
<span data-ttu-id="e01f0-127">IP-адрес источника.</span><span class="sxs-lookup"><span data-stu-id="e01f0-127">Source IP address.</span></span>

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

### <span data-ttu-id="e01f0-128">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="e01f0-128">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="e01f0-129">Идентификатор целевого сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e01f0-129">Target network interface Id.</span></span>

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

### <span data-ttu-id="e01f0-130">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="e01f0-130">-TargetVirtualMachineId</span></span>
<span data-ttu-id="e01f0-131">Целевой ИД виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e01f0-131">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="e01f0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e01f0-132">CommonParameters</span></span>
<span data-ttu-id="e01f0-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e01f0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e01f0-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e01f0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e01f0-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e01f0-135">INPUTS</span></span>

### <span data-ttu-id="e01f0-136">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e01f0-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="e01f0-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e01f0-137">System.String</span></span>

## <span data-ttu-id="e01f0-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e01f0-138">OUTPUTS</span></span>

### <span data-ttu-id="e01f0-139">Microsoft. Azure. Commands. Network. Models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="e01f0-139">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="e01f0-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="e01f0-140">NOTES</span></span>
<span data-ttu-id="e01f0-141">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, далее, прыжок</span><span class="sxs-lookup"><span data-stu-id="e01f0-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="e01f0-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e01f0-142">RELATED LINKS</span></span>

[<span data-ttu-id="e01f0-143">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e01f0-143">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="e01f0-144">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e01f0-144">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="e01f0-145">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e01f0-145">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="e01f0-146">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e01f0-146">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="e01f0-147">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e01f0-147">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e01f0-148">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e01f0-148">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="e01f0-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e01f0-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="e01f0-150">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e01f0-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e01f0-151">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e01f0-151">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="e01f0-152">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e01f0-152">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e01f0-153">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e01f0-153">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e01f0-154">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e01f0-154">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

