---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 048eeb08b820f5eccd76a74587d4949f1f9de110
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100408412"
---
# <span data-ttu-id="9ecd9-101">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9ecd9-101">Stop-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="9ecd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ecd9-102">SYNOPSIS</span></span>
<span data-ttu-id="9ecd9-103">Остановка сеанса захвата пакетов</span><span class="sxs-lookup"><span data-stu-id="9ecd9-103">Stops a running packet capture session</span></span>

## <span data-ttu-id="9ecd9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9ecd9-104">SYNTAX</span></span>

### <span data-ttu-id="9ecd9-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9ecd9-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ecd9-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="9ecd9-106">SetByName</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ecd9-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="9ecd9-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ecd9-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ecd9-108">DESCRIPTION</span></span>
<span data-ttu-id="9ecd9-109">Сеанс Stop-AzNetworkWatcherPacketCapture прекращает сеанс захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="9ecd9-109">The Stop-AzNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="9ecd9-110">После окончания сеанса файл захвата пакетов загружается в хранилище и (или) локально в VM-файле (в зависимости от его конфигурации).</span><span class="sxs-lookup"><span data-stu-id="9ecd9-110">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="9ecd9-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9ecd9-111">EXAMPLES</span></span>

### <span data-ttu-id="9ecd9-112">Пример 1. Остановка сеанса захвата пакетов</span><span class="sxs-lookup"><span data-stu-id="9ecd9-112">Example 1: Stop a packet capture session</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="9ecd9-113">В этом примере мы останавливаем сеанс захвата пакетов PacketCaptureTest.</span><span class="sxs-lookup"><span data-stu-id="9ecd9-113">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="9ecd9-114">После окончания сеанса файл захвата пакетов загружается в хранилище и (или) локально в VM-файле (в зависимости от его конфигурации).</span><span class="sxs-lookup"><span data-stu-id="9ecd9-114">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="9ecd9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ecd9-115">PARAMETERS</span></span>

### <span data-ttu-id="9ecd9-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ecd9-116">-AsJob</span></span>
<span data-ttu-id="9ecd9-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9ecd9-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ecd9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ecd9-118">-DefaultProfile</span></span>
<span data-ttu-id="9ecd9-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9ecd9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ecd9-120">-Location</span><span class="sxs-lookup"><span data-stu-id="9ecd9-120">-Location</span></span>
<span data-ttu-id="9ecd9-121">Расположение сетевого просмотра.</span><span class="sxs-lookup"><span data-stu-id="9ecd9-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="9ecd9-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9ecd9-122">-NetworkWatcher</span></span>
<span data-ttu-id="9ecd9-123">Сетевой ресурс для просмотра.</span><span class="sxs-lookup"><span data-stu-id="9ecd9-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="9ecd9-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="9ecd9-124">-NetworkWatcherName</span></span>
<span data-ttu-id="9ecd9-125">Имя сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="9ecd9-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="9ecd9-126">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="9ecd9-126">-PacketCaptureName</span></span>
<span data-ttu-id="9ecd9-127">Имя захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="9ecd9-127">The packet capture name.</span></span>

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

### <span data-ttu-id="9ecd9-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ecd9-128">-PassThru</span></span>
<span data-ttu-id="9ecd9-129">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="9ecd9-129">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="9ecd9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ecd9-130">-ResourceGroupName</span></span>
<span data-ttu-id="9ecd9-131">Имя группы ресурсов сетевого watcher.</span><span class="sxs-lookup"><span data-stu-id="9ecd9-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="9ecd9-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ecd9-132">-Confirm</span></span>
<span data-ttu-id="9ecd9-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9ecd9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ecd9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ecd9-134">-WhatIf</span></span>
<span data-ttu-id="9ecd9-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ecd9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ecd9-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9ecd9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ecd9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ecd9-137">CommonParameters</span></span>
<span data-ttu-id="9ecd9-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ecd9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ecd9-139">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ecd9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ecd9-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9ecd9-140">INPUTS</span></span>

### <span data-ttu-id="9ecd9-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9ecd9-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="9ecd9-142">System.String</span><span class="sxs-lookup"><span data-stu-id="9ecd9-142">System.String</span></span>

## <span data-ttu-id="9ecd9-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9ecd9-143">OUTPUTS</span></span>

### <span data-ttu-id="9ecd9-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9ecd9-144">System.Boolean</span></span>

## <span data-ttu-id="9ecd9-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9ecd9-145">NOTES</span></span>
<span data-ttu-id="9ecd9-146">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, network, networking, network watcher, packet, capture, traffic</span><span class="sxs-lookup"><span data-stu-id="9ecd9-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="9ecd9-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ecd9-147">RELATED LINKS</span></span>

[<span data-ttu-id="9ecd9-148">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9ecd9-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9ecd9-149">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="9ecd9-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="9ecd9-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9ecd9-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9ecd9-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9ecd9-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9ecd9-152">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9ecd9-152">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="9ecd9-153">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9ecd9-153">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="9ecd9-154">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9ecd9-154">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="9ecd9-155">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="9ecd9-155">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="9ecd9-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="9ecd9-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="9ecd9-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="9ecd9-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="9ecd9-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="9ecd9-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="9ecd9-159">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="9ecd9-159">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="9ecd9-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="9ecd9-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="9ecd9-161">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9ecd9-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9ecd9-162">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="9ecd9-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="9ecd9-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="9ecd9-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="9ecd9-164">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9ecd9-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9ecd9-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9ecd9-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9ecd9-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9ecd9-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9ecd9-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="9ecd9-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="9ecd9-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9ecd9-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9ecd9-169">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9ecd9-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9ecd9-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="9ecd9-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="9ecd9-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="9ecd9-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="9ecd9-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="9ecd9-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="9ecd9-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="9ecd9-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="9ecd9-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9ecd9-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
