---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 83d7da65ad8c525d4c37ab1b5f78eb72bf1d9f49
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519868"
---
# <span data-ttu-id="d61d0-101">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d61d0-101">Start-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="d61d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d61d0-102">SYNOPSIS</span></span>
<span data-ttu-id="d61d0-103">Запуск монитора подключения</span><span class="sxs-lookup"><span data-stu-id="d61d0-103">Start a connection monitor</span></span>

## <span data-ttu-id="d61d0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d61d0-104">SYNTAX</span></span>

### <span data-ttu-id="d61d0-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d61d0-105">SetByName (Default)</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d61d0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d61d0-106">SetByResource</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d61d0-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d61d0-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d61d0-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d61d0-108">SetByResourceId</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d61d0-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="d61d0-109">SetByInputObject</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d61d0-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d61d0-110">DESCRIPTION</span></span>
<span data-ttu-id="d61d0-111">С Start-AzNetworkWatcherConnectionMonitor запускается указанный монитор подключения.</span><span class="sxs-lookup"><span data-stu-id="d61d0-111">The Start-AzNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="d61d0-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d61d0-112">EXAMPLES</span></span>

### <span data-ttu-id="d61d0-113">Пример 1. Запуск монитора подключения</span><span class="sxs-lookup"><span data-stu-id="d61d0-113">Example 1: Start a connection monitor</span></span>
```
PS C:\> Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="d61d0-114">В этом примере мы запускаем монитор подключения, заданный именем и сетевым контролем</span><span class="sxs-lookup"><span data-stu-id="d61d0-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="d61d0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d61d0-115">PARAMETERS</span></span>

### <span data-ttu-id="d61d0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d61d0-116">-AsJob</span></span>
<span data-ttu-id="d61d0-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d61d0-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d61d0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d61d0-118">-DefaultProfile</span></span>
<span data-ttu-id="d61d0-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d61d0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d61d0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d61d0-120">-InputObject</span></span>
<span data-ttu-id="d61d0-121">Объект монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="d61d0-121">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d61d0-122">-Location</span><span class="sxs-lookup"><span data-stu-id="d61d0-122">-Location</span></span>
<span data-ttu-id="d61d0-123">Расположение сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="d61d0-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d61d0-124">-Name</span><span class="sxs-lookup"><span data-stu-id="d61d0-124">-Name</span></span>
<span data-ttu-id="d61d0-125">Имя монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="d61d0-125">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d61d0-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d61d0-126">-NetworkWatcher</span></span>
<span data-ttu-id="d61d0-127">Сетевой ресурс для просмотра.</span><span class="sxs-lookup"><span data-stu-id="d61d0-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="d61d0-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d61d0-128">-NetworkWatcherName</span></span>
<span data-ttu-id="d61d0-129">Имя сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="d61d0-129">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d61d0-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d61d0-130">-PassThru</span></span>
<span data-ttu-id="d61d0-131">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="d61d0-131">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="d61d0-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d61d0-132">-ResourceGroupName</span></span>
<span data-ttu-id="d61d0-133">Имя группы ресурсов сетевого watcher.</span><span class="sxs-lookup"><span data-stu-id="d61d0-133">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d61d0-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d61d0-134">-ResourceId</span></span>
<span data-ttu-id="d61d0-135">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="d61d0-135">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d61d0-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d61d0-136">-Confirm</span></span>
<span data-ttu-id="d61d0-137">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d61d0-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d61d0-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d61d0-138">-WhatIf</span></span>
<span data-ttu-id="d61d0-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d61d0-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d61d0-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d61d0-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d61d0-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d61d0-141">CommonParameters</span></span>
<span data-ttu-id="d61d0-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d61d0-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d61d0-143">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d61d0-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d61d0-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d61d0-144">INPUTS</span></span>

### <span data-ttu-id="d61d0-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d61d0-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="d61d0-146">System.String</span><span class="sxs-lookup"><span data-stu-id="d61d0-146">System.String</span></span>

### <span data-ttu-id="d61d0-147">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="d61d0-147">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="d61d0-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d61d0-148">OUTPUTS</span></span>

### <span data-ttu-id="d61d0-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d61d0-149">System.Boolean</span></span>

## <span data-ttu-id="d61d0-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d61d0-150">NOTES</span></span>
<span data-ttu-id="d61d0-151">Ключевые слова: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, network watcher, connection monitor</span><span class="sxs-lookup"><span data-stu-id="d61d0-151">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="d61d0-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d61d0-152">RELATED LINKS</span></span>

[<span data-ttu-id="d61d0-153">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d61d0-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d61d0-154">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d61d0-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d61d0-155">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d61d0-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d61d0-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d61d0-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d61d0-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d61d0-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d61d0-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d61d0-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d61d0-159">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d61d0-159">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="d61d0-160">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d61d0-160">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d61d0-161">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d61d0-161">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d61d0-162">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d61d0-162">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d61d0-163">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d61d0-163">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d61d0-164">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d61d0-164">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d61d0-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d61d0-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d61d0-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d61d0-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="d61d0-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d61d0-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d61d0-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d61d0-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d61d0-169">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d61d0-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d61d0-170">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d61d0-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d61d0-171">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d61d0-171">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="d61d0-172">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d61d0-172">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d61d0-173">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d61d0-173">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="d61d0-174">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d61d0-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d61d0-175">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d61d0-175">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d61d0-176">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d61d0-176">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="d61d0-177">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d61d0-177">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="d61d0-178">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d61d0-178">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="d61d0-179">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d61d0-179">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
