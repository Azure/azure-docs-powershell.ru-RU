---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5AECCBD7-1FDE-4217-9F59-36328062E669
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityGroup.md
ms.openlocfilehash: 46106379160ee593748a95489c2641d43114d863
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902897"
---
# <span data-ttu-id="211f7-101">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="211f7-101">Get-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="211f7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="211f7-102">SYNOPSIS</span></span>
<span data-ttu-id="211f7-103">Получает сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="211f7-103">Gets a network security group.</span></span>

## <span data-ttu-id="211f7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="211f7-104">SYNTAX</span></span>

### <span data-ttu-id="211f7-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="211f7-105">NoExpand</span></span>
```
Get-AzNetworkSecurityGroup [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="211f7-106">Кройте</span><span class="sxs-lookup"><span data-stu-id="211f7-106">Expand</span></span>
```
Get-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="211f7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="211f7-107">DESCRIPTION</span></span>
<span data-ttu-id="211f7-108">Командлет **Get-AzNetworkSecurityGroup** получает сетевую группу безопасности Azure.</span><span class="sxs-lookup"><span data-stu-id="211f7-108">The **Get-AzNetworkSecurityGroup** cmdlet gets an Azure network security group.</span></span>

## <span data-ttu-id="211f7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="211f7-109">EXAMPLES</span></span>

### <span data-ttu-id="211f7-110">1. получение существующей группы безопасности сети</span><span class="sxs-lookup"><span data-stu-id="211f7-110">1: Retrieve an existing network security group</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName "rg1"

Name                        : nsg1
ResourceGroupName           : rg1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provider
                              s/Microsoft.Network/networkInterfaces/nsg1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
VirtualMachine              : null
IpConfigurations            : [
                                {
                                  "Name": "ipconfig1",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/networkInterfaces/nsg1/ipConfigurations/ipcon
                              fig1",
                                  "PrivateIpAddress": "x.x.x.x",
                                  "PrivateIpAllocationMethod": "Dynamic",
                                  "Subnet": {
                                    "Delegations": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/virtualNetworks/vnetcrptestps2673/subnets/subnetcrptestp
                              s2673",
                                    "ServiceAssociationLinks": []
                                  },
                                  "PublicIpAddress": {
                                    "IpTags": [],
                                    "Zones": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/publicIPAddresses/pubipcrptestps2673"
                                  },
                                  "ProvisioningState": "Succeeded",
                                  "PrivateIpAddressVersion": "IPv4",
                                  "LoadBalancerBackendAddressPools": [],
                                  "LoadBalancerInboundNatRules": [],
                                  "Primary": true,
                                  "ApplicationGatewayBackendAddressPools": [],
                                  "ApplicationSecurityGroups": []
                                }
                              ]
DnsSettings                 : {
                                "DnsServers": [],
                                "AppliedDnsServers": [],
                                "InternalDomainNameSuffix": "xxxxxxxxxxxxxxx.xx.internal.cloudapp.net"
                              }
EnableIPForwarding          : False
EnableAcceleratedNetworking : False
NetworkSecurityGroup        : null
Primary                     :
MacAddress                  :
```

<span data-ttu-id="211f7-111">Эта команда возвращает содержимое группы безопасности сети Azure "nsg1" в группе ресурсов "Rg1"</span><span class="sxs-lookup"><span data-stu-id="211f7-111">This command returns contents of Azure network security group "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="211f7-112">2. Перечисление существующих групп безопасности сети с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="211f7-112">2: List existing network security groups using filtering</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg*

Name                        : nsg1
ResourceGroupName           : rg1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provider
                              s/Microsoft.Network/networkInterfaces/nsg1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
VirtualMachine              : null
IpConfigurations            : [
                                {
                                  "Name": "ipconfig1",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/networkInterfaces/nsg1/ipConfigurations/ipcon
                              fig1",
                                  "PrivateIpAddress": "x.x.x.x",
                                  "PrivateIpAllocationMethod": "Dynamic",
                                  "Subnet": {
                                    "Delegations": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/virtualNetworks/vnetcrptestps2673/subnets/subnetcrptestp
                              s2673",
                                    "ServiceAssociationLinks": []
                                  },
                                  "PublicIpAddress": {
                                    "IpTags": [],
                                    "Zones": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                              /providers/Microsoft.Network/publicIPAddresses/pubipcrptestps2673"
                                  },
                                  "ProvisioningState": "Succeeded",
                                  "PrivateIpAddressVersion": "IPv4",
                                  "LoadBalancerBackendAddressPools": [],
                                  "LoadBalancerInboundNatRules": [],
                                  "Primary": true,
                                  "ApplicationGatewayBackendAddressPools": [],
                                  "ApplicationSecurityGroups": []
                                }
                              ]
DnsSettings                 : {
                                "DnsServers": [],
                                "AppliedDnsServers": [],
                                "InternalDomainNameSuffix": "xxxxxxxxxxxxxxx.xx.internal.cloudapp.net"
                              }
EnableIPForwarding          : False
EnableAcceleratedNetworking : False
NetworkSecurityGroup        : null
Primary                     :
MacAddress                  :
```

<span data-ttu-id="211f7-113">Эта команда возвращает содержимое групп безопасности сети Azure, которые начинаются с "NSG".</span><span class="sxs-lookup"><span data-stu-id="211f7-113">This command returns contents of Azure network security groups that start with "nsg"</span></span>

## <span data-ttu-id="211f7-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="211f7-114">PARAMETERS</span></span>

### <span data-ttu-id="211f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="211f7-115">-DefaultProfile</span></span>
<span data-ttu-id="211f7-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="211f7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="211f7-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="211f7-117">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="211f7-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="211f7-118">-Name</span></span>
<span data-ttu-id="211f7-119">Указывает имя сетевой группы безопасности, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="211f7-119">Specifies the name of the network security group that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="211f7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="211f7-120">-ResourceGroupName</span></span>
<span data-ttu-id="211f7-121">Указывает имя группы ресурсов, к которой принадлежит Сетевая группа безопасности.</span><span class="sxs-lookup"><span data-stu-id="211f7-121">Specifies the name of the resource group that the network security group belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="211f7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="211f7-122">CommonParameters</span></span>
<span data-ttu-id="211f7-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="211f7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="211f7-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="211f7-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="211f7-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="211f7-125">INPUTS</span></span>

### <span data-ttu-id="211f7-126">System. String</span><span class="sxs-lookup"><span data-stu-id="211f7-126">System.String</span></span>

## <span data-ttu-id="211f7-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="211f7-127">OUTPUTS</span></span>

### <span data-ttu-id="211f7-128">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="211f7-128">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="211f7-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="211f7-129">NOTES</span></span>

## <span data-ttu-id="211f7-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="211f7-130">RELATED LINKS</span></span>

[<span data-ttu-id="211f7-131">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="211f7-131">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="211f7-132">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="211f7-132">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)

[<span data-ttu-id="211f7-133">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="211f7-133">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)


