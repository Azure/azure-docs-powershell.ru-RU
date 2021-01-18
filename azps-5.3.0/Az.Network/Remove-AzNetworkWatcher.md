---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: cce361870f6dc65f644264e52b331c209177668f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518045"
---
# <span data-ttu-id="baed7-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="baed7-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="baed7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="baed7-102">SYNOPSIS</span></span>
<span data-ttu-id="baed7-103">Удаляет network Watcher.</span><span class="sxs-lookup"><span data-stu-id="baed7-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="baed7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="baed7-104">SYNTAX</span></span>

### <span data-ttu-id="baed7-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="baed7-105">SetByResource</span></span>
```
Remove-AzNetworkWatcher -NetworkWatcher <PSNetworkWatcher> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="baed7-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="baed7-106">SetByName</span></span>
```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="baed7-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="baed7-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcher -Location <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="baed7-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="baed7-108">DESCRIPTION</span></span>
<span data-ttu-id="baed7-109">С Remove-AzNetworkWatcher удаляется ресурс Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="baed7-109">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="baed7-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="baed7-110">EXAMPLES</span></span>

### <span data-ttu-id="baed7-111">Пример 1. Создание и удаление сетевого watcher</span><span class="sxs-lookup"><span data-stu-id="baed7-111">Example 1: Create and delete a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="baed7-112">В этом примере в группе ресурсов создается network Watcher, а затем сразу удаляется.</span><span class="sxs-lookup"><span data-stu-id="baed7-112">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="baed7-113">Обратите внимание, что для каждого региона можно создать только одно сетевое смотритель.</span><span class="sxs-lookup"><span data-stu-id="baed7-113">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="baed7-114">Чтобы скрыть запрос при удалении виртуальной сети, используйте флаг -Force.</span><span class="sxs-lookup"><span data-stu-id="baed7-114">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="baed7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="baed7-115">PARAMETERS</span></span>

### <span data-ttu-id="baed7-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="baed7-116">-AsJob</span></span>
<span data-ttu-id="baed7-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="baed7-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baed7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baed7-118">-DefaultProfile</span></span>
<span data-ttu-id="baed7-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="baed7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="baed7-120">-Location</span><span class="sxs-lookup"><span data-stu-id="baed7-120">-Location</span></span>
<span data-ttu-id="baed7-121">Расположение сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="baed7-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="baed7-122">-Name</span><span class="sxs-lookup"><span data-stu-id="baed7-122">-Name</span></span>
<span data-ttu-id="baed7-123">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="baed7-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="baed7-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="baed7-124">-NetworkWatcher</span></span>
<span data-ttu-id="baed7-125">Сетевой ресурс для просмотра.</span><span class="sxs-lookup"><span data-stu-id="baed7-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="baed7-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="baed7-126">-PassThru</span></span>
<span data-ttu-id="baed7-127">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="baed7-127">Returns an object representing the item with which you are working.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baed7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baed7-128">-ResourceGroupName</span></span>
<span data-ttu-id="baed7-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="baed7-129">The resource group name.</span></span>

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

### <span data-ttu-id="baed7-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="baed7-130">-Confirm</span></span>
<span data-ttu-id="baed7-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="baed7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="baed7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="baed7-132">-WhatIf</span></span>
<span data-ttu-id="baed7-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="baed7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="baed7-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="baed7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="baed7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baed7-135">CommonParameters</span></span>
<span data-ttu-id="baed7-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baed7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baed7-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baed7-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baed7-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="baed7-138">INPUTS</span></span>

### <span data-ttu-id="baed7-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="baed7-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="baed7-140">System.String</span><span class="sxs-lookup"><span data-stu-id="baed7-140">System.String</span></span>

## <span data-ttu-id="baed7-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="baed7-141">OUTPUTS</span></span>

### <span data-ttu-id="baed7-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="baed7-142">System.Boolean</span></span>

## <span data-ttu-id="baed7-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="baed7-143">NOTES</span></span>
<span data-ttu-id="baed7-144">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking, network watcher,</span><span class="sxs-lookup"><span data-stu-id="baed7-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="baed7-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="baed7-145">RELATED LINKS</span></span>

[<span data-ttu-id="baed7-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="baed7-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="baed7-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="baed7-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="baed7-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="baed7-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="baed7-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="baed7-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="baed7-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="baed7-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="baed7-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="baed7-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="baed7-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="baed7-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="baed7-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="baed7-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="baed7-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="baed7-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="baed7-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="baed7-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="baed7-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="baed7-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="baed7-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="baed7-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="baed7-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="baed7-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="baed7-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="baed7-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="baed7-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="baed7-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="baed7-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="baed7-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="baed7-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="baed7-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="baed7-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="baed7-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="baed7-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="baed7-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="baed7-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="baed7-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="baed7-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="baed7-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="baed7-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="baed7-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="baed7-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="baed7-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="baed7-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="baed7-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="baed7-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="baed7-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="baed7-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="baed7-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="baed7-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="baed7-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
