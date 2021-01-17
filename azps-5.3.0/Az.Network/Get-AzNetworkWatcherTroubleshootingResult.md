---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: db3e3e529fd5c056acf793cd14280ef688c58a81
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422108"
---
# <span data-ttu-id="c8de1-101">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c8de1-101">Get-AzNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="c8de1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8de1-102">SYNOPSIS</span></span>
<span data-ttu-id="c8de1-103">Возвращает результаты устранения ранее запущенной или запущенной операции устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="c8de1-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

## <span data-ttu-id="c8de1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c8de1-104">SYNTAX</span></span>

### <span data-ttu-id="c8de1-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c8de1-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8de1-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="c8de1-106">SetByName</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8de1-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c8de1-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -Location <String> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8de1-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8de1-108">DESCRIPTION</span></span>
<span data-ttu-id="c8de1-109">Этот Get-AzNetworkWatcherTroubleshootingResult получает результаты устранения неполадок, которые были заранее запущены или Start-AzNetworkWatcherResourceTroubleshooting работе.</span><span class="sxs-lookup"><span data-stu-id="c8de1-109">The Get-AzNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="c8de1-110">Если операция устранения неполадок еще не завершена, ее завершение может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="c8de1-110">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="c8de1-111">В настоящее время поддерживаются виртуальные сетевые шлюзы и подключения.</span><span class="sxs-lookup"><span data-stu-id="c8de1-111">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="c8de1-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c8de1-112">EXAMPLES</span></span>

### <span data-ttu-id="c8de1-113">Пример 1. Начало устранения неполадок виртуального сетевого шлюза и извлечение результата</span><span class="sxs-lookup"><span data-stu-id="c8de1-113">Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="c8de1-114">В примере выше начнется устранение неполадок виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="c8de1-114">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="c8de1-115">Операция может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="c8de1-115">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="c8de1-116">После начала работы по устранению неполадок Get-AzNetworkWatcherTroubleshootingResult ресурсу будет выполнен вызов для получения результата этого звонка.</span><span class="sxs-lookup"><span data-stu-id="c8de1-116">After troubleshooting has started, a Get-AzNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="c8de1-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8de1-117">PARAMETERS</span></span>

### <span data-ttu-id="c8de1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8de1-118">-DefaultProfile</span></span>
<span data-ttu-id="c8de1-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c8de1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8de1-120">-Location</span><span class="sxs-lookup"><span data-stu-id="c8de1-120">-Location</span></span>
<span data-ttu-id="c8de1-121">Расположение сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="c8de1-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="c8de1-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c8de1-122">-NetworkWatcher</span></span>
<span data-ttu-id="c8de1-123">Сетевой ресурс для просмотра.</span><span class="sxs-lookup"><span data-stu-id="c8de1-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="c8de1-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c8de1-124">-NetworkWatcherName</span></span>
<span data-ttu-id="c8de1-125">Имя сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="c8de1-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="c8de1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8de1-126">-ResourceGroupName</span></span>
<span data-ttu-id="c8de1-127">Имя группы ресурсов сетевого watcher.</span><span class="sxs-lookup"><span data-stu-id="c8de1-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c8de1-128">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="c8de1-128">-TargetResourceId</span></span>
<span data-ttu-id="c8de1-129">ИД целевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="c8de1-129">The target resource ID.</span></span>

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

### <span data-ttu-id="c8de1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8de1-130">CommonParameters</span></span>
<span data-ttu-id="c8de1-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8de1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8de1-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8de1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8de1-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c8de1-133">INPUTS</span></span>

### <span data-ttu-id="c8de1-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c8de1-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="c8de1-135">System.String</span><span class="sxs-lookup"><span data-stu-id="c8de1-135">System.String</span></span>

## <span data-ttu-id="c8de1-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c8de1-136">OUTPUTS</span></span>

### <span data-ttu-id="c8de1-137">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c8de1-137">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="c8de1-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c8de1-138">NOTES</span></span>
<span data-ttu-id="c8de1-139">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, network, networking, network watcher, troubleshoot, VPN, connection</span><span class="sxs-lookup"><span data-stu-id="c8de1-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="c8de1-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8de1-140">RELATED LINKS</span></span>

[<span data-ttu-id="c8de1-141">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c8de1-141">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="c8de1-142">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c8de1-142">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="c8de1-143">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c8de1-143">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="c8de1-144">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c8de1-144">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="c8de1-145">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c8de1-145">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c8de1-146">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c8de1-146">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="c8de1-147">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c8de1-147">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c8de1-148">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c8de1-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c8de1-149">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c8de1-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="c8de1-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c8de1-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c8de1-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c8de1-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c8de1-152">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c8de1-152">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c8de1-153">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c8de1-153">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c8de1-154">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c8de1-154">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="c8de1-155">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c8de1-155">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="c8de1-156">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c8de1-156">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c8de1-157">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c8de1-157">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c8de1-158">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c8de1-158">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c8de1-159">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c8de1-159">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c8de1-160">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c8de1-160">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c8de1-161">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c8de1-161">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c8de1-162">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c8de1-162">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c8de1-163">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c8de1-163">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c8de1-164">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c8de1-164">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c8de1-165">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c8de1-165">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="c8de1-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c8de1-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="c8de1-167">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c8de1-167">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
