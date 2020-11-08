---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: 710f35a96872ccf840810d8c2fe5189cccdbcaed
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94064841"
---
# <span data-ttu-id="22a77-101">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="22a77-101">Get-AzNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="22a77-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="22a77-102">SYNOPSIS</span></span>
<span data-ttu-id="22a77-103">Возвращает результат устранения неполадок, описанных в операции, выполняемой ранее или в ходе устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="22a77-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

## <span data-ttu-id="22a77-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="22a77-104">SYNTAX</span></span>

### <span data-ttu-id="22a77-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="22a77-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22a77-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="22a77-106">SetByName</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22a77-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="22a77-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -Location <String> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22a77-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="22a77-108">DESCRIPTION</span></span>
<span data-ttu-id="22a77-109">Командлет Get-AzNetworkWatcherTroubleshootingResult получает результаты устранения неполадок, вызванных предыдущим запуском или выполнением Start-AzNetworkWatcherResourceTroubleshooting операции.</span><span class="sxs-lookup"><span data-stu-id="22a77-109">The Get-AzNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="22a77-110">Если в данный момент выполняется операция устранения неполадок, выполнение этой операции может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="22a77-110">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="22a77-111">В настоящее время поддерживаются шлюзы и соединения виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="22a77-111">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="22a77-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="22a77-112">EXAMPLES</span></span>

### <span data-ttu-id="22a77-113">Пример 1: запуск устранения неполадок на шлюзе виртуальной сети и получение результата</span><span class="sxs-lookup"><span data-stu-id="22a77-113">Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="22a77-114">В приведенном выше примере начинается устранение неполадок шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="22a77-114">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="22a77-115">Выполнение операции может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="22a77-115">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="22a77-116">После того как устранение неполадок будет запущено, для ресурса будет выполнен звонок Get-AzNetworkWatcherTroubleshootingResult, чтобы получить результат этого звонка.</span><span class="sxs-lookup"><span data-stu-id="22a77-116">After troubleshooting has started, a Get-AzNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="22a77-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="22a77-117">PARAMETERS</span></span>

### <span data-ttu-id="22a77-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22a77-118">-DefaultProfile</span></span>
<span data-ttu-id="22a77-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="22a77-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22a77-120">-Location</span><span class="sxs-lookup"><span data-stu-id="22a77-120">-Location</span></span>
<span data-ttu-id="22a77-121">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="22a77-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="22a77-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="22a77-122">-NetworkWatcher</span></span>
<span data-ttu-id="22a77-123">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="22a77-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="22a77-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="22a77-124">-NetworkWatcherName</span></span>
<span data-ttu-id="22a77-125">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="22a77-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="22a77-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22a77-126">-ResourceGroupName</span></span>
<span data-ttu-id="22a77-127">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="22a77-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="22a77-128">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="22a77-128">-TargetResourceId</span></span>
<span data-ttu-id="22a77-129">Идентификатор целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="22a77-129">The target resource ID.</span></span>

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

### <span data-ttu-id="22a77-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22a77-130">CommonParameters</span></span>
<span data-ttu-id="22a77-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="22a77-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22a77-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22a77-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22a77-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="22a77-133">INPUTS</span></span>

### <span data-ttu-id="22a77-134">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="22a77-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="22a77-135">System. String</span><span class="sxs-lookup"><span data-stu-id="22a77-135">System.String</span></span>

## <span data-ttu-id="22a77-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="22a77-136">OUTPUTS</span></span>

### <span data-ttu-id="22a77-137">Microsoft. Azure. Commands. Network. Models. PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="22a77-137">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="22a77-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="22a77-138">NOTES</span></span>
<span data-ttu-id="22a77-139">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, устранение неполадок, VPN, подключение</span><span class="sxs-lookup"><span data-stu-id="22a77-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="22a77-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="22a77-140">RELATED LINKS</span></span>

[<span data-ttu-id="22a77-141">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="22a77-141">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="22a77-142">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="22a77-142">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="22a77-143">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="22a77-143">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="22a77-144">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="22a77-144">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="22a77-145">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="22a77-145">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="22a77-146">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="22a77-146">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="22a77-147">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="22a77-147">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="22a77-148">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="22a77-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="22a77-149">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="22a77-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="22a77-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="22a77-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="22a77-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="22a77-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="22a77-152">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="22a77-152">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="22a77-153">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="22a77-153">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="22a77-154">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="22a77-154">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="22a77-155">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="22a77-155">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="22a77-156">Остановить-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="22a77-156">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="22a77-157">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="22a77-157">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="22a77-158">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="22a77-158">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="22a77-159">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="22a77-159">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="22a77-160">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="22a77-160">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="22a77-161">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="22a77-161">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="22a77-162">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="22a77-162">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="22a77-163">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="22a77-163">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="22a77-164">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="22a77-164">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="22a77-165">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="22a77-165">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="22a77-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="22a77-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="22a77-167">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="22a77-167">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
