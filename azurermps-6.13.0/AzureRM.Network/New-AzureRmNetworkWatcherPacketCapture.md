---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: ab7b6176f8453d1a3e5e0001e6b6c1e47c4de1cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569792"
---
# <span data-ttu-id="22b8f-101">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="22b8f-101">New-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="22b8f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="22b8f-102">SYNOPSIS</span></span>
<span data-ttu-id="22b8f-103">Создание нового ресурса захвата пакетов и запуск сеанса захвата пакетов на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="22b8f-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22b8f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="22b8f-104">SYNTAX</span></span>

### <span data-ttu-id="22b8f-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="22b8f-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22b8f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="22b8f-106">SetByName</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22b8f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="22b8f-107">SetByLocation</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22b8f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="22b8f-108">DESCRIPTION</span></span>
<span data-ttu-id="22b8f-109">Командлет New-AzureRmNetworkWatcherPacketCapture создает новый ресурс захвата пакетов и начинает сеанс захвата пакетов на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="22b8f-109">The New-AzureRmNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="22b8f-110">Продолжительность сеансов захвата пакетов можно настроить с помощью ограничения по времени или ограничения на размер.</span><span class="sxs-lookup"><span data-stu-id="22b8f-110">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="22b8f-111">Также можно настроить объем данных, захваченных для каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="22b8f-111">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="22b8f-112">Фильтры можно применять к текущему сеансу захвата пакетов, что позволяет настраивать тип записанных пакетов.</span><span class="sxs-lookup"><span data-stu-id="22b8f-112">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="22b8f-113">Фильтры могут ограничивать пакеты на локальных и удаленных IP-адресах & диапазоны адресов, локальные и удаленные порты & диапазоны портов и протокол уровня сеанса для захвата.</span><span class="sxs-lookup"><span data-stu-id="22b8f-113">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="22b8f-114">Фильтры дописываются с помощью композиции, и можно применять несколько фильтров для обеспечения детальности захвата.</span><span class="sxs-lookup"><span data-stu-id="22b8f-114">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="22b8f-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="22b8f-115">EXAMPLES</span></span>

### <span data-ttu-id="22b8f-116">Пример 1: создание захвата пакетов с несколькими фильтрами</span><span class="sxs-lookup"><span data-stu-id="22b8f-116">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="22b8f-117">В этом примере мы создаем запись пакета с именем "PacketCaptureTest" с несколькими фильтрами и ограничением по времени.</span><span class="sxs-lookup"><span data-stu-id="22b8f-117">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="22b8f-118">После завершения сеанса он будет сохранен в указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="22b8f-118">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="22b8f-119">Примечание: для создания захваченных пакетов на целевой виртуальной машине должно быть установлено расширение сетевого наблюдателя Azure.</span><span class="sxs-lookup"><span data-stu-id="22b8f-119">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="22b8f-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="22b8f-120">PARAMETERS</span></span>

### <span data-ttu-id="22b8f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22b8f-121">-AsJob</span></span>
<span data-ttu-id="22b8f-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="22b8f-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22b8f-123">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="22b8f-123">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="22b8f-124">Байты для захвата на один пакет.</span><span class="sxs-lookup"><span data-stu-id="22b8f-124">Bytes to capture per packet.</span></span>

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

### <span data-ttu-id="22b8f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22b8f-125">-DefaultProfile</span></span>
<span data-ttu-id="22b8f-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="22b8f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22b8f-127">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="22b8f-127">-Filter</span></span>
<span data-ttu-id="22b8f-128">Фильтры для сеанса записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="22b8f-128">Filters for packet capture session.</span></span>

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

### <span data-ttu-id="22b8f-129">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="22b8f-129">-LocalFilePath</span></span>
<span data-ttu-id="22b8f-130">Путь к локальному файлу.</span><span class="sxs-lookup"><span data-stu-id="22b8f-130">Local file path.</span></span>

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

### <span data-ttu-id="22b8f-131">-Location</span><span class="sxs-lookup"><span data-stu-id="22b8f-131">-Location</span></span>
<span data-ttu-id="22b8f-132">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="22b8f-132">Location of the network watcher.</span></span>

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

### <span data-ttu-id="22b8f-133">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="22b8f-133">-NetworkWatcher</span></span>
<span data-ttu-id="22b8f-134">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="22b8f-134">The network watcher resource.</span></span>

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

### <span data-ttu-id="22b8f-135">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="22b8f-135">-NetworkWatcherName</span></span>
<span data-ttu-id="22b8f-136">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="22b8f-136">The name of network watcher.</span></span>

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

### <span data-ttu-id="22b8f-137">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="22b8f-137">-PacketCaptureName</span></span>
<span data-ttu-id="22b8f-138">Имя захвата пакета.</span><span class="sxs-lookup"><span data-stu-id="22b8f-138">The packet capture name.</span></span>

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

### <span data-ttu-id="22b8f-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22b8f-139">-ResourceGroupName</span></span>
<span data-ttu-id="22b8f-140">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="22b8f-140">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="22b8f-141">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="22b8f-141">-StorageAccountId</span></span>
<span data-ttu-id="22b8f-142">Идентификатор учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="22b8f-142">Storage account Id.</span></span>

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

### <span data-ttu-id="22b8f-143">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="22b8f-143">-StoragePath</span></span>
<span data-ttu-id="22b8f-144">Путь к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="22b8f-144">Storage path.</span></span>

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

### <span data-ttu-id="22b8f-145">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="22b8f-145">-TargetVirtualMachineId</span></span>
<span data-ttu-id="22b8f-146">Целевой ИД виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="22b8f-146">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="22b8f-147">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="22b8f-147">-TimeLimitInSeconds</span></span>
<span data-ttu-id="22b8f-148">Ограничение по времени (в секундах).</span><span class="sxs-lookup"><span data-stu-id="22b8f-148">Time limit in seconds.</span></span>

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

### <span data-ttu-id="22b8f-149">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="22b8f-149">-TotalBytesPerSession</span></span>
<span data-ttu-id="22b8f-150">Общее количество байтов на сеанс.</span><span class="sxs-lookup"><span data-stu-id="22b8f-150">Total bytes per session.</span></span>

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

### <span data-ttu-id="22b8f-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22b8f-151">-Confirm</span></span>
<span data-ttu-id="22b8f-152">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="22b8f-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22b8f-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22b8f-153">-WhatIf</span></span>
<span data-ttu-id="22b8f-154">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="22b8f-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22b8f-155">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="22b8f-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22b8f-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22b8f-156">CommonParameters</span></span>
<span data-ttu-id="22b8f-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="22b8f-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22b8f-158">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22b8f-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22b8f-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="22b8f-159">INPUTS</span></span>

### <span data-ttu-id="22b8f-160">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="22b8f-160">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="22b8f-161">Параметры: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="22b8f-161">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="22b8f-162">System. String</span><span class="sxs-lookup"><span data-stu-id="22b8f-162">System.String</span></span>
<span data-ttu-id="22b8f-163">Параметры: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="22b8f-163">Parameters: NetworkWatcherName (ByValue)</span></span>

### <span data-ttu-id="22b8f-164">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="22b8f-164">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="22b8f-165">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="22b8f-165">OUTPUTS</span></span>

### <span data-ttu-id="22b8f-166">Microsoft. Azure. Commands. Network. Models. PSPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="22b8f-166">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureResult</span></span>

## <span data-ttu-id="22b8f-167">Пуск</span><span class="sxs-lookup"><span data-stu-id="22b8f-167">NOTES</span></span>
<span data-ttu-id="22b8f-168">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, пакет, захват, трафик</span><span class="sxs-lookup"><span data-stu-id="22b8f-168">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="22b8f-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="22b8f-169">RELATED LINKS</span></span>

[<span data-ttu-id="22b8f-170">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="22b8f-170">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="22b8f-171">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="22b8f-171">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="22b8f-172">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="22b8f-172">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="22b8f-173">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="22b8f-173">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="22b8f-174">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="22b8f-174">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="22b8f-175">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="22b8f-175">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="22b8f-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="22b8f-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="22b8f-177">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="22b8f-177">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="22b8f-178">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="22b8f-178">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="22b8f-179">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="22b8f-179">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="22b8f-180">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="22b8f-180">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="22b8f-181">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="22b8f-181">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="22b8f-182">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="22b8f-182">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="22b8f-183">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="22b8f-183">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="22b8f-184">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="22b8f-184">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="22b8f-185">Остановить-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="22b8f-185">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="22b8f-186">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="22b8f-186">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="22b8f-187">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="22b8f-187">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="22b8f-188">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="22b8f-188">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="22b8f-189">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="22b8f-189">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="22b8f-190">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="22b8f-190">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="22b8f-191">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="22b8f-191">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="22b8f-192">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="22b8f-192">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="22b8f-193">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="22b8f-193">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="22b8f-194">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="22b8f-194">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="22b8f-195">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="22b8f-195">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="22b8f-196">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="22b8f-196">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)


