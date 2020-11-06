---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 0c84927ede94724da94351a219c9c0ec594c688d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570252"
---
# <span data-ttu-id="78563-101">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="78563-101">New-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="78563-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="78563-102">SYNOPSIS</span></span>
<span data-ttu-id="78563-103">Создание нового ресурса захвата пакетов и запуск сеанса захвата пакетов на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="78563-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78563-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="78563-104">SYNTAX</span></span>

### <span data-ttu-id="78563-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="78563-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78563-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="78563-106">SetByName</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78563-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78563-107">DESCRIPTION</span></span>
<span data-ttu-id="78563-108">Командлет New-AzureRmNetworkWatcherPacketCapture создает новый ресурс захвата пакетов и начинает сеанс захвата пакетов на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="78563-108">The New-AzureRmNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="78563-109">Продолжительность сеансов захвата пакетов можно настроить с помощью ограничения по времени или ограничения на размер.</span><span class="sxs-lookup"><span data-stu-id="78563-109">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="78563-110">Также можно настроить объем данных, захваченных для каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="78563-110">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="78563-111">Фильтры можно применять к текущему сеансу захвата пакетов, что позволяет настраивать тип записанных пакетов.</span><span class="sxs-lookup"><span data-stu-id="78563-111">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="78563-112">Фильтры могут ограничивать пакеты на локальных и удаленных IP-адресах & диапазоны адресов, локальные и удаленные порты & диапазоны портов и протокол уровня сеанса для захвата.</span><span class="sxs-lookup"><span data-stu-id="78563-112">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="78563-113">Фильтры дописываются с помощью композиции, и можно применять несколько фильтров для обеспечения детальности захвата.</span><span class="sxs-lookup"><span data-stu-id="78563-113">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="78563-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="78563-114">EXAMPLES</span></span>

### <span data-ttu-id="78563-115">---Пример 1: создание захвата пакетов с несколькими фильтрами---</span><span class="sxs-lookup"><span data-stu-id="78563-115">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="78563-116">В этом примере мы создаем запись пакета с именем "PacketCaptureTest" с несколькими фильтрами и ограничением по времени.</span><span class="sxs-lookup"><span data-stu-id="78563-116">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="78563-117">После завершения сеанса он будет сохранен в указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="78563-117">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="78563-118">Примечание: для создания захваченных пакетов на целевой виртуальной машине должно быть установлено расширение сетевого наблюдателя Azure.</span><span class="sxs-lookup"><span data-stu-id="78563-118">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="78563-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="78563-119">PARAMETERS</span></span>

### <span data-ttu-id="78563-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78563-120">-AsJob</span></span>
<span data-ttu-id="78563-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="78563-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="78563-122">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="78563-122">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="78563-123">Байты для захвата на один пакет.</span><span class="sxs-lookup"><span data-stu-id="78563-123">Bytes to capture per packet.</span></span>

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

### <span data-ttu-id="78563-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78563-124">-DefaultProfile</span></span>
<span data-ttu-id="78563-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="78563-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78563-126">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="78563-126">-Filter</span></span>
<span data-ttu-id="78563-127">Фильтры для сеанса записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="78563-127">Filters for packet capture session.</span></span>

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

### <span data-ttu-id="78563-128">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="78563-128">-LocalFilePath</span></span>
<span data-ttu-id="78563-129">Путь к локальному файлу.</span><span class="sxs-lookup"><span data-stu-id="78563-129">Local file path.</span></span>

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

### <span data-ttu-id="78563-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="78563-130">-NetworkWatcher</span></span>
<span data-ttu-id="78563-131">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="78563-131">The network watcher resource.</span></span>

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

### <span data-ttu-id="78563-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="78563-132">-NetworkWatcherName</span></span>
<span data-ttu-id="78563-133">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="78563-133">The name of network watcher.</span></span>

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

### <span data-ttu-id="78563-134">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="78563-134">-PacketCaptureName</span></span>
<span data-ttu-id="78563-135">Имя захвата пакета.</span><span class="sxs-lookup"><span data-stu-id="78563-135">The packet capture name.</span></span>

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

### <span data-ttu-id="78563-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78563-136">-ResourceGroupName</span></span>
<span data-ttu-id="78563-137">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="78563-137">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="78563-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="78563-138">-StorageAccountId</span></span>
<span data-ttu-id="78563-139">Идентификатор учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="78563-139">Storage account Id.</span></span>

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

### <span data-ttu-id="78563-140">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="78563-140">-StoragePath</span></span>
<span data-ttu-id="78563-141">Путь к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="78563-141">Storage path.</span></span>

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

### <span data-ttu-id="78563-142">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="78563-142">-TargetVirtualMachineId</span></span>
<span data-ttu-id="78563-143">Целевой ИД виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="78563-143">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="78563-144">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="78563-144">-TimeLimitInSeconds</span></span>
<span data-ttu-id="78563-145">Ограничение по времени (в секундах).</span><span class="sxs-lookup"><span data-stu-id="78563-145">Time limit in seconds.</span></span>

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

### <span data-ttu-id="78563-146">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="78563-146">-TotalBytesPerSession</span></span>
<span data-ttu-id="78563-147">Общее количество байтов на сеанс.</span><span class="sxs-lookup"><span data-stu-id="78563-147">Total bytes per session.</span></span>

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

### <span data-ttu-id="78563-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78563-148">-Confirm</span></span>
<span data-ttu-id="78563-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="78563-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78563-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78563-150">-WhatIf</span></span>
<span data-ttu-id="78563-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="78563-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78563-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="78563-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78563-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78563-153">CommonParameters</span></span>
<span data-ttu-id="78563-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="78563-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78563-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78563-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78563-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="78563-156">INPUTS</span></span>

### <span data-ttu-id="78563-157">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="78563-157">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="78563-158">System. String System. Nullable \` 1 \[ \[ System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="78563-158">System.String System.Nullable\`1\[\[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

## <span data-ttu-id="78563-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="78563-159">OUTPUTS</span></span>

### <span data-ttu-id="78563-160">Microsoft. Azure. Commands. Network. Models. PSPacketCapture</span><span class="sxs-lookup"><span data-stu-id="78563-160">Microsoft.Azure.Commands.Network.Models.PSPacketCapture</span></span>

## <span data-ttu-id="78563-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="78563-161">NOTES</span></span>
<span data-ttu-id="78563-162">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, пакет, захват, трафик</span><span class="sxs-lookup"><span data-stu-id="78563-162">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="78563-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78563-163">RELATED LINKS</span></span>

[<span data-ttu-id="78563-164">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="78563-164">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="78563-165">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="78563-165">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="78563-166">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="78563-166">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="78563-167">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="78563-167">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="78563-168">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="78563-168">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="78563-169">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="78563-169">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="78563-170">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="78563-170">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="78563-171">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="78563-171">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="78563-172">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="78563-172">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="78563-173">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="78563-173">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="78563-174">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="78563-174">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="78563-175">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="78563-175">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)


