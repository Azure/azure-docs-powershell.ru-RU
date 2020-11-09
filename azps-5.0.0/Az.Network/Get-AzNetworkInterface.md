---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E066BBFA-2E03-431D-85D1-99F230B6AC59
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterface.md
ms.openlocfilehash: 1f49c2de253b41db97719933111a5ec2f9b861d5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246214"
---
# <span data-ttu-id="572a6-101">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="572a6-101">Get-AzNetworkInterface</span></span>

## <span data-ttu-id="572a6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="572a6-102">SYNOPSIS</span></span>
<span data-ttu-id="572a6-103">Возвращает сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="572a6-103">Gets a network interface.</span></span>

## <span data-ttu-id="572a6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="572a6-104">SYNTAX</span></span>

### <span data-ttu-id="572a6-105">NoExpandStandAloneNic (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="572a6-105">NoExpandStandAloneNic (Default)</span></span>
```
Get-AzNetworkInterface [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="572a6-106">ExpandStandAloneNic</span><span class="sxs-lookup"><span data-stu-id="572a6-106">ExpandStandAloneNic</span></span>
```
Get-AzNetworkInterface -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="572a6-107">NoExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="572a6-107">NoExpandScaleSetNic</span></span>
```
Get-AzNetworkInterface [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="572a6-108">ExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="572a6-108">ExpandScaleSetNic</span></span>
```
Get-AzNetworkInterface -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="572a6-109">GetByResourceIdExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="572a6-109">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzNetworkInterface -ResourceId <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="572a6-110">GetByResourceIdNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="572a6-110">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzNetworkInterface -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="572a6-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="572a6-111">DESCRIPTION</span></span>
<span data-ttu-id="572a6-112">Командлет **Get-AzNetworkInterface** получает сетевой интерфейс Azure или список сетевых интерфейсов Azure в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="572a6-112">The **Get-AzNetworkInterface** cmdlet gets an Azure network interface or a list of Azure network interfaces in a resource group.</span></span>

## <span data-ttu-id="572a6-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="572a6-113">EXAMPLES</span></span>

### <span data-ttu-id="572a6-114">Пример 1: получение всех сетевых интерфейсов</span><span class="sxs-lookup"><span data-stu-id="572a6-114">Example 1: Get all network interfaces</span></span>
```
PS C:\> Get-AzNetworkInterface

Name                        : test1
ResourceGroupName           : ResourceGroup1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/providers/Micros
                              oft.Network/networkInterfaces/test1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
VirtualMachine              : {
                                "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provide
                              rs/Microsoft.Compute/virtualMachines/test1"
                              }
IpConfigurations            : [
                                {
                                  "Name": "test1",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provi
                              ders/Microsoft.Network/networkInterfaces/test1/ipConfigurations/test1",
                                  "PrivateIpAddress": "x.x.x.x",
                                  "PrivateIpAllocationMethod": "Dynamic",
                                  "Subnet": {
                                    "Delegations": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/pro
                              viders/Microsoft.Network/virtualNetworks/test1/subnets/test1",
                                    "ServiceAssociationLinks": []
                                  },
                                  "PublicIpAddress": {
                                    "IpTags": [],
                                    "Zones": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/pro
                              viders/Microsoft.Network/publicIPAddresses/test1"
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
                                "AppliedDnsServers": []
                              }
EnableIPForwarding          : False
EnableAcceleratedNetworking : False
NetworkSecurityGroup        : {
                                "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provide
                              rs/Microsoft.Network/networkSecurityGroups/test1"
                              }
Primary                     : True
MacAddress                  :
```

<span data-ttu-id="572a6-115">Эта команда получает все сетевые интерфейсы для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="572a6-115">This command gets all network interfaces for the current subscription.</span></span>

### <span data-ttu-id="572a6-116">Пример 2: получение всех сетевых интерфейсов с определенным состоянием подготовки</span><span class="sxs-lookup"><span data-stu-id="572a6-116">Example 2: Get all network interfaces with a specific provisioning state</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" | Where-Object {$_.ProvisioningState -eq 'Succeeded'}

Name                        : test1
ResourceGroupName           : ResourceGroup1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/providers/Micros
                              oft.Network/networkInterfaces/test1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
VirtualMachine              : {
                                "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provide
                              rs/Microsoft.Compute/virtualMachines/test1"
                              }
IpConfigurations            : [
                                {
                                  "Name": "test1",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provi
                              ders/Microsoft.Network/networkInterfaces/test1/ipConfigurations/test1",
                                  "PrivateIpAddress": "x.x.x.x",
                                  "PrivateIpAllocationMethod": "Dynamic",
                                  "Subnet": {
                                    "Delegations": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/pro
                              viders/Microsoft.Network/virtualNetworks/test1/subnets/test1",
                                    "ServiceAssociationLinks": []
                                  },
                                  "PublicIpAddress": {
                                    "IpTags": [],
                                    "Zones": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/pro
                              viders/Microsoft.Network/publicIPAddresses/test1"
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
                                "AppliedDnsServers": []
                              }
EnableIPForwarding          : False
EnableAcceleratedNetworking : False
NetworkSecurityGroup        : {
                                "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provide
                              rs/Microsoft.Network/networkSecurityGroups/test1"
                              }
Primary                     : True
MacAddress                  :
```

<span data-ttu-id="572a6-117">Эта команда получает все сетевые интерфейсы в группе ресурсов с именем ResourceGroup1, для которой успешно определено состояние подготовки.</span><span class="sxs-lookup"><span data-stu-id="572a6-117">This command gets all network interfaces in the resource group named ResourceGroup1 that has a provisioning state of succeeded.</span></span>

### <span data-ttu-id="572a6-118">Пример 3: получение сетевых интерфейсов с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="572a6-118">Example 3: Get network interfaces using filtering</span></span>
```
PS C:\> Get-AzNetworkInterface -Name test*

Name                        : test1
ResourceGroupName           : ResourceGroup1
Location                    : eastus
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/providers/Micros
                              oft.Network/networkInterfaces/test1
Etag                        : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid                : 00000000-0000-0000-0000-000000000000
ProvisioningState           : Succeeded
Tags                        :
VirtualMachine              : {
                                "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provide
                              rs/Microsoft.Compute/virtualMachines/test1"
                              }
IpConfigurations            : [
                                {
                                  "Name": "test1",
                                  "Etag": "W/\"00000000-0000-0000-0000-000000000000\"",
                                  "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provi
                              ders/Microsoft.Network/networkInterfaces/test1/ipConfigurations/test1",
                                  "PrivateIpAddress": "x.x.x.x",
                                  "PrivateIpAllocationMethod": "Dynamic",
                                  "Subnet": {
                                    "Delegations": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/pro
                              viders/Microsoft.Network/virtualNetworks/test1/subnets/test1",
                                    "ServiceAssociationLinks": []
                                  },
                                  "PublicIpAddress": {
                                    "IpTags": [],
                                    "Zones": [],
                                    "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/pro
                              viders/Microsoft.Network/publicIPAddresses/test1"
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
                                "AppliedDnsServers": []
                              }
EnableIPForwarding          : False
EnableAcceleratedNetworking : False
NetworkSecurityGroup        : {
                                "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup1/provide
                              rs/Microsoft.Network/networkSecurityGroups/test1"
                              }
Primary                     : True
MacAddress                  :
```

<span data-ttu-id="572a6-119">Эта команда получает все сетевые интерфейсы для текущей подписки, которые начинаются с "Test".</span><span class="sxs-lookup"><span data-stu-id="572a6-119">This command gets all network interfaces for the current subscription that start with "test".</span></span>

## <span data-ttu-id="572a6-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="572a6-120">PARAMETERS</span></span>

### <span data-ttu-id="572a6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="572a6-121">-DefaultProfile</span></span>
<span data-ttu-id="572a6-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="572a6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="572a6-123">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="572a6-123">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic, GetByResourceIdExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="572a6-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="572a6-124">-Name</span></span>
<span data-ttu-id="572a6-125">Указывает имя сетевого интерфейса, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="572a6-125">Specifies the name of the network interface that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneNic, NoExpandScaleSetNic
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="572a6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="572a6-126">-ResourceGroupName</span></span>
<span data-ttu-id="572a6-127">Указывает имя группы ресурсов, из которой этот командлет получает сетевые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="572a6-127">Specifies the name of the resource group from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneNic
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, NoExpandScaleSetNic, ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="572a6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="572a6-128">-ResourceId</span></span>
<span data-ttu-id="572a6-129">Идентификатор диспетчера ресурсов Azure сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="572a6-129">The Azure resource manager id of the network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="572a6-130">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="572a6-130">-VirtualMachineIndex</span></span>
<span data-ttu-id="572a6-131">Указывает индекс виртуальной машины в наборе масштабов виртуальных машин, на основе которого этот командлет получает сетевые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="572a6-131">Specifies the virtual machine index of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetNic
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="572a6-132">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="572a6-132">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="572a6-133">Указывает имя набора масштабов виртуальной машины, на основе которого этот командлет получает сетевые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="572a6-133">Specifies the name of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetNic
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="572a6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="572a6-134">CommonParameters</span></span>
<span data-ttu-id="572a6-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="572a6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="572a6-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="572a6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="572a6-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="572a6-137">INPUTS</span></span>

### <span data-ttu-id="572a6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="572a6-138">System.String</span></span>

## <span data-ttu-id="572a6-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="572a6-139">OUTPUTS</span></span>

### <span data-ttu-id="572a6-140">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="572a6-140">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="572a6-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="572a6-141">NOTES</span></span>

## <span data-ttu-id="572a6-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="572a6-142">RELATED LINKS</span></span>

[<span data-ttu-id="572a6-143">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="572a6-143">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="572a6-144">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="572a6-144">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="572a6-145">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="572a6-145">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)

