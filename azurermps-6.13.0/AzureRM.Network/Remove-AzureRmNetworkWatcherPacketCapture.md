---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 0c0568dc11411e27af1db9d9e3d59c0026b0a39a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568464"
---
# <span data-ttu-id="29c83-101">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="29c83-101">Remove-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="29c83-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="29c83-102">SYNOPSIS</span></span>
<span data-ttu-id="29c83-103">Удаляет ресурс захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="29c83-103">Removes a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29c83-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="29c83-104">SYNTAX</span></span>

### <span data-ttu-id="29c83-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="29c83-105">SetByResource (Default)</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29c83-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="29c83-106">SetByName</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29c83-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="29c83-107">SetByLocation</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29c83-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="29c83-108">DESCRIPTION</span></span>
<span data-ttu-id="29c83-109">Remove-AzureRmNetworkWatcherPacketCapture удаляет ресурс захвата пакетов.</span><span class="sxs-lookup"><span data-stu-id="29c83-109">The Remove-AzureRmNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="29c83-110">Рекомендуется вызвать Stop-AzureRmNetworkWatcherPacketCapture перед вызовом Remove-AzureRmNetworkWatcherPacketCapture.</span><span class="sxs-lookup"><span data-stu-id="29c83-110">It is recommended to call Stop-AzureRmNetworkWatcherPacketCapture before calling Remove-AzureRmNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="29c83-111">Если сеанс захвата пакетов выполняется при вызове Remove-AzureRmNetworkWatcherPacketCapture, возможно, захват пакетов не сохранен.</span><span class="sxs-lookup"><span data-stu-id="29c83-111">If the packet capture session is running when Remove-AzureRmNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="29c83-112">Если сеанс остановлен до удаления файла. Cap, содержащего данные захвата, они не удаляются.</span><span class="sxs-lookup"><span data-stu-id="29c83-112">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="29c83-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="29c83-113">EXAMPLES</span></span>

### <span data-ttu-id="29c83-114">Пример 1: Удаление сеанса захвата пакетов</span><span class="sxs-lookup"><span data-stu-id="29c83-114">Example 1: Remove a packet capture session</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="29c83-115">В этом примере мы удалим существующий сеанс захвата пакетов с именем "PacketCaptureTest".</span><span class="sxs-lookup"><span data-stu-id="29c83-115">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="29c83-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="29c83-116">PARAMETERS</span></span>

### <span data-ttu-id="29c83-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29c83-117">-AsJob</span></span>
<span data-ttu-id="29c83-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="29c83-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="29c83-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29c83-119">-DefaultProfile</span></span>
<span data-ttu-id="29c83-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="29c83-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29c83-121">-Location</span><span class="sxs-lookup"><span data-stu-id="29c83-121">-Location</span></span>
<span data-ttu-id="29c83-122">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="29c83-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="29c83-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="29c83-123">-NetworkWatcher</span></span>
<span data-ttu-id="29c83-124">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="29c83-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="29c83-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="29c83-125">-NetworkWatcherName</span></span>
<span data-ttu-id="29c83-126">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="29c83-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="29c83-127">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="29c83-127">-PacketCaptureName</span></span>
<span data-ttu-id="29c83-128">Имя захвата пакета.</span><span class="sxs-lookup"><span data-stu-id="29c83-128">The packet capture name.</span></span>

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

### <span data-ttu-id="29c83-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29c83-129">-PassThru</span></span>
<span data-ttu-id="29c83-130">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="29c83-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="29c83-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29c83-131">-ResourceGroupName</span></span>
<span data-ttu-id="29c83-132">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="29c83-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="29c83-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29c83-133">-Confirm</span></span>
<span data-ttu-id="29c83-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="29c83-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29c83-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29c83-135">-WhatIf</span></span>
<span data-ttu-id="29c83-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="29c83-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29c83-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="29c83-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29c83-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29c83-138">CommonParameters</span></span>
<span data-ttu-id="29c83-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="29c83-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29c83-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29c83-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29c83-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="29c83-141">INPUTS</span></span>

### <span data-ttu-id="29c83-142">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="29c83-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="29c83-143">Параметры: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="29c83-143">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="29c83-144">System. String</span><span class="sxs-lookup"><span data-stu-id="29c83-144">System.String</span></span>
<span data-ttu-id="29c83-145">Параметры: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="29c83-145">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="29c83-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="29c83-146">OUTPUTS</span></span>

### <span data-ttu-id="29c83-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="29c83-147">System.Boolean</span></span>

## <span data-ttu-id="29c83-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="29c83-148">NOTES</span></span>
<span data-ttu-id="29c83-149">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, пакет, захват, трафик, удаление</span><span class="sxs-lookup"><span data-stu-id="29c83-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="29c83-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="29c83-150">RELATED LINKS</span></span>

[<span data-ttu-id="29c83-151">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="29c83-151">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="29c83-152">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="29c83-152">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="29c83-153">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="29c83-153">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="29c83-154">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="29c83-154">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="29c83-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="29c83-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="29c83-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="29c83-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="29c83-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="29c83-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="29c83-158">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="29c83-158">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="29c83-159">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="29c83-159">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="29c83-160">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="29c83-160">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="29c83-161">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="29c83-161">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="29c83-162">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="29c83-162">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="29c83-163">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="29c83-163">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="29c83-164">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="29c83-164">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="29c83-165">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="29c83-165">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="29c83-166">Остановить-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29c83-166">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="29c83-167">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29c83-167">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="29c83-168">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29c83-168">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="29c83-169">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="29c83-169">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="29c83-170">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29c83-170">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="29c83-171">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29c83-171">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="29c83-172">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="29c83-172">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="29c83-173">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="29c83-173">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="29c83-174">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="29c83-174">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="29c83-175">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="29c83-175">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="29c83-176">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="29c83-176">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="29c83-177">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29c83-177">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
