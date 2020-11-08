---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: 7c8f33d8339bb873b713acabd71ca57fe9107383
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078902"
---
# <span data-ttu-id="1b66b-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1b66b-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="1b66b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1b66b-102">SYNOPSIS</span></span>
<span data-ttu-id="1b66b-103">Создание нового ресурса сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="1b66b-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="1b66b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1b66b-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b66b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b66b-105">DESCRIPTION</span></span>
<span data-ttu-id="1b66b-106">Командлет New-AzNetworkWatcher создает новый ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="1b66b-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="1b66b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1b66b-107">EXAMPLES</span></span>

### <span data-ttu-id="1b66b-108">Пример 1: Создание наблюдателя сети</span><span class="sxs-lookup"><span data-stu-id="1b66b-108">Example 1: Create a Network Watcher</span></span>
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

<span data-ttu-id="1b66b-109">В этом примере создается новый наблюдатель сети внутри созданной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1b66b-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="1b66b-110">Обратите внимание, что для каждого региона на каждую подписку может быть создано только один наблюдатель сети.</span><span class="sxs-lookup"><span data-stu-id="1b66b-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="1b66b-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1b66b-111">PARAMETERS</span></span>

### <span data-ttu-id="1b66b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b66b-112">-DefaultProfile</span></span>
<span data-ttu-id="1b66b-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1b66b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b66b-114">-Location</span><span class="sxs-lookup"><span data-stu-id="1b66b-114">-Location</span></span>
<span data-ttu-id="1b66b-115">Поиска.</span><span class="sxs-lookup"><span data-stu-id="1b66b-115">Location.</span></span>

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

### <span data-ttu-id="1b66b-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1b66b-116">-Name</span></span>
<span data-ttu-id="1b66b-117">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="1b66b-117">The network watcher name.</span></span>

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

### <span data-ttu-id="1b66b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b66b-118">-ResourceGroupName</span></span>
<span data-ttu-id="1b66b-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1b66b-119">The resource group name.</span></span>

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

### <span data-ttu-id="1b66b-120">-Тег</span><span class="sxs-lookup"><span data-stu-id="1b66b-120">-Tag</span></span>
<span data-ttu-id="1b66b-121">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="1b66b-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1b66b-122">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="1b66b-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1b66b-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b66b-123">-Confirm</span></span>
<span data-ttu-id="1b66b-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1b66b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b66b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b66b-125">-WhatIf</span></span>
<span data-ttu-id="1b66b-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1b66b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b66b-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1b66b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b66b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b66b-128">CommonParameters</span></span>
<span data-ttu-id="1b66b-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1b66b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b66b-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b66b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b66b-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1b66b-131">INPUTS</span></span>

### <span data-ttu-id="1b66b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1b66b-132">System.String</span></span>

### <span data-ttu-id="1b66b-133">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1b66b-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1b66b-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b66b-134">OUTPUTS</span></span>

### <span data-ttu-id="1b66b-135">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1b66b-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="1b66b-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="1b66b-136">NOTES</span></span>
<span data-ttu-id="1b66b-137">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети</span><span class="sxs-lookup"><span data-stu-id="1b66b-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="1b66b-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1b66b-138">RELATED LINKS</span></span>

[<span data-ttu-id="1b66b-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1b66b-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="1b66b-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1b66b-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="1b66b-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1b66b-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="1b66b-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="1b66b-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="1b66b-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1b66b-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="1b66b-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="1b66b-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="1b66b-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="1b66b-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="1b66b-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1b66b-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1b66b-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="1b66b-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="1b66b-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1b66b-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1b66b-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1b66b-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1b66b-150">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1b66b-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1b66b-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b66b-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="1b66b-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1b66b-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="1b66b-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="1b66b-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="1b66b-154">Остановить-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b66b-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1b66b-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b66b-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1b66b-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b66b-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1b66b-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="1b66b-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="1b66b-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b66b-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1b66b-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b66b-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1b66b-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="1b66b-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="1b66b-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="1b66b-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="1b66b-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="1b66b-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="1b66b-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="1b66b-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="1b66b-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="1b66b-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="1b66b-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b66b-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
