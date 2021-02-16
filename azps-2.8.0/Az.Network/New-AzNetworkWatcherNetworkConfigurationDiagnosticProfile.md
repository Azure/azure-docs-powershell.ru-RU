---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatchernetworkconfigurationdiagnosticprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
ms.openlocfilehash: fe3438e43bc623da0ba69b3b1224a47df8b15f1f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100414685"
---
# <span data-ttu-id="f97fd-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="f97fd-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="f97fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f97fd-102">SYNOPSIS</span></span>
<span data-ttu-id="f97fd-103">Создание нового объекта диагностики конфигурации сети.</span><span class="sxs-lookup"><span data-stu-id="f97fd-103">Creates a new network configuration diagnostic profile object.</span></span> <span data-ttu-id="f97fd-104">Этот объект используется для ограничения конфигурации сети во время сеанса диагностики с использованием указанных критериев.</span><span class="sxs-lookup"><span data-stu-id="f97fd-104">This object is used to restrict the network configuration during a diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="f97fd-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f97fd-105">SYNTAX</span></span>

```
New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction <String> -Protocol <String>
 -Source <String> -Destination <String> -DestinationPort <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f97fd-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f97fd-106">DESCRIPTION</span></span>
<span data-ttu-id="f97fd-107">С помощью New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile-профиля создается новый объект профиля диагностики.</span><span class="sxs-lookup"><span data-stu-id="f97fd-107">The New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet creates a new diagnostic profile object.</span></span> <span data-ttu-id="f97fd-108">Этот объект используется для ограничения конфигурации сети во время сеанса диагностики конфигурации сети с использованием указанных критериев.</span><span class="sxs-lookup"><span data-stu-id="f97fd-108">This object is used to restrict the network configuration during a network configuration diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="f97fd-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f97fd-109">EXAMPLES</span></span>

### <span data-ttu-id="f97fd-110">Пример 1. Сеанс диагностики конфигурации сети для VM и указанного профиля сети</span><span class="sxs-lookup"><span data-stu-id="f97fd-110">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
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

## <span data-ttu-id="f97fd-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f97fd-111">PARAMETERS</span></span>

### <span data-ttu-id="f97fd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f97fd-112">-DefaultProfile</span></span>
<span data-ttu-id="f97fd-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f97fd-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f97fd-114">-Destination</span><span class="sxs-lookup"><span data-stu-id="f97fd-114">-Destination</span></span>
<span data-ttu-id="f97fd-115">Пункт назначения для трафика.</span><span class="sxs-lookup"><span data-stu-id="f97fd-115">Traffic destination.</span></span>
<span data-ttu-id="f97fd-116">Можно принимать значения"\*", "IP-адрес/CIDR", "Тег службы".</span><span class="sxs-lookup"><span data-stu-id="f97fd-116">Accepted values are: '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="f97fd-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="f97fd-117">-DestinationPort</span></span>
<span data-ttu-id="f97fd-118">Порт назначения для трафика.</span><span class="sxs-lookup"><span data-stu-id="f97fd-118">Traffic destination port.</span></span>
<span data-ttu-id="f97fd-119">Допустимые значения: "\*", "порт" (например, 3389) и диапазон порта (например, 80-100).</span><span class="sxs-lookup"><span data-stu-id="f97fd-119">Accepted values are '\*', port (for example, 3389) and port range (for example, 80-100).</span></span>

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

### <span data-ttu-id="f97fd-120">-Direction</span><span class="sxs-lookup"><span data-stu-id="f97fd-120">-Direction</span></span>
<span data-ttu-id="f97fd-121">Направление трафика.</span><span class="sxs-lookup"><span data-stu-id="f97fd-121">The direction of the traffic.</span></span>
<span data-ttu-id="f97fd-122">Можно принимать значения "Входящие" и "Исходящие".</span><span class="sxs-lookup"><span data-stu-id="f97fd-122">Accepted values are 'Inbound' and 'Outbound'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f97fd-123">-Protocol</span><span class="sxs-lookup"><span data-stu-id="f97fd-123">-Protocol</span></span>
<span data-ttu-id="f97fd-124">Протокол для проверки.</span><span class="sxs-lookup"><span data-stu-id="f97fd-124">Protocol to be verified on.</span></span>
<span data-ttu-id="f97fd-125">Можно принимать значения "\*", TCP, UDP.</span><span class="sxs-lookup"><span data-stu-id="f97fd-125">Accepted values are '\*', TCP, UDP.</span></span>

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

### <span data-ttu-id="f97fd-126">-Source</span><span class="sxs-lookup"><span data-stu-id="f97fd-126">-Source</span></span>
<span data-ttu-id="f97fd-127">Источник трафика.</span><span class="sxs-lookup"><span data-stu-id="f97fd-127">Traffic source.</span></span>
<span data-ttu-id="f97fd-128">Принимаются значения "\*", "IP-адрес/CIDR", "Тег службы".</span><span class="sxs-lookup"><span data-stu-id="f97fd-128">Accepted values are '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="f97fd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f97fd-129">CommonParameters</span></span>
<span data-ttu-id="f97fd-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f97fd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f97fd-131">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f97fd-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f97fd-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f97fd-132">INPUTS</span></span>

### <span data-ttu-id="f97fd-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f97fd-133">System.String</span></span>

## <span data-ttu-id="f97fd-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f97fd-134">OUTPUTS</span></span>

### <span data-ttu-id="f97fd-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="f97fd-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="f97fd-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f97fd-136">NOTES</span></span>
<span data-ttu-id="f97fd-137">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span><span class="sxs-lookup"><span data-stu-id="f97fd-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="f97fd-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f97fd-138">RELATED LINKS</span></span>

[<span data-ttu-id="f97fd-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f97fd-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="f97fd-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f97fd-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="f97fd-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f97fd-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="f97fd-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f97fd-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="f97fd-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f97fd-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f97fd-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f97fd-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="f97fd-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f97fd-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f97fd-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f97fd-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f97fd-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f97fd-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="f97fd-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f97fd-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f97fd-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f97fd-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f97fd-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f97fd-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f97fd-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="f97fd-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="f97fd-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f97fd-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="f97fd-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="f97fd-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="f97fd-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f97fd-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f97fd-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f97fd-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f97fd-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f97fd-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f97fd-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="f97fd-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="f97fd-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f97fd-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f97fd-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f97fd-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f97fd-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="f97fd-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="f97fd-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="f97fd-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="f97fd-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="f97fd-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="f97fd-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="f97fd-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="f97fd-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="f97fd-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="f97fd-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f97fd-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
