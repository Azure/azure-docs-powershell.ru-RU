---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/stop-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: b0446488668b0473e387563983bb264f6c4078b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951843"
---
# <span data-ttu-id="a5d24-101">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a5d24-101">Stop-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="a5d24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5d24-102">SYNOPSIS</span></span>
<span data-ttu-id="a5d24-103">Остановка сеанса захвата пакетов</span><span class="sxs-lookup"><span data-stu-id="a5d24-103">Stops a running packet capture session</span></span>

## <span data-ttu-id="a5d24-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a5d24-104">SYNTAX</span></span>

### <span data-ttu-id="a5d24-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a5d24-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5d24-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a5d24-106">SetByName</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5d24-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="a5d24-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5d24-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5d24-108">DESCRIPTION</span></span>
<span data-ttu-id="a5d24-109">Сеанс Stop-AzNetworkWatcherPacketCapture прекращает сеанс захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="a5d24-109">The Stop-AzNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="a5d24-110">После окончания сеанса файл захвата пакетов загружается в хранилище и (или) локально в VM-файле (в зависимости от его конфигурации).</span><span class="sxs-lookup"><span data-stu-id="a5d24-110">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="a5d24-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a5d24-111">EXAMPLES</span></span>

### <span data-ttu-id="a5d24-112">Пример 1. Остановка сеанса захвата пакетов</span><span class="sxs-lookup"><span data-stu-id="a5d24-112">Example 1: Stop a packet capture session</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="a5d24-113">В этом примере мы останавливаем сеанс захвата пакетов PacketCaptureTest.</span><span class="sxs-lookup"><span data-stu-id="a5d24-113">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="a5d24-114">После окончания сеанса файл захвата пакетов загружается в хранилище и (или) локально в VM-файле (в зависимости от его конфигурации).</span><span class="sxs-lookup"><span data-stu-id="a5d24-114">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="a5d24-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5d24-115">PARAMETERS</span></span>

### <span data-ttu-id="a5d24-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5d24-116">-AsJob</span></span>
<span data-ttu-id="a5d24-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a5d24-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a5d24-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5d24-118">-DefaultProfile</span></span>
<span data-ttu-id="a5d24-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a5d24-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5d24-120">-Location</span><span class="sxs-lookup"><span data-stu-id="a5d24-120">-Location</span></span>
<span data-ttu-id="a5d24-121">Расположение сетевого просмотра.</span><span class="sxs-lookup"><span data-stu-id="a5d24-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="a5d24-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a5d24-122">-NetworkWatcher</span></span>
<span data-ttu-id="a5d24-123">Сетевой ресурс для просмотра.</span><span class="sxs-lookup"><span data-stu-id="a5d24-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="a5d24-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a5d24-124">-NetworkWatcherName</span></span>
<span data-ttu-id="a5d24-125">Имя сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="a5d24-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="a5d24-126">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="a5d24-126">-PacketCaptureName</span></span>
<span data-ttu-id="a5d24-127">Имя захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="a5d24-127">The packet capture name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d24-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5d24-128">-PassThru</span></span>
<span data-ttu-id="a5d24-129">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="a5d24-129">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="a5d24-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5d24-130">-ResourceGroupName</span></span>
<span data-ttu-id="a5d24-131">Имя группы ресурсов сетевого watcher.</span><span class="sxs-lookup"><span data-stu-id="a5d24-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a5d24-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5d24-132">-Confirm</span></span>
<span data-ttu-id="a5d24-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a5d24-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5d24-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5d24-134">-WhatIf</span></span>
<span data-ttu-id="a5d24-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5d24-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5d24-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a5d24-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5d24-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5d24-137">CommonParameters</span></span>
<span data-ttu-id="a5d24-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5d24-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5d24-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5d24-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5d24-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a5d24-140">INPUTS</span></span>

### <span data-ttu-id="a5d24-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a5d24-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="a5d24-142">System.String</span><span class="sxs-lookup"><span data-stu-id="a5d24-142">System.String</span></span>

## <span data-ttu-id="a5d24-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a5d24-143">OUTPUTS</span></span>

### <span data-ttu-id="a5d24-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a5d24-144">System.Boolean</span></span>

## <span data-ttu-id="a5d24-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a5d24-145">NOTES</span></span>
<span data-ttu-id="a5d24-146">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, network, networking, network watcher, packet, capture, traffic</span><span class="sxs-lookup"><span data-stu-id="a5d24-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="a5d24-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5d24-147">RELATED LINKS</span></span>

[<span data-ttu-id="a5d24-148">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a5d24-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a5d24-149">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a5d24-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="a5d24-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a5d24-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a5d24-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a5d24-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a5d24-152">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a5d24-152">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="a5d24-153">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a5d24-153">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="a5d24-154">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a5d24-154">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="a5d24-155">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a5d24-155">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="a5d24-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a5d24-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="a5d24-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a5d24-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a5d24-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a5d24-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="a5d24-159">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a5d24-159">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a5d24-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a5d24-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="a5d24-161">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a5d24-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a5d24-162">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5d24-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="a5d24-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="a5d24-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="a5d24-164">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a5d24-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a5d24-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a5d24-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a5d24-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a5d24-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a5d24-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="a5d24-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="a5d24-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a5d24-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a5d24-169">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a5d24-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a5d24-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="a5d24-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="a5d24-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="a5d24-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="a5d24-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="a5d24-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="a5d24-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="a5d24-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="a5d24-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a5d24-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
