---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 1a28b061b10dc28fd5ecc0fe20cd817d7d1699b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729937"
---
# <span data-ttu-id="89cbb-101">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="89cbb-101">Stop-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="89cbb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="89cbb-102">SYNOPSIS</span></span>
<span data-ttu-id="89cbb-103">Остановка сеанса сбора запущенных пакетов</span><span class="sxs-lookup"><span data-stu-id="89cbb-103">Stops a running packet capture session</span></span>

## <span data-ttu-id="89cbb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="89cbb-104">SYNTAX</span></span>

### <span data-ttu-id="89cbb-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="89cbb-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89cbb-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="89cbb-106">SetByName</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89cbb-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="89cbb-107">SetByLocation</span></span>
```
Stop-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89cbb-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89cbb-108">DESCRIPTION</span></span>
<span data-ttu-id="89cbb-109">Stop-AzNetworkWatcherPacketCapture останавливает выполнение сеанса захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="89cbb-109">The Stop-AzNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="89cbb-110">После остановки сеанса файл записи пакетов загружается в хранилище и (или) локально хранится на виртуальной машине в зависимости от ее конфигурации.</span><span class="sxs-lookup"><span data-stu-id="89cbb-110">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="89cbb-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="89cbb-111">EXAMPLES</span></span>

### <span data-ttu-id="89cbb-112">Пример 1: остановка сеанса захвата пакетов</span><span class="sxs-lookup"><span data-stu-id="89cbb-112">Example 1: Stop a packet capture session</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="89cbb-113">В этом примере мы прерывать сеанс захвата запущенных пакетов с именем "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="89cbb-113">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="89cbb-114">После остановки сеанса файл записи пакетов загружается в хранилище и (или) локально хранится на виртуальной машине в зависимости от ее конфигурации.</span><span class="sxs-lookup"><span data-stu-id="89cbb-114">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="89cbb-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="89cbb-115">PARAMETERS</span></span>

### <span data-ttu-id="89cbb-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89cbb-116">-AsJob</span></span>
<span data-ttu-id="89cbb-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="89cbb-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="89cbb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89cbb-118">-DefaultProfile</span></span>
<span data-ttu-id="89cbb-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="89cbb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89cbb-120">-Location</span><span class="sxs-lookup"><span data-stu-id="89cbb-120">-Location</span></span>
<span data-ttu-id="89cbb-121">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="89cbb-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="89cbb-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="89cbb-122">-NetworkWatcher</span></span>
<span data-ttu-id="89cbb-123">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="89cbb-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="89cbb-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="89cbb-124">-NetworkWatcherName</span></span>
<span data-ttu-id="89cbb-125">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="89cbb-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="89cbb-126">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="89cbb-126">-PacketCaptureName</span></span>
<span data-ttu-id="89cbb-127">Имя захвата пакета.</span><span class="sxs-lookup"><span data-stu-id="89cbb-127">The packet capture name.</span></span>

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

### <span data-ttu-id="89cbb-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89cbb-128">-PassThru</span></span>
<span data-ttu-id="89cbb-129">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="89cbb-129">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="89cbb-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89cbb-130">-ResourceGroupName</span></span>
<span data-ttu-id="89cbb-131">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="89cbb-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="89cbb-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89cbb-132">-Confirm</span></span>
<span data-ttu-id="89cbb-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="89cbb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89cbb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89cbb-134">-WhatIf</span></span>
<span data-ttu-id="89cbb-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="89cbb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89cbb-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="89cbb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89cbb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89cbb-137">CommonParameters</span></span>
<span data-ttu-id="89cbb-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="89cbb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89cbb-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89cbb-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89cbb-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="89cbb-140">INPUTS</span></span>

### <span data-ttu-id="89cbb-141">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="89cbb-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="89cbb-142">System. String</span><span class="sxs-lookup"><span data-stu-id="89cbb-142">System.String</span></span>

## <span data-ttu-id="89cbb-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="89cbb-143">OUTPUTS</span></span>

### <span data-ttu-id="89cbb-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="89cbb-144">System.Boolean</span></span>

## <span data-ttu-id="89cbb-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="89cbb-145">NOTES</span></span>
<span data-ttu-id="89cbb-146">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, пакет, захват, трафик</span><span class="sxs-lookup"><span data-stu-id="89cbb-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="89cbb-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89cbb-147">RELATED LINKS</span></span>

[<span data-ttu-id="89cbb-148">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="89cbb-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="89cbb-149">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="89cbb-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="89cbb-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="89cbb-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="89cbb-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="89cbb-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="89cbb-152">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="89cbb-152">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="89cbb-153">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="89cbb-153">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="89cbb-154">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="89cbb-154">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="89cbb-155">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="89cbb-155">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="89cbb-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="89cbb-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="89cbb-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="89cbb-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="89cbb-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="89cbb-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="89cbb-159">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="89cbb-159">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="89cbb-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="89cbb-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="89cbb-161">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="89cbb-161">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="89cbb-162">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="89cbb-162">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="89cbb-163">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="89cbb-163">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="89cbb-164">Остановить-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="89cbb-164">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="89cbb-165">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="89cbb-165">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="89cbb-166">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="89cbb-166">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="89cbb-167">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="89cbb-167">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="89cbb-168">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="89cbb-168">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="89cbb-169">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="89cbb-169">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="89cbb-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="89cbb-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="89cbb-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="89cbb-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="89cbb-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="89cbb-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="89cbb-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="89cbb-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="89cbb-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="89cbb-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
