---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
ms.openlocfilehash: d26f50768c561e05b4dc27ad829c063b73c5a336
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569307"
---
# <span data-ttu-id="a7a96-101">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a7a96-101">Get-AzureRmNetworkWatcherNextHop</span></span>

## <span data-ttu-id="a7a96-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a7a96-102">SYNOPSIS</span></span>
<span data-ttu-id="a7a96-103">Получает следующий прыжок от виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a7a96-103">Gets the next hop from a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7a96-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a7a96-104">SYNTAX</span></span>

### <span data-ttu-id="a7a96-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a7a96-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7a96-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a7a96-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7a96-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7a96-107">DESCRIPTION</span></span>
<span data-ttu-id="a7a96-108">Командлет Get-AzureRmNetworkWatcherNextHop получает следующий прыжок от виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a7a96-108">The Get-AzureRmNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="a7a96-109">Следующий прыжок позволяет просматривать тип ресурса Azure, соответствующий IP-адрес ресурса и правило таблицы маршрутизации, ответственное за маршрут.</span><span class="sxs-lookup"><span data-stu-id="a7a96-109">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="a7a96-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a7a96-110">EXAMPLES</span></span>

### <span data-ttu-id="a7a96-111">--Пример 1: получение следующего прыжка при общении с IP-адресом Интернет--</span><span class="sxs-lookup"><span data-stu-id="a7a96-111">-- Example 1: Get the Next Hop when communicating with an Internet IP --</span></span>
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

<span data-ttu-id="a7a96-112">Перейти к следующему прыжку для исходящей связи с основным сетевым интерфейсом на указанном виртуальном Vachineе в 204.79.197.200 (www.bing.com)</span><span class="sxs-lookup"><span data-stu-id="a7a96-112">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="a7a96-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a7a96-113">PARAMETERS</span></span>

### <span data-ttu-id="a7a96-114">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="a7a96-114">-DestinationIPAddress</span></span>
<span data-ttu-id="a7a96-115">IP-адрес назначения.</span><span class="sxs-lookup"><span data-stu-id="a7a96-115">Destination IP address.</span></span>

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

### <span data-ttu-id="a7a96-116">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a7a96-116">-NetworkWatcher</span></span>
<span data-ttu-id="a7a96-117">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="a7a96-117">The network watcher resource.</span></span>

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

### <span data-ttu-id="a7a96-118">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a7a96-118">-NetworkWatcherName</span></span>
<span data-ttu-id="a7a96-119">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="a7a96-119">The name of network watcher.</span></span>

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

### <span data-ttu-id="a7a96-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7a96-120">-ResourceGroupName</span></span>
<span data-ttu-id="a7a96-121">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="a7a96-121">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a7a96-122">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="a7a96-122">-SourceIPAddress</span></span>
<span data-ttu-id="a7a96-123">IP-адрес источника.</span><span class="sxs-lookup"><span data-stu-id="a7a96-123">Source IP address.</span></span>

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

### <span data-ttu-id="a7a96-124">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="a7a96-124">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="a7a96-125">Идентификатор целевого сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a7a96-125">Target network interface Id.</span></span>

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

### <span data-ttu-id="a7a96-126">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="a7a96-126">-TargetVirtualMachineId</span></span>
<span data-ttu-id="a7a96-127">Целевой ИД виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a7a96-127">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="a7a96-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7a96-128">-DefaultProfile</span></span>
<span data-ttu-id="a7a96-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a7a96-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7a96-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7a96-130">CommonParameters</span></span>
<span data-ttu-id="a7a96-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a7a96-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7a96-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7a96-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7a96-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a7a96-133">INPUTS</span></span>

### <span data-ttu-id="a7a96-134">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a7a96-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="a7a96-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a7a96-135">System.String</span></span>

## <span data-ttu-id="a7a96-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7a96-136">OUTPUTS</span></span>

### <span data-ttu-id="a7a96-137">Microsoft. Azure. Commands. Network. Models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="a7a96-137">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="a7a96-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="a7a96-138">NOTES</span></span>
<span data-ttu-id="a7a96-139">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, далее, прыжок</span><span class="sxs-lookup"><span data-stu-id="a7a96-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="a7a96-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7a96-140">RELATED LINKS</span></span>

[<span data-ttu-id="a7a96-141">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a7a96-141">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a7a96-142">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a7a96-142">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a7a96-143">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a7a96-143">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a7a96-144">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a7a96-144">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="a7a96-145">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a7a96-145">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a7a96-146">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a7a96-146">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="a7a96-147">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a7a96-147">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a7a96-148">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a7a96-148">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a7a96-149">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a7a96-149">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="a7a96-150">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a7a96-150">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a7a96-151">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a7a96-151">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a7a96-152">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a7a96-152">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

