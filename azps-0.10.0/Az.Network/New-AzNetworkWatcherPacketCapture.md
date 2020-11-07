---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 6844db506ee8a55c7d0c16f54946e35349059ae4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909633"
---
# <span data-ttu-id="5c846-101">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5c846-101">New-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="5c846-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5c846-102">SYNOPSIS</span></span>
<span data-ttu-id="5c846-103">Создание нового ресурса захвата пакетов и запуск сеанса захвата пакетов на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="5c846-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

## <span data-ttu-id="5c846-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5c846-104">SYNTAX</span></span>

### <span data-ttu-id="5c846-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5c846-105">SetByResource (Default)</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c846-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="5c846-106">SetByName</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c846-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c846-107">DESCRIPTION</span></span>
<span data-ttu-id="5c846-108">Командлет New-AzNetworkWatcherPacketCapture создает новый ресурс захвата пакетов и начинает сеанс захвата пакетов на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="5c846-108">The New-AzNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="5c846-109">Продолжительность сеансов захвата пакетов можно настроить с помощью ограничения по времени или ограничения на размер.</span><span class="sxs-lookup"><span data-stu-id="5c846-109">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="5c846-110">Также можно настроить объем данных, захваченных для каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="5c846-110">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="5c846-111">Фильтры можно применять к текущему сеансу захвата пакетов, что позволяет настраивать тип записанных пакетов.</span><span class="sxs-lookup"><span data-stu-id="5c846-111">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="5c846-112">Фильтры могут ограничивать пакеты на локальных и удаленных IP-адресах & диапазоны адресов, локальные и удаленные порты & диапазоны портов и протокол уровня сеанса для захвата.</span><span class="sxs-lookup"><span data-stu-id="5c846-112">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="5c846-113">Фильтры дописываются с помощью композиции, и можно применять несколько фильтров для обеспечения детальности захвата.</span><span class="sxs-lookup"><span data-stu-id="5c846-113">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="5c846-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5c846-114">EXAMPLES</span></span>

### <span data-ttu-id="5c846-115">---Пример 1: создание захвата пакетов с несколькими фильтрами---</span><span class="sxs-lookup"><span data-stu-id="5c846-115">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="5c846-116">В этом примере мы создаем запись пакета с именем "PacketCaptureTest" с несколькими фильтрами и ограничением по времени.</span><span class="sxs-lookup"><span data-stu-id="5c846-116">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="5c846-117">После завершения сеанса он будет сохранен в указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="5c846-117">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="5c846-118">Примечание: для создания захваченных пакетов на целевой виртуальной машине должно быть установлено расширение сетевого наблюдателя Azure.</span><span class="sxs-lookup"><span data-stu-id="5c846-118">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="5c846-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5c846-119">PARAMETERS</span></span>

### <span data-ttu-id="5c846-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c846-120">-AsJob</span></span>
<span data-ttu-id="5c846-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5c846-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5c846-122">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="5c846-122">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="5c846-123">Байты для захвата на один пакет.</span><span class="sxs-lookup"><span data-stu-id="5c846-123">Bytes to capture per packet.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c846-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c846-124">-DefaultProfile</span></span>
<span data-ttu-id="5c846-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5c846-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c846-126">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="5c846-126">-Filter</span></span>
<span data-ttu-id="5c846-127">Фильтры для сеанса записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="5c846-127">Filters for packet capture session.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c846-128">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="5c846-128">-LocalFilePath</span></span>
<span data-ttu-id="5c846-129">Путь к локальному файлу.</span><span class="sxs-lookup"><span data-stu-id="5c846-129">Local file path.</span></span>

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

### <span data-ttu-id="5c846-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5c846-130">-NetworkWatcher</span></span>
<span data-ttu-id="5c846-131">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="5c846-131">The network watcher resource.</span></span>

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

### <span data-ttu-id="5c846-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="5c846-132">-NetworkWatcherName</span></span>
<span data-ttu-id="5c846-133">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="5c846-133">The name of network watcher.</span></span>

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

### <span data-ttu-id="5c846-134">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="5c846-134">-PacketCaptureName</span></span>
<span data-ttu-id="5c846-135">Имя захвата пакета.</span><span class="sxs-lookup"><span data-stu-id="5c846-135">The packet capture name.</span></span>

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

### <span data-ttu-id="5c846-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c846-136">-ResourceGroupName</span></span>
<span data-ttu-id="5c846-137">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="5c846-137">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="5c846-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="5c846-138">-StorageAccountId</span></span>
<span data-ttu-id="5c846-139">Идентификатор учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="5c846-139">Storage account Id.</span></span>

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

### <span data-ttu-id="5c846-140">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="5c846-140">-StoragePath</span></span>
<span data-ttu-id="5c846-141">Путь к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="5c846-141">Storage path.</span></span>

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

### <span data-ttu-id="5c846-142">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="5c846-142">-TargetVirtualMachineId</span></span>
<span data-ttu-id="5c846-143">Целевой ИД виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5c846-143">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="5c846-144">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="5c846-144">-TimeLimitInSeconds</span></span>
<span data-ttu-id="5c846-145">Ограничение по времени (в секундах).</span><span class="sxs-lookup"><span data-stu-id="5c846-145">Time limit in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c846-146">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="5c846-146">-TotalBytesPerSession</span></span>
<span data-ttu-id="5c846-147">Общее количество байтов на сеанс.</span><span class="sxs-lookup"><span data-stu-id="5c846-147">Total bytes per session.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c846-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c846-148">-Confirm</span></span>
<span data-ttu-id="5c846-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5c846-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c846-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c846-150">-WhatIf</span></span>
<span data-ttu-id="5c846-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5c846-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c846-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5c846-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c846-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c846-153">CommonParameters</span></span>
<span data-ttu-id="5c846-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5c846-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c846-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c846-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c846-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5c846-156">INPUTS</span></span>

### <span data-ttu-id="5c846-157">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5c846-157">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="5c846-158">System. String System. Nullable \` 1 \[ \[ System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="5c846-158">System.String System.Nullable\`1\[\[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

## <span data-ttu-id="5c846-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c846-159">OUTPUTS</span></span>

### <span data-ttu-id="5c846-160">Microsoft. Azure. Commands. Network. Models. PSPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5c846-160">Microsoft.Azure.Commands.Network.Models.PSPacketCapture</span></span>

## <span data-ttu-id="5c846-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="5c846-161">NOTES</span></span>
<span data-ttu-id="5c846-162">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, пакет, захват, трафик</span><span class="sxs-lookup"><span data-stu-id="5c846-162">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="5c846-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c846-163">RELATED LINKS</span></span>

[<span data-ttu-id="5c846-164">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5c846-164">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="5c846-165">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5c846-165">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5c846-166">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5c846-166">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5c846-167">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5c846-167">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5c846-168">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5c846-168">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="5c846-169">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5c846-169">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="5c846-170">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5c846-170">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="5c846-171">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="5c846-171">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="5c846-172">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5c846-172">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="5c846-173">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5c846-173">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="5c846-174">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5c846-174">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="5c846-175">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="5c846-175">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)


