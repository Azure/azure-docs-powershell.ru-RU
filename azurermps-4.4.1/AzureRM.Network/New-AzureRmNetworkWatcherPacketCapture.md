---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 87ae0ab7be4ace85d9f02a5637ea29dd27b0ae14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567567"
---
# <span data-ttu-id="0d7d0-101">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0d7d0-101">New-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="0d7d0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d7d0-102">SYNOPSIS</span></span>
<span data-ttu-id="0d7d0-103">Создание нового ресурса захвата пакетов и запуск сеанса захвата пакетов на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="0d7d0-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d7d0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d7d0-104">SYNTAX</span></span>

### <span data-ttu-id="0d7d0-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0d7d0-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d7d0-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="0d7d0-106">SetByName</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d7d0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d7d0-107">DESCRIPTION</span></span>
<span data-ttu-id="0d7d0-108">Командлет New-AzureRmNetworkWatcherPacketCapture создает новый ресурс захвата пакетов и начинает сеанс захвата пакетов на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="0d7d0-108">The New-AzureRmNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="0d7d0-109">Продолжительность сеансов захвата пакетов можно настроить с помощью ограничения по времени или ограничения на размер.</span><span class="sxs-lookup"><span data-stu-id="0d7d0-109">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="0d7d0-110">Также можно настроить объем данных, захваченных для каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="0d7d0-110">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="0d7d0-111">Фильтры можно применять к текущему сеансу захвата пакетов, что позволяет настраивать тип записанных пакетов.</span><span class="sxs-lookup"><span data-stu-id="0d7d0-111">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="0d7d0-112">Фильтры могут ограничивать пакеты на локальных и удаленных IP-адресах & диапазоны адресов, локальные и удаленные порты & диапазоны портов и протокол уровня сеанса для захвата.</span><span class="sxs-lookup"><span data-stu-id="0d7d0-112">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="0d7d0-113">Фильтры дописываются с помощью композиции, и можно применять несколько фильтров для обеспечения детальности захвата.</span><span class="sxs-lookup"><span data-stu-id="0d7d0-113">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="0d7d0-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d7d0-114">EXAMPLES</span></span>

### <span data-ttu-id="0d7d0-115">---Пример 1: создание захвата пакетов с несколькими фильтрами---</span><span class="sxs-lookup"><span data-stu-id="0d7d0-115">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="0d7d0-116">В этом примере мы создаем запись пакета с именем "PacketCaptureTest" с несколькими фильтрами и ограничением по времени.</span><span class="sxs-lookup"><span data-stu-id="0d7d0-116">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="0d7d0-117">После завершения сеанса он будет сохранен в указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0d7d0-117">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="0d7d0-118">Примечание: для создания захваченных пакетов на целевой виртуальной машине должно быть установлено расширение сетевого наблюдателя Azure.</span><span class="sxs-lookup"><span data-stu-id="0d7d0-118">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="0d7d0-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d7d0-119">PARAMETERS</span></span>

### <span data-ttu-id="0d7d0-120">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="0d7d0-120">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="0d7d0-121">Байты для захвата на один пакет.</span><span class="sxs-lookup"><span data-stu-id="0d7d0-121">Bytes to capture per packet.</span></span>

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

### <span data-ttu-id="0d7d0-122">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="0d7d0-122">-Filter</span></span>
<span data-ttu-id="0d7d0-123">Фильтры для сеанса записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="0d7d0-123">Filters for packet capture session.</span></span>

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

### <span data-ttu-id="0d7d0-124">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="0d7d0-124">-LocalFilePath</span></span>
<span data-ttu-id="0d7d0-125">Путь к локальному файлу.</span><span class="sxs-lookup"><span data-stu-id="0d7d0-125">Local file path.</span></span>

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

### <span data-ttu-id="0d7d0-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0d7d0-126">-NetworkWatcher</span></span>
<span data-ttu-id="0d7d0-127">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="0d7d0-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="0d7d0-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="0d7d0-128">-NetworkWatcherName</span></span>
<span data-ttu-id="0d7d0-129">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="0d7d0-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="0d7d0-130">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="0d7d0-130">-PacketCaptureName</span></span>
<span data-ttu-id="0d7d0-131">Имя захвата пакета.</span><span class="sxs-lookup"><span data-stu-id="0d7d0-131">The packet capture name.</span></span>

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

### <span data-ttu-id="0d7d0-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d7d0-132">-ResourceGroupName</span></span>
<span data-ttu-id="0d7d0-133">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="0d7d0-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="0d7d0-134">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="0d7d0-134">-StorageAccountId</span></span>
<span data-ttu-id="0d7d0-135">Идентификатор учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0d7d0-135">Storage account Id.</span></span>

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

### <span data-ttu-id="0d7d0-136">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="0d7d0-136">-StoragePath</span></span>
<span data-ttu-id="0d7d0-137">Путь к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="0d7d0-137">Storage path.</span></span>

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

### <span data-ttu-id="0d7d0-138">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="0d7d0-138">-TargetVirtualMachineId</span></span>
<span data-ttu-id="0d7d0-139">Целевой ИД виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0d7d0-139">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="0d7d0-140">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="0d7d0-140">-TimeLimitInSeconds</span></span>
<span data-ttu-id="0d7d0-141">Ограничение по времени (в секундах).</span><span class="sxs-lookup"><span data-stu-id="0d7d0-141">Time limit in seconds.</span></span>

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

### <span data-ttu-id="0d7d0-142">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="0d7d0-142">-TotalBytesPerSession</span></span>
<span data-ttu-id="0d7d0-143">Общее количество байтов на сеанс.</span><span class="sxs-lookup"><span data-stu-id="0d7d0-143">Total bytes per session.</span></span>

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

### <span data-ttu-id="0d7d0-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d7d0-144">-Confirm</span></span>
<span data-ttu-id="0d7d0-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0d7d0-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d7d0-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d7d0-146">-WhatIf</span></span>
<span data-ttu-id="0d7d0-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0d7d0-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d7d0-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0d7d0-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d7d0-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d7d0-149">-DefaultProfile</span></span>
<span data-ttu-id="0d7d0-150">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0d7d0-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d7d0-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d7d0-151">CommonParameters</span></span>
<span data-ttu-id="0d7d0-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d7d0-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d7d0-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d7d0-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d7d0-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d7d0-154">INPUTS</span></span>

### <span data-ttu-id="0d7d0-155">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0d7d0-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="0d7d0-156">System. String System. Nullable \` 1 \[ \[ System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="0d7d0-156">System.String System.Nullable\`1\[\[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

## <span data-ttu-id="0d7d0-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d7d0-157">OUTPUTS</span></span>

### <span data-ttu-id="0d7d0-158">Microsoft. Azure. Commands. Network. Models. PSPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0d7d0-158">Microsoft.Azure.Commands.Network.Models.PSPacketCapture</span></span>

## <span data-ttu-id="0d7d0-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d7d0-159">NOTES</span></span>
<span data-ttu-id="0d7d0-160">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, пакет, захват, трафик</span><span class="sxs-lookup"><span data-stu-id="0d7d0-160">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="0d7d0-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d7d0-161">RELATED LINKS</span></span>

[<span data-ttu-id="0d7d0-162">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0d7d0-162">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="0d7d0-163">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0d7d0-163">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0d7d0-164">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0d7d0-164">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0d7d0-165">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0d7d0-165">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0d7d0-166">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0d7d0-166">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="0d7d0-167">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0d7d0-167">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="0d7d0-168">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0d7d0-168">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="0d7d0-169">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0d7d0-169">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="0d7d0-170">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0d7d0-170">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="0d7d0-171">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0d7d0-171">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0d7d0-172">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0d7d0-172">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="0d7d0-173">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0d7d0-173">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)


