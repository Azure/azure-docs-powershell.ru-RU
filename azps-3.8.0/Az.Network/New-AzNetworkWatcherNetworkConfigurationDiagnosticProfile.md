---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatchernetworkconfigurationdiagnosticprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
ms.openlocfilehash: 009f294cd4d0277b925f36c3d6b7cc4e50e7f733
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066251"
---
# <span data-ttu-id="321f1-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="321f1-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="321f1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="321f1-102">SYNOPSIS</span></span>
<span data-ttu-id="321f1-103">Создание нового объекта профиля диагностики конфигурации сети.</span><span class="sxs-lookup"><span data-stu-id="321f1-103">Creates a new network configuration diagnostic profile object.</span></span> <span data-ttu-id="321f1-104">Этот объект используется для ограничения конфигурации сети во время диагностического сеанса с указанными условиями.</span><span class="sxs-lookup"><span data-stu-id="321f1-104">This object is used to restrict the network configuration during a diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="321f1-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="321f1-105">SYNTAX</span></span>

```
New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction <String> -Protocol <String>
 -Source <String> -Destination <String> -DestinationPort <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="321f1-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="321f1-106">DESCRIPTION</span></span>
<span data-ttu-id="321f1-107">Командлет New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile создает новый объект профиля диагностики.</span><span class="sxs-lookup"><span data-stu-id="321f1-107">The New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet creates a new diagnostic profile object.</span></span> <span data-ttu-id="321f1-108">Этот объект используется для ограничения конфигурации сети во время сеанса диагностики конфигурации сети с использованием указанных условий.</span><span class="sxs-lookup"><span data-stu-id="321f1-108">This object is used to restrict the network configuration during a network configuration diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="321f1-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="321f1-109">EXAMPLES</span></span>

### <span data-ttu-id="321f1-110">Пример 1: вызов диагностического сеанса диагностики конфигурации сети для виртуальной машины и указанного сетевого профиля</span><span class="sxs-lookup"><span data-stu-id="321f1-110">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
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

## <span data-ttu-id="321f1-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="321f1-111">PARAMETERS</span></span>

### <span data-ttu-id="321f1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="321f1-112">-DefaultProfile</span></span>
<span data-ttu-id="321f1-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="321f1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="321f1-114">-Destination</span><span class="sxs-lookup"><span data-stu-id="321f1-114">-Destination</span></span>
<span data-ttu-id="321f1-115">Назначение трафика.</span><span class="sxs-lookup"><span data-stu-id="321f1-115">Traffic destination.</span></span>
<span data-ttu-id="321f1-116">Допустимые значения: "\*", IP-адрес/CIDR, тег обслуживания.</span><span class="sxs-lookup"><span data-stu-id="321f1-116">Accepted values are: '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="321f1-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="321f1-117">-DestinationPort</span></span>
<span data-ttu-id="321f1-118">Порт назначения трафика.</span><span class="sxs-lookup"><span data-stu-id="321f1-118">Traffic destination port.</span></span>
<span data-ttu-id="321f1-119">Допустимые значения: "\*", "порт" (например, 3389) и диапазон портов (например, 80-100).</span><span class="sxs-lookup"><span data-stu-id="321f1-119">Accepted values are '\*', port (for example, 3389) and port range (for example, 80-100).</span></span>

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

### <span data-ttu-id="321f1-120">-Направление</span><span class="sxs-lookup"><span data-stu-id="321f1-120">-Direction</span></span>
<span data-ttu-id="321f1-121">Направление трафика.</span><span class="sxs-lookup"><span data-stu-id="321f1-121">The direction of the traffic.</span></span>
<span data-ttu-id="321f1-122">Допустимые значения "входящий" и "Исходящие"</span><span class="sxs-lookup"><span data-stu-id="321f1-122">Accepted values are 'Inbound' and 'Outbound'</span></span>

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

### <span data-ttu-id="321f1-123">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="321f1-123">-Protocol</span></span>
<span data-ttu-id="321f1-124">Проверяемый протокол.</span><span class="sxs-lookup"><span data-stu-id="321f1-124">Protocol to be verified on.</span></span>
<span data-ttu-id="321f1-125">Допустимые значения: "\*", TCP, UDP.</span><span class="sxs-lookup"><span data-stu-id="321f1-125">Accepted values are '\*', TCP, UDP.</span></span>

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

### <span data-ttu-id="321f1-126">-Source (источник)</span><span class="sxs-lookup"><span data-stu-id="321f1-126">-Source</span></span>
<span data-ttu-id="321f1-127">Источник трафика.</span><span class="sxs-lookup"><span data-stu-id="321f1-127">Traffic source.</span></span>
<span data-ttu-id="321f1-128">Допустимые значения: "\*", IP-адрес/CIDR, тег обслуживания.</span><span class="sxs-lookup"><span data-stu-id="321f1-128">Accepted values are '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="321f1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="321f1-129">CommonParameters</span></span>
<span data-ttu-id="321f1-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="321f1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="321f1-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="321f1-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="321f1-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="321f1-132">INPUTS</span></span>

### <span data-ttu-id="321f1-133">System. String</span><span class="sxs-lookup"><span data-stu-id="321f1-133">System.String</span></span>

## <span data-ttu-id="321f1-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="321f1-134">OUTPUTS</span></span>

### <span data-ttu-id="321f1-135">Microsoft. Azure. Commands. Network. Models. PSNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="321f1-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="321f1-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="321f1-136">NOTES</span></span>
<span data-ttu-id="321f1-137">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель, диагностика, профиль</span><span class="sxs-lookup"><span data-stu-id="321f1-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="321f1-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="321f1-138">RELATED LINKS</span></span>

[<span data-ttu-id="321f1-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="321f1-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="321f1-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="321f1-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="321f1-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="321f1-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="321f1-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="321f1-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="321f1-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="321f1-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="321f1-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="321f1-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="321f1-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="321f1-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="321f1-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="321f1-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="321f1-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="321f1-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="321f1-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="321f1-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="321f1-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="321f1-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="321f1-150">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="321f1-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="321f1-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="321f1-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="321f1-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="321f1-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="321f1-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="321f1-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="321f1-154">Остановить-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="321f1-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="321f1-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="321f1-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="321f1-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="321f1-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="321f1-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="321f1-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="321f1-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="321f1-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="321f1-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="321f1-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="321f1-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="321f1-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="321f1-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="321f1-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="321f1-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="321f1-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="321f1-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="321f1-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="321f1-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="321f1-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="321f1-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="321f1-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
