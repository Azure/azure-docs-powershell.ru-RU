---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 8e2e7a25b2c6e2c9eaa5e53234d7c1c9c3d0fa9f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909910"
---
# <span data-ttu-id="bdc12-101">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bdc12-101">Get-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="bdc12-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bdc12-102">SYNOPSIS</span></span>
<span data-ttu-id="bdc12-103">Возвращает сведения о ресурсе и его свойствах и состоянии.</span><span class="sxs-lookup"><span data-stu-id="bdc12-103">Gets information and properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="bdc12-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bdc12-104">SYNTAX</span></span>

### <span data-ttu-id="bdc12-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bdc12-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bdc12-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="bdc12-106">SetByName</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdc12-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bdc12-107">DESCRIPTION</span></span>
<span data-ttu-id="bdc12-108">Get-AzNetworkWatcherPacketCapture получает свойства и состояние ресурса захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="bdc12-108">The Get-AzNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="bdc12-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bdc12-109">EXAMPLES</span></span>

### <span data-ttu-id="bdc12-110">---Пример 1: создание захвата пакетов с несколькими фильтрами и получение их состояния---</span><span class="sxs-lookup"><span data-stu-id="bdc12-110">--- Example 1: Create a Packet Capture with multiple filters and retrieve its status ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="bdc12-111">В этом примере мы создаем запись пакета с именем "PacketCaptureTest" с несколькими фильтрами и ограничением по времени.</span><span class="sxs-lookup"><span data-stu-id="bdc12-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="bdc12-112">После завершения сеанса он будет сохранен в указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="bdc12-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="bdc12-113">Затем вызовите Get-AzNetworkWatcherPacketCapture, чтобы получить состояние сеанса захвата.</span><span class="sxs-lookup"><span data-stu-id="bdc12-113">We then call Get-AzNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> 

<span data-ttu-id="bdc12-114">Примечание: для создания захваченных пакетов на целевой виртуальной машине должно быть установлено расширение сетевого наблюдателя Azure.</span><span class="sxs-lookup"><span data-stu-id="bdc12-114">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="bdc12-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bdc12-115">PARAMETERS</span></span>

### <span data-ttu-id="bdc12-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bdc12-116">-AsJob</span></span>
<span data-ttu-id="bdc12-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="bdc12-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bdc12-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdc12-118">-DefaultProfile</span></span>
<span data-ttu-id="bdc12-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bdc12-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdc12-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bdc12-120">-NetworkWatcher</span></span>
<span data-ttu-id="bdc12-121">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="bdc12-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="bdc12-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="bdc12-122">-NetworkWatcherName</span></span>
<span data-ttu-id="bdc12-123">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="bdc12-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="bdc12-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="bdc12-124">-PacketCaptureName</span></span>
<span data-ttu-id="bdc12-125">Имя захвата пакета.</span><span class="sxs-lookup"><span data-stu-id="bdc12-125">The packet capture name.</span></span>

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

### <span data-ttu-id="bdc12-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdc12-126">-ResourceGroupName</span></span>
<span data-ttu-id="bdc12-127">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="bdc12-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="bdc12-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdc12-128">CommonParameters</span></span>
<span data-ttu-id="bdc12-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bdc12-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdc12-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdc12-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdc12-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bdc12-131">INPUTS</span></span>

### <span data-ttu-id="bdc12-132">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bdc12-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="bdc12-133">System. String</span><span class="sxs-lookup"><span data-stu-id="bdc12-133">System.String</span></span>

## <span data-ttu-id="bdc12-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bdc12-134">OUTPUTS</span></span>

### <span data-ttu-id="bdc12-135">Microsoft. Azure. Commands. Network. Models. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="bdc12-135">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="bdc12-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="bdc12-136">NOTES</span></span>
<span data-ttu-id="bdc12-137">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, пакет, захват, трафик</span><span class="sxs-lookup"><span data-stu-id="bdc12-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="bdc12-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bdc12-138">RELATED LINKS</span></span>

[<span data-ttu-id="bdc12-139">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bdc12-139">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bdc12-140">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="bdc12-140">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="bdc12-141">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bdc12-141">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bdc12-142">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bdc12-142">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bdc12-143">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bdc12-143">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="bdc12-144">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bdc12-144">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="bdc12-145">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bdc12-145">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="bdc12-146">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="bdc12-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="bdc12-147">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="bdc12-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="bdc12-148">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="bdc12-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="bdc12-149">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="bdc12-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="bdc12-150">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="bdc12-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

