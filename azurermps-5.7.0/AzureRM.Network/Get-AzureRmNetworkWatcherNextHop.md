---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
ms.openlocfilehash: 641678db33e8e7436bda103f95863aefbf31eb96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559015"
---
# <span data-ttu-id="c0485-101">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c0485-101">Get-AzureRmNetworkWatcherNextHop</span></span>

## <span data-ttu-id="c0485-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c0485-102">SYNOPSIS</span></span>
<span data-ttu-id="c0485-103">Получает следующий прыжок от виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c0485-103">Gets the next hop from a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0485-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c0485-104">SYNTAX</span></span>

### <span data-ttu-id="c0485-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c0485-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0485-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="c0485-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0485-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0485-107">DESCRIPTION</span></span>
<span data-ttu-id="c0485-108">Командлет Get-AzureRmNetworkWatcherNextHop получает следующий прыжок от виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c0485-108">The Get-AzureRmNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="c0485-109">Следующий прыжок позволяет просматривать тип ресурса Azure, соответствующий IP-адрес ресурса и правило таблицы маршрутизации, ответственное за маршрут.</span><span class="sxs-lookup"><span data-stu-id="c0485-109">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="c0485-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c0485-110">EXAMPLES</span></span>

### <span data-ttu-id="c0485-111">--Пример 1: получение следующего прыжка при общении с IP-адресом Интернет--</span><span class="sxs-lookup"><span data-stu-id="c0485-111">-- Example 1: Get the Next Hop when communicating with an Internet IP --</span></span>
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

<span data-ttu-id="c0485-112">Перейти к следующему прыжку для исходящей связи с основным сетевым интерфейсом на указанном виртуальном Vachineе в 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="c0485-112">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="c0485-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c0485-113">PARAMETERS</span></span>

### <span data-ttu-id="c0485-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0485-114">-AsJob</span></span>
<span data-ttu-id="c0485-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c0485-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c0485-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0485-116">-DefaultProfile</span></span>
<span data-ttu-id="c0485-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c0485-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0485-118">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="c0485-118">-DestinationIPAddress</span></span>
<span data-ttu-id="c0485-119">IP-адрес назначения.</span><span class="sxs-lookup"><span data-stu-id="c0485-119">Destination IP address.</span></span>

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

### <span data-ttu-id="c0485-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0485-120">-NetworkWatcher</span></span>
<span data-ttu-id="c0485-121">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="c0485-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="c0485-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c0485-122">-NetworkWatcherName</span></span>
<span data-ttu-id="c0485-123">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="c0485-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="c0485-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0485-124">-ResourceGroupName</span></span>
<span data-ttu-id="c0485-125">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="c0485-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c0485-126">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="c0485-126">-SourceIPAddress</span></span>
<span data-ttu-id="c0485-127">IP-адрес источника.</span><span class="sxs-lookup"><span data-stu-id="c0485-127">Source IP address.</span></span>

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

### <span data-ttu-id="c0485-128">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="c0485-128">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="c0485-129">Идентификатор целевого сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c0485-129">Target network interface Id.</span></span>

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

### <span data-ttu-id="c0485-130">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="c0485-130">-TargetVirtualMachineId</span></span>
<span data-ttu-id="c0485-131">Целевой ИД виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c0485-131">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="c0485-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0485-132">CommonParameters</span></span>
<span data-ttu-id="c0485-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c0485-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0485-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0485-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0485-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c0485-135">INPUTS</span></span>

### <span data-ttu-id="c0485-136">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0485-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="c0485-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c0485-137">System.String</span></span>

## <span data-ttu-id="c0485-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0485-138">OUTPUTS</span></span>

### <span data-ttu-id="c0485-139">Microsoft. Azure. Commands. Network. Models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="c0485-139">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="c0485-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="c0485-140">NOTES</span></span>
<span data-ttu-id="c0485-141">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, далее, прыжок</span><span class="sxs-lookup"><span data-stu-id="c0485-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="c0485-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0485-142">RELATED LINKS</span></span>

[<span data-ttu-id="c0485-143">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0485-143">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c0485-144">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0485-144">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c0485-145">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c0485-145">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c0485-146">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c0485-146">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="c0485-147">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c0485-147">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c0485-148">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c0485-148">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="c0485-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c0485-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c0485-150">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c0485-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c0485-151">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c0485-151">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="c0485-152">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c0485-152">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c0485-153">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c0485-153">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c0485-154">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c0485-154">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

