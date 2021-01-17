---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: f6762b074c9b185d12666fb8ea92fcaf15a46b05
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329450"
---
# <span data-ttu-id="185d7-101">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="185d7-101">New-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="185d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="185d7-102">SYNOPSIS</span></span>
<span data-ttu-id="185d7-103">Создание нового ресурса для захвата пакетов и начало сеанса захвата пакетов на VM-</span><span class="sxs-lookup"><span data-stu-id="185d7-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

## <span data-ttu-id="185d7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="185d7-104">SYNTAX</span></span>

### <span data-ttu-id="185d7-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="185d7-105">SetByResource (Default)</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="185d7-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="185d7-106">SetByName</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="185d7-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="185d7-107">SetByLocation</span></span>
```
New-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="185d7-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="185d7-108">DESCRIPTION</span></span>
<span data-ttu-id="185d7-109">С New-AzNetworkWatcherPacketCapture создается новый ресурс для захвата пакетов и начинается сеанс захвата пакетов на VM-</span><span class="sxs-lookup"><span data-stu-id="185d7-109">The New-AzNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="185d7-110">Продолжительность сеансов захвата пакетов можно настроить с помощью ограничения по времени или по размеру.</span><span class="sxs-lookup"><span data-stu-id="185d7-110">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="185d7-111">Также можно настроить объем данных для каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="185d7-111">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="185d7-112">Фильтры можно применять к заданным сеансам захвата пакетов, что позволяет настраивать тип захватимого пакета.</span><span class="sxs-lookup"><span data-stu-id="185d7-112">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="185d7-113">Фильтры могут ограничивать пакеты для локальных и удаленных IP-адресов & адресов, локальных и удаленных портов & диапазонов портов и протоколов сеанса.</span><span class="sxs-lookup"><span data-stu-id="185d7-113">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="185d7-114">Фильтры можно составить, а затем применить несколько фильтров, чтобы получить детализацию снимка.</span><span class="sxs-lookup"><span data-stu-id="185d7-114">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="185d7-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="185d7-115">EXAMPLES</span></span>

### <span data-ttu-id="185d7-116">Пример 1. Создание пакета с несколькими фильтрами</span><span class="sxs-lookup"><span data-stu-id="185d7-116">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="185d7-117">В этом примере мы создали пакет PacketCaptureTest с несколькими фильтрами и ограничением по времени.</span><span class="sxs-lookup"><span data-stu-id="185d7-117">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="185d7-118">После завершения сеанса он будет сохранен в указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="185d7-118">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="185d7-119">Примечание. Для создания снимков пакетов на целевой виртуальной машине необходимо установить расширение Azure Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="185d7-119">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="185d7-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="185d7-120">PARAMETERS</span></span>

### <span data-ttu-id="185d7-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="185d7-121">-AsJob</span></span>
<span data-ttu-id="185d7-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="185d7-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="185d7-123">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="185d7-123">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="185d7-124">Bytes to capture per packet.</span><span class="sxs-lookup"><span data-stu-id="185d7-124">Bytes to capture per packet.</span></span>

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

### <span data-ttu-id="185d7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="185d7-125">-DefaultProfile</span></span>
<span data-ttu-id="185d7-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="185d7-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="185d7-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="185d7-127">-Filter</span></span>
<span data-ttu-id="185d7-128">Фильтры для сеанса захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="185d7-128">Filters for packet capture session.</span></span>

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

### <span data-ttu-id="185d7-129">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="185d7-129">-LocalFilePath</span></span>
<span data-ttu-id="185d7-130">Путь к локальному файлу.</span><span class="sxs-lookup"><span data-stu-id="185d7-130">Local file path.</span></span>

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

### <span data-ttu-id="185d7-131">-Location</span><span class="sxs-lookup"><span data-stu-id="185d7-131">-Location</span></span>
<span data-ttu-id="185d7-132">Расположение сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="185d7-132">Location of the network watcher.</span></span>

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

### <span data-ttu-id="185d7-133">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="185d7-133">-NetworkWatcher</span></span>
<span data-ttu-id="185d7-134">Сетевой ресурс для просмотра.</span><span class="sxs-lookup"><span data-stu-id="185d7-134">The network watcher resource.</span></span>

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

### <span data-ttu-id="185d7-135">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="185d7-135">-NetworkWatcherName</span></span>
<span data-ttu-id="185d7-136">Имя сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="185d7-136">The name of network watcher.</span></span>

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

### <span data-ttu-id="185d7-137">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="185d7-137">-PacketCaptureName</span></span>
<span data-ttu-id="185d7-138">Имя захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="185d7-138">The packet capture name.</span></span>

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

### <span data-ttu-id="185d7-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="185d7-139">-ResourceGroupName</span></span>
<span data-ttu-id="185d7-140">Имя группы ресурсов сетевого watcher.</span><span class="sxs-lookup"><span data-stu-id="185d7-140">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="185d7-141">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="185d7-141">-StorageAccountId</span></span>
<span data-ttu-id="185d7-142">ИД учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="185d7-142">Storage account Id.</span></span>

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

### <span data-ttu-id="185d7-143">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="185d7-143">-StoragePath</span></span>
<span data-ttu-id="185d7-144">Путь к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="185d7-144">Storage path.</span></span>

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

### <span data-ttu-id="185d7-145">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="185d7-145">-TargetVirtualMachineId</span></span>
<span data-ttu-id="185d7-146">ИД целевой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="185d7-146">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="185d7-147">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="185d7-147">-TimeLimitInSeconds</span></span>
<span data-ttu-id="185d7-148">Ограничение по времени в секундах.</span><span class="sxs-lookup"><span data-stu-id="185d7-148">Time limit in seconds.</span></span>

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

### <span data-ttu-id="185d7-149">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="185d7-149">-TotalBytesPerSession</span></span>
<span data-ttu-id="185d7-150">Общее количествобайтов в сеансе.</span><span class="sxs-lookup"><span data-stu-id="185d7-150">Total bytes per session.</span></span>

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

### <span data-ttu-id="185d7-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="185d7-151">-Confirm</span></span>
<span data-ttu-id="185d7-152">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="185d7-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="185d7-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="185d7-153">-WhatIf</span></span>
<span data-ttu-id="185d7-154">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="185d7-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="185d7-155">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="185d7-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="185d7-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="185d7-156">CommonParameters</span></span>
<span data-ttu-id="185d7-157">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="185d7-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="185d7-158">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="185d7-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="185d7-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="185d7-159">INPUTS</span></span>

### <span data-ttu-id="185d7-160">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="185d7-160">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="185d7-161">System.String</span><span class="sxs-lookup"><span data-stu-id="185d7-161">System.String</span></span>

### <span data-ttu-id="185d7-162">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="185d7-162">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="185d7-163">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="185d7-163">OUTPUTS</span></span>

### <span data-ttu-id="185d7-164">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="185d7-164">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureResult</span></span>

## <span data-ttu-id="185d7-165">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="185d7-165">NOTES</span></span>
<span data-ttu-id="185d7-166">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, network, networking, network watcher, packet, capture, traffic</span><span class="sxs-lookup"><span data-stu-id="185d7-166">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="185d7-167">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="185d7-167">RELATED LINKS</span></span>

[<span data-ttu-id="185d7-168">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="185d7-168">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="185d7-169">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="185d7-169">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="185d7-170">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="185d7-170">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="185d7-171">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="185d7-171">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="185d7-172">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="185d7-172">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="185d7-173">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="185d7-173">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="185d7-174">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="185d7-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="185d7-175">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="185d7-175">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="185d7-176">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="185d7-176">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="185d7-177">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="185d7-177">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="185d7-178">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="185d7-178">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="185d7-179">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="185d7-179">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="185d7-180">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="185d7-180">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="185d7-181">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="185d7-181">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="185d7-182">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="185d7-182">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="185d7-183">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="185d7-183">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="185d7-184">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="185d7-184">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="185d7-185">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="185d7-185">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="185d7-186">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="185d7-186">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="185d7-187">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="185d7-187">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="185d7-188">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="185d7-188">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="185d7-189">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="185d7-189">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="185d7-190">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="185d7-190">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="185d7-191">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="185d7-191">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="185d7-192">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="185d7-192">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="185d7-193">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="185d7-193">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="185d7-194">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="185d7-194">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)


