---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 37da72dd26df32dddee0ea28d2378418e9e4922e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249959"
---
# <span data-ttu-id="dc3c6-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="dc3c6-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="dc3c6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc3c6-102">SYNOPSIS</span></span>
<span data-ttu-id="dc3c6-103">Просмотр настроенных и эффективных правил сетевой группы безопасности, примененных к виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="dc3c6-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="dc3c6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc3c6-104">SYNTAX</span></span>

### <span data-ttu-id="dc3c6-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dc3c6-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc3c6-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="dc3c6-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc3c6-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="dc3c6-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc3c6-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc3c6-108">DESCRIPTION</span></span>
<span data-ttu-id="dc3c6-109">Get-AzNetworkWatcherSecurityGroupView позволяет просматривать настроенные и эффективные правила групп безопасности сети, примененные к ВМ.</span><span class="sxs-lookup"><span data-stu-id="dc3c6-109">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="dc3c6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc3c6-110">EXAMPLES</span></span>

### <span data-ttu-id="dc3c6-111">Пример 1: вызов представления группы безопасности на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="dc3c6-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="dc3c6-112">В приведенном выше примере сначала нужно получить доступ к региональному наблюдатель сети, а затем виртуальной машине в регионе.</span><span class="sxs-lookup"><span data-stu-id="dc3c6-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="dc3c6-113">Затем мы создаем на выбранной виртуальной машине вызов представления группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="dc3c6-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="dc3c6-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc3c6-114">PARAMETERS</span></span>

### <span data-ttu-id="dc3c6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc3c6-115">-AsJob</span></span>
<span data-ttu-id="dc3c6-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="dc3c6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dc3c6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc3c6-117">-DefaultProfile</span></span>
<span data-ttu-id="dc3c6-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc3c6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc3c6-119">-Location</span><span class="sxs-lookup"><span data-stu-id="dc3c6-119">-Location</span></span>
<span data-ttu-id="dc3c6-120">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="dc3c6-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="dc3c6-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dc3c6-121">-NetworkWatcher</span></span>
<span data-ttu-id="dc3c6-122">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="dc3c6-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="dc3c6-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="dc3c6-123">-NetworkWatcherName</span></span>
<span data-ttu-id="dc3c6-124">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="dc3c6-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="dc3c6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc3c6-125">-ResourceGroupName</span></span>
<span data-ttu-id="dc3c6-126">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="dc3c6-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="dc3c6-127">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="dc3c6-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="dc3c6-128">Идентификатор целевой виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="dc3c6-128">The target VM Id</span></span>

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

### <span data-ttu-id="dc3c6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc3c6-129">CommonParameters</span></span>
<span data-ttu-id="dc3c6-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dc3c6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc3c6-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc3c6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc3c6-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dc3c6-132">INPUTS</span></span>

### <span data-ttu-id="dc3c6-133">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dc3c6-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="dc3c6-134">System. String</span><span class="sxs-lookup"><span data-stu-id="dc3c6-134">System.String</span></span>

## <span data-ttu-id="dc3c6-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc3c6-135">OUTPUTS</span></span>

### <span data-ttu-id="dc3c6-136">Microsoft. Azure. Commands. Network. Models. PSSecurityGroupViewResult</span><span class="sxs-lookup"><span data-stu-id="dc3c6-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="dc3c6-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc3c6-137">NOTES</span></span>
<span data-ttu-id="dc3c6-138">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, поток, IP</span><span class="sxs-lookup"><span data-stu-id="dc3c6-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="dc3c6-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc3c6-139">RELATED LINKS</span></span>

[<span data-ttu-id="dc3c6-140">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dc3c6-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="dc3c6-141">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dc3c6-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="dc3c6-142">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="dc3c6-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="dc3c6-143">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="dc3c6-143">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="dc3c6-144">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="dc3c6-144">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="dc3c6-145">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="dc3c6-145">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="dc3c6-146">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="dc3c6-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="dc3c6-147">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dc3c6-147">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dc3c6-148">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="dc3c6-148">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="dc3c6-149">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dc3c6-149">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dc3c6-150">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dc3c6-150">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dc3c6-151">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="dc3c6-151">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="dc3c6-152">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc3c6-152">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="dc3c6-153">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="dc3c6-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="dc3c6-154">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="dc3c6-154">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="dc3c6-155">Остановить-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dc3c6-155">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dc3c6-156">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dc3c6-156">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dc3c6-157">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dc3c6-157">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dc3c6-158">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="dc3c6-158">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="dc3c6-159">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dc3c6-159">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dc3c6-160">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dc3c6-160">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="dc3c6-161">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="dc3c6-161">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="dc3c6-162">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="dc3c6-162">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="dc3c6-163">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="dc3c6-163">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="dc3c6-164">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="dc3c6-164">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="dc3c6-165">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="dc3c6-165">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="dc3c6-166">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="dc3c6-166">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)