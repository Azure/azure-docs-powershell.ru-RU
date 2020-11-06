---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
ms.openlocfilehash: 6e9700f91a9d6f8db5983604a0146f9d864dafd8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569371"
---
# <span data-ttu-id="100b0-101">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="100b0-101">Test-AzureRmNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="100b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="100b0-102">SYNOPSIS</span></span>
<span data-ttu-id="100b0-103">Возвращает значение, указывающее, разрешен или запрещен пакет в определенном месте.</span><span class="sxs-lookup"><span data-stu-id="100b0-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="100b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="100b0-104">SYNTAX</span></span>

### <span data-ttu-id="100b0-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="100b0-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="100b0-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="100b0-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="100b0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="100b0-107">DESCRIPTION</span></span>
<span data-ttu-id="100b0-108">Командлет Test-AzureRmNetworkWatcherIPFlow, для определенного ресурса виртуальной машины и пакета в указанном направлении с использованием локальных и удаленных, IP-адресов и портов, возвращает сведения о том, является ли пакет разрешенным или нет.</span><span class="sxs-lookup"><span data-stu-id="100b0-108">The Test-AzureRmNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="100b0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="100b0-109">EXAMPLES</span></span>

### <span data-ttu-id="100b0-110">---Пример 1: запуск Test-AzureRmNetworkWatcherIPFlow---</span><span class="sxs-lookup"><span data-stu-id="100b0-110">--- Example 1: Run Test-AzureRmNetworkWatcherIPFlow ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="100b0-111">Получить доступ к сетевому ресурсу в области "Западная Центральная часть США" для этой подписки, а затем получает виртуальную машину и связанные с ней сетевые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="100b0-111">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="100b0-112">Затем для первого сетевого интерфейса запускается Test-AzureRmNetworkWatcherIPFlow с помощью первого IP-адреса из первого сетевого интерфейса для исходящего подключения к IP-адресу в Интернете.</span><span class="sxs-lookup"><span data-stu-id="100b0-112">Then for the first Network Interface, runs Test-AzureRmNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="100b0-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="100b0-113">PARAMETERS</span></span>

### <span data-ttu-id="100b0-114">-Направление</span><span class="sxs-lookup"><span data-stu-id="100b0-114">-Direction</span></span>
<span data-ttu-id="100b0-115">Бокс.</span><span class="sxs-lookup"><span data-stu-id="100b0-115">Direction.</span></span>

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

### <span data-ttu-id="100b0-116">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="100b0-116">-LocalIPAddress</span></span>
<span data-ttu-id="100b0-117">Локальный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="100b0-117">Local IP Address.</span></span>

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

### <span data-ttu-id="100b0-118">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="100b0-118">-LocalPort</span></span>
<span data-ttu-id="100b0-119">Локальный порт.</span><span class="sxs-lookup"><span data-stu-id="100b0-119">Local Port.</span></span>

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

### <span data-ttu-id="100b0-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="100b0-120">-NetworkWatcher</span></span>
<span data-ttu-id="100b0-121">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="100b0-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="100b0-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="100b0-122">-NetworkWatcherName</span></span>
<span data-ttu-id="100b0-123">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="100b0-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="100b0-124">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="100b0-124">-Protocol</span></span>
<span data-ttu-id="100b0-125">NNTP.</span><span class="sxs-lookup"><span data-stu-id="100b0-125">Protocol.</span></span>

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

### <span data-ttu-id="100b0-126">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="100b0-126">-RemoteIPAddress</span></span>
<span data-ttu-id="100b0-127">Удаленный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="100b0-127">Remote IP Address.</span></span>

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

### <span data-ttu-id="100b0-128">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="100b0-128">-RemotePort</span></span>
<span data-ttu-id="100b0-129">Удаленный порт.</span><span class="sxs-lookup"><span data-stu-id="100b0-129">Remote port.</span></span>

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

### <span data-ttu-id="100b0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="100b0-130">-ResourceGroupName</span></span>
<span data-ttu-id="100b0-131">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="100b0-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="100b0-132">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="100b0-132">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="100b0-133">Идентификатор целевого сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="100b0-133">Target network interface Id.</span></span>

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

### <span data-ttu-id="100b0-134">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="100b0-134">-TargetVirtualMachineId</span></span>
<span data-ttu-id="100b0-135">Целевой ИД виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="100b0-135">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="100b0-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="100b0-136">-DefaultProfile</span></span>
<span data-ttu-id="100b0-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="100b0-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="100b0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="100b0-138">CommonParameters</span></span>
<span data-ttu-id="100b0-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="100b0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="100b0-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="100b0-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="100b0-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="100b0-141">INPUTS</span></span>

### <span data-ttu-id="100b0-142">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="100b0-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="100b0-143">System. String</span><span class="sxs-lookup"><span data-stu-id="100b0-143">System.String</span></span>

## <span data-ttu-id="100b0-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="100b0-144">OUTPUTS</span></span>

### <span data-ttu-id="100b0-145">Microsoft. Azure. Commands. Network. Models. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="100b0-145">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="100b0-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="100b0-146">NOTES</span></span>
<span data-ttu-id="100b0-147">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, поток, IP</span><span class="sxs-lookup"><span data-stu-id="100b0-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="100b0-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="100b0-148">RELATED LINKS</span></span>

[<span data-ttu-id="100b0-149">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="100b0-149">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="100b0-150">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="100b0-150">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="100b0-151">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="100b0-151">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="100b0-152">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="100b0-152">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="100b0-153">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="100b0-153">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="100b0-154">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="100b0-154">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="100b0-155">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="100b0-155">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="100b0-156">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="100b0-156">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="100b0-157">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="100b0-157">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="100b0-158">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="100b0-158">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="100b0-159">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="100b0-159">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="100b0-160">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="100b0-160">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
