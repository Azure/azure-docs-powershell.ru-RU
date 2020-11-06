---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchertopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTopology.md
ms.openlocfilehash: 527102bc6ee80215885efc0be42bbf740d21aa06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564283"
---
# <span data-ttu-id="c95a4-101">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c95a4-101">Get-AzureRmNetworkWatcherTopology</span></span>

## <span data-ttu-id="c95a4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c95a4-102">SYNOPSIS</span></span>
<span data-ttu-id="c95a4-103">Получает сетевое представление ресурсов и их связей в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c95a4-103">Gets a network level view of resources and their relationships in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c95a4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c95a4-104">SYNTAX</span></span>

### <span data-ttu-id="c95a4-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c95a4-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherTopology -NetworkWatcher <PSNetworkWatcher> -TargetResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c95a4-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="c95a4-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherTopology -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c95a4-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c95a4-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherTopology -Location <String> -TargetResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c95a4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c95a4-108">DESCRIPTION</span></span>
<span data-ttu-id="c95a4-109">Get-AzureRmNetworkWatcherTopology командлетом сетевое представление ресурсов и их связей в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c95a4-109">The Get-AzureRmNetworkWatcherTopology cmdlet a network level view of resources and their relationships in a resource group.</span></span> <span data-ttu-id="c95a4-110">Примечание. Если ресурсы из нескольких областей находятся в группе ресурсов, в выходных данных JSON будут включены только ресурсы, находящиеся в той же области, что и наблюдатель сети.</span><span class="sxs-lookup"><span data-stu-id="c95a4-110">Note: If resources from multiple regions reside in the resource group, only the resources in the same region as the Network Watcher will be included in the JSON output.</span></span>

## <span data-ttu-id="c95a4-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c95a4-111">EXAMPLES</span></span>

### <span data-ttu-id="c95a4-112">Пример 1: получение топологии Azure</span><span class="sxs-lookup"><span data-stu-id="c95a4-112">Example 1: Get an Azure Topology</span></span>
```
$networkWatcher = Get-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG 
Get-AzureRmNetworkWatcherTopology -NetworkWatcher $networkWatcher -ResourceGroupName testresourcegroup

Id                : e33d80cf-4f76-4b8f-b51c-5bb8eba80103
CreatedDateTime   : 0/00/0000 9:21:51 PM
LastModified      : 0/00/0000 4:53:29 AM
TopologyResources : [
                      {
                        "Name": "testresourcegroup-vnet",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/virtualNetworks/testresourcegroup-vnet",
                        "Location": "westcentralus",
                        "TopologyAssociations": [
                          {
                            "Name": "default",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/virtualNetworks/testresourcegroup-vnet/subnets/default",
                            "AssociationType": "Contains"
                          }
                        ]
                      },
                      {
                        "Name": "default",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/virtualNetworks/testresourcegroup-vnet/subnets/default",
                        "Location": "westcentralus",
                        "TopologyAssociations": []
                      },
                      {
                        "Name": "VM0",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Compute/virtualMachines/VM0",
                        "TopologyAssociations": [
                          {
                            "Name": "vm0131",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkInterfaces/vm0131",
                            "AssociationType": "Contains"
                          }
                        ]
                      },
                      {
                        "Name": "vm0131",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkInterfaces/vm0131",
                        "Location": "westcentralus",
                        "TopologyAssociations": [
                          {
                            "Name": "VM0",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Compute/virtualMachines/VM0",
                            "AssociationType": "Associated"
                          },
                          {
                            "Name": "VM0-nsg",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkSecurityGroups/VM0-nsg",
                            "AssociationType": "Associated"
                          },
                          {
                            "Name": "default",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/virtualNetworks/testresourcegroup-vnet/subnets/default",
                            "AssociationType": "Associated"
                          },
                          {
                            "Name": "VM0-ip",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/publicIPAddresses/VM0-ip",
                            "AssociationType": "Associated"
                          }
                        ]
                      },
                      {
                        "Name": "VM0-nsg",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkSecurityGroups/VM0-nsg",
                        "Location": "westcentralus",
                        "TopologyAssociations": [
                          {
                            "Name": "default-allow-rdp",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkSecurityGroups/VM0-nsg/securityRules/default-allow-rdp",
                            "AssociationType": "Contains"
                          }
                        ]
                      },
                      {
                        "Name": "default-allow-rdp",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkSecurityGroups/VM0-nsg/securityRules/default-allow-rdp",
                        "Location": "westcentralus",
                        "TopologyAssociations": []
                      },
                      {
                        "Name": "VM0-ip",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/publicIPAddresses/VM0-ip",
                        "Location": "westcentralus",
                        "TopologyAssociations": [
                          {
                            "Name": "vm0131",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkInterfaces/vm0131",
                            "AssociationType": "Associated"
                          }
                        ]
                      }
                    ]
```

<span data-ttu-id="c95a4-113">В этом примере выполняется командлет Get-AzureRmNetworkWatcherTopology в группе ресурсов, которая включает виртуальные машины, NIC, NSG и общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="c95a4-113">In this example we run the Get-AzureRmNetworkWatcherTopology cmdlet on a resource group that contains a VM, Nic, NSG, and public IP.</span></span>

## <span data-ttu-id="c95a4-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c95a4-114">PARAMETERS</span></span>

### <span data-ttu-id="c95a4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c95a4-115">-DefaultProfile</span></span>
<span data-ttu-id="c95a4-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c95a4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c95a4-117">-Location</span><span class="sxs-lookup"><span data-stu-id="c95a4-117">-Location</span></span>
<span data-ttu-id="c95a4-118">Расположение наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="c95a4-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="c95a4-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c95a4-119">-NetworkWatcher</span></span>
<span data-ttu-id="c95a4-120">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="c95a4-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="c95a4-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c95a4-121">-NetworkWatcherName</span></span>
<span data-ttu-id="c95a4-122">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="c95a4-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="c95a4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c95a4-123">-ResourceGroupName</span></span>
<span data-ttu-id="c95a4-124">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="c95a4-124">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c95a4-125">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c95a4-125">-TargetResourceGroupName</span></span>
<span data-ttu-id="c95a4-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c95a4-126">The resource group name.</span></span>

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

### <span data-ttu-id="c95a4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c95a4-127">CommonParameters</span></span>
<span data-ttu-id="c95a4-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c95a4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c95a4-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c95a4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c95a4-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c95a4-130">INPUTS</span></span>

### <span data-ttu-id="c95a4-131">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c95a4-131">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="c95a4-132">Параметры: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c95a4-132">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="c95a4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c95a4-133">System.String</span></span>
<span data-ttu-id="c95a4-134">Параметры: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c95a4-134">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="c95a4-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c95a4-135">OUTPUTS</span></span>

### <span data-ttu-id="c95a4-136">Microsoft. Azure. Commands. Network. Models. PSTopology</span><span class="sxs-lookup"><span data-stu-id="c95a4-136">Microsoft.Azure.Commands.Network.Models.PSTopology</span></span>

## <span data-ttu-id="c95a4-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="c95a4-137">NOTES</span></span>
<span data-ttu-id="c95a4-138">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, топология, просмотр</span><span class="sxs-lookup"><span data-stu-id="c95a4-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, topology, view</span></span> 

## <span data-ttu-id="c95a4-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c95a4-139">RELATED LINKS</span></span>

[<span data-ttu-id="c95a4-140">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c95a4-140">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c95a4-141">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c95a4-141">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c95a4-142">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c95a4-142">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c95a4-143">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c95a4-143">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="c95a4-144">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c95a4-144">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c95a4-145">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c95a4-145">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="c95a4-146">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c95a4-146">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c95a4-147">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c95a4-147">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c95a4-148">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c95a4-148">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="c95a4-149">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c95a4-149">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c95a4-150">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c95a4-150">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c95a4-151">Остановить-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c95a4-151">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c95a4-152">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c95a4-152">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c95a4-153">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c95a4-153">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="c95a4-154">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c95a4-154">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="c95a4-155">Остановить-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c95a4-155">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c95a4-156">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c95a4-156">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c95a4-157">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c95a4-157">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c95a4-158">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c95a4-158">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c95a4-159">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c95a4-159">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c95a4-160">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c95a4-160">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c95a4-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c95a4-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c95a4-162">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c95a4-162">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c95a4-163">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c95a4-163">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c95a4-164">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c95a4-164">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="c95a4-165">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c95a4-165">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="c95a4-166">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c95a4-166">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)

