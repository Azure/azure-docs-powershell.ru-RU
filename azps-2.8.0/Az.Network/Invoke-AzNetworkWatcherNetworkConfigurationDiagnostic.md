---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/invoke-aznetworkwatchernetworkconfigurationdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic.md
ms.openlocfilehash: a064b69bbb5104521d81ca69f295748bfd65462f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100414430"
---
# <span data-ttu-id="490ef-101">Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="490ef-101">Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic</span></span>

## <span data-ttu-id="490ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="490ef-102">SYNOPSIS</span></span>
<span data-ttu-id="490ef-103">Вызов сеанса диагностики конфигурации сети для определенных профилей сети на целевом ресурсе.</span><span class="sxs-lookup"><span data-stu-id="490ef-103">Invoke network configuration diagnostic session for specified network profiles on target resource.</span></span>

## <span data-ttu-id="490ef-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="490ef-104">SYNTAX</span></span>

### <span data-ttu-id="490ef-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="490ef-105">SetByResource (Default)</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="490ef-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="490ef-106">SetByName</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="490ef-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="490ef-107">SetByLocation</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -Location <String> -TargetResourceId <String>
 [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="490ef-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="490ef-108">SetByResourceId</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -ResourceId <String> -TargetResourceId <String>
 [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="490ef-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="490ef-109">DESCRIPTION</span></span>
<span data-ttu-id="490ef-110">С Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic вызвать сеанс диагностики конфигурации сети для определенных профилей сети на целевом ресурсе.</span><span class="sxs-lookup"><span data-stu-id="490ef-110">The Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic cmdlet invoke network configuration diagnostic session for specified network profiles on target resource.</span></span>

## <span data-ttu-id="490ef-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="490ef-111">EXAMPLES</span></span>

### <span data-ttu-id="490ef-112">Пример 1. Сеанс диагностики конфигурации сети для VM и указанного профиля сети</span><span class="sxs-lookup"><span data-stu-id="490ef-112">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
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

## <span data-ttu-id="490ef-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="490ef-113">PARAMETERS</span></span>

### <span data-ttu-id="490ef-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="490ef-114">-AsJob</span></span>
<span data-ttu-id="490ef-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="490ef-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="490ef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="490ef-116">-DefaultProfile</span></span>
<span data-ttu-id="490ef-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="490ef-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="490ef-118">-Location</span><span class="sxs-lookup"><span data-stu-id="490ef-118">-Location</span></span>
<span data-ttu-id="490ef-119">Расположение сетевого просмотра.</span><span class="sxs-lookup"><span data-stu-id="490ef-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="490ef-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="490ef-120">-NetworkWatcher</span></span>
<span data-ttu-id="490ef-121">Сетевой ресурс для просмотра.</span><span class="sxs-lookup"><span data-stu-id="490ef-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="490ef-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="490ef-122">-NetworkWatcherName</span></span>
<span data-ttu-id="490ef-123">Имя сетевого смотритела.</span><span class="sxs-lookup"><span data-stu-id="490ef-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="490ef-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="490ef-124">-Profile</span></span>
<span data-ttu-id="490ef-125">Список диагностических профилей конфигурации сети.</span><span class="sxs-lookup"><span data-stu-id="490ef-125">List of network configuration diagnostic profiles.</span></span>

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

### <span data-ttu-id="490ef-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="490ef-126">-ResourceGroupName</span></span>
<span data-ttu-id="490ef-127">Имя группы ресурсов сетевого watcher.</span><span class="sxs-lookup"><span data-stu-id="490ef-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="490ef-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="490ef-128">-ResourceId</span></span>
<span data-ttu-id="490ef-129">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="490ef-129">Resource ID.</span></span>

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

### <span data-ttu-id="490ef-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="490ef-130">-TargetResourceId</span></span>
<span data-ttu-id="490ef-131">ИД целевого ресурса для диагностики конфигурации сети.</span><span class="sxs-lookup"><span data-stu-id="490ef-131">The ID of the target resource to perform network configuration diagnostic.</span></span>
<span data-ttu-id="490ef-132">Допустимые параметры: VM, NetworkInterface, VMSS/NetworkInterface и Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="490ef-132">Valid options are VM, NetworkInterface, VMSS/NetworkInterface and Application Gateway.</span></span>

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

### <span data-ttu-id="490ef-133">-VerbosityLevel</span><span class="sxs-lookup"><span data-stu-id="490ef-133">-VerbosityLevel</span></span>
<span data-ttu-id="490ef-134">Уровень глагольности.</span><span class="sxs-lookup"><span data-stu-id="490ef-134">Verbosity level.</span></span>
<span data-ttu-id="490ef-135">Допустимые значения: обычные, минимальные, полные.</span><span class="sxs-lookup"><span data-stu-id="490ef-135">Accepted values are 'Normal', 'Minimum', 'Full'.</span></span>

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

### <span data-ttu-id="490ef-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="490ef-136">CommonParameters</span></span>
<span data-ttu-id="490ef-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="490ef-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="490ef-138">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="490ef-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="490ef-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="490ef-139">INPUTS</span></span>

### <span data-ttu-id="490ef-140">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="490ef-140">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="490ef-141">System.String</span><span class="sxs-lookup"><span data-stu-id="490ef-141">System.String</span></span>

## <span data-ttu-id="490ef-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="490ef-142">OUTPUTS</span></span>

### <span data-ttu-id="490ef-143">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticResponse</span><span class="sxs-lookup"><span data-stu-id="490ef-143">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticResponse</span></span>

## <span data-ttu-id="490ef-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="490ef-144">NOTES</span></span>
<span data-ttu-id="490ef-145">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span><span class="sxs-lookup"><span data-stu-id="490ef-145">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="490ef-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="490ef-146">RELATED LINKS</span></span>

[<span data-ttu-id="490ef-147">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="490ef-147">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="490ef-148">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="490ef-148">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="490ef-149">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="490ef-149">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="490ef-150">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="490ef-150">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="490ef-151">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="490ef-151">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="490ef-152">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="490ef-152">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="490ef-153">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="490ef-153">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="490ef-154">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="490ef-154">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="490ef-155">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="490ef-155">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="490ef-156">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="490ef-156">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="490ef-157">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="490ef-157">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="490ef-158">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="490ef-158">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="490ef-159">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="490ef-159">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="490ef-160">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="490ef-160">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="490ef-161">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="490ef-161">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="490ef-162">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="490ef-162">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="490ef-163">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="490ef-163">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="490ef-164">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="490ef-164">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="490ef-165">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="490ef-165">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="490ef-166">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="490ef-166">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="490ef-167">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="490ef-167">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="490ef-168">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="490ef-168">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="490ef-169">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="490ef-169">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="490ef-170">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="490ef-170">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="490ef-171">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="490ef-171">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="490ef-172">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="490ef-172">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="490ef-173">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="490ef-173">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
