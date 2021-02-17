---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: f38250a4beed7eb05f758e17a1d3d17f1d76f86e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405199"
---
# <span data-ttu-id="6eead-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6eead-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="6eead-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6eead-102">SYNOPSIS</span></span>
<span data-ttu-id="6eead-103">Создание ресурса Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="6eead-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="6eead-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6eead-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6eead-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6eead-105">DESCRIPTION</span></span>
<span data-ttu-id="6eead-106">С New-AzNetworkWatcher создается новый ресурс Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="6eead-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="6eead-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6eead-107">EXAMPLES</span></span>

### <span data-ttu-id="6eead-108">Пример 1. Создание сетевого watcher</span><span class="sxs-lookup"><span data-stu-id="6eead-108">Example 1: Create a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="6eead-109">В этом примере создается сетевой просмотр в новой группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6eead-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="6eead-110">Обратите внимание, что для каждого региона можно создать только одно сетевое смотритель.</span><span class="sxs-lookup"><span data-stu-id="6eead-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="6eead-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6eead-111">PARAMETERS</span></span>

### <span data-ttu-id="6eead-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eead-112">-DefaultProfile</span></span>
<span data-ttu-id="6eead-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6eead-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6eead-114">-Location</span><span class="sxs-lookup"><span data-stu-id="6eead-114">-Location</span></span>
<span data-ttu-id="6eead-115">"Расположение".</span><span class="sxs-lookup"><span data-stu-id="6eead-115">Location.</span></span>

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

### <span data-ttu-id="6eead-116">-Name</span><span class="sxs-lookup"><span data-stu-id="6eead-116">-Name</span></span>
<span data-ttu-id="6eead-117">Имя сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="6eead-117">The network watcher name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6eead-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eead-118">-ResourceGroupName</span></span>
<span data-ttu-id="6eead-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6eead-119">The resource group name.</span></span>

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

### <span data-ttu-id="6eead-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="6eead-120">-Tag</span></span>
<span data-ttu-id="6eead-121">Пары значений ключа в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="6eead-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6eead-122">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="6eead-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6eead-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6eead-123">-Confirm</span></span>
<span data-ttu-id="6eead-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6eead-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eead-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6eead-125">-WhatIf</span></span>
<span data-ttu-id="6eead-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6eead-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6eead-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6eead-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eead-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eead-128">CommonParameters</span></span>
<span data-ttu-id="6eead-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6eead-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eead-130">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6eead-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eead-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6eead-131">INPUTS</span></span>

### <span data-ttu-id="6eead-132">System.String</span><span class="sxs-lookup"><span data-stu-id="6eead-132">System.String</span></span>

### <span data-ttu-id="6eead-133">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="6eead-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6eead-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6eead-134">OUTPUTS</span></span>

### <span data-ttu-id="6eead-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6eead-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="6eead-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6eead-136">NOTES</span></span>
<span data-ttu-id="6eead-137">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking, network watcher,</span><span class="sxs-lookup"><span data-stu-id="6eead-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="6eead-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6eead-138">RELATED LINKS</span></span>

[<span data-ttu-id="6eead-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6eead-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="6eead-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6eead-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="6eead-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6eead-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="6eead-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="6eead-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="6eead-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="6eead-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="6eead-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="6eead-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="6eead-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="6eead-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="6eead-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6eead-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6eead-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="6eead-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="6eead-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6eead-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6eead-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6eead-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6eead-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6eead-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6eead-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="6eead-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="6eead-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="6eead-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="6eead-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="6eead-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="6eead-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6eead-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6eead-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6eead-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6eead-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6eead-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6eead-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="6eead-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="6eead-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6eead-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6eead-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6eead-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6eead-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="6eead-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="6eead-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="6eead-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="6eead-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="6eead-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="6eead-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="6eead-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="6eead-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="6eead-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="6eead-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6eead-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
