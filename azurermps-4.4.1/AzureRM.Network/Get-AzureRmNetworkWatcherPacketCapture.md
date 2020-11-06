---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 4cf1cb9149c0f821ad0e6164cd7c817b12ccc147
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562460"
---
# <span data-ttu-id="294b8-101">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="294b8-101">Get-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="294b8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="294b8-102">SYNOPSIS</span></span>
<span data-ttu-id="294b8-103">Возвращает сведения о ресурсе и его свойствах и состоянии.</span><span class="sxs-lookup"><span data-stu-id="294b8-103">Gets information and properties and status of a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="294b8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="294b8-104">SYNTAX</span></span>

### <span data-ttu-id="294b8-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="294b8-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="294b8-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="294b8-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="294b8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="294b8-107">DESCRIPTION</span></span>
<span data-ttu-id="294b8-108">Get-AzureRmNetworkWatcherPacketCapture получает свойства и состояние ресурса захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="294b8-108">The Get-AzureRmNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="294b8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="294b8-109">EXAMPLES</span></span>

### <span data-ttu-id="294b8-110">---Пример 1: создание захвата пакетов с несколькими фильтрами и получение их состояния---</span><span class="sxs-lookup"><span data-stu-id="294b8-110">--- Example 1: Create a Packet Capture with multiple filters and retrieve its status ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="294b8-111">В этом примере мы создаем запись пакета с именем "PacketCaptureTest" с несколькими фильтрами и ограничением по времени.</span><span class="sxs-lookup"><span data-stu-id="294b8-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="294b8-112">После завершения сеанса он будет сохранен в указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="294b8-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="294b8-113">Затем вызовите Get-AzureRmNetworkWatcherPacketCapture, чтобы получить состояние сеанса захвата.</span><span class="sxs-lookup"><span data-stu-id="294b8-113">We then call Get-AzureRmNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> 

<span data-ttu-id="294b8-114">Примечание: для создания захваченных пакетов на целевой виртуальной машине должно быть установлено расширение сетевого наблюдателя Azure.</span><span class="sxs-lookup"><span data-stu-id="294b8-114">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="294b8-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="294b8-115">PARAMETERS</span></span>

### <span data-ttu-id="294b8-116">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="294b8-116">-NetworkWatcher</span></span>
<span data-ttu-id="294b8-117">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="294b8-117">The network watcher resource.</span></span>

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

### <span data-ttu-id="294b8-118">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="294b8-118">-NetworkWatcherName</span></span>
<span data-ttu-id="294b8-119">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="294b8-119">The name of network watcher.</span></span>

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

### <span data-ttu-id="294b8-120">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="294b8-120">-PacketCaptureName</span></span>
<span data-ttu-id="294b8-121">Имя захвата пакета.</span><span class="sxs-lookup"><span data-stu-id="294b8-121">The packet capture name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="294b8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="294b8-122">-ResourceGroupName</span></span>
<span data-ttu-id="294b8-123">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="294b8-123">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="294b8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="294b8-124">-DefaultProfile</span></span>
<span data-ttu-id="294b8-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="294b8-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="294b8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="294b8-126">CommonParameters</span></span>
<span data-ttu-id="294b8-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="294b8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="294b8-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="294b8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="294b8-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="294b8-129">INPUTS</span></span>

### <span data-ttu-id="294b8-130">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="294b8-130">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="294b8-131">System. String</span><span class="sxs-lookup"><span data-stu-id="294b8-131">System.String</span></span>

## <span data-ttu-id="294b8-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="294b8-132">OUTPUTS</span></span>

### <span data-ttu-id="294b8-133">Microsoft. Azure. Commands. Network. Models. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="294b8-133">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="294b8-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="294b8-134">NOTES</span></span>
<span data-ttu-id="294b8-135">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, пакет, захват, трафик</span><span class="sxs-lookup"><span data-stu-id="294b8-135">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="294b8-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="294b8-136">RELATED LINKS</span></span>

[<span data-ttu-id="294b8-137">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="294b8-137">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="294b8-138">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="294b8-138">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="294b8-139">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="294b8-139">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="294b8-140">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="294b8-140">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="294b8-141">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="294b8-141">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="294b8-142">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="294b8-142">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="294b8-143">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="294b8-143">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="294b8-144">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="294b8-144">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="294b8-145">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="294b8-145">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="294b8-146">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="294b8-146">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="294b8-147">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="294b8-147">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="294b8-148">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="294b8-148">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

