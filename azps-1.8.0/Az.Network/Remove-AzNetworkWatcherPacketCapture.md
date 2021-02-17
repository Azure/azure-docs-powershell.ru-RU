---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 35bd138a682eaca3b58ba82190961d3b7d7e3e26
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401799"
---
# <span data-ttu-id="d4496-101">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d4496-101">Remove-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="d4496-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4496-102">SYNOPSIS</span></span>
<span data-ttu-id="d4496-103">Удаляет ресурс захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="d4496-103">Removes a packet capture resource.</span></span>

## <span data-ttu-id="d4496-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d4496-104">SYNTAX</span></span>

### <span data-ttu-id="d4496-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d4496-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4496-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="d4496-106">SetByName</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4496-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d4496-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4496-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4496-108">DESCRIPTION</span></span>
<span data-ttu-id="d4496-109">При Remove-AzNetworkWatcherPacketCapture удаляется ресурс для захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="d4496-109">The Remove-AzNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="d4496-110">Рекомендуется позвонить в Stop-AzNetworkWatcherPacketCapture перед вызовом Remove-AzNetworkWatcherPacketCapture.</span><span class="sxs-lookup"><span data-stu-id="d4496-110">It is recommended to call Stop-AzNetworkWatcherPacketCapture before calling Remove-AzNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="d4496-111">Если во время сеанса захвата пакетов Remove-AzNetworkWatcherPacketCapture это называется, возможно, он не сохранен.</span><span class="sxs-lookup"><span data-stu-id="d4496-111">If the packet capture session is running when Remove-AzNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="d4496-112">Если сеанс остановлен до удаления, CAP-файл, содержащий данные захвата, не удаляется.</span><span class="sxs-lookup"><span data-stu-id="d4496-112">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="d4496-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d4496-113">EXAMPLES</span></span>

### <span data-ttu-id="d4496-114">Пример 1. Удаление сеанса захвата пакетов</span><span class="sxs-lookup"><span data-stu-id="d4496-114">Example 1: Remove a packet capture session</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="d4496-115">В этом примере мы удаляем существующий сеанс захвата пакетов PacketCaptureTest.</span><span class="sxs-lookup"><span data-stu-id="d4496-115">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="d4496-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4496-116">PARAMETERS</span></span>

### <span data-ttu-id="d4496-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4496-117">-AsJob</span></span>
<span data-ttu-id="d4496-118">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d4496-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4496-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4496-119">-DefaultProfile</span></span>
<span data-ttu-id="d4496-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d4496-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4496-121">-Location</span><span class="sxs-lookup"><span data-stu-id="d4496-121">-Location</span></span>
<span data-ttu-id="d4496-122">Расположение сетевого просмотра.</span><span class="sxs-lookup"><span data-stu-id="d4496-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d4496-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d4496-123">-NetworkWatcher</span></span>
<span data-ttu-id="d4496-124">Сетевой ресурс для просмотра.</span><span class="sxs-lookup"><span data-stu-id="d4496-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="d4496-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d4496-125">-NetworkWatcherName</span></span>
<span data-ttu-id="d4496-126">Имя сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="d4496-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="d4496-127">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="d4496-127">-PacketCaptureName</span></span>
<span data-ttu-id="d4496-128">Имя захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="d4496-128">The packet capture name.</span></span>

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

### <span data-ttu-id="d4496-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4496-129">-PassThru</span></span>
<span data-ttu-id="d4496-130">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="d4496-130">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="d4496-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4496-131">-ResourceGroupName</span></span>
<span data-ttu-id="d4496-132">Имя группы ресурсов сетевого watcher.</span><span class="sxs-lookup"><span data-stu-id="d4496-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d4496-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4496-133">-Confirm</span></span>
<span data-ttu-id="d4496-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d4496-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4496-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4496-135">-WhatIf</span></span>
<span data-ttu-id="d4496-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4496-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4496-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d4496-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4496-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4496-138">CommonParameters</span></span>
<span data-ttu-id="d4496-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4496-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4496-140">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4496-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4496-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4496-141">INPUTS</span></span>

### <span data-ttu-id="d4496-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d4496-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="d4496-143">System.String</span><span class="sxs-lookup"><span data-stu-id="d4496-143">System.String</span></span>

## <span data-ttu-id="d4496-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d4496-144">OUTPUTS</span></span>

### <span data-ttu-id="d4496-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d4496-145">System.Boolean</span></span>

## <span data-ttu-id="d4496-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d4496-146">NOTES</span></span>
<span data-ttu-id="d4496-147">Ключевые слова: azure, azurerm, arm, resource, resource, management, manager, network, network, network, network watcher, packet, capture, traffic, remove</span><span class="sxs-lookup"><span data-stu-id="d4496-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="d4496-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4496-148">RELATED LINKS</span></span>

[<span data-ttu-id="d4496-149">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d4496-149">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d4496-150">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d4496-150">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d4496-151">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d4496-151">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d4496-152">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d4496-152">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d4496-153">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d4496-153">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d4496-154">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d4496-154">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d4496-155">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d4496-155">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d4496-156">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d4496-156">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d4496-157">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d4496-157">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d4496-158">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d4496-158">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d4496-159">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d4496-159">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d4496-160">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d4496-160">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d4496-161">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4496-161">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="d4496-162">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d4496-162">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d4496-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d4496-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="d4496-164">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d4496-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d4496-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d4496-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d4496-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d4496-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d4496-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d4496-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="d4496-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d4496-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d4496-169">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d4496-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d4496-170">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d4496-170">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="d4496-171">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d4496-171">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="d4496-172">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d4496-172">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="d4496-173">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d4496-173">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="d4496-174">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d4496-174">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="d4496-175">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d4496-175">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
