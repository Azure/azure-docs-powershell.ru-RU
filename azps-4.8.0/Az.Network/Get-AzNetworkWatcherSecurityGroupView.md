---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: ec1b53799b92f0a68c20110dfe78f9af7b8391c2
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100410418"
---
# <span data-ttu-id="61d4c-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="61d4c-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="61d4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61d4c-102">SYNOPSIS</span></span>
<span data-ttu-id="61d4c-103">Просмотреть настроенные и эффективные правила группы безопасности сети, применяемые на VM-</span><span class="sxs-lookup"><span data-stu-id="61d4c-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="61d4c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="61d4c-104">SYNTAX</span></span>

### <span data-ttu-id="61d4c-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="61d4c-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61d4c-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="61d4c-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61d4c-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="61d4c-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61d4c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61d4c-108">DESCRIPTION</span></span>
<span data-ttu-id="61d4c-109">Этот Get-AzNetworkWatcherSecurityGroupView позволяет просматривать настроенные и эффективные правила группы безопасности сети, примененные на VM-проекте.</span><span class="sxs-lookup"><span data-stu-id="61d4c-109">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="61d4c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="61d4c-110">EXAMPLES</span></span>

### <span data-ttu-id="61d4c-111">Пример 1. Вызов представления группы безопасности на VM</span><span class="sxs-lookup"><span data-stu-id="61d4c-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="61d4c-112">В примере выше мы сначала получаем региональный сетевой watcher, а затем VM в этом регионе.</span><span class="sxs-lookup"><span data-stu-id="61d4c-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="61d4c-113">Затем мы звоним в представление группы безопасности с указанной VM-камерой.</span><span class="sxs-lookup"><span data-stu-id="61d4c-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="61d4c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61d4c-114">PARAMETERS</span></span>

### <span data-ttu-id="61d4c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61d4c-115">-AsJob</span></span>
<span data-ttu-id="61d4c-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="61d4c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="61d4c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61d4c-117">-DefaultProfile</span></span>
<span data-ttu-id="61d4c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="61d4c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61d4c-119">-Location</span><span class="sxs-lookup"><span data-stu-id="61d4c-119">-Location</span></span>
<span data-ttu-id="61d4c-120">Расположение сетевого просмотра.</span><span class="sxs-lookup"><span data-stu-id="61d4c-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="61d4c-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="61d4c-121">-NetworkWatcher</span></span>
<span data-ttu-id="61d4c-122">Сетевой ресурс для просмотра.</span><span class="sxs-lookup"><span data-stu-id="61d4c-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="61d4c-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="61d4c-123">-NetworkWatcherName</span></span>
<span data-ttu-id="61d4c-124">Имя сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="61d4c-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="61d4c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61d4c-125">-ResourceGroupName</span></span>
<span data-ttu-id="61d4c-126">Имя группы ресурсов сетевого watcher.</span><span class="sxs-lookup"><span data-stu-id="61d4c-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="61d4c-127">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="61d4c-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="61d4c-128">Целевой ИД VM</span><span class="sxs-lookup"><span data-stu-id="61d4c-128">The target VM Id</span></span>

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

### <span data-ttu-id="61d4c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61d4c-129">CommonParameters</span></span>
<span data-ttu-id="61d4c-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61d4c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61d4c-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61d4c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61d4c-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61d4c-132">INPUTS</span></span>

### <span data-ttu-id="61d4c-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="61d4c-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="61d4c-134">System.String</span><span class="sxs-lookup"><span data-stu-id="61d4c-134">System.String</span></span>

## <span data-ttu-id="61d4c-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="61d4c-135">OUTPUTS</span></span>

### <span data-ttu-id="61d4c-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span><span class="sxs-lookup"><span data-stu-id="61d4c-136">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="61d4c-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="61d4c-137">NOTES</span></span>
<span data-ttu-id="61d4c-138">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span><span class="sxs-lookup"><span data-stu-id="61d4c-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="61d4c-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61d4c-139">RELATED LINKS</span></span>

[<span data-ttu-id="61d4c-140">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="61d4c-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="61d4c-141">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="61d4c-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="61d4c-142">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="61d4c-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="61d4c-143">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="61d4c-143">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="61d4c-144">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="61d4c-144">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="61d4c-145">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="61d4c-145">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="61d4c-146">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="61d4c-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="61d4c-147">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="61d4c-147">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="61d4c-148">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="61d4c-148">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="61d4c-149">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="61d4c-149">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="61d4c-150">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="61d4c-150">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="61d4c-151">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="61d4c-151">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="61d4c-152">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="61d4c-152">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="61d4c-153">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="61d4c-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="61d4c-154">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="61d4c-154">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="61d4c-155">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="61d4c-155">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="61d4c-156">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="61d4c-156">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="61d4c-157">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="61d4c-157">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="61d4c-158">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="61d4c-158">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="61d4c-159">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="61d4c-159">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="61d4c-160">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="61d4c-160">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="61d4c-161">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="61d4c-161">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="61d4c-162">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="61d4c-162">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="61d4c-163">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="61d4c-163">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="61d4c-164">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="61d4c-164">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="61d4c-165">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="61d4c-165">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="61d4c-166">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="61d4c-166">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
