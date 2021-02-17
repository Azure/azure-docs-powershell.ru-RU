---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47FE9EF4-6000-4096-8F04-26A0C6661FDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 7d90ffff788239996f7b79f7e56493611db86e04
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100213529"
---
# <span data-ttu-id="46846-101">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="46846-101">Remove-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="46846-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46846-102">SYNOPSIS</span></span>
<span data-ttu-id="46846-103">Удаляет конфигурацию подсети из виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="46846-103">Removes a subnet configuration from a virtual network.</span></span>

## <span data-ttu-id="46846-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="46846-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46846-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46846-105">DESCRIPTION</span></span>
<span data-ttu-id="46846-106">Командлет **Remove-AzVirtualNetworkSubnetConfig** удаляет подсеть из виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="46846-106">The **Remove-AzVirtualNetworkSubnetConfig** cmdlet removes a subnet from an Azure virtual network.</span></span>

## <span data-ttu-id="46846-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="46846-107">EXAMPLES</span></span>

### <span data-ttu-id="46846-108">1. Удаление подсети из виртуальной сети и обновление виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="46846-108">1: Remove a subnet from a virtual network and update the virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet 
    $frontendSubnet,$backendSubnet

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork 
    $virtualNetwork
    $virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="46846-109">В этом примере создаются группа ресурсов и виртуальная сеть с двумя подсетями.</span><span class="sxs-lookup"><span data-stu-id="46846-109">This example creates a resource group and a virtual network with two subnets.</span></span> <span data-ttu-id="46846-110">Затем она использует команду Remove-AzVirtualNetworkSubnetConfig для удаления подсети "Backend subend" из представления виртуальной сети в памяти.</span><span class="sxs-lookup"><span data-stu-id="46846-110">It then uses the Remove-AzVirtualNetworkSubnetConfig command to remove the backend subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="46846-111">Set-AzVirtualNetwork называется изменением виртуальной сети на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="46846-111">Set-AzVirtualNetwork is then called to modify the virtual network on the server side.</span></span>

## <span data-ttu-id="46846-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46846-112">PARAMETERS</span></span>

### <span data-ttu-id="46846-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46846-113">-DefaultProfile</span></span>
<span data-ttu-id="46846-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="46846-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46846-115">-Name</span><span class="sxs-lookup"><span data-stu-id="46846-115">-Name</span></span>
<span data-ttu-id="46846-116">Имя удаляемой конфигурации подсети.</span><span class="sxs-lookup"><span data-stu-id="46846-116">Specifies the name of the subnet configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46846-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="46846-117">-VirtualNetwork</span></span>
<span data-ttu-id="46846-118">Объект **VirtualNetwork,** который содержит конфигурацию подсети, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="46846-118">Specifies the **VirtualNetwork** object that contains the subnet configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46846-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46846-119">CommonParameters</span></span>
<span data-ttu-id="46846-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46846-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46846-121">Дополнительные сведения см. в http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="46846-121">For more information, see [about_CommonParameters] (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46846-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="46846-122">INPUTS</span></span>

### <span data-ttu-id="46846-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="46846-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="46846-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="46846-124">OUTPUTS</span></span>

### <span data-ttu-id="46846-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="46846-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="46846-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="46846-126">NOTES</span></span>

## <span data-ttu-id="46846-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46846-127">RELATED LINKS</span></span>

[<span data-ttu-id="46846-128">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="46846-128">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="46846-129">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="46846-129">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="46846-130">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="46846-130">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="46846-131">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="46846-131">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


