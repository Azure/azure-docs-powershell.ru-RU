---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermnetworkwatcheripflow
schema: 2.0.0
ms.openlocfilehash: 6147697826dbc475c5871acab1f037af21c2b84d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913557"
---
# <span data-ttu-id="77251-101">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="77251-101">Test-AzureRmNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="77251-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="77251-102">SYNOPSIS</span></span>
<span data-ttu-id="77251-103">Возвращает значение, указывающее, разрешен или запрещен пакет в определенном месте.</span><span class="sxs-lookup"><span data-stu-id="77251-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77251-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="77251-104">SYNTAX</span></span>

### <span data-ttu-id="77251-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="77251-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77251-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="77251-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77251-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77251-107">DESCRIPTION</span></span>
<span data-ttu-id="77251-108">Командлет Test-AzureRmNetworkWatcherIPFlow, для определенного ресурса виртуальной машины и пакета в указанном направлении с использованием локальных и удаленных, IP-адресов и портов, возвращает сведения о том, является ли пакет разрешенным или нет.</span><span class="sxs-lookup"><span data-stu-id="77251-108">The Test-AzureRmNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="77251-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="77251-109">EXAMPLES</span></span>

### <span data-ttu-id="77251-110">---Пример 1: запуск Test-AzureRmNetworkWatcherIPFlow---</span><span class="sxs-lookup"><span data-stu-id="77251-110">--- Example 1: Run Test-AzureRmNetworkWatcherIPFlow ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="77251-111">Получить доступ к сетевому ресурсу в области "Западная Центральная часть США" для этой подписки, а затем получает виртуальную машину и связанные с ней сетевые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="77251-111">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="77251-112">Затем для первого сетевого интерфейса запускается Test-AzureRmNetworkWatcherIPFlow с помощью первого IP-адреса из первого сетевого интерфейса для исходящего подключения к IP-адресу в Интернете.</span><span class="sxs-lookup"><span data-stu-id="77251-112">Then for the first Network Interface, runs Test-AzureRmNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="77251-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="77251-113">PARAMETERS</span></span>

### <span data-ttu-id="77251-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77251-114">-AsJob</span></span>
<span data-ttu-id="77251-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="77251-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="77251-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77251-116">-DefaultProfile</span></span>
<span data-ttu-id="77251-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="77251-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77251-118">-Направление</span><span class="sxs-lookup"><span data-stu-id="77251-118">-Direction</span></span>
<span data-ttu-id="77251-119">Бокс.</span><span class="sxs-lookup"><span data-stu-id="77251-119">Direction.</span></span>

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

### <span data-ttu-id="77251-120">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="77251-120">-LocalIPAddress</span></span>
<span data-ttu-id="77251-121">Локальный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="77251-121">Local IP Address.</span></span>

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

### <span data-ttu-id="77251-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="77251-122">-LocalPort</span></span>
<span data-ttu-id="77251-123">Локальный порт.</span><span class="sxs-lookup"><span data-stu-id="77251-123">Local Port.</span></span>

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

### <span data-ttu-id="77251-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="77251-124">-NetworkWatcher</span></span>
<span data-ttu-id="77251-125">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="77251-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="77251-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="77251-126">-NetworkWatcherName</span></span>
<span data-ttu-id="77251-127">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="77251-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="77251-128">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="77251-128">-Protocol</span></span>
<span data-ttu-id="77251-129">NNTP.</span><span class="sxs-lookup"><span data-stu-id="77251-129">Protocol.</span></span>

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

### <span data-ttu-id="77251-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="77251-130">-RemoteIPAddress</span></span>
<span data-ttu-id="77251-131">Удаленный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="77251-131">Remote IP Address.</span></span>

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

### <span data-ttu-id="77251-132">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="77251-132">-RemotePort</span></span>
<span data-ttu-id="77251-133">Удаленный порт.</span><span class="sxs-lookup"><span data-stu-id="77251-133">Remote port.</span></span>

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

### <span data-ttu-id="77251-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77251-134">-ResourceGroupName</span></span>
<span data-ttu-id="77251-135">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="77251-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="77251-136">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="77251-136">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="77251-137">Идентификатор целевого сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="77251-137">Target network interface Id.</span></span>

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

### <span data-ttu-id="77251-138">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="77251-138">-TargetVirtualMachineId</span></span>
<span data-ttu-id="77251-139">Целевой ИД виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="77251-139">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="77251-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77251-140">CommonParameters</span></span>
<span data-ttu-id="77251-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="77251-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77251-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77251-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77251-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="77251-143">INPUTS</span></span>

### <span data-ttu-id="77251-144">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="77251-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="77251-145">System. String</span><span class="sxs-lookup"><span data-stu-id="77251-145">System.String</span></span>

## <span data-ttu-id="77251-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="77251-146">OUTPUTS</span></span>

### <span data-ttu-id="77251-147">Microsoft. Azure. Commands. Network. Models. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="77251-147">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="77251-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="77251-148">NOTES</span></span>
<span data-ttu-id="77251-149">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, поток, IP</span><span class="sxs-lookup"><span data-stu-id="77251-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="77251-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77251-150">RELATED LINKS</span></span>

[<span data-ttu-id="77251-151">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="77251-151">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="77251-152">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="77251-152">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="77251-153">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="77251-153">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="77251-154">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="77251-154">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="77251-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="77251-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="77251-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="77251-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="77251-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="77251-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="77251-158">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="77251-158">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="77251-159">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="77251-159">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="77251-160">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="77251-160">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="77251-161">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="77251-161">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="77251-162">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="77251-162">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
