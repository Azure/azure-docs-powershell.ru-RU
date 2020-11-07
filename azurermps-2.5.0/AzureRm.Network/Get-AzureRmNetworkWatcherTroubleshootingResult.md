---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchertroubleshootingresult
schema: 2.0.0
ms.openlocfilehash: a2caff32969ac771140bd8c6a5a3b142f4d61485
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913830"
---
# <span data-ttu-id="becfe-101">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="becfe-101">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="becfe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="becfe-102">SYNOPSIS</span></span>
<span data-ttu-id="becfe-103">Возвращает результат устранения неполадок, описанных в операции, выполняемой ранее или в ходе устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="becfe-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="becfe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="becfe-104">SYNTAX</span></span>

### <span data-ttu-id="becfe-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="becfe-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="becfe-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="becfe-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="becfe-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="becfe-107">DESCRIPTION</span></span>
<span data-ttu-id="becfe-108">Командлет Get-AzureRmNetworkWatcherTroubleshootingResult получает результаты устранения неполадок, вызванных предыдущим запуском или выполнением Start-AzureRmNetworkWatcherResourceTroubleshooting операции.</span><span class="sxs-lookup"><span data-stu-id="becfe-108">The Get-AzureRmNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzureRmNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="becfe-109">Если в данный момент выполняется операция устранения неполадок, выполнение этой операции может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="becfe-109">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="becfe-110">В настоящее время поддерживаются шлюзы и соединения виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="becfe-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="becfe-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="becfe-111">EXAMPLES</span></span>

### <span data-ttu-id="becfe-112">---Пример 1: запуск устранения неполадок на шлюзе виртуальной сети и получение результата---</span><span class="sxs-lookup"><span data-stu-id="becfe-112">--- Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="becfe-113">В приведенном выше примере начинается устранение неполадок шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="becfe-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="becfe-114">Выполнение операции может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="becfe-114">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="becfe-115">После того как устранение неполадок будет запущено, для ресурса будет выполнен звонок Get-AzureRmNetworkWatcherTroubleshootingResult, чтобы получить результат этого звонка.</span><span class="sxs-lookup"><span data-stu-id="becfe-115">After troubleshooting has started, a Get-AzureRmNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="becfe-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="becfe-116">PARAMETERS</span></span>

### <span data-ttu-id="becfe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="becfe-117">-DefaultProfile</span></span>
<span data-ttu-id="becfe-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="becfe-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="becfe-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="becfe-119">-NetworkWatcher</span></span>
<span data-ttu-id="becfe-120">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="becfe-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="becfe-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="becfe-121">-NetworkWatcherName</span></span>
<span data-ttu-id="becfe-122">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="becfe-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="becfe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="becfe-123">-ResourceGroupName</span></span>
<span data-ttu-id="becfe-124">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="becfe-124">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="becfe-125">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="becfe-125">-TargetResourceId</span></span>
<span data-ttu-id="becfe-126">Идентификатор целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="becfe-126">The target resource ID.</span></span>

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

### <span data-ttu-id="becfe-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="becfe-127">CommonParameters</span></span>
<span data-ttu-id="becfe-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="becfe-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="becfe-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="becfe-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="becfe-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="becfe-130">INPUTS</span></span>

### <span data-ttu-id="becfe-131">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="becfe-131">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="becfe-132">System. String</span><span class="sxs-lookup"><span data-stu-id="becfe-132">System.String</span></span>

## <span data-ttu-id="becfe-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="becfe-133">OUTPUTS</span></span>

### <span data-ttu-id="becfe-134">Microsoft. Azure. Commands. Network. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="becfe-134">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="becfe-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="becfe-135">NOTES</span></span>
<span data-ttu-id="becfe-136">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, устранение неполадок, VPN, подключение</span><span class="sxs-lookup"><span data-stu-id="becfe-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="becfe-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="becfe-137">RELATED LINKS</span></span>

[<span data-ttu-id="becfe-138">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="becfe-138">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="becfe-139">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="becfe-139">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="becfe-140">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="becfe-140">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="becfe-141">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="becfe-141">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="becfe-142">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="becfe-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="becfe-143">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="becfe-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="becfe-144">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="becfe-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="becfe-145">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="becfe-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="becfe-146">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="becfe-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="becfe-147">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="becfe-147">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="becfe-148">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="becfe-148">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="becfe-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="becfe-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="becfe-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="becfe-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)
