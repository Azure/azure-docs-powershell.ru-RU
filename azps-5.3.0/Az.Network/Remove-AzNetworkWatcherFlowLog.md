---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 9906af7da12f76650ebbe45ff764da78c90ef340
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507786"
---
# <span data-ttu-id="5743c-101">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="5743c-101">Remove-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="5743c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5743c-102">SYNOPSIS</span></span>
<span data-ttu-id="5743c-103">Удаляет указанный ресурс журнала потоков.</span><span class="sxs-lookup"><span data-stu-id="5743c-103">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="5743c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5743c-104">SYNTAX</span></span>

### <span data-ttu-id="5743c-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5743c-105">SetByName (Default)</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5743c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5743c-106">SetByResource</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5743c-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="5743c-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherFlowLog -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5743c-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5743c-108">SetByResourceId</span></span>
```
Remove-AzNetworkWatcherFlowLog -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5743c-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="5743c-109">SetByInputObject</span></span>
```
Remove-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5743c-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5743c-110">DESCRIPTION</span></span>
<span data-ttu-id="5743c-111">Удаляет указанный ресурс журнала потоков.</span><span class="sxs-lookup"><span data-stu-id="5743c-111">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="5743c-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5743c-112">EXAMPLES</span></span>

### <span data-ttu-id="5743c-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5743c-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

## <span data-ttu-id="5743c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5743c-114">PARAMETERS</span></span>

### <span data-ttu-id="5743c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5743c-115">-AsJob</span></span>
<span data-ttu-id="5743c-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5743c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5743c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5743c-117">-DefaultProfile</span></span>
<span data-ttu-id="5743c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5743c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5743c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5743c-119">-InputObject</span></span>
<span data-ttu-id="5743c-120">Объект журнала потоков.</span><span class="sxs-lookup"><span data-stu-id="5743c-120">Flow log object.</span></span>

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

### <span data-ttu-id="5743c-121">-Location</span><span class="sxs-lookup"><span data-stu-id="5743c-121">-Location</span></span>
<span data-ttu-id="5743c-122">Расположение сетевого просмотра.</span><span class="sxs-lookup"><span data-stu-id="5743c-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="5743c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5743c-123">-Name</span></span>
<span data-ttu-id="5743c-124">Имя журнала потоков.</span><span class="sxs-lookup"><span data-stu-id="5743c-124">The flow log name.</span></span>

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

### <span data-ttu-id="5743c-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5743c-125">-NetworkWatcher</span></span>
<span data-ttu-id="5743c-126">Сетевой ресурс для просмотра.</span><span class="sxs-lookup"><span data-stu-id="5743c-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="5743c-127">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="5743c-127">-NetworkWatcherName</span></span>
<span data-ttu-id="5743c-128">Имя сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="5743c-128">The name of network watcher.</span></span>

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

### <span data-ttu-id="5743c-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5743c-129">-PassThru</span></span>
<span data-ttu-id="5743c-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="5743c-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="5743c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5743c-131">-ResourceGroupName</span></span>
<span data-ttu-id="5743c-132">Имя группы ресурсов сетевого watcher.</span><span class="sxs-lookup"><span data-stu-id="5743c-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="5743c-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5743c-133">-ResourceId</span></span>
<span data-ttu-id="5743c-134">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="5743c-134">Resource ID.</span></span>

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

### <span data-ttu-id="5743c-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5743c-135">-Confirm</span></span>
<span data-ttu-id="5743c-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5743c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5743c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5743c-137">-WhatIf</span></span>
<span data-ttu-id="5743c-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5743c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5743c-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5743c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5743c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5743c-140">CommonParameters</span></span>
<span data-ttu-id="5743c-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5743c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5743c-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5743c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5743c-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5743c-143">INPUTS</span></span>

### <span data-ttu-id="5743c-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5743c-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="5743c-145">System.String</span><span class="sxs-lookup"><span data-stu-id="5743c-145">System.String</span></span>

### <span data-ttu-id="5743c-146">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="5743c-146">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="5743c-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5743c-147">OUTPUTS</span></span>

### <span data-ttu-id="5743c-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5743c-148">System.Boolean</span></span>

## <span data-ttu-id="5743c-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5743c-149">NOTES</span></span>

## <span data-ttu-id="5743c-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5743c-150">RELATED LINKS</span></span>

[<span data-ttu-id="5743c-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5743c-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="5743c-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5743c-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="5743c-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5743c-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="5743c-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5743c-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="5743c-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5743c-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="5743c-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5743c-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="5743c-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="5743c-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="5743c-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5743c-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5743c-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5743c-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="5743c-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5743c-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5743c-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5743c-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5743c-162">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5743c-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5743c-163">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="5743c-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="5743c-164">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="5743c-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="5743c-165">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="5743c-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="5743c-166">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5743c-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5743c-167">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5743c-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5743c-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5743c-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5743c-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="5743c-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="5743c-170">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5743c-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5743c-171">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5743c-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5743c-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="5743c-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="5743c-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="5743c-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="5743c-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="5743c-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="5743c-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="5743c-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="5743c-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="5743c-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="5743c-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5743c-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="5743c-178">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="5743c-178">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="5743c-179">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="5743c-179">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="5743c-180">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="5743c-180">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)
