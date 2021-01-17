---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzBastion.md
ms.openlocfilehash: e2e2feacaefb0ce29c77263c0b733f503b8e9a74
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416108"
---
# <span data-ttu-id="fecd5-101">New-AzBastion</span><span class="sxs-lookup"><span data-stu-id="fecd5-101">New-AzBastion</span></span>

## <span data-ttu-id="fecd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fecd5-102">SYNOPSIS</span></span>
<span data-ttu-id="fecd5-103">Создает ресурс на высвечи.</span><span class="sxs-lookup"><span data-stu-id="fecd5-103">Creates a bastion resource.</span></span>

## <span data-ttu-id="fecd5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fecd5-104">SYNTAX</span></span>

### <span data-ttu-id="fecd5-105">ByPublicIpAddressByVirtualNetwork (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fecd5-105">ByPublicIpAddressByVirtualNetwork (Default)</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddress <PSPublicIpAddress>
 -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fecd5-106">ByPublicIpAddressByVirtualNetworkRGNameByVirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="fecd5-106">ByPublicIpAddressByVirtualNetworkRGNameByVirtualNetworkName</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddress <PSPublicIpAddress>
 -VirtualNetworkRgName <String> -VirtualNetworkName <String> [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fecd5-107">ByPublicIpAddressByVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="fecd5-107">ByPublicIpAddressByVirtualNetworkId</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddress <PSPublicIpAddress>
 -VirtualNetworkId <String> [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fecd5-108">ByPublicIpAddressIdByVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fecd5-108">ByPublicIpAddressIdByVirtualNetwork</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressId <String>
 -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fecd5-109">ByPublicIpAddressIdByVirtualNetworkRGNameByVirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="fecd5-109">ByPublicIpAddressIdByVirtualNetworkRGNameByVirtualNetworkName</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressId <String>
 -VirtualNetworkRgName <String> -VirtualNetworkName <String> [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fecd5-110">ByPublicIpAddressIdByVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="fecd5-110">ByPublicIpAddressIdByVirtualNetworkId</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressId <String> -VirtualNetworkId <String>
 [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fecd5-111">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fecd5-111">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetwork</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressRgName <String>
 -PublicIpAddressName <String> -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fecd5-112">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="fecd5-112">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkRGNameByVirtualNetworkName</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressRgName <String>
 -PublicIpAddressName <String> -VirtualNetworkRgName <String> -VirtualNetworkName <String> [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fecd5-113">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="fecd5-113">ByPublicIpAddressRgNameByPublicIpAddressNameByVirtualNetworkId</span></span>
```
New-AzBastion -ResourceGroupName <String> -Name <String> -PublicIpAddressRgName <String>
 -PublicIpAddressName <String> -VirtualNetworkId <String> [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fecd5-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fecd5-114">DESCRIPTION</span></span>
<span data-ttu-id="fecd5-115">Создает ресурс на высвечи. Для этого потребуется общедоступный IP-адрес и VirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="fecd5-115">Creates a bastion resource.This will need a Public Ip Address and a VirtualNetwork.</span></span> <span data-ttu-id="fecd5-116">В этой службе VirtualNetwork должна быть подсеть с именем AzureBastionSubnet. Для создания PUBIC IP-адреса необходимо использовать стандартный SKU.</span><span class="sxs-lookup"><span data-stu-id="fecd5-116">There must be a subnet with name AzureBastionSubnet in this VirtualNetwork.The Pubic Ip Address must be created with Sku Standard.</span></span>

## <span data-ttu-id="fecd5-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fecd5-117">EXAMPLES</span></span>

### <span data-ttu-id="fecd5-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fecd5-118">Example 1</span></span>
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

### <span data-ttu-id="fecd5-119">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fecd5-119">Example 2</span></span>
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

## <span data-ttu-id="fecd5-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fecd5-120">PARAMETERS</span></span>

### <span data-ttu-id="fecd5-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fecd5-121">-AsJob</span></span>
<span data-ttu-id="fecd5-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="fecd5-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fecd5-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fecd5-123">-Confirm</span></span>
<span data-ttu-id="fecd5-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="fecd5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fecd5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fecd5-125">-DefaultProfile</span></span>
<span data-ttu-id="fecd5-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fecd5-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fecd5-127">-Name</span><span class="sxs-lookup"><span data-stu-id="fecd5-127">-Name</span></span>
<span data-ttu-id="fecd5-128">Название базы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fecd5-128">The bastion resource name.</span></span>

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

### <span data-ttu-id="fecd5-129">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fecd5-129">-PublicIpAddress</span></span>
<span data-ttu-id="fecd5-130">Объект public IP address for bastion (Объект общего IP-адреса).</span><span class="sxs-lookup"><span data-stu-id="fecd5-130">The public IP address object for bastion.</span></span>

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

### <span data-ttu-id="fecd5-131">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="fecd5-131">-PublicIpAddressId</span></span>
<span data-ttu-id="fecd5-132">Общедоступный IP-адрес, ид ресурса Azure для использования в условиях использования.</span><span class="sxs-lookup"><span data-stu-id="fecd5-132">The public Ip address Azure resource Id for bastion.</span></span>

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

### <span data-ttu-id="fecd5-133">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="fecd5-133">-PublicIpAddressName</span></span>
<span data-ttu-id="fecd5-134">Имя ресурса для использования общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="fecd5-134">The public Ip address resource name for bastion.</span></span>

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

### <span data-ttu-id="fecd5-135">-PublicIpAddressRgName</span><span class="sxs-lookup"><span data-stu-id="fecd5-135">-PublicIpAddressRgName</span></span>
<span data-ttu-id="fecd5-136">Имя группы ресурсов для общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="fecd5-136">The public Ip address resource group name for bastion.</span></span>

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

### <span data-ttu-id="fecd5-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fecd5-137">-ResourceGroupName</span></span>
<span data-ttu-id="fecd5-138">Название группы ресурсов, для которой нужно создать подпись.</span><span class="sxs-lookup"><span data-stu-id="fecd5-138">The resource group name where you need to create bastion.</span></span>

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

### <span data-ttu-id="fecd5-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="fecd5-139">-Tag</span></span>
<span data-ttu-id="fecd5-140">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="fecd5-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="fecd5-141">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fecd5-141">-VirtualNetwork</span></span>
<span data-ttu-id="fecd5-142">Объект виртуальной сети для набок.</span><span class="sxs-lookup"><span data-stu-id="fecd5-142">The virtual network object for bastion.</span></span>

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

### <span data-ttu-id="fecd5-143">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="fecd5-143">-VirtualNetworkId</span></span>
<span data-ttu-id="fecd5-144">ИД ресурсов виртуальной сети Azure для использования в условиях баз данных.</span><span class="sxs-lookup"><span data-stu-id="fecd5-144">The virtual network Azure resource Id for bastion.</span></span>

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

### <span data-ttu-id="fecd5-145">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="fecd5-145">-VirtualNetworkName</span></span>
<span data-ttu-id="fecd5-146">Имя виртуального сетевого ресурса для подписи.</span><span class="sxs-lookup"><span data-stu-id="fecd5-146">The virtual network resource name for bastion.</span></span>

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

### <span data-ttu-id="fecd5-147">-VirtualNetworkRgName</span><span class="sxs-lookup"><span data-stu-id="fecd5-147">-VirtualNetworkRgName</span></span>
<span data-ttu-id="fecd5-148">Имя группы ресурсов виртуальной сети для использования в названии.</span><span class="sxs-lookup"><span data-stu-id="fecd5-148">The virtual network resource group name for bastion.</span></span>

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

### <span data-ttu-id="fecd5-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fecd5-149">-WhatIf</span></span>
<span data-ttu-id="fecd5-150">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fecd5-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fecd5-151">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fecd5-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fecd5-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fecd5-152">CommonParameters</span></span>
<span data-ttu-id="fecd5-153">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fecd5-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fecd5-154">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fecd5-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fecd5-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fecd5-155">INPUTS</span></span>

### <span data-ttu-id="fecd5-156">Нет</span><span class="sxs-lookup"><span data-stu-id="fecd5-156">None</span></span>

## <span data-ttu-id="fecd5-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fecd5-157">OUTPUTS</span></span>

### <span data-ttu-id="fecd5-158">Microsoft.Azure.Commands.Network.Models.PSBastion</span><span class="sxs-lookup"><span data-stu-id="fecd5-158">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

## <span data-ttu-id="fecd5-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fecd5-159">NOTES</span></span>

## <span data-ttu-id="fecd5-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fecd5-160">RELATED LINKS</span></span>
[<span data-ttu-id="fecd5-161">Get-AzBastion</span><span class="sxs-lookup"><span data-stu-id="fecd5-161">Get-AzBastion</span></span>](./Get-AzBastion.md)

[<span data-ttu-id="fecd5-162">Remove-AzBastion</span><span class="sxs-lookup"><span data-stu-id="fecd5-162">Remove-AzBastion</span></span>](./Remove-AzBastion.md)