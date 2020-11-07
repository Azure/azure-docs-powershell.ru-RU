---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherpacketcapture
schema: 2.0.0
ms.openlocfilehash: aeadada7c6e2e2d7cb94a484e7ca3223e03b4426
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913456"
---
# <span data-ttu-id="e0ecd-101">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e0ecd-101">Get-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="e0ecd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e0ecd-102">SYNOPSIS</span></span>
<span data-ttu-id="e0ecd-103">Возвращает сведения о ресурсе и его свойствах и состоянии.</span><span class="sxs-lookup"><span data-stu-id="e0ecd-103">Gets information and properties and status of a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0ecd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e0ecd-104">SYNTAX</span></span>

### <span data-ttu-id="e0ecd-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e0ecd-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0ecd-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="e0ecd-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0ecd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0ecd-107">DESCRIPTION</span></span>
<span data-ttu-id="e0ecd-108">Get-AzureRmNetworkWatcherPacketCapture получает свойства и состояние ресурса захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="e0ecd-108">The Get-AzureRmNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="e0ecd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e0ecd-109">EXAMPLES</span></span>

### <span data-ttu-id="e0ecd-110">---Пример 1: создание захвата пакетов с несколькими фильтрами и получение их состояния---</span><span class="sxs-lookup"><span data-stu-id="e0ecd-110">--- Example 1: Create a Packet Capture with multiple filters and retrieve its status ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="e0ecd-111">В этом примере мы создаем запись пакета с именем "PacketCaptureTest" с несколькими фильтрами и ограничением по времени.</span><span class="sxs-lookup"><span data-stu-id="e0ecd-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="e0ecd-112">После завершения сеанса он будет сохранен в указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e0ecd-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="e0ecd-113">Затем вызовите Get-AzureRmNetworkWatcherPacketCapture, чтобы получить состояние сеанса захвата.</span><span class="sxs-lookup"><span data-stu-id="e0ecd-113">We then call Get-AzureRmNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> 

<span data-ttu-id="e0ecd-114">Примечание: для создания захваченных пакетов на целевой виртуальной машине должно быть установлено расширение сетевого наблюдателя Azure.</span><span class="sxs-lookup"><span data-stu-id="e0ecd-114">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="e0ecd-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e0ecd-115">PARAMETERS</span></span>

### <span data-ttu-id="e0ecd-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0ecd-116">-AsJob</span></span>
<span data-ttu-id="e0ecd-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e0ecd-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e0ecd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0ecd-118">-DefaultProfile</span></span>
<span data-ttu-id="e0ecd-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e0ecd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0ecd-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e0ecd-120">-NetworkWatcher</span></span>
<span data-ttu-id="e0ecd-121">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="e0ecd-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="e0ecd-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e0ecd-122">-NetworkWatcherName</span></span>
<span data-ttu-id="e0ecd-123">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="e0ecd-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="e0ecd-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="e0ecd-124">-PacketCaptureName</span></span>
<span data-ttu-id="e0ecd-125">Имя захвата пакета.</span><span class="sxs-lookup"><span data-stu-id="e0ecd-125">The packet capture name.</span></span>

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

### <span data-ttu-id="e0ecd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0ecd-126">-ResourceGroupName</span></span>
<span data-ttu-id="e0ecd-127">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="e0ecd-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="e0ecd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0ecd-128">CommonParameters</span></span>
<span data-ttu-id="e0ecd-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e0ecd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0ecd-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0ecd-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0ecd-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e0ecd-131">INPUTS</span></span>

### <span data-ttu-id="e0ecd-132">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e0ecd-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="e0ecd-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e0ecd-133">System.String</span></span>

## <span data-ttu-id="e0ecd-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0ecd-134">OUTPUTS</span></span>

### <span data-ttu-id="e0ecd-135">Microsoft. Azure. Commands. Network. Models. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="e0ecd-135">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="e0ecd-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="e0ecd-136">NOTES</span></span>
<span data-ttu-id="e0ecd-137">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, пакет, захват, трафик</span><span class="sxs-lookup"><span data-stu-id="e0ecd-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="e0ecd-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0ecd-138">RELATED LINKS</span></span>

[<span data-ttu-id="e0ecd-139">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e0ecd-139">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e0ecd-140">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e0ecd-140">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="e0ecd-141">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e0ecd-141">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e0ecd-142">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e0ecd-142">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e0ecd-143">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e0ecd-143">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="e0ecd-144">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e0ecd-144">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="e0ecd-145">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e0ecd-145">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="e0ecd-146">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e0ecd-146">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="e0ecd-147">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e0ecd-147">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="e0ecd-148">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e0ecd-148">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e0ecd-149">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e0ecd-149">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="e0ecd-150">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e0ecd-150">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

