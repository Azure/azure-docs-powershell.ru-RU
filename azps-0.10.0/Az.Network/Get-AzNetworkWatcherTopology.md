---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherTopology.md
ms.openlocfilehash: 72f5c803c7fa4f4693da3660c41f73eadb464ab7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909905"
---
# <span data-ttu-id="eeffd-101">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="eeffd-101">Get-AzNetworkWatcherTopology</span></span>

## <span data-ttu-id="eeffd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eeffd-102">SYNOPSIS</span></span>
<span data-ttu-id="eeffd-103">Получает сетевое представление ресурсов и их связей в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eeffd-103">Gets a network level view of resources and their relationships in a resource group.</span></span>

## <span data-ttu-id="eeffd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eeffd-104">SYNTAX</span></span>

### <span data-ttu-id="eeffd-105">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eeffd-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTopology -NetworkWatcher <PSNetworkWatcher> -TargetResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eeffd-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="eeffd-106">SetByName</span></span>
```
Get-AzNetworkWatcherTopology -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eeffd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eeffd-107">DESCRIPTION</span></span>
<span data-ttu-id="eeffd-108">Get-AzNetworkWatcherTopology командлетом сетевое представление ресурсов и их связей в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eeffd-108">The Get-AzNetworkWatcherTopology cmdlet a network level view of resources and their relationships in a resource group.</span></span> <span data-ttu-id="eeffd-109">Примечание. Если ресурсы из нескольких областей находятся в группе ресурсов, в выходных данных JSON будут включены только ресурсы, находящиеся в той же области, что и наблюдатель сети.</span><span class="sxs-lookup"><span data-stu-id="eeffd-109">Note: If resources from multiple regions reside in the resource group, only the resources in the same region as the Network Watcher will be included in the JSON output.</span></span>

## <span data-ttu-id="eeffd-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eeffd-110">EXAMPLES</span></span>

### <span data-ttu-id="eeffd-111">--------------------------Примере 1: получение топологии Azure--------------------------</span><span class="sxs-lookup"><span data-stu-id="eeffd-111">--------------------------  Example 1: Get an Azure Topology  --------------------------</span></span>
```
$networkWatcher = Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG 
Get-AzNetworkWatcherTopology -NetworkWatcher $networkWatcher -ResourceGroupName testresourcegroup

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

<span data-ttu-id="eeffd-112">В этом примере выполняется командлет Get-AzNetworkWatcherTopology в группе ресурсов, которая включает виртуальные машины, NIC, NSG и общедоступный IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="eeffd-112">In this example we run the Get-AzNetworkWatcherTopology cmdlet on a resource group that contains a VM, Nic, NSG, and public IP.</span></span>

## <span data-ttu-id="eeffd-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eeffd-113">PARAMETERS</span></span>

### <span data-ttu-id="eeffd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeffd-114">-DefaultProfile</span></span>
<span data-ttu-id="eeffd-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eeffd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeffd-116">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="eeffd-116">-NetworkWatcher</span></span>
<span data-ttu-id="eeffd-117">Ресурс сетевого наблюдателя.</span><span class="sxs-lookup"><span data-stu-id="eeffd-117">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eeffd-118">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="eeffd-118">-NetworkWatcherName</span></span>
<span data-ttu-id="eeffd-119">Имя наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="eeffd-119">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eeffd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eeffd-120">-ResourceGroupName</span></span>
<span data-ttu-id="eeffd-121">Имя группы ресурсов наблюдателя сети.</span><span class="sxs-lookup"><span data-stu-id="eeffd-121">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeffd-122">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eeffd-122">-TargetResourceGroupName</span></span>
<span data-ttu-id="eeffd-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eeffd-123">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeffd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeffd-124">CommonParameters</span></span>
<span data-ttu-id="eeffd-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eeffd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeffd-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eeffd-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeffd-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eeffd-127">INPUTS</span></span>

### <span data-ttu-id="eeffd-128">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="eeffd-128">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="eeffd-129">System. String</span><span class="sxs-lookup"><span data-stu-id="eeffd-129">System.String</span></span>

## <span data-ttu-id="eeffd-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eeffd-130">OUTPUTS</span></span>

### <span data-ttu-id="eeffd-131">Microsoft. Azure. Commands. Network. Models. PSTopology</span><span class="sxs-lookup"><span data-stu-id="eeffd-131">Microsoft.Azure.Commands.Network.Models.PSTopology</span></span>

## <span data-ttu-id="eeffd-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="eeffd-132">NOTES</span></span>
<span data-ttu-id="eeffd-133">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, сеть, сеть, наблюдатель сети, топология, просмотр</span><span class="sxs-lookup"><span data-stu-id="eeffd-133">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, topology, view</span></span> 

## <span data-ttu-id="eeffd-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eeffd-134">RELATED LINKS</span></span>

[<span data-ttu-id="eeffd-135">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="eeffd-135">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="eeffd-136">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="eeffd-136">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="eeffd-137">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="eeffd-137">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="eeffd-138">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="eeffd-138">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="eeffd-139">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="eeffd-139">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="eeffd-140">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="eeffd-140">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="eeffd-141">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="eeffd-141">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="eeffd-142">Остановить-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="eeffd-142">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="eeffd-143">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="eeffd-143">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="eeffd-144">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="eeffd-144">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="eeffd-145">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="eeffd-145">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="eeffd-146">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="eeffd-146">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

