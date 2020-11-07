---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
ms.openlocfilehash: 307bb2c954526b744f31763f0d3a09d0163c8057
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910981"
---
# <span data-ttu-id="25e2c-101">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="25e2c-101">Test-AzNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="25e2c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="25e2c-102">SYNOPSIS</span></span>
<span data-ttu-id="25e2c-103">Возвращает значение, указывающее, разрешен или запрещен пакет в определенном месте.</span><span class="sxs-lookup"><span data-stu-id="25e2c-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

## <span data-ttu-id="25e2c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="25e2c-104">SYNTAX</span></span>

### <span data-ttu-id="25e2c-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="25e2c-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25e2c-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="25e2c-106">SetByName</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25e2c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="25e2c-107">DESCRIPTION</span></span>
<span data-ttu-id="25e2c-108">Командлет Test-AzNetworkWatcherIPFlow, для определенного ресурса виртуальной машины и пакета в указанном направлении с использованием локальных и удаленных, IP-адресов и портов, возвращает сведения о том, является ли пакет разрешенным или нет.</span><span class="sxs-lookup"><span data-stu-id="25e2c-108">The Test-AzNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="25e2c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="25e2c-109">EXAMPLES</span></span>

### <span data-ttu-id="25e2c-110">---Пример 1: запуск Test-AzNetworkWatcherIPFlow---</span><span class="sxs-lookup"><span data-stu-id="25e2c-110">--- Example 1: Run Test-AzNetworkWatcherIPFlow ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="25e2c-111">Получить доступ к сетевому ресурсу в области "Западная Центральная часть США" для этой подписки, а затем получает виртуальную машину и связанные с ней сетевые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="25e2c-111">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="25e2c-112">Затем для первого сетевого интерфейса запускается Test-AzNetworkWatcherIPFlow с помощью первого IP-адреса из первого сетевого интерфейса для исходящего подключения к IP-адресу в Интернете.</span><span class="sxs-lookup"><span data-stu-id="25e2c-112">Then for the first Network Interface, runs Test-AzNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="25e2c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="25e2c-113">PARAMETERS</span></span>

### <span data-ttu-id="25e2c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25e2c-114">-AsJob</span></span>
<span data-ttu-id="25e2c-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="25e2c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25e2c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25e2c-116">-DefaultProfile</span></span>
<span data-ttu-id="25e2c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="25e2c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25e2c-118">-Направление</span><span class="sxs-lookup"><span data-stu-id="25e2c-118">-Direction</span></span>
<span data-ttu-id="25e2c-119">Бокс.</span><span class="sxs-lookup"><span data-stu-id="25e2c-119">Direction.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Inbound, Outbound

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25e2c-120">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="25e2c-120">-LocalIPAddress</span></span>
<span data-ttu-id="25e2c-121">Локальный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="25e2c-121">Local IP Address.</span></span>

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

### <span data-ttu-id="25e2c-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="25e2c-122">-LocalPort</span></span>
<span data-ttu-id="25e2c-123">Локальный порт.</span><span class="sxs-lookup"><span data-stu-id="25e2c-123">Local Port.</span></span>

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

### <span data-ttu-id="25e2c-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="25e2c-124">-NetworkWatcher</span></span>
<span data-ttu-id="25e2c-125">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="25e2c-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="25e2c-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="25e2c-126">-NetworkWatcherName</span></span>
<span data-ttu-id="25e2c-127">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="25e2c-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="25e2c-128">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="25e2c-128">-Protocol</span></span>
<span data-ttu-id="25e2c-129">NNTP.</span><span class="sxs-lookup"><span data-stu-id="25e2c-129">Protocol.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25e2c-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="25e2c-130">-RemoteIPAddress</span></span>
<span data-ttu-id="25e2c-131">Удаленный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="25e2c-131">Remote IP Address.</span></span>

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

### <span data-ttu-id="25e2c-132">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="25e2c-132">-RemotePort</span></span>
<span data-ttu-id="25e2c-133">Удаленный порт.</span><span class="sxs-lookup"><span data-stu-id="25e2c-133">Remote port.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25e2c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25e2c-134">-ResourceGroupName</span></span>
<span data-ttu-id="25e2c-135">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="25e2c-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="25e2c-136">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="25e2c-136">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="25e2c-137">Идентификатор целевого сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="25e2c-137">Target network interface Id.</span></span>

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

### <span data-ttu-id="25e2c-138">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="25e2c-138">-TargetVirtualMachineId</span></span>
<span data-ttu-id="25e2c-139">Целевой ИД виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="25e2c-139">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="25e2c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25e2c-140">CommonParameters</span></span>
<span data-ttu-id="25e2c-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="25e2c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25e2c-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25e2c-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25e2c-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="25e2c-143">INPUTS</span></span>

### <span data-ttu-id="25e2c-144">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="25e2c-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="25e2c-145">System. String</span><span class="sxs-lookup"><span data-stu-id="25e2c-145">System.String</span></span>

## <span data-ttu-id="25e2c-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="25e2c-146">OUTPUTS</span></span>

### <span data-ttu-id="25e2c-147">Microsoft. Azure. Commands. Network. Models. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="25e2c-147">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="25e2c-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="25e2c-148">NOTES</span></span>
<span data-ttu-id="25e2c-149">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, поток, IP</span><span class="sxs-lookup"><span data-stu-id="25e2c-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="25e2c-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="25e2c-150">RELATED LINKS</span></span>

[<span data-ttu-id="25e2c-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="25e2c-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="25e2c-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="25e2c-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="25e2c-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="25e2c-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="25e2c-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="25e2c-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="25e2c-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="25e2c-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="25e2c-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="25e2c-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="25e2c-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="25e2c-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="25e2c-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="25e2c-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="25e2c-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="25e2c-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="25e2c-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="25e2c-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="25e2c-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="25e2c-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="25e2c-162">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="25e2c-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)
