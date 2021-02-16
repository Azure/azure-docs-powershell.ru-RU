---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: 5c11eecb00aa97fc90aecc770a77285f77be988b
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100408480"
---
# <span data-ttu-id="61024-101">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="61024-101">Start-AzNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="61024-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61024-102">SYNOPSIS</span></span>
<span data-ttu-id="61024-103">Начало устранения неполадок сетевого ресурса в Azure.</span><span class="sxs-lookup"><span data-stu-id="61024-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

## <span data-ttu-id="61024-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="61024-104">SYNTAX</span></span>

### <span data-ttu-id="61024-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="61024-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -StorageId <String> -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61024-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="61024-106">SetByName</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61024-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="61024-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -Location <String> -TargetResourceId <String> -StorageId <String>
 -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61024-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61024-108">DESCRIPTION</span></span>
<span data-ttu-id="61024-109">Новый Start-AzNetworkWatcherResourceTroubleshooting запускает устранение неполадок сетевого ресурса в Azure и возвращает сведения о потенциальных проблемах и их устранении.</span><span class="sxs-lookup"><span data-stu-id="61024-109">The Start-AzNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="61024-110">В настоящее время поддерживаются виртуальные сетевые шлюзы и подключения.</span><span class="sxs-lookup"><span data-stu-id="61024-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="61024-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="61024-111">EXAMPLES</span></span>

### <span data-ttu-id="61024-112">Пример 1. Начало устранения неполадок виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="61024-112">Example 1: Start Troubleshooting on a Virtual Network Gateway</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="61024-113">В примере выше начнется устранение неполадок виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="61024-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="61024-114">Операция может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="61024-114">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="61024-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61024-115">PARAMETERS</span></span>

### <span data-ttu-id="61024-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61024-116">-DefaultProfile</span></span>
<span data-ttu-id="61024-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="61024-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61024-118">-Location</span><span class="sxs-lookup"><span data-stu-id="61024-118">-Location</span></span>
<span data-ttu-id="61024-119">Расположение сетевого просмотра.</span><span class="sxs-lookup"><span data-stu-id="61024-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="61024-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="61024-120">-NetworkWatcher</span></span>
<span data-ttu-id="61024-121">Сетевой ресурс для просмотра.</span><span class="sxs-lookup"><span data-stu-id="61024-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="61024-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="61024-122">-NetworkWatcherName</span></span>
<span data-ttu-id="61024-123">Имя сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="61024-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="61024-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61024-124">-ResourceGroupName</span></span>
<span data-ttu-id="61024-125">Имя группы ресурсов сетевого watcher.</span><span class="sxs-lookup"><span data-stu-id="61024-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="61024-126">-StorageId</span><span class="sxs-lookup"><span data-stu-id="61024-126">-StorageId</span></span>
<span data-ttu-id="61024-127">ИД хранилища.</span><span class="sxs-lookup"><span data-stu-id="61024-127">The storage ID.</span></span>

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

### <span data-ttu-id="61024-128">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="61024-128">-StoragePath</span></span>
<span data-ttu-id="61024-129">Путь к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="61024-129">The storage path.</span></span>

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

### <span data-ttu-id="61024-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="61024-130">-TargetResourceId</span></span>
<span data-ttu-id="61024-131">Определяет его ИД, который нужно устранить.</span><span class="sxs-lookup"><span data-stu-id="61024-131">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="61024-132">Пример формата: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span><span class="sxs-lookup"><span data-stu-id="61024-132">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="61024-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61024-133">CommonParameters</span></span>
<span data-ttu-id="61024-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61024-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61024-135">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61024-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61024-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61024-136">INPUTS</span></span>

### <span data-ttu-id="61024-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="61024-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="61024-138">System.String</span><span class="sxs-lookup"><span data-stu-id="61024-138">System.String</span></span>

## <span data-ttu-id="61024-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="61024-139">OUTPUTS</span></span>

### <span data-ttu-id="61024-140">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="61024-140">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="61024-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="61024-141">NOTES</span></span>
<span data-ttu-id="61024-142">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, network, networking, network watcher, troubleshoot, VPN, connection</span><span class="sxs-lookup"><span data-stu-id="61024-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="61024-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61024-143">RELATED LINKS</span></span>

[<span data-ttu-id="61024-144">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="61024-144">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="61024-145">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="61024-145">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="61024-146">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="61024-146">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="61024-147">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="61024-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="61024-148">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="61024-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="61024-149">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="61024-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="61024-150">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="61024-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="61024-151">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="61024-151">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="61024-152">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="61024-152">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="61024-153">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="61024-153">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="61024-154">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="61024-154">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="61024-155">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="61024-155">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="61024-156">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="61024-156">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="61024-157">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="61024-157">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="61024-158">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="61024-158">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="61024-159">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="61024-159">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="61024-160">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="61024-160">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="61024-161">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="61024-161">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="61024-162">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="61024-162">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="61024-163">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="61024-163">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="61024-164">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="61024-164">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="61024-165">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="61024-165">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="61024-166">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="61024-166">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="61024-167">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="61024-167">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="61024-168">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="61024-168">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="61024-169">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="61024-169">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="61024-170">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="61024-170">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
