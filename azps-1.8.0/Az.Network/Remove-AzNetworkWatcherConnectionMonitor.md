---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 71b717ec1777dfd55e29925e82923d8d9f8d7a37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730133"
---
# <span data-ttu-id="3567f-101">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3567f-101">Remove-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="3567f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3567f-102">SYNOPSIS</span></span>
<span data-ttu-id="3567f-103">Удаление монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="3567f-103">Remove connection monitor.</span></span>

## <span data-ttu-id="3567f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3567f-104">SYNTAX</span></span>

### <span data-ttu-id="3567f-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3567f-105">SetByName (Default)</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3567f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3567f-106">SetByResource</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3567f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="3567f-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3567f-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3567f-108">SetByResourceId</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3567f-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="3567f-109">SetByInputObject</span></span>
```
Remove-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3567f-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3567f-110">DESCRIPTION</span></span>
<span data-ttu-id="3567f-111">Командлет Remove-AzNetworkWatcherConnectionMonitor удаляет указанный монитор подключения.</span><span class="sxs-lookup"><span data-stu-id="3567f-111">The remove-AzNetworkWatcherConnectionMonitor cmdlet removes the specified connection monitor.</span></span>

## <span data-ttu-id="3567f-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3567f-112">EXAMPLES</span></span>

### <span data-ttu-id="3567f-113">Пример 1: Удаление указанного монитора подключений</span><span class="sxs-lookup"><span data-stu-id="3567f-113">Example 1: Remove the specified connection monitor</span></span>
```
PS C:\> Remove-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="3567f-114">В этом примере мы удалим монитор подключений, заданный по местоположению и названию.</span><span class="sxs-lookup"><span data-stu-id="3567f-114">In this example we delete the connection monitor specified by location and name.</span></span>

## <span data-ttu-id="3567f-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3567f-115">PARAMETERS</span></span>

### <span data-ttu-id="3567f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3567f-116">-AsJob</span></span>
<span data-ttu-id="3567f-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3567f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3567f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3567f-118">-DefaultProfile</span></span>
<span data-ttu-id="3567f-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3567f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3567f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3567f-120">-InputObject</span></span>
<span data-ttu-id="3567f-121">Объект монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="3567f-121">Connection monitor object.</span></span>

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

### <span data-ttu-id="3567f-122">-Location</span><span class="sxs-lookup"><span data-stu-id="3567f-122">-Location</span></span>
<span data-ttu-id="3567f-123">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="3567f-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="3567f-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3567f-124">-Name</span></span>
<span data-ttu-id="3567f-125">Имя монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="3567f-125">The connection monitor name.</span></span>

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

### <span data-ttu-id="3567f-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3567f-126">-NetworkWatcher</span></span>
<span data-ttu-id="3567f-127">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="3567f-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="3567f-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3567f-128">-NetworkWatcherName</span></span>
<span data-ttu-id="3567f-129">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="3567f-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="3567f-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3567f-130">-PassThru</span></span>
<span data-ttu-id="3567f-131">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="3567f-131">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="3567f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3567f-132">-ResourceGroupName</span></span>
<span data-ttu-id="3567f-133">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="3567f-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="3567f-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3567f-134">-ResourceId</span></span>
<span data-ttu-id="3567f-135">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="3567f-135">Resource ID.</span></span>

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

### <span data-ttu-id="3567f-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3567f-136">-Confirm</span></span>
<span data-ttu-id="3567f-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3567f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3567f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3567f-138">-WhatIf</span></span>
<span data-ttu-id="3567f-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3567f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3567f-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3567f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3567f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3567f-141">CommonParameters</span></span>
<span data-ttu-id="3567f-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3567f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3567f-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3567f-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3567f-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3567f-144">INPUTS</span></span>

### <span data-ttu-id="3567f-145">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3567f-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="3567f-146">System. String</span><span class="sxs-lookup"><span data-stu-id="3567f-146">System.String</span></span>

### <span data-ttu-id="3567f-147">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="3567f-147">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="3567f-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3567f-148">OUTPUTS</span></span>

### <span data-ttu-id="3567f-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3567f-149">System.Boolean</span></span>

## <span data-ttu-id="3567f-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="3567f-150">NOTES</span></span>
<span data-ttu-id="3567f-151">Ключевые слова: Azure, azurerm, ARM, Resource, подключение, управление, диспетчер, сеть, сеть, сетевое наблюдатель, монитор подключений</span><span class="sxs-lookup"><span data-stu-id="3567f-151">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="3567f-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3567f-152">RELATED LINKS</span></span>

[<span data-ttu-id="3567f-153">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3567f-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="3567f-154">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3567f-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="3567f-155">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3567f-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="3567f-156">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="3567f-156">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="3567f-157">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3567f-157">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="3567f-158">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="3567f-158">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="3567f-159">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="3567f-159">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="3567f-160">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3567f-160">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3567f-161">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="3567f-161">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="3567f-162">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3567f-162">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3567f-163">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3567f-163">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3567f-164">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3567f-164">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3567f-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3567f-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3567f-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="3567f-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="3567f-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3567f-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3567f-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3567f-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3567f-169">Остановить-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3567f-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3567f-170">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3567f-170">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3567f-171">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="3567f-171">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="3567f-172">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="3567f-172">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="3567f-173">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="3567f-173">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="3567f-174">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="3567f-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="3567f-175">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3567f-175">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3567f-176">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="3567f-176">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="3567f-177">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="3567f-177">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="3567f-178">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="3567f-178">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="3567f-179">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="3567f-179">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)
