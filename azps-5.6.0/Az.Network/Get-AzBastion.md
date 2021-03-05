---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzBastion.md
ms.openlocfilehash: ed9e51ea360921aa720dad6dd596248039e3508e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997786"
---
# <span data-ttu-id="99f5e-101">Get-AzBastion</span><span class="sxs-lookup"><span data-stu-id="99f5e-101">Get-AzBastion</span></span>

## <span data-ttu-id="99f5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99f5e-102">SYNOPSIS</span></span>
<span data-ttu-id="99f5e-103">Возвращает ресурс бастов или ресурсы бастов.</span><span class="sxs-lookup"><span data-stu-id="99f5e-103">Gets a Bastion resource or Bastion resources.</span></span>

## <span data-ttu-id="99f5e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="99f5e-104">SYNTAX</span></span>

### <span data-ttu-id="99f5e-105">ListBySubscriptionId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="99f5e-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzBastion [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99f5e-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99f5e-106">ListByResourceGroupName</span></span>
```
Get-AzBastion [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99f5e-107">ByResourceGroupNameByName</span><span class="sxs-lookup"><span data-stu-id="99f5e-107">ByResourceGroupNameByName</span></span>
```
Get-AzBastion -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99f5e-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="99f5e-108">ByResourceId</span></span>
```
Get-AzBastion -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="99f5e-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="99f5e-109">DESCRIPTION</span></span>
<span data-ttu-id="99f5e-110">Для **этого можно выбрать** один или несколько из подписок в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="99f5e-110">The **Get-Bastion** cmdlet gets one or more bastions in a resource group or subscritption.</span></span>

## <span data-ttu-id="99f5e-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="99f5e-111">EXAMPLES</span></span>

### <span data-ttu-id="99f5e-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="99f5e-112">Example 1</span></span>
```powershell
Get-AzBastion

ResourceGroupName    : abagarwaProd-PPTest
Location             : westcentralus
ResourceGuid         :
Type                 : Microsoft.Network/bastionHosts
Tag                  : {}
TagsTable            :
Name                 : abagarwaProd-PPTest-vnet-bastion
Etag                 : W/"55702e34-348f-4b79-bf44-9c306623b7c7"
Id                   : /subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/abagarwaProd-PPTest/providers/Microsoft.Network/bastionHosts/abagarwaProd-PPTest-vnet-bastion

IpConfigurations     : {IpConf}
DnsName              : bst-f594cc74-c21e-44c3-ad5e-5bb93933965f.bastion.azure.com
ProvisioningState    : Succeeded
IpConfigurationsText : [
                         {
                           "Name": "IpConf",
                           "Etag": "W/\"7ae27d14-9260-4e2d-8c48-47e9628a3e3b\"",
                           "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionTest/providers/Microsoft.Network/bastionHosts/BastionTest-vnet-bastion/bastionHostIpConfigurations/IpConf",
                           "Subnet": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionTest/providers/Microsoft.Network/virtualNetworks/BastionTest-vnet/subnets/default"
                           },
                           "PublicIpAddress": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionTest/providers/Microsoft.Network/publicIPAddresses/BastionTest-vnet-ip"
                           },
                           "ProvisioningState": "Succeeded",
                           "PrivateIpAllocationMethod": "Dynamic"
                         }
                       ]
ResourceGroupName    : BastionTest
Location             : westcentralus
ResourceGuid         :
Type                 : Microsoft.Network/bastionHosts
Tag                  : {}
TagsTable            :
Name                 : BastionTest-vnet-bastion
Etag                 : W/"7ae27d14-9260-4e2d-8c48-47e9628a3e3b"
Id                   : /subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionTest/providers/Microsoft.Network/bastionHosts/BastionTest-vnet-bastion

IpConfigurations     : {IpConf}
DnsName              : bst-32359e0c-d6a5-45f1-b196-2f9a4b4b77e8.bastion.azure.com
ProvisioningState    : Succeeded
IpConfigurationsText : [
                         {
                           "Name": "IpConf",
                           "Etag": "W/\"bd537319-3379-4caf-a8dc-be4506f9dd3a\"",
                           "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps1621/providers/Microsoft.Network/bastionHosts/ps5581/bastionHostIpConfigurations/IpConf",
                           "Subnet": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps1621/providers/Microsoft.Network/virtualNetworks/ps7070/subnets/AzureBastionSubnet"
                           },
                           "PublicIpAddress": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps1621/providers/Microsoft.Network/publicIPAddresses/ps2217"
                           },
                           "ProvisioningState": "Succeeded",
                           "PrivateIpAllocationMethod": "Dynamic"
                         }
                       ]
ResourceGroupName    : ps1621
Location             : westcentralus
ResourceGuid         :
Type                 : Microsoft.Network/bastionHosts
Tag                  :
TagsTable            :
Name                 : ps5581
Etag                 : W/"bd537319-3379-4caf-a8dc-be4506f9dd3a"
Id                   : /subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps1621/providers/Microsoft.Network/bastionHosts/ps5581

IpConfigurations     : {IpConf}
DnsName              : bst-aee29973-3b60-44c1-a1de-bd8636e79127.bastion.azure.com
ProvisioningState    : Succeeded
IpConfigurationsText : [
                         {
                           "Name": "IpConf",
                           "Etag": "W/\"42f723dd-f1de-4fd0-b307-3fe82f0b50f7\"",
                           "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps3151/providers/Microsoft.Network/bastionHosts/ps8815/bastionHostIpConfigurations/IpConf",
                           "Subnet": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps3151/providers/Microsoft.Network/virtualNetworks/ps5766/subnets/AzureBastionSubnet"
                           },
                           "PublicIpAddress": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps3151/providers/Microsoft.Network/publicIPAddresses/ps2773"
                           },
                           "ProvisioningState": "Succeeded",
                           "PrivateIpAllocationMethod": "Dynamic"
                         }
                       ]
ResourceGroupName    : ps3151
Location             : westcentralus
ResourceGuid         :
Type                 : Microsoft.Network/bastionHosts
Tag                  :
TagsTable            :
Name                 : ps8815
Etag                 : W/"42f723dd-f1de-4fd0-b307-3fe82f0b50f7"
Id                   : /subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps3151/providers/Microsoft.Network/bastionHosts/ps8815

IpConfigurations     : {IpConf}
DnsName              : bst-746c229d-f144-4699-a7ea-303a15a70457.bastion.azure.com
ProvisioningState    : Succeeded
IpConfigurationsText : [
                         {
                           "Name": "IpConf",
                           "Etag": "W/\"0b11e3e7-330b-4727-b073-dfe458429fcf\"",
                           "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps3429/providers/Microsoft.Network/bastionHosts/ps7790/bastionHostIpConfigurations/IpConf",
                           "Subnet": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps3429/providers/Microsoft.Network/virtualNetworks/ps7582/subnets/AzureBastionSubnet"
                           },
                           "PublicIpAddress": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps3429/providers/Microsoft.Network/publicIPAddresses/ps8199"
                           },
                           "ProvisioningState": "Succeeded",
                           "PrivateIpAllocationMethod": "Dynamic"
                         }
                       ]
```

### <span data-ttu-id="99f5e-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="99f5e-113">Example 2</span></span>
```powershell
Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion"

IpConfigurations     : {IpConf}
DnsName              : bst-0597f607-ab71-46c2-ab2a-777bfa887aff.bastion.azure.com
ProvisioningState    : Succeeded
IpConfigurationsText : [
                         {
                           "Name": "IpConf",
                           "Etag": "W/\"4d023823-3ea8-439a-ac00-20f16fb0c9b2\"",
                           "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/bastionHosts/testBastion/bastionHostIpConfigurations/IpConf",
                           "Subnet": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/virtualNetworks/TestVnet/subnets/AzureBastionSubnet"
                           },
                           "PublicIpAddress": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/publicIPAddresses/Test-Ip"
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
Name                 : testBastion
Etag                 : W/"4d023823-3ea8-439a-ac00-20f16fb0c9b2"
Id                   : /subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/bastionHosts/testBastion
```

## <span data-ttu-id="99f5e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99f5e-114">PARAMETERS</span></span>

### <span data-ttu-id="99f5e-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="99f5e-115">-Confirm</span></span>
<span data-ttu-id="99f5e-116">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="99f5e-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99f5e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99f5e-117">-DefaultProfile</span></span>
<span data-ttu-id="99f5e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="99f5e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99f5e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="99f5e-119">-Name</span></span>
<span data-ttu-id="99f5e-120">Название базы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="99f5e-120">The bastion resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupNameByName
Aliases: ResourceName, BastionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99f5e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99f5e-121">-ResourceGroupName</span></span>
<span data-ttu-id="99f5e-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="99f5e-122">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByResourceGroupNameByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99f5e-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99f5e-123">-ResourceId</span></span>
<span data-ttu-id="99f5e-124">ИД ресурсов Bastion Azure</span><span class="sxs-lookup"><span data-stu-id="99f5e-124">The bastion Azure resource Id</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99f5e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99f5e-125">-WhatIf</span></span>
<span data-ttu-id="99f5e-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99f5e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99f5e-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="99f5e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99f5e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99f5e-128">CommonParameters</span></span>
<span data-ttu-id="99f5e-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99f5e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99f5e-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="99f5e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99f5e-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="99f5e-131">INPUTS</span></span>

### <span data-ttu-id="99f5e-132">Нет</span><span class="sxs-lookup"><span data-stu-id="99f5e-132">None</span></span>

## <span data-ttu-id="99f5e-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="99f5e-133">OUTPUTS</span></span>

### <span data-ttu-id="99f5e-134">Microsoft.Azure.Commands.Network.Models.PSBastion</span><span class="sxs-lookup"><span data-stu-id="99f5e-134">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

### <span data-ttu-id="99f5e-135">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Commands.Network.Models.PSBastion, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.13.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="99f5e-135">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSBastion, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.13.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="99f5e-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="99f5e-136">NOTES</span></span>

## <span data-ttu-id="99f5e-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="99f5e-137">RELATED LINKS</span></span>
[<span data-ttu-id="99f5e-138">New-AzBastion</span><span class="sxs-lookup"><span data-stu-id="99f5e-138">New-AzBastion</span></span>](./New-AzBastion.md)

[<span data-ttu-id="99f5e-139">Remove-AzBastion</span><span class="sxs-lookup"><span data-stu-id="99f5e-139">Remove-AzBastion</span></span>](./Remove-AzBastion.md)
