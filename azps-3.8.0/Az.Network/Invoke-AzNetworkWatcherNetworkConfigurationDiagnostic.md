---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/invoke-aznetworkwatchernetworkconfigurationdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic.md
ms.openlocfilehash: 8e1215adc9b6f6ab72d752fd58771f5155a8bc25
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074852"
---
# <span data-ttu-id="9ed14-101">Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="9ed14-101">Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic</span></span>

## <span data-ttu-id="9ed14-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9ed14-102">SYNOPSIS</span></span>
<span data-ttu-id="9ed14-103">Вызов диагностического сеанса конфигурации сети для указанных профилей сети в целевом ресурсе.</span><span class="sxs-lookup"><span data-stu-id="9ed14-103">Invoke network configuration diagnostic session for specified network profiles on target resource.</span></span>

## <span data-ttu-id="9ed14-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9ed14-104">SYNTAX</span></span>

### <span data-ttu-id="9ed14-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9ed14-105">SetByResource (Default)</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ed14-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="9ed14-106">SetByName</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ed14-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="9ed14-107">SetByLocation</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -Location <String> -TargetResourceId <String>
 [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ed14-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9ed14-108">SetByResourceId</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -ResourceId <String> -TargetResourceId <String>
 [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ed14-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ed14-109">DESCRIPTION</span></span>
<span data-ttu-id="9ed14-110">Командлет Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic вызов диагностического сеанса конфигурации сети для указанных сетевых профилей на целевом ресурсе.</span><span class="sxs-lookup"><span data-stu-id="9ed14-110">The Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic cmdlet invoke network configuration diagnostic session for specified network profiles on target resource.</span></span>

## <span data-ttu-id="9ed14-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9ed14-111">EXAMPLES</span></span>

### <span data-ttu-id="9ed14-112">Пример 1: вызов диагностического сеанса диагностики конфигурации сети для виртуальной машины и указанного сетевого профиля</span><span class="sxs-lookup"><span data-stu-id="9ed14-112">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
```
PS C:\> $profile = New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction Inbound -Protocol Tcp -Source 10.1.1.4 -Destination * -DestinationPort 50
PS C:\> Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -Location eastus -TargetResourceId /subscriptions/61cc8a98-a8be-4bfe-a04e-0b461f93fe35/resourceGroups/NwRgEastUS/providers/Microsoft.Compute/virtualMachines/vm1 -Profile $profile

Results : [
            {
              "Profile": {
                "Direction": "Inbound",
                "Protocol": "Tcp",
                "Source": "10.1.1.4",
                "Destination": "*",
                "DestinationPort": "50"
              },
              "NetworkSecurityGroupResult": {
                "SecurityRuleAccessResult": "Allow",
                "EvaluatedNetworkSecurityGroups": [
                  {
                    "NetworkSecurityGroupId": "/subscriptions/61cc8a98-a8be-4bfe-a04e-0b461f93fe35/resourceGroups/clean
          upservice/providers/Microsoft.Network/networkSecurityGroups/rg-cleanupservice-nsg1",
                    "MatchedRule": {
                      "RuleName": "UserRule_Cleanuptool-Allow-4001",
                      "Action": "Allow"
                    },
                    "RulesEvaluationResult": [
                      {
                        "Name": "UserRule_Cleanuptool-Allow-100",
                        "ProtocolMatched": true,
                        "SourceMatched": false,
                        "SourcePortMatched": true,
                        "DestinationMatched": true,
                        "DestinationPortMatched": false
                      },
```

## <span data-ttu-id="9ed14-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9ed14-113">PARAMETERS</span></span>

### <span data-ttu-id="9ed14-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ed14-114">-AsJob</span></span>
<span data-ttu-id="9ed14-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9ed14-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ed14-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ed14-116">-DefaultProfile</span></span>
<span data-ttu-id="9ed14-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9ed14-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ed14-118">-Location</span><span class="sxs-lookup"><span data-stu-id="9ed14-118">-Location</span></span>
<span data-ttu-id="9ed14-119">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="9ed14-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="9ed14-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9ed14-120">-NetworkWatcher</span></span>
<span data-ttu-id="9ed14-121">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="9ed14-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="9ed14-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="9ed14-122">-NetworkWatcherName</span></span>
<span data-ttu-id="9ed14-123">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="9ed14-123">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ed14-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="9ed14-124">-Profile</span></span>
<span data-ttu-id="9ed14-125">Список профилей диагностики конфигурации сети.</span><span class="sxs-lookup"><span data-stu-id="9ed14-125">List of network configuration diagnostic profiles.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ed14-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ed14-126">-ResourceGroupName</span></span>
<span data-ttu-id="9ed14-127">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="9ed14-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="9ed14-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ed14-128">-ResourceId</span></span>
<span data-ttu-id="9ed14-129">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="9ed14-129">Resource ID.</span></span>

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

### <span data-ttu-id="9ed14-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="9ed14-130">-TargetResourceId</span></span>
<span data-ttu-id="9ed14-131">Идентификатор целевого ресурса, для которого нужно выполнить диагностику сетевой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="9ed14-131">The ID of the target resource to perform network configuration diagnostic.</span></span>
<span data-ttu-id="9ed14-132">Допустимые параметры: VM, NetworkInterface, VMSS/NetworkInterface и Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="9ed14-132">Valid options are VM, NetworkInterface, VMSS/NetworkInterface and Application Gateway.</span></span>

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

### <span data-ttu-id="9ed14-133">-VerbosityLevel</span><span class="sxs-lookup"><span data-stu-id="9ed14-133">-VerbosityLevel</span></span>
<span data-ttu-id="9ed14-134">Уровень детализации.</span><span class="sxs-lookup"><span data-stu-id="9ed14-134">Verbosity level.</span></span>
<span data-ttu-id="9ed14-135">Допустимые значения: "обычный", "минимум", "полный".</span><span class="sxs-lookup"><span data-stu-id="9ed14-135">Accepted values are 'Normal', 'Minimum', 'Full'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ed14-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ed14-136">CommonParameters</span></span>
<span data-ttu-id="9ed14-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9ed14-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ed14-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ed14-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ed14-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9ed14-139">INPUTS</span></span>

### <span data-ttu-id="9ed14-140">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9ed14-140">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="9ed14-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9ed14-141">System.String</span></span>

## <span data-ttu-id="9ed14-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ed14-142">OUTPUTS</span></span>

### <span data-ttu-id="9ed14-143">Microsoft. Azure. Commands. Network. Models. PSNetworkConfigurationDiagnosticResponse</span><span class="sxs-lookup"><span data-stu-id="9ed14-143">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticResponse</span></span>

## <span data-ttu-id="9ed14-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="9ed14-144">NOTES</span></span>
<span data-ttu-id="9ed14-145">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель, диагностика, профиль</span><span class="sxs-lookup"><span data-stu-id="9ed14-145">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="9ed14-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ed14-146">RELATED LINKS</span></span>

[<span data-ttu-id="9ed14-147">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9ed14-147">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="9ed14-148">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9ed14-148">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="9ed14-149">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9ed14-149">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="9ed14-150">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="9ed14-150">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="9ed14-151">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="9ed14-151">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="9ed14-152">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="9ed14-152">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="9ed14-153">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="9ed14-153">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="9ed14-154">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9ed14-154">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9ed14-155">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="9ed14-155">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="9ed14-156">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9ed14-156">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9ed14-157">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9ed14-157">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9ed14-158">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9ed14-158">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9ed14-159">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="9ed14-159">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="9ed14-160">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="9ed14-160">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="9ed14-161">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="9ed14-161">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="9ed14-162">Остановить-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9ed14-162">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9ed14-163">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9ed14-163">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9ed14-164">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9ed14-164">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9ed14-165">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="9ed14-165">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="9ed14-166">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9ed14-166">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9ed14-167">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9ed14-167">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9ed14-168">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="9ed14-168">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="9ed14-169">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="9ed14-169">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="9ed14-170">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="9ed14-170">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="9ed14-171">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="9ed14-171">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="9ed14-172">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="9ed14-172">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="9ed14-173">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9ed14-173">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
