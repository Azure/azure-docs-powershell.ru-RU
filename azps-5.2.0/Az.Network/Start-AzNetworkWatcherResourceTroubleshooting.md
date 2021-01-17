---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: 0776b10a14236ac4806ccc166f24b1dd5a3ee3de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395495"
---
# <span data-ttu-id="85903-101">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="85903-101">Start-AzNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="85903-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85903-102">SYNOPSIS</span></span>
<span data-ttu-id="85903-103">Начало устранения неполадок сетевого ресурса в Azure.</span><span class="sxs-lookup"><span data-stu-id="85903-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

## <span data-ttu-id="85903-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="85903-104">SYNTAX</span></span>

### <span data-ttu-id="85903-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="85903-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -StorageId <String> -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85903-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="85903-106">SetByName</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85903-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="85903-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -Location <String> -TargetResourceId <String> -StorageId <String>
 -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85903-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="85903-108">DESCRIPTION</span></span>
<span data-ttu-id="85903-109">Новый Start-AzNetworkWatcherResourceTroubleshooting запускает устранение неполадок сетевого ресурса в Azure и возвращает сведения о потенциальных проблемах и их устранении.</span><span class="sxs-lookup"><span data-stu-id="85903-109">The Start-AzNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="85903-110">В настоящее время поддерживаются виртуальные сетевые шлюзы и подключения.</span><span class="sxs-lookup"><span data-stu-id="85903-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="85903-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="85903-111">EXAMPLES</span></span>

### <span data-ttu-id="85903-112">Пример 1. Начало устранения неполадок виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="85903-112">Example 1: Start Troubleshooting on a Virtual Network Gateway</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="85903-113">В примере выше начнется устранение неполадок виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="85903-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="85903-114">Операция может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="85903-114">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="85903-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85903-115">PARAMETERS</span></span>

### <span data-ttu-id="85903-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85903-116">-DefaultProfile</span></span>
<span data-ttu-id="85903-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="85903-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85903-118">-Location</span><span class="sxs-lookup"><span data-stu-id="85903-118">-Location</span></span>
<span data-ttu-id="85903-119">Расположение сетевого просмотра.</span><span class="sxs-lookup"><span data-stu-id="85903-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="85903-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="85903-120">-NetworkWatcher</span></span>
<span data-ttu-id="85903-121">Сетевой ресурс для просмотра.</span><span class="sxs-lookup"><span data-stu-id="85903-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="85903-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="85903-122">-NetworkWatcherName</span></span>
<span data-ttu-id="85903-123">Имя сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="85903-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="85903-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85903-124">-ResourceGroupName</span></span>
<span data-ttu-id="85903-125">Имя группы ресурсов сетевого watcher.</span><span class="sxs-lookup"><span data-stu-id="85903-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="85903-126">-StorageId</span><span class="sxs-lookup"><span data-stu-id="85903-126">-StorageId</span></span>
<span data-ttu-id="85903-127">ИД хранилища.</span><span class="sxs-lookup"><span data-stu-id="85903-127">The storage ID.</span></span>

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

### <span data-ttu-id="85903-128">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="85903-128">-StoragePath</span></span>
<span data-ttu-id="85903-129">Путь к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="85903-129">The storage path.</span></span>

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

### <span data-ttu-id="85903-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="85903-130">-TargetResourceId</span></span>
<span data-ttu-id="85903-131">Определяет его ИД, который нужно устранить.</span><span class="sxs-lookup"><span data-stu-id="85903-131">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="85903-132">Пример формата: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span><span class="sxs-lookup"><span data-stu-id="85903-132">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="85903-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85903-133">CommonParameters</span></span>
<span data-ttu-id="85903-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85903-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85903-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85903-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85903-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="85903-136">INPUTS</span></span>

### <span data-ttu-id="85903-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="85903-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="85903-138">System.String</span><span class="sxs-lookup"><span data-stu-id="85903-138">System.String</span></span>

## <span data-ttu-id="85903-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="85903-139">OUTPUTS</span></span>

### <span data-ttu-id="85903-140">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="85903-140">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="85903-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="85903-141">NOTES</span></span>
<span data-ttu-id="85903-142">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, network, networking, network watcher, troubleshoot, VPN, connection</span><span class="sxs-lookup"><span data-stu-id="85903-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="85903-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="85903-143">RELATED LINKS</span></span>

[<span data-ttu-id="85903-144">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="85903-144">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="85903-145">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="85903-145">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="85903-146">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="85903-146">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="85903-147">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="85903-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="85903-148">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="85903-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="85903-149">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="85903-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="85903-150">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="85903-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="85903-151">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="85903-151">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="85903-152">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="85903-152">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="85903-153">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="85903-153">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="85903-154">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="85903-154">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="85903-155">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="85903-155">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="85903-156">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="85903-156">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="85903-157">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="85903-157">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="85903-158">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="85903-158">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="85903-159">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="85903-159">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="85903-160">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="85903-160">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="85903-161">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="85903-161">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="85903-162">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="85903-162">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="85903-163">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="85903-163">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="85903-164">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="85903-164">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="85903-165">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="85903-165">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="85903-166">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="85903-166">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="85903-167">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="85903-167">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="85903-168">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="85903-168">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="85903-169">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="85903-169">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="85903-170">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="85903-170">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
