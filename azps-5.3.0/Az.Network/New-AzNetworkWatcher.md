---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: 7c8f33d8339bb873b713acabd71ca57fe9107383
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505530"
---
# <span data-ttu-id="51271-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="51271-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="51271-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51271-102">SYNOPSIS</span></span>
<span data-ttu-id="51271-103">Создание ресурса Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="51271-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="51271-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="51271-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51271-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="51271-105">DESCRIPTION</span></span>
<span data-ttu-id="51271-106">С New-AzNetworkWatcher создается новый ресурс Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="51271-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="51271-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="51271-107">EXAMPLES</span></span>

### <span data-ttu-id="51271-108">Пример 1. Создание сетевого watcher</span><span class="sxs-lookup"><span data-stu-id="51271-108">Example 1: Create a Network Watcher</span></span>
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

<span data-ttu-id="51271-109">В этом примере создается сетевой просмотр в новой группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="51271-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="51271-110">Обратите внимание, что для каждого региона можно создать только одно сетевое смотритель.</span><span class="sxs-lookup"><span data-stu-id="51271-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="51271-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51271-111">PARAMETERS</span></span>

### <span data-ttu-id="51271-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51271-112">-DefaultProfile</span></span>
<span data-ttu-id="51271-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="51271-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51271-114">-Location</span><span class="sxs-lookup"><span data-stu-id="51271-114">-Location</span></span>
<span data-ttu-id="51271-115">"Расположение".</span><span class="sxs-lookup"><span data-stu-id="51271-115">Location.</span></span>

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

### <span data-ttu-id="51271-116">-Name</span><span class="sxs-lookup"><span data-stu-id="51271-116">-Name</span></span>
<span data-ttu-id="51271-117">Имя сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="51271-117">The network watcher name.</span></span>

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

### <span data-ttu-id="51271-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51271-118">-ResourceGroupName</span></span>
<span data-ttu-id="51271-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="51271-119">The resource group name.</span></span>

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

### <span data-ttu-id="51271-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="51271-120">-Tag</span></span>
<span data-ttu-id="51271-121">Пары "ключевое значение" в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="51271-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="51271-122">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="51271-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="51271-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51271-123">-Confirm</span></span>
<span data-ttu-id="51271-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="51271-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51271-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51271-125">-WhatIf</span></span>
<span data-ttu-id="51271-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51271-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51271-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="51271-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51271-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51271-128">CommonParameters</span></span>
<span data-ttu-id="51271-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51271-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51271-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51271-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51271-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="51271-131">INPUTS</span></span>

### <span data-ttu-id="51271-132">System.String</span><span class="sxs-lookup"><span data-stu-id="51271-132">System.String</span></span>

### <span data-ttu-id="51271-133">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="51271-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="51271-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="51271-134">OUTPUTS</span></span>

### <span data-ttu-id="51271-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="51271-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="51271-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="51271-136">NOTES</span></span>
<span data-ttu-id="51271-137">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span><span class="sxs-lookup"><span data-stu-id="51271-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="51271-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="51271-138">RELATED LINKS</span></span>

[<span data-ttu-id="51271-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="51271-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="51271-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="51271-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="51271-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="51271-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="51271-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="51271-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="51271-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="51271-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="51271-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="51271-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="51271-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="51271-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="51271-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="51271-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="51271-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="51271-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="51271-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="51271-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="51271-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="51271-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="51271-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="51271-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="51271-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="51271-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="51271-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="51271-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="51271-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="51271-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="51271-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="51271-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="51271-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="51271-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="51271-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="51271-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="51271-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="51271-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="51271-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="51271-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="51271-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="51271-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="51271-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="51271-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="51271-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="51271-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="51271-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="51271-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="51271-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="51271-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="51271-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="51271-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="51271-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="51271-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
