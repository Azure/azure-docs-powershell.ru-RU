---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: cce361870f6dc65f644264e52b331c209177668f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234921"
---
# <span data-ttu-id="78d0e-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="78d0e-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="78d0e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="78d0e-102">SYNOPSIS</span></span>
<span data-ttu-id="78d0e-103">Удаление наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="78d0e-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="78d0e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="78d0e-104">SYNTAX</span></span>

### <span data-ttu-id="78d0e-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="78d0e-105">SetByResource</span></span>
```
Remove-AzNetworkWatcher -NetworkWatcher <PSNetworkWatcher> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78d0e-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="78d0e-106">SetByName</span></span>
```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78d0e-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="78d0e-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcher -Location <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78d0e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78d0e-108">DESCRIPTION</span></span>
<span data-ttu-id="78d0e-109">Командлет Remove-AzNetworkWatcher удаляет ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="78d0e-109">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="78d0e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="78d0e-110">EXAMPLES</span></span>

### <span data-ttu-id="78d0e-111">Пример 1: создание и удаление наблюдателя сети</span><span class="sxs-lookup"><span data-stu-id="78d0e-111">Example 1: Create and delete a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="78d0e-112">В этом примере в группе ресурсов создается наблюдатель сети, а затем немедленно удаляется.</span><span class="sxs-lookup"><span data-stu-id="78d0e-112">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="78d0e-113">Обратите внимание, что для каждого региона на каждую подписку может быть создано только один наблюдатель сети.</span><span class="sxs-lookup"><span data-stu-id="78d0e-113">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="78d0e-114">Чтобы отключить вывод запроса при удалении виртуальной сети, используйте флаг-force.</span><span class="sxs-lookup"><span data-stu-id="78d0e-114">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="78d0e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="78d0e-115">PARAMETERS</span></span>

### <span data-ttu-id="78d0e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78d0e-116">-AsJob</span></span>
<span data-ttu-id="78d0e-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="78d0e-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="78d0e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78d0e-118">-DefaultProfile</span></span>
<span data-ttu-id="78d0e-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="78d0e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78d0e-120">-Location</span><span class="sxs-lookup"><span data-stu-id="78d0e-120">-Location</span></span>
<span data-ttu-id="78d0e-121">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="78d0e-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="78d0e-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="78d0e-122">-Name</span></span>
<span data-ttu-id="78d0e-123">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="78d0e-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78d0e-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="78d0e-124">-NetworkWatcher</span></span>
<span data-ttu-id="78d0e-125">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="78d0e-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="78d0e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78d0e-126">-PassThru</span></span>
<span data-ttu-id="78d0e-127">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="78d0e-127">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="78d0e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78d0e-128">-ResourceGroupName</span></span>
<span data-ttu-id="78d0e-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="78d0e-129">The resource group name.</span></span>

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

### <span data-ttu-id="78d0e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78d0e-130">-Confirm</span></span>
<span data-ttu-id="78d0e-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="78d0e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78d0e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78d0e-132">-WhatIf</span></span>
<span data-ttu-id="78d0e-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="78d0e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78d0e-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="78d0e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78d0e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78d0e-135">CommonParameters</span></span>
<span data-ttu-id="78d0e-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="78d0e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78d0e-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78d0e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78d0e-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="78d0e-138">INPUTS</span></span>

### <span data-ttu-id="78d0e-139">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="78d0e-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="78d0e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="78d0e-140">System.String</span></span>

## <span data-ttu-id="78d0e-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="78d0e-141">OUTPUTS</span></span>

### <span data-ttu-id="78d0e-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="78d0e-142">System.Boolean</span></span>

## <span data-ttu-id="78d0e-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="78d0e-143">NOTES</span></span>
<span data-ttu-id="78d0e-144">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети</span><span class="sxs-lookup"><span data-stu-id="78d0e-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="78d0e-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78d0e-145">RELATED LINKS</span></span>

[<span data-ttu-id="78d0e-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="78d0e-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="78d0e-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="78d0e-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="78d0e-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="78d0e-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="78d0e-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="78d0e-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="78d0e-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="78d0e-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="78d0e-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="78d0e-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="78d0e-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="78d0e-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="78d0e-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="78d0e-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="78d0e-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="78d0e-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="78d0e-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="78d0e-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="78d0e-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="78d0e-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="78d0e-157">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="78d0e-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="78d0e-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="78d0e-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="78d0e-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="78d0e-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="78d0e-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="78d0e-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="78d0e-161">Остановить-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="78d0e-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="78d0e-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="78d0e-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="78d0e-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="78d0e-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="78d0e-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="78d0e-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="78d0e-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="78d0e-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="78d0e-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="78d0e-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="78d0e-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="78d0e-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="78d0e-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="78d0e-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="78d0e-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="78d0e-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="78d0e-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="78d0e-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="78d0e-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="78d0e-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="78d0e-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="78d0e-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
