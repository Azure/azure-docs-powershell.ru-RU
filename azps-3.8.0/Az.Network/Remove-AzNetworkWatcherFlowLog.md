---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 8a5f911529a4fc6f1ceb4e242b0e751e5f1a528f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074062"
---
# <span data-ttu-id="9393e-101">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="9393e-101">Remove-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="9393e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9393e-102">SYNOPSIS</span></span>
<span data-ttu-id="9393e-103">Удаляет указанный ресурс журнала потока.</span><span class="sxs-lookup"><span data-stu-id="9393e-103">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="9393e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9393e-104">SYNTAX</span></span>

### <span data-ttu-id="9393e-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9393e-105">SetByName (Default)</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9393e-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9393e-106">SetByResource</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9393e-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="9393e-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherFlowLog -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9393e-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9393e-108">SetByResourceId</span></span>
```
Remove-AzNetworkWatcherFlowLog -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9393e-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="9393e-109">SetByInputObject</span></span>
```
Remove-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9393e-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9393e-110">DESCRIPTION</span></span>
<span data-ttu-id="9393e-111">Удаляет указанный ресурс журнала потока.</span><span class="sxs-lookup"><span data-stu-id="9393e-111">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="9393e-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9393e-112">EXAMPLES</span></span>

### <span data-ttu-id="9393e-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9393e-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

## <span data-ttu-id="9393e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9393e-114">PARAMETERS</span></span>

### <span data-ttu-id="9393e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9393e-115">-AsJob</span></span>
<span data-ttu-id="9393e-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9393e-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9393e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9393e-117">-DefaultProfile</span></span>
<span data-ttu-id="9393e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9393e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9393e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9393e-119">-InputObject</span></span>
<span data-ttu-id="9393e-120">Объект журнала потока.</span><span class="sxs-lookup"><span data-stu-id="9393e-120">Flow log object.</span></span>

```yaml
Type: PSFlowLogResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9393e-121">-Location</span><span class="sxs-lookup"><span data-stu-id="9393e-121">-Location</span></span>
<span data-ttu-id="9393e-122">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="9393e-122">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9393e-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9393e-123">-Name</span></span>
<span data-ttu-id="9393e-124">Имя журнала потока.</span><span class="sxs-lookup"><span data-stu-id="9393e-124">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: FlowLogName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9393e-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9393e-125">-NetworkWatcher</span></span>
<span data-ttu-id="9393e-126">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="9393e-126">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9393e-127">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="9393e-127">-NetworkWatcherName</span></span>
<span data-ttu-id="9393e-128">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="9393e-128">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9393e-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9393e-129">-PassThru</span></span>
<span data-ttu-id="9393e-130">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="9393e-130">{{ Fill PassThru Description }}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9393e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9393e-131">-ResourceGroupName</span></span>
<span data-ttu-id="9393e-132">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="9393e-132">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9393e-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9393e-133">-ResourceId</span></span>
<span data-ttu-id="9393e-134">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="9393e-134">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9393e-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9393e-135">-Confirm</span></span>
<span data-ttu-id="9393e-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9393e-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9393e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9393e-137">-WhatIf</span></span>
<span data-ttu-id="9393e-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9393e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9393e-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9393e-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9393e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9393e-140">CommonParameters</span></span>
<span data-ttu-id="9393e-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9393e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9393e-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9393e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9393e-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9393e-143">INPUTS</span></span>

### <span data-ttu-id="9393e-144">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9393e-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="9393e-145">System. String</span><span class="sxs-lookup"><span data-stu-id="9393e-145">System.String</span></span>

### <span data-ttu-id="9393e-146">Microsoft. Azure. Commands. Network. Models. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="9393e-146">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="9393e-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9393e-147">OUTPUTS</span></span>

### <span data-ttu-id="9393e-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9393e-148">System.Boolean</span></span>

## <span data-ttu-id="9393e-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="9393e-149">NOTES</span></span>

## <span data-ttu-id="9393e-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9393e-150">RELATED LINKS</span></span>

[<span data-ttu-id="9393e-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9393e-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="9393e-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9393e-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="9393e-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9393e-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="9393e-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="9393e-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="9393e-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="9393e-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="9393e-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="9393e-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="9393e-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="9393e-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="9393e-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9393e-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9393e-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="9393e-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="9393e-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9393e-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9393e-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9393e-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9393e-162">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9393e-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9393e-163">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="9393e-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="9393e-164">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="9393e-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="9393e-165">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="9393e-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="9393e-166">Остановить-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9393e-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9393e-167">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9393e-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9393e-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9393e-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9393e-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="9393e-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="9393e-170">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9393e-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9393e-171">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9393e-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9393e-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="9393e-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="9393e-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="9393e-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="9393e-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="9393e-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="9393e-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="9393e-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="9393e-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="9393e-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="9393e-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9393e-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="9393e-178">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="9393e-178">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog)

[<span data-ttu-id="9393e-179">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="9393e-179">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog)

[<span data-ttu-id="9393e-180">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="9393e-180">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)