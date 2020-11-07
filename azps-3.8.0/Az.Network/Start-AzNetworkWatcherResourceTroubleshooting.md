---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: e8e8b9dfd217f9407af8db18a5f468d7d971c97d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911930"
---
# <span data-ttu-id="e4eb4-101">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e4eb4-101">Start-AzNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="e4eb4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e4eb4-102">SYNOPSIS</span></span>
<span data-ttu-id="e4eb4-103">Запуск устранения неполадок в сетевом ресурсе в Azure.</span><span class="sxs-lookup"><span data-stu-id="e4eb4-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

## <span data-ttu-id="e4eb4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e4eb4-104">SYNTAX</span></span>

### <span data-ttu-id="e4eb4-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e4eb4-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -StorageId <String> -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4eb4-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="e4eb4-106">SetByName</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4eb4-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="e4eb4-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -Location <String> -TargetResourceId <String> -StorageId <String>
 -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4eb4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4eb4-108">DESCRIPTION</span></span>
<span data-ttu-id="e4eb4-109">Командлет Start-AzNetworkWatcherResourceTroubleshooting запускает устранение неполадок для сетевых ресурсов в Azure и возвращает сведения о возможных проблемах и снижении риска.</span><span class="sxs-lookup"><span data-stu-id="e4eb4-109">The Start-AzNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="e4eb4-110">В настоящее время поддерживаются шлюзы и соединения виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="e4eb4-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="e4eb4-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e4eb4-111">EXAMPLES</span></span>

### <span data-ttu-id="e4eb4-112">Пример 1: запуск устранения неполадок на шлюзе виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="e4eb4-112">Example 1: Start Troubleshooting on a Virtual Network Gateway</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="e4eb4-113">В приведенном выше примере начинается устранение неполадок шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="e4eb4-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="e4eb4-114">Выполнение операции может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="e4eb4-114">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="e4eb4-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e4eb4-115">PARAMETERS</span></span>

### <span data-ttu-id="e4eb4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4eb4-116">-DefaultProfile</span></span>
<span data-ttu-id="e4eb4-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e4eb4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4eb4-118">-Location</span><span class="sxs-lookup"><span data-stu-id="e4eb4-118">-Location</span></span>
<span data-ttu-id="e4eb4-119">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="e4eb4-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="e4eb4-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e4eb4-120">-NetworkWatcher</span></span>
<span data-ttu-id="e4eb4-121">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="e4eb4-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="e4eb4-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e4eb4-122">-NetworkWatcherName</span></span>
<span data-ttu-id="e4eb4-123">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="e4eb4-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="e4eb4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4eb4-124">-ResourceGroupName</span></span>
<span data-ttu-id="e4eb4-125">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="e4eb4-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="e4eb4-126">-StorageId</span><span class="sxs-lookup"><span data-stu-id="e4eb4-126">-StorageId</span></span>
<span data-ttu-id="e4eb4-127">Идентификатор хранилища.</span><span class="sxs-lookup"><span data-stu-id="e4eb4-127">The storage ID.</span></span>

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

### <span data-ttu-id="e4eb4-128">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="e4eb4-128">-StoragePath</span></span>
<span data-ttu-id="e4eb4-129">Путь к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="e4eb4-129">The storage path.</span></span>

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

### <span data-ttu-id="e4eb4-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="e4eb4-130">-TargetResourceId</span></span>
<span data-ttu-id="e4eb4-131">Указывает идентификатор ресурса для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="e4eb4-131">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="e4eb4-132">Пример формата: "/Subscriptions/$ {subscriptionId}/resourceGroups/$ {resourceGroupName}/providers/Microsoft.Network/connections/$ {connectionName}"</span><span class="sxs-lookup"><span data-stu-id="e4eb4-132">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="e4eb4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4eb4-133">CommonParameters</span></span>
<span data-ttu-id="e4eb4-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e4eb4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4eb4-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4eb4-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4eb4-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e4eb4-136">INPUTS</span></span>

### <span data-ttu-id="e4eb4-137">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e4eb4-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="e4eb4-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e4eb4-138">System.String</span></span>

## <span data-ttu-id="e4eb4-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4eb4-139">OUTPUTS</span></span>

### <span data-ttu-id="e4eb4-140">Microsoft. Azure. Commands. Network. Models. PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="e4eb4-140">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="e4eb4-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="e4eb4-141">NOTES</span></span>
<span data-ttu-id="e4eb4-142">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, устранение неполадок, VPN, подключение</span><span class="sxs-lookup"><span data-stu-id="e4eb4-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="e4eb4-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e4eb4-143">RELATED LINKS</span></span>

[<span data-ttu-id="e4eb4-144">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e4eb4-144">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="e4eb4-145">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e4eb4-145">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="e4eb4-146">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e4eb4-146">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="e4eb4-147">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e4eb4-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="e4eb4-148">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e4eb4-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e4eb4-149">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e4eb4-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="e4eb4-150">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e4eb4-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="e4eb4-151">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e4eb4-151">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e4eb4-152">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e4eb4-152">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="e4eb4-153">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e4eb4-153">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e4eb4-154">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e4eb4-154">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e4eb4-155">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e4eb4-155">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e4eb4-156">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4eb4-156">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="e4eb4-157">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e4eb4-157">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="e4eb4-158">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="e4eb4-158">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="e4eb4-159">Остановить-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e4eb4-159">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e4eb4-160">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e4eb4-160">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e4eb4-161">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e4eb4-161">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e4eb4-162">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="e4eb4-162">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="e4eb4-163">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e4eb4-163">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e4eb4-164">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e4eb4-164">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e4eb4-165">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="e4eb4-165">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="e4eb4-166">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="e4eb4-166">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="e4eb4-167">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="e4eb4-167">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="e4eb4-168">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="e4eb4-168">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="e4eb4-169">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="e4eb4-169">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="e4eb4-170">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e4eb4-170">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)