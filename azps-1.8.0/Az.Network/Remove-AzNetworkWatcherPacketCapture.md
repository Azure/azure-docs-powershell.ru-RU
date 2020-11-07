---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: d99b085f5137c9f18d4dda50fce0654954266f37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730130"
---
# <span data-ttu-id="2a7a9-101">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2a7a9-101">Remove-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="2a7a9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2a7a9-102">SYNOPSIS</span></span>
<span data-ttu-id="2a7a9-103">Удаляет ресурс захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="2a7a9-103">Removes a packet capture resource.</span></span>

## <span data-ttu-id="2a7a9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2a7a9-104">SYNTAX</span></span>

### <span data-ttu-id="2a7a9-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2a7a9-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a7a9-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="2a7a9-106">SetByName</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a7a9-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="2a7a9-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a7a9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a7a9-108">DESCRIPTION</span></span>
<span data-ttu-id="2a7a9-109">Remove-AzNetworkWatcherPacketCapture удаляет ресурс захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="2a7a9-109">The Remove-AzNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="2a7a9-110">Рекомендуется вызвать Stop-AzNetworkWatcherPacketCapture перед вызовом Remove-AzNetworkWatcherPacketCapture.</span><span class="sxs-lookup"><span data-stu-id="2a7a9-110">It is recommended to call Stop-AzNetworkWatcherPacketCapture before calling Remove-AzNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="2a7a9-111">Если сеанс захвата пакетов выполняется при вызове Remove-AzNetworkWatcherPacketCapture, возможно, захват пакетов не сохранен.</span><span class="sxs-lookup"><span data-stu-id="2a7a9-111">If the packet capture session is running when Remove-AzNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="2a7a9-112">Если сеанс остановлен до удаления файла. Cap, содержащего данные захвата, они не удаляются.</span><span class="sxs-lookup"><span data-stu-id="2a7a9-112">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="2a7a9-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2a7a9-113">EXAMPLES</span></span>

### <span data-ttu-id="2a7a9-114">Пример 1: Удаление сеанса захвата пакетов</span><span class="sxs-lookup"><span data-stu-id="2a7a9-114">Example 1: Remove a packet capture session</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="2a7a9-115">В этом примере мы удалим существующий сеанс захвата пакетов с именем "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="2a7a9-115">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="2a7a9-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2a7a9-116">PARAMETERS</span></span>

### <span data-ttu-id="2a7a9-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a7a9-117">-AsJob</span></span>
<span data-ttu-id="2a7a9-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2a7a9-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2a7a9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a7a9-119">-DefaultProfile</span></span>
<span data-ttu-id="2a7a9-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a7a9-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a7a9-121">-Location</span><span class="sxs-lookup"><span data-stu-id="2a7a9-121">-Location</span></span>
<span data-ttu-id="2a7a9-122">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="2a7a9-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="2a7a9-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2a7a9-123">-NetworkWatcher</span></span>
<span data-ttu-id="2a7a9-124">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="2a7a9-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="2a7a9-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2a7a9-125">-NetworkWatcherName</span></span>
<span data-ttu-id="2a7a9-126">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="2a7a9-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="2a7a9-127">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="2a7a9-127">-PacketCaptureName</span></span>
<span data-ttu-id="2a7a9-128">Имя захвата пакета.</span><span class="sxs-lookup"><span data-stu-id="2a7a9-128">The packet capture name.</span></span>

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

### <span data-ttu-id="2a7a9-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a7a9-129">-PassThru</span></span>
<span data-ttu-id="2a7a9-130">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="2a7a9-130">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="2a7a9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a7a9-131">-ResourceGroupName</span></span>
<span data-ttu-id="2a7a9-132">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="2a7a9-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2a7a9-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a7a9-133">-Confirm</span></span>
<span data-ttu-id="2a7a9-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2a7a9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a7a9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a7a9-135">-WhatIf</span></span>
<span data-ttu-id="2a7a9-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2a7a9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a7a9-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2a7a9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a7a9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a7a9-138">CommonParameters</span></span>
<span data-ttu-id="2a7a9-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2a7a9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a7a9-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a7a9-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a7a9-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2a7a9-141">INPUTS</span></span>

### <span data-ttu-id="2a7a9-142">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2a7a9-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="2a7a9-143">System. String</span><span class="sxs-lookup"><span data-stu-id="2a7a9-143">System.String</span></span>

## <span data-ttu-id="2a7a9-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a7a9-144">OUTPUTS</span></span>

### <span data-ttu-id="2a7a9-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2a7a9-145">System.Boolean</span></span>

## <span data-ttu-id="2a7a9-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="2a7a9-146">NOTES</span></span>
<span data-ttu-id="2a7a9-147">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, пакет, захват, трафик, удаление</span><span class="sxs-lookup"><span data-stu-id="2a7a9-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="2a7a9-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a7a9-148">RELATED LINKS</span></span>

[<span data-ttu-id="2a7a9-149">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2a7a9-149">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="2a7a9-150">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2a7a9-150">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="2a7a9-151">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2a7a9-151">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="2a7a9-152">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2a7a9-152">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="2a7a9-153">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2a7a9-153">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2a7a9-154">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2a7a9-154">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="2a7a9-155">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2a7a9-155">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2a7a9-156">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2a7a9-156">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2a7a9-157">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2a7a9-157">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="2a7a9-158">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2a7a9-158">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2a7a9-159">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2a7a9-159">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2a7a9-160">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2a7a9-160">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2a7a9-161">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2a7a9-161">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="2a7a9-162">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2a7a9-162">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="2a7a9-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="2a7a9-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="2a7a9-164">Остановить-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2a7a9-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2a7a9-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2a7a9-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2a7a9-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2a7a9-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2a7a9-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2a7a9-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="2a7a9-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2a7a9-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2a7a9-169">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2a7a9-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2a7a9-170">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2a7a9-170">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="2a7a9-171">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2a7a9-171">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="2a7a9-172">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="2a7a9-172">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="2a7a9-173">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2a7a9-173">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="2a7a9-174">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="2a7a9-174">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="2a7a9-175">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2a7a9-175">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
