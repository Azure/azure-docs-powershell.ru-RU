---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzBastion.md
ms.openlocfilehash: e2e2feacaefb0ce29c77263c0b733f503b8e9a74
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248556"
---
# <span data-ttu-id="d729f-101">New-AzBastion</span><span class="sxs-lookup"><span data-stu-id="d729f-101">New-AzBastion</span></span>

## <span data-ttu-id="d729f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d729f-102">SYNOPSIS</span></span>
<span data-ttu-id="d729f-103">Создает ресурс Bastion.</span><span class="sxs-lookup"><span data-stu-id="d729f-103">Creates a bastion resource.</span></span>

## <span data-ttu-id="d729f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d729f-104">SYNTAX</span></span>

### <span data-ttu-id="d729f-105">ByPublicIpAddressByVirtualNetwork (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d729f-105">ByPublicIpAddressByVirtualNetwork (Default)</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddress <PSPublicIpAddress>
 -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d729f-106">ByPublicIpAddressByVirtualNetworkRGNameByVirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="d729f-106">ByPublicIpAddressByVirtualNetworkRGNameByVirtualNetworkName</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddress <PSPublicIpAddress>
 -VirtualNetworkRgName <String> -VirtualNetworkName <String> [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d729f-107">ByPublicIpAddressByVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="d729f-107">ByPublicIpAddressByVirtualNetworkId</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddress <PSPublicIpAddress>
 -VirtualNetworkId <String> [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d729f-108">ByPublicIpAddressIdByVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d729f-108">ByPublicIpAddressIdByVirtualNetwork</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressId <String>
 -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d729f-109">ByPublicIpAddressIdByVirtualNetworkRGNameByVirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="d729f-109">ByPublicIpAddressIdByVirtualNetworkRGNameByVirtualNetworkName</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressId <String>
 -VirtualNetworkRgName <String> -VirtualNetworkName <String> [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d729f-110">ByPublicIpAddressIdByVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="d729f-110">ByPublicIpAddressIdByVirtualNetworkId</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressId <String> -VirtualNetworkId <String>
 [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d729f-111">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d729f-111">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetwork</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressRgName <String>
 -PublicIpAddressName <String> -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d729f-112">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="d729f-112">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressRgName <String>
 -PublicIpAddressName <String> -VirtualNetworkRgName <String> -VirtualNetworkName <String> [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d729f-113">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="d729f-113">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkId</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressRgName <String>
 -PublicIpAddressName <String> -VirtualNetworkId <String> [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d729f-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d729f-114">DESCRIPTION</span></span>
<span data-ttu-id="d729f-115">Создает ресурс Bastion. Для этого вам понадобятся общедоступные IP-адреса и VirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="d729f-115">Creates a bastion resource.This will need a Public Ip Address and a VirtualNetwork.</span></span> <span data-ttu-id="d729f-116">В этом VirtualNetwork должна быть подсеть с именем AzureBastionSubnet. IP-адрес pubic должен быть создан с использованием стандартного SKU.</span><span class="sxs-lookup"><span data-stu-id="d729f-116">There must be a subnet with name AzureBastionSubnet in this VirtualNetwork.The Pubic Ip Address must be created with Sku Standard.</span></span>

## <span data-ttu-id="d729f-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d729f-117">EXAMPLES</span></span>

### <span data-ttu-id="d729f-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d729f-118">Example 1</span></span>
```powershell
$subnetName = "AzureBastionSubnet"
$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.0.0/24
$vnet = New-AzVirtualNetwork -Name "TestVnet" -ResourceGroupName "BastionPowershellTest" -Location "westeurope" -AddressPrefix 10.0.0.0/16 -Subnet $subnet
$publicip = New-AzPublicIpAddress -ResourceGroupName "BastionPowershellTest" -name "Test-Ip" -location "westeurope" -AllocationMethod Dynamic -Sku Standard
$bastion = New-AzBastion -ResourceGroupName "BastionPowershellTest" â€“Name "test-Bastion2" -PublicIpAddress $publicip -VirtualNetwork $vnet

IpConfigurations     : {IpConf}
DnsName              : bst-a9ca868f-ddab-4a50-9f45-a443ea8a0187.bastion.azure.com
ProvisioningState    : Succeeded
IpConfigurationsText : [
                         {
                           "Subnet": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/virtualNetworks/TestVnet/subnets/AzureBastionSubnet"
                           },
                           "PublicIpAddress": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/publicIPAddresses/Test-Ip"
                           },
                           "ProvisioningState": "Succeeded",
                           "PrivateIpAllocationMethod": "Dynamic",
                           "Name": "IpConf",
                           "Etag": "W/\"ed810ccd-b3f6-4e22-891e-b0ed0a26d6dd\"",
                           "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/bastionHosts/test-Bastion2/bastionHostIpConfigurations/IpConf"
                         }
                       ]
ResourceGroupName    : BastionPowershellTest
Location             : westeurope
ResourceGuid         :
Type                 : Microsoft.Network/bastionHosts
Tag                  :
TagsTable            :
Name                 : test-Bastion2
Etag                 : W/"ed810ccd-b3f6-4e22-891e-b0ed0a26d6dd"
Id                   : /subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/bastionHosts/test-Bastion2

This example creates a bastion attached to virtual network "vnet" in the same resource group as the bastion.
There must be a subnet with name AzureBastionSubnet in this vnet.
The Ip Address must be created with Sku Standard.
```

### <span data-ttu-id="d729f-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d729f-119">Example 2</span></span>
```powershell
$vnet = Get-AzVirtualNetwork -ResourceGroupName "BastionPowershellTest" -Name "testVnet2"
Add-AzVirtualNetworkSubnetConfig -Name "AzureBastionSubnet" -VirtualNetwork $vnet -AddressPrefix "10.0.0.0/24"
$vnet| Set-AzVirtualNetwork
New-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion2" -PublicIpAddressRgName "BastionPowershellTest" -PublicIpAddressName "testIp2" -VirtualNetworkRgName "BastionPowershellTest" -VirtualNetworkName "testVnet2"

IpConfigurations     : {IpConf}
DnsName              : bst-53757658-c4fd-4908-b1a7-0849e555d489.bastion.azure.com
ProvisioningState    : Succeeded
IpConfigurationsText : [
                         {
                           "Name": "IpConf",
                           "Etag": "W/\"7460e5f6-ad41-438b-a595-a63346ed8f16\"",
                           "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/bastionHosts/testBastion2/bastionHostIpConfigurations/IpConf",
                           "Subnet": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/virtualNetworks/testVnet2/subnets/AzureBastionSubnet"
                           },
                           "PublicIpAddress": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/publicIPAddresses/testIp2"
                           },
                           "ProvisioningState": "Succeeded",
                           "PrivateIpAllocationMethod": "Dynamic"
                         }
                       ]
ResourceGroupName    : BastionPowershellTest
Location             : westeurope
ResourceGuid         :
Type                 : Microsoft.Network/bastionHosts
Tag                  :
TagsTable            :
Name                 : testBastion2
Etag                 : W/"7460e5f6-ad41-438b-a595-a63346ed8f16"
Id                   : /subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/bastionHosts/testBastion2
```

## <span data-ttu-id="d729f-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d729f-120">PARAMETERS</span></span>

### <span data-ttu-id="d729f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d729f-121">-AsJob</span></span>
<span data-ttu-id="d729f-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d729f-122">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d729f-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d729f-123">-Confirm</span></span>
<span data-ttu-id="d729f-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d729f-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d729f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d729f-125">-DefaultProfile</span></span>
<span data-ttu-id="d729f-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d729f-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d729f-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d729f-127">-Name</span></span>
<span data-ttu-id="d729f-128">Имя ресурса Bastion.</span><span class="sxs-lookup"><span data-stu-id="d729f-128">The bastion resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, BastionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d729f-129">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="d729f-129">-PublicIpAddress</span></span>
<span data-ttu-id="d729f-130">Объект общедоступного IP-адреса для Bastion.</span><span class="sxs-lookup"><span data-stu-id="d729f-130">The public IP address object for bastion.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: ByPublicIpAddressByVirtualNetwork, ByPublicIpAddressByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressByVirtualNetworkId
Aliases: PublicIpAddressObject

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d729f-131">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="d729f-131">-PublicIpAddressId</span></span>
<span data-ttu-id="d729f-132">Идентификатор ресурса Azure общедоступного IP-адреса для Bastion.</span><span class="sxs-lookup"><span data-stu-id="d729f-132">The public Ip address Azure resource Id for bastion.</span></span>

```yaml
Type: String
Parameter Sets: ByPublicIpAddressIdByVirtualNetwork, ByPublicIpAddressIdByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressIdByVirtualNetworkId
Aliases: PublicIpAddressResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d729f-133">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="d729f-133">-PublicIpAddressName</span></span>
<span data-ttu-id="d729f-134">Имя ресурса общедоступного IP-адреса для Bastion.</span><span class="sxs-lookup"><span data-stu-id="d729f-134">The public Ip address resource name for bastion.</span></span>

```yaml
Type: String
Parameter Sets: ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetwork, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d729f-135">-PublicIpAddressRgName</span><span class="sxs-lookup"><span data-stu-id="d729f-135">-PublicIpAddressRgName</span></span>
<span data-ttu-id="d729f-136">Имя группы ресурсов "общедоступный IP-адрес" для Bastion.</span><span class="sxs-lookup"><span data-stu-id="d729f-136">The public Ip address resource group name for bastion.</span></span>

```yaml
Type: String
Parameter Sets: ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetwork, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkId
Aliases: PublicIpAddressResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d729f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d729f-137">-ResourceGroupName</span></span>
<span data-ttu-id="d729f-138">Имя группы ресурсов, в которой необходимо создать Bastion.</span><span class="sxs-lookup"><span data-stu-id="d729f-138">The resource group name where you need to create bastion.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d729f-139">-Тег</span><span class="sxs-lookup"><span data-stu-id="d729f-139">-Tag</span></span>
<span data-ttu-id="d729f-140">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d729f-140">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d729f-141">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d729f-141">-VirtualNetwork</span></span>
<span data-ttu-id="d729f-142">Объект виртуальной сети для Bastion.</span><span class="sxs-lookup"><span data-stu-id="d729f-142">The virtual network object for bastion.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: ByPublicIpAddressByVirtualNetwork, ByPublicIpAddressIdByVirtualNetwork, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetwork
Aliases: VirtualNetworkObject

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d729f-143">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="d729f-143">-VirtualNetworkId</span></span>
<span data-ttu-id="d729f-144">Идентификатор ресурса Azure виртуальной сети для Bastion.</span><span class="sxs-lookup"><span data-stu-id="d729f-144">The virtual network Azure resource Id for bastion.</span></span>

```yaml
Type: String
Parameter Sets: ByPublicIpAddressByVirtualNetworkId, ByPublicIpAddressIdByVirtualNetworkId, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkId
Aliases: VirtualNetworkResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d729f-145">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="d729f-145">-VirtualNetworkName</span></span>
<span data-ttu-id="d729f-146">Имя ресурса виртуальной сети для Bastion.</span><span class="sxs-lookup"><span data-stu-id="d729f-146">The virtual network resource name for bastion.</span></span>

```yaml
Type: String
Parameter Sets: ByPublicIpAddressByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressIdByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d729f-147">-VirtualNetworkRgName</span><span class="sxs-lookup"><span data-stu-id="d729f-147">-VirtualNetworkRgName</span></span>
<span data-ttu-id="d729f-148">Имя группы ресурсов виртуальной сети для Bastion.</span><span class="sxs-lookup"><span data-stu-id="d729f-148">The virtual network resource group name for bastion.</span></span>

```yaml
Type: String
Parameter Sets: ByPublicIpAddressByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressIdByVirtualNetworkRGNameByVirtualNetworkName, ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName
Aliases: VirtualNetworkResourceGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d729f-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d729f-149">-WhatIf</span></span>
<span data-ttu-id="d729f-150">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d729f-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d729f-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d729f-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d729f-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d729f-152">CommonParameters</span></span>
<span data-ttu-id="d729f-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d729f-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d729f-154">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d729f-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d729f-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d729f-155">INPUTS</span></span>

### <span data-ttu-id="d729f-156">Ничего</span><span class="sxs-lookup"><span data-stu-id="d729f-156">None</span></span>

## <span data-ttu-id="d729f-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d729f-157">OUTPUTS</span></span>

### <span data-ttu-id="d729f-158">Microsoft. Azure. Commands. Network. Models. PSBastion</span><span class="sxs-lookup"><span data-stu-id="d729f-158">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

## <span data-ttu-id="d729f-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="d729f-159">NOTES</span></span>

## <span data-ttu-id="d729f-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d729f-160">RELATED LINKS</span></span>
[<span data-ttu-id="d729f-161">Get-AzBastion</span><span class="sxs-lookup"><span data-stu-id="d729f-161">Get-AzBastion</span></span>](./Get-AzBastion.md)

[<span data-ttu-id="d729f-162">Remove-AzBastion</span><span class="sxs-lookup"><span data-stu-id="d729f-162">Remove-AzBastion</span></span>](./Remove-AzBastion.md)