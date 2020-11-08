---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: f6762b074c9b185d12666fb8ea92fcaf15a46b05
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248117"
---
# <span data-ttu-id="0dbaf-101">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0dbaf-101">New-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="0dbaf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0dbaf-102">SYNOPSIS</span></span>
<span data-ttu-id="0dbaf-103">Создание нового ресурса захвата пакетов и запуск сеанса захвата пакетов на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

## <span data-ttu-id="0dbaf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0dbaf-104">SYNTAX</span></span>

### <span data-ttu-id="0dbaf-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0dbaf-105">SetByResource (Default)</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dbaf-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="0dbaf-106">SetByName</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0dbaf-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="0dbaf-107">SetByLocation</span></span>
```
New-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0dbaf-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0dbaf-108">DESCRIPTION</span></span>
<span data-ttu-id="0dbaf-109">Командлет New-AzNetworkWatcherPacketCapture создает новый ресурс захвата пакетов и начинает сеанс захвата пакетов на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-109">The New-AzNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="0dbaf-110">Продолжительность сеансов захвата пакетов можно настроить с помощью ограничения по времени или ограничения на размер.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-110">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="0dbaf-111">Также можно настроить объем данных, захваченных для каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-111">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="0dbaf-112">Фильтры можно применять к текущему сеансу захвата пакетов, что позволяет настраивать тип записанных пакетов.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-112">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="0dbaf-113">Фильтры могут ограничивать пакеты на локальных и удаленных IP-адресах & диапазоны адресов, локальные и удаленные порты & диапазоны портов и протокол уровня сеанса для захвата.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-113">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="0dbaf-114">Фильтры дописываются с помощью композиции, и можно применять несколько фильтров для обеспечения детальности захвата.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-114">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="0dbaf-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0dbaf-115">EXAMPLES</span></span>

### <span data-ttu-id="0dbaf-116">Пример 1: создание захвата пакетов с несколькими фильтрами</span><span class="sxs-lookup"><span data-stu-id="0dbaf-116">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="0dbaf-117">В этом примере мы создаем запись пакета с именем "PacketCaptureTest" с несколькими фильтрами и ограничением по времени.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-117">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="0dbaf-118">После завершения сеанса он будет сохранен в указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-118">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="0dbaf-119">Примечание: для создания захваченных пакетов на целевой виртуальной машине должно быть установлено расширение сетевого наблюдателя Azure.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-119">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="0dbaf-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0dbaf-120">PARAMETERS</span></span>

### <span data-ttu-id="0dbaf-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0dbaf-121">-AsJob</span></span>
<span data-ttu-id="0dbaf-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0dbaf-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0dbaf-123">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="0dbaf-123">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="0dbaf-124">Байты для захвата на один пакет.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-124">Bytes to capture per packet.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dbaf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dbaf-125">-DefaultProfile</span></span>
<span data-ttu-id="0dbaf-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0dbaf-127">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="0dbaf-127">-Filter</span></span>
<span data-ttu-id="0dbaf-128">Фильтры для сеанса записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-128">Filters for packet capture session.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dbaf-129">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="0dbaf-129">-LocalFilePath</span></span>
<span data-ttu-id="0dbaf-130">Путь к локальному файлу.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-130">Local file path.</span></span>

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

### <span data-ttu-id="0dbaf-131">-Location</span><span class="sxs-lookup"><span data-stu-id="0dbaf-131">-Location</span></span>
<span data-ttu-id="0dbaf-132">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-132">Location of the network watcher.</span></span>

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

### <span data-ttu-id="0dbaf-133">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0dbaf-133">-NetworkWatcher</span></span>
<span data-ttu-id="0dbaf-134">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-134">The network watcher resource.</span></span>

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

### <span data-ttu-id="0dbaf-135">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="0dbaf-135">-NetworkWatcherName</span></span>
<span data-ttu-id="0dbaf-136">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-136">The name of network watcher.</span></span>

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

### <span data-ttu-id="0dbaf-137">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="0dbaf-137">-PacketCaptureName</span></span>
<span data-ttu-id="0dbaf-138">Имя захвата пакета.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-138">The packet capture name.</span></span>

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

### <span data-ttu-id="0dbaf-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dbaf-139">-ResourceGroupName</span></span>
<span data-ttu-id="0dbaf-140">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-140">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="0dbaf-141">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="0dbaf-141">-StorageAccountId</span></span>
<span data-ttu-id="0dbaf-142">Идентификатор учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-142">Storage account Id.</span></span>

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

### <span data-ttu-id="0dbaf-143">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="0dbaf-143">-StoragePath</span></span>
<span data-ttu-id="0dbaf-144">Путь к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-144">Storage path.</span></span>

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

### <span data-ttu-id="0dbaf-145">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="0dbaf-145">-TargetVirtualMachineId</span></span>
<span data-ttu-id="0dbaf-146">Целевой ИД виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-146">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="0dbaf-147">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="0dbaf-147">-TimeLimitInSeconds</span></span>
<span data-ttu-id="0dbaf-148">Ограничение по времени (в секундах).</span><span class="sxs-lookup"><span data-stu-id="0dbaf-148">Time limit in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dbaf-149">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="0dbaf-149">-TotalBytesPerSession</span></span>
<span data-ttu-id="0dbaf-150">Общее количество байтов на сеанс.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-150">Total bytes per session.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dbaf-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0dbaf-151">-Confirm</span></span>
<span data-ttu-id="0dbaf-152">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dbaf-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dbaf-153">-WhatIf</span></span>
<span data-ttu-id="0dbaf-154">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0dbaf-155">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dbaf-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dbaf-156">CommonParameters</span></span>
<span data-ttu-id="0dbaf-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0dbaf-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dbaf-158">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dbaf-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dbaf-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0dbaf-159">INPUTS</span></span>

### <span data-ttu-id="0dbaf-160">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0dbaf-160">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="0dbaf-161">System. String</span><span class="sxs-lookup"><span data-stu-id="0dbaf-161">System.String</span></span>

### <span data-ttu-id="0dbaf-162">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0dbaf-162">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="0dbaf-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0dbaf-163">OUTPUTS</span></span>

### <span data-ttu-id="0dbaf-164">Microsoft. Azure. Commands. Network. Models. PSPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="0dbaf-164">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureResult</span></span>

## <span data-ttu-id="0dbaf-165">Пуск</span><span class="sxs-lookup"><span data-stu-id="0dbaf-165">NOTES</span></span>
<span data-ttu-id="0dbaf-166">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, пакет, захват, трафик</span><span class="sxs-lookup"><span data-stu-id="0dbaf-166">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="0dbaf-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0dbaf-167">RELATED LINKS</span></span>

[<span data-ttu-id="0dbaf-168">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0dbaf-168">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="0dbaf-169">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0dbaf-169">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="0dbaf-170">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0dbaf-170">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="0dbaf-171">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0dbaf-171">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="0dbaf-172">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0dbaf-172">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0dbaf-173">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0dbaf-173">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="0dbaf-174">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0dbaf-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="0dbaf-175">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0dbaf-175">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0dbaf-176">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0dbaf-176">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="0dbaf-177">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0dbaf-177">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0dbaf-178">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0dbaf-178">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0dbaf-179">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0dbaf-179">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0dbaf-180">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="0dbaf-180">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="0dbaf-181">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0dbaf-181">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="0dbaf-182">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="0dbaf-182">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="0dbaf-183">Остановить-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0dbaf-183">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0dbaf-184">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0dbaf-184">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0dbaf-185">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0dbaf-185">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0dbaf-186">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="0dbaf-186">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="0dbaf-187">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0dbaf-187">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0dbaf-188">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0dbaf-188">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="0dbaf-189">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="0dbaf-189">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="0dbaf-190">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="0dbaf-190">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="0dbaf-191">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="0dbaf-191">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="0dbaf-192">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="0dbaf-192">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="0dbaf-193">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="0dbaf-193">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="0dbaf-194">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="0dbaf-194">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)


