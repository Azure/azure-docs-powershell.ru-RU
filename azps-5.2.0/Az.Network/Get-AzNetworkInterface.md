---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E066BBFA-2E03-431D-85D1-99F230B6AC59
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterface.md
ms.openlocfilehash: 1f49c2de253b41db97719933111a5ec2f9b861d5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393455"
---
# <span data-ttu-id="1e798-101">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="1e798-101">Get-AzNetworkInterface</span></span>

## <span data-ttu-id="1e798-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e798-102">SYNOPSIS</span></span>
<span data-ttu-id="1e798-103">Получает сетевой интерфейс.</span><span class="sxs-lookup"><span data-stu-id="1e798-103">Gets a network interface.</span></span>

## <span data-ttu-id="1e798-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1e798-104">SYNTAX</span></span>

### <span data-ttu-id="1e798-105">NoExpandStandAloneNic (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1e798-105">NoExpandStandAloneNic (Default)</span></span>
```
Get-AzNetworkInterface [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e798-106">ExpandStandAloneNic</span><span class="sxs-lookup"><span data-stu-id="1e798-106">ExpandStandAloneNic</span></span>
```
Get-AzNetworkInterface -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e798-107">NoExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="1e798-107">NoExpandScaleSetNic</span></span>
```
Get-AzNetworkInterface [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e798-108">ExpandScaleSetNic</span><span class="sxs-lookup"><span data-stu-id="1e798-108">ExpandScaleSetNic</span></span>
```
Get-AzNetworkInterface -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1e798-109">GetByResourceIdExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e798-109">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzNetworkInterface -ResourceId <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1e798-110">GetByResourceIdNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e798-110">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzNetworkInterface -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e798-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e798-111">DESCRIPTION</span></span>
<span data-ttu-id="1e798-112">Командлет **Get-AzNetworkInterface** получает сетевой интерфейс Azure или список сетевых интерфейсов Azure в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1e798-112">The **Get-AzNetworkInterface** cmdlet gets an Azure network interface or a list of Azure network interfaces in a resource group.</span></span>

## <span data-ttu-id="1e798-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1e798-113">EXAMPLES</span></span>

### <span data-ttu-id="1e798-114">Пример 1. Получить все сетевые интерфейсы</span><span class="sxs-lookup"><span data-stu-id="1e798-114">Example 1: Get all network interfaces</span></span>
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

<span data-ttu-id="1e798-115">Эта команда получает все сетевые интерфейсы для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="1e798-115">This command gets all network interfaces for the current subscription.</span></span>

### <span data-ttu-id="1e798-116">Пример 2. Получите все сетевые интерфейсы с определенным состоянием подготовка</span><span class="sxs-lookup"><span data-stu-id="1e798-116">Example 2: Get all network interfaces with a specific provisioning state</span></span>
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

<span data-ttu-id="1e798-117">Эта команда получает все сетевые интерфейсы в группе ресурсов ResourceGroup1 с состоянием подготовка успешно.</span><span class="sxs-lookup"><span data-stu-id="1e798-117">This command gets all network interfaces in the resource group named ResourceGroup1 that has a provisioning state of succeeded.</span></span>

### <span data-ttu-id="1e798-118">Пример 3. Использование фильтров для сетевых интерфейсов</span><span class="sxs-lookup"><span data-stu-id="1e798-118">Example 3: Get network interfaces using filtering</span></span>
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

<span data-ttu-id="1e798-119">Эта команда получает все сетевые интерфейсы для текущей подписки, которые начинаются с "test".</span><span class="sxs-lookup"><span data-stu-id="1e798-119">This command gets all network interfaces for the current subscription that start with "test".</span></span>

## <span data-ttu-id="1e798-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e798-120">PARAMETERS</span></span>

### <span data-ttu-id="1e798-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e798-121">-DefaultProfile</span></span>
<span data-ttu-id="1e798-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1e798-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e798-123">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="1e798-123">-ExpandResource</span></span>
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

### <span data-ttu-id="1e798-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1e798-124">-Name</span></span>
<span data-ttu-id="1e798-125">Указывает имя сетевого интерфейса, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e798-125">Specifies the name of the network interface that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1e798-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e798-126">-ResourceGroupName</span></span>
<span data-ttu-id="1e798-127">Имя группы ресурсов, из которой этот cmdlet получает сетевые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="1e798-127">Specifies the name of the resource group from which this cmdlet gets network interfaces.</span></span>

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

### <span data-ttu-id="1e798-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e798-128">-ResourceId</span></span>
<span data-ttu-id="1e798-129">ИД диспетчера ресурсов Azure в сетевом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="1e798-129">The Azure resource manager id of the network interface.</span></span>

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

### <span data-ttu-id="1e798-130">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="1e798-130">-VirtualMachineIndex</span></span>
<span data-ttu-id="1e798-131">Определяет индекс виртуальной машины для набора масштаба виртуальной машины, из которого этот cmdlet получает сетевые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="1e798-131">Specifies the virtual machine index of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

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

### <span data-ttu-id="1e798-132">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="1e798-132">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="1e798-133">Имя набора масштаба виртуальной машины, из которого этот cmdlet получает сетевые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="1e798-133">Specifies the name of the virtual machine scale set from which this cmdlet gets network interfaces.</span></span>

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

### <span data-ttu-id="1e798-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e798-134">CommonParameters</span></span>
<span data-ttu-id="1e798-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e798-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e798-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e798-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e798-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1e798-137">INPUTS</span></span>

### <span data-ttu-id="1e798-138">System.String</span><span class="sxs-lookup"><span data-stu-id="1e798-138">System.String</span></span>

## <span data-ttu-id="1e798-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1e798-139">OUTPUTS</span></span>

### <span data-ttu-id="1e798-140">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="1e798-140">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="1e798-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1e798-141">NOTES</span></span>

## <span data-ttu-id="1e798-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1e798-142">RELATED LINKS</span></span>

[<span data-ttu-id="1e798-143">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="1e798-143">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="1e798-144">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="1e798-144">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="1e798-145">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="1e798-145">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)


