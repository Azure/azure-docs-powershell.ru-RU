---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatchernetworkconfigurationdiagnosticprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
ms.openlocfilehash: c559001c68126c42c3d4ae6eaead2beda3ded5f0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234987"
---
# <span data-ttu-id="8c4cc-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="8c4cc-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="8c4cc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8c4cc-102">SYNOPSIS</span></span>
<span data-ttu-id="8c4cc-103">Создание нового объекта профиля диагностики конфигурации сети.</span><span class="sxs-lookup"><span data-stu-id="8c4cc-103">Creates a new network configuration diagnostic profile object.</span></span> <span data-ttu-id="8c4cc-104">Этот объект используется для ограничения конфигурации сети во время диагностического сеанса с указанными условиями.</span><span class="sxs-lookup"><span data-stu-id="8c4cc-104">This object is used to restrict the network configuration during a diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="8c4cc-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8c4cc-105">SYNTAX</span></span>

```
New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction <String> -Protocol <String>
 -Source <String> -Destination <String> -DestinationPort <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8c4cc-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c4cc-106">DESCRIPTION</span></span>
<span data-ttu-id="8c4cc-107">Командлет New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile создает новый объект профиля диагностики.</span><span class="sxs-lookup"><span data-stu-id="8c4cc-107">The New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet creates a new diagnostic profile object.</span></span> <span data-ttu-id="8c4cc-108">Этот объект используется для ограничения конфигурации сети во время сеанса диагностики конфигурации сети с использованием указанных условий.</span><span class="sxs-lookup"><span data-stu-id="8c4cc-108">This object is used to restrict the network configuration during a network configuration diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="8c4cc-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8c4cc-109">EXAMPLES</span></span>

### <span data-ttu-id="8c4cc-110">Пример 1: вызов диагностического сеанса диагностики конфигурации сети для виртуальной машины и указанного сетевого профиля</span><span class="sxs-lookup"><span data-stu-id="8c4cc-110">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
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

## <span data-ttu-id="8c4cc-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8c4cc-111">PARAMETERS</span></span>

### <span data-ttu-id="8c4cc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c4cc-112">-DefaultProfile</span></span>
<span data-ttu-id="8c4cc-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8c4cc-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c4cc-114">-Destination</span><span class="sxs-lookup"><span data-stu-id="8c4cc-114">-Destination</span></span>
<span data-ttu-id="8c4cc-115">Назначение трафика.</span><span class="sxs-lookup"><span data-stu-id="8c4cc-115">Traffic destination.</span></span>
<span data-ttu-id="8c4cc-116">Допустимые значения: "\*", IP-адрес/CIDR, тег обслуживания.</span><span class="sxs-lookup"><span data-stu-id="8c4cc-116">Accepted values are: '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="8c4cc-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="8c4cc-117">-DestinationPort</span></span>
<span data-ttu-id="8c4cc-118">Порт назначения трафика.</span><span class="sxs-lookup"><span data-stu-id="8c4cc-118">Traffic destination port.</span></span>
<span data-ttu-id="8c4cc-119">Допустимые значения: "\*", "порт" (например, 3389) и диапазон портов (например, 80-100).</span><span class="sxs-lookup"><span data-stu-id="8c4cc-119">Accepted values are '\*', port (for example, 3389) and port range (for example, 80-100).</span></span>

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

### <span data-ttu-id="8c4cc-120">-Направление</span><span class="sxs-lookup"><span data-stu-id="8c4cc-120">-Direction</span></span>
<span data-ttu-id="8c4cc-121">Направление трафика.</span><span class="sxs-lookup"><span data-stu-id="8c4cc-121">The direction of the traffic.</span></span>
<span data-ttu-id="8c4cc-122">Допустимые значения "входящий" и "Исходящие"</span><span class="sxs-lookup"><span data-stu-id="8c4cc-122">Accepted values are 'Inbound' and 'Outbound'</span></span>

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

### <span data-ttu-id="8c4cc-123">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="8c4cc-123">-Protocol</span></span>
<span data-ttu-id="8c4cc-124">Проверяемый протокол.</span><span class="sxs-lookup"><span data-stu-id="8c4cc-124">Protocol to be verified on.</span></span>
<span data-ttu-id="8c4cc-125">Допустимые значения: "\*", TCP, UDP.</span><span class="sxs-lookup"><span data-stu-id="8c4cc-125">Accepted values are '\*', TCP, UDP.</span></span>

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

### <span data-ttu-id="8c4cc-126">-Source (источник)</span><span class="sxs-lookup"><span data-stu-id="8c4cc-126">-Source</span></span>
<span data-ttu-id="8c4cc-127">Источник трафика.</span><span class="sxs-lookup"><span data-stu-id="8c4cc-127">Traffic source.</span></span>
<span data-ttu-id="8c4cc-128">Допустимые значения: "\*", IP-адрес/CIDR, тег обслуживания.</span><span class="sxs-lookup"><span data-stu-id="8c4cc-128">Accepted values are '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="8c4cc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c4cc-129">CommonParameters</span></span>
<span data-ttu-id="8c4cc-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8c4cc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c4cc-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c4cc-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c4cc-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8c4cc-132">INPUTS</span></span>

### <span data-ttu-id="8c4cc-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8c4cc-133">System.String</span></span>

## <span data-ttu-id="8c4cc-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c4cc-134">OUTPUTS</span></span>

### <span data-ttu-id="8c4cc-135">Microsoft. Azure. Commands. Network. Models. PSNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="8c4cc-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="8c4cc-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="8c4cc-136">NOTES</span></span>
<span data-ttu-id="8c4cc-137">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель, диагностика, профиль</span><span class="sxs-lookup"><span data-stu-id="8c4cc-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="8c4cc-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c4cc-138">RELATED LINKS</span></span>

[<span data-ttu-id="8c4cc-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8c4cc-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="8c4cc-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8c4cc-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="8c4cc-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8c4cc-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="8c4cc-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8c4cc-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="8c4cc-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8c4cc-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="8c4cc-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8c4cc-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="8c4cc-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="8c4cc-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="8c4cc-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8c4cc-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8c4cc-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8c4cc-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="8c4cc-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8c4cc-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8c4cc-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8c4cc-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8c4cc-150">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8c4cc-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8c4cc-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c4cc-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="8c4cc-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8c4cc-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="8c4cc-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="8c4cc-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="8c4cc-154">Остановить-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8c4cc-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8c4cc-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8c4cc-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8c4cc-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8c4cc-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8c4cc-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="8c4cc-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="8c4cc-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8c4cc-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8c4cc-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8c4cc-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8c4cc-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="8c4cc-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="8c4cc-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="8c4cc-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="8c4cc-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="8c4cc-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="8c4cc-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="8c4cc-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="8c4cc-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="8c4cc-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="8c4cc-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8c4cc-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
