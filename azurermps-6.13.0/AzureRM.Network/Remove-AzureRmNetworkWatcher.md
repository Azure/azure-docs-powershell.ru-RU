---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
ms.openlocfilehash: a242c1cbeda2a110f7bb58e8c320f2e9b4d60ac8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568466"
---
# <span data-ttu-id="2cdc1-101">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2cdc1-101">Remove-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="2cdc1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2cdc1-102">SYNOPSIS</span></span>
<span data-ttu-id="2cdc1-103">Удаление наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="2cdc1-103">Removes a Network Watcher.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cdc1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2cdc1-104">SYNTAX</span></span>

### <span data-ttu-id="2cdc1-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2cdc1-105">SetByResource</span></span>
```
Remove-AzureRmNetworkWatcher -NetworkWatcher <PSNetworkWatcher> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cdc1-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="2cdc1-106">SetByName</span></span>
```
Remove-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cdc1-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="2cdc1-107">SetByLocation</span></span>
```
Remove-AzureRmNetworkWatcher -Location <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cdc1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2cdc1-108">DESCRIPTION</span></span>
<span data-ttu-id="2cdc1-109">Командлет Remove-AzureRmNetworkWatcher удаляет ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="2cdc1-109">The Remove-AzureRmNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="2cdc1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2cdc1-110">EXAMPLES</span></span>

### <span data-ttu-id="2cdc1-111">Пример 1: создание и удаление наблюдателя сети</span><span class="sxs-lookup"><span data-stu-id="2cdc1-111">Example 1: Create and delete a Network Watcher</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="2cdc1-112">В этом примере в группе ресурсов создается наблюдатель сети, а затем немедленно удаляется.</span><span class="sxs-lookup"><span data-stu-id="2cdc1-112">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="2cdc1-113">Обратите внимание, что для каждого региона на каждую подписку может быть создано только один наблюдатель сети.</span><span class="sxs-lookup"><span data-stu-id="2cdc1-113">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="2cdc1-114">Чтобы отключить вывод запроса при удалении виртуальной сети, используйте флаг-force.</span><span class="sxs-lookup"><span data-stu-id="2cdc1-114">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="2cdc1-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2cdc1-115">PARAMETERS</span></span>

### <span data-ttu-id="2cdc1-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2cdc1-116">-AsJob</span></span>
<span data-ttu-id="2cdc1-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2cdc1-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2cdc1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cdc1-118">-DefaultProfile</span></span>
<span data-ttu-id="2cdc1-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2cdc1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cdc1-120">-Location</span><span class="sxs-lookup"><span data-stu-id="2cdc1-120">-Location</span></span>
<span data-ttu-id="2cdc1-121">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="2cdc1-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="2cdc1-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2cdc1-122">-Name</span></span>
<span data-ttu-id="2cdc1-123">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="2cdc1-123">The resource name.</span></span>

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

### <span data-ttu-id="2cdc1-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2cdc1-124">-NetworkWatcher</span></span>
<span data-ttu-id="2cdc1-125">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="2cdc1-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="2cdc1-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2cdc1-126">-PassThru</span></span>
<span data-ttu-id="2cdc1-127">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="2cdc1-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2cdc1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cdc1-128">-ResourceGroupName</span></span>
<span data-ttu-id="2cdc1-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2cdc1-129">The resource group name.</span></span>

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

### <span data-ttu-id="2cdc1-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2cdc1-130">-Confirm</span></span>
<span data-ttu-id="2cdc1-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2cdc1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cdc1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cdc1-132">-WhatIf</span></span>
<span data-ttu-id="2cdc1-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2cdc1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cdc1-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2cdc1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cdc1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cdc1-135">CommonParameters</span></span>
<span data-ttu-id="2cdc1-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2cdc1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cdc1-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cdc1-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cdc1-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2cdc1-138">INPUTS</span></span>

### <span data-ttu-id="2cdc1-139">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2cdc1-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="2cdc1-140">Параметры: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2cdc1-140">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="2cdc1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2cdc1-141">System.String</span></span>
<span data-ttu-id="2cdc1-142">Параметры: Name (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2cdc1-142">Parameters: Name (ByValue)</span></span>

## <span data-ttu-id="2cdc1-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2cdc1-143">OUTPUTS</span></span>

### <span data-ttu-id="2cdc1-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2cdc1-144">System.Boolean</span></span>

## <span data-ttu-id="2cdc1-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="2cdc1-145">NOTES</span></span>
<span data-ttu-id="2cdc1-146">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети</span><span class="sxs-lookup"><span data-stu-id="2cdc1-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="2cdc1-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2cdc1-147">RELATED LINKS</span></span>

[<span data-ttu-id="2cdc1-148">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2cdc1-148">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2cdc1-149">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2cdc1-149">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2cdc1-150">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2cdc1-150">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2cdc1-151">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2cdc1-151">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="2cdc1-152">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2cdc1-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2cdc1-153">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2cdc1-153">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="2cdc1-154">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2cdc1-154">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2cdc1-155">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2cdc1-155">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2cdc1-156">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2cdc1-156">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="2cdc1-157">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2cdc1-157">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2cdc1-158">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2cdc1-158">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2cdc1-159">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2cdc1-159">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2cdc1-160">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2cdc1-160">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="2cdc1-161">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2cdc1-161">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="2cdc1-162">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="2cdc1-162">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="2cdc1-163">Остановить-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2cdc1-163">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2cdc1-164">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2cdc1-164">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2cdc1-165">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2cdc1-165">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2cdc1-166">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2cdc1-166">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="2cdc1-167">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2cdc1-167">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2cdc1-168">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2cdc1-168">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2cdc1-169">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2cdc1-169">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="2cdc1-170">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2cdc1-170">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="2cdc1-171">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="2cdc1-171">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="2cdc1-172">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2cdc1-172">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="2cdc1-173">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="2cdc1-173">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="2cdc1-174">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2cdc1-174">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
