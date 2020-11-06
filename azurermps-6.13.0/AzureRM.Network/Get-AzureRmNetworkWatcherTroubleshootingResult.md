---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: 527d0fd33629ed7e1fcecdd23ba7cf8c93822f16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568476"
---
# <span data-ttu-id="6d35d-101">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="6d35d-101">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="6d35d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6d35d-102">SYNOPSIS</span></span>
<span data-ttu-id="6d35d-103">Возвращает результат устранения неполадок, описанных в операции, выполняемой ранее или в ходе устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="6d35d-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d35d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6d35d-104">SYNTAX</span></span>

### <span data-ttu-id="6d35d-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6d35d-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d35d-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="6d35d-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d35d-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="6d35d-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -Location <String> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d35d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d35d-108">DESCRIPTION</span></span>
<span data-ttu-id="6d35d-109">Командлет Get-AzureRmNetworkWatcherTroubleshootingResult получает результаты устранения неполадок, вызванных предыдущим запуском или выполнением Start-AzureRmNetworkWatcherResourceTroubleshooting операции.</span><span class="sxs-lookup"><span data-stu-id="6d35d-109">The Get-AzureRmNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzureRmNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="6d35d-110">Если в данный момент выполняется операция устранения неполадок, выполнение этой операции может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="6d35d-110">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="6d35d-111">В настоящее время поддерживаются шлюзы и соединения виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="6d35d-111">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="6d35d-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6d35d-112">EXAMPLES</span></span>

### <span data-ttu-id="6d35d-113">Пример 1: запуск устранения неполадок на шлюзе виртуальной сети и получение результата</span><span class="sxs-lookup"><span data-stu-id="6d35d-113">Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="6d35d-114">В приведенном выше примере начинается устранение неполадок шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="6d35d-114">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="6d35d-115">Выполнение операции может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="6d35d-115">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="6d35d-116">После того как устранение неполадок будет запущено, для ресурса будет выполнен звонок Get-AzureRmNetworkWatcherTroubleshootingResult, чтобы получить результат этого звонка.</span><span class="sxs-lookup"><span data-stu-id="6d35d-116">After troubleshooting has started, a Get-AzureRmNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="6d35d-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6d35d-117">PARAMETERS</span></span>

### <span data-ttu-id="6d35d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d35d-118">-DefaultProfile</span></span>
<span data-ttu-id="6d35d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6d35d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d35d-120">-Location</span><span class="sxs-lookup"><span data-stu-id="6d35d-120">-Location</span></span>
<span data-ttu-id="6d35d-121">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="6d35d-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="6d35d-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6d35d-122">-NetworkWatcher</span></span>
<span data-ttu-id="6d35d-123">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="6d35d-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="6d35d-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="6d35d-124">-NetworkWatcherName</span></span>
<span data-ttu-id="6d35d-125">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="6d35d-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="6d35d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d35d-126">-ResourceGroupName</span></span>
<span data-ttu-id="6d35d-127">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="6d35d-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="6d35d-128">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="6d35d-128">-TargetResourceId</span></span>
<span data-ttu-id="6d35d-129">Идентификатор целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="6d35d-129">The target resource ID.</span></span>

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

### <span data-ttu-id="6d35d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d35d-130">CommonParameters</span></span>
<span data-ttu-id="6d35d-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6d35d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d35d-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d35d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d35d-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6d35d-133">INPUTS</span></span>

### <span data-ttu-id="6d35d-134">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6d35d-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="6d35d-135">Параметры: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6d35d-135">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="6d35d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6d35d-136">System.String</span></span>
<span data-ttu-id="6d35d-137">Параметры: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6d35d-137">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="6d35d-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d35d-138">OUTPUTS</span></span>

### <span data-ttu-id="6d35d-139">Microsoft. Azure. Commands. Network. Models. PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="6d35d-139">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="6d35d-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="6d35d-140">NOTES</span></span>
<span data-ttu-id="6d35d-141">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, устранение неполадок, VPN, подключение</span><span class="sxs-lookup"><span data-stu-id="6d35d-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="6d35d-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d35d-142">RELATED LINKS</span></span>

[<span data-ttu-id="6d35d-143">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6d35d-143">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="6d35d-144">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6d35d-144">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="6d35d-145">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6d35d-145">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="6d35d-146">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="6d35d-146">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="6d35d-147">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="6d35d-147">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="6d35d-148">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="6d35d-148">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="6d35d-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="6d35d-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="6d35d-150">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6d35d-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6d35d-151">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="6d35d-151">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="6d35d-152">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6d35d-152">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6d35d-153">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6d35d-153">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6d35d-154">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6d35d-154">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6d35d-155">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d35d-155">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="6d35d-156">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="6d35d-156">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="6d35d-157">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="6d35d-157">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="6d35d-158">Остановить-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6d35d-158">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6d35d-159">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6d35d-159">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6d35d-160">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6d35d-160">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6d35d-161">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="6d35d-161">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="6d35d-162">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6d35d-162">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6d35d-163">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6d35d-163">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6d35d-164">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="6d35d-164">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="6d35d-165">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="6d35d-165">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="6d35d-166">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="6d35d-166">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="6d35d-167">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="6d35d-167">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="6d35d-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="6d35d-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="6d35d-169">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6d35d-169">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
