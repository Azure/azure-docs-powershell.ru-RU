---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47FE9EF4-6000-4096-8F04-26A0C6661FDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 7d90ffff788239996f7b79f7e56493611db86e04
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236000"
---
# <span data-ttu-id="b0db2-101">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b0db2-101">Remove-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="b0db2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b0db2-102">SYNOPSIS</span></span>
<span data-ttu-id="b0db2-103">Удаление конфигурации подсети из виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="b0db2-103">Removes a subnet configuration from a virtual network.</span></span>

## <span data-ttu-id="b0db2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b0db2-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0db2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0db2-105">DESCRIPTION</span></span>
<span data-ttu-id="b0db2-106">Командлет **Remove-AzVirtualNetworkSubnetConfig** удаляет подсеть из виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="b0db2-106">The **Remove-AzVirtualNetworkSubnetConfig** cmdlet removes a subnet from an Azure virtual network.</span></span>

## <span data-ttu-id="b0db2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b0db2-107">EXAMPLES</span></span>

### <span data-ttu-id="b0db2-108">1: удалите подсеть из виртуальной сети и обновите виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="b0db2-108">1: Remove a subnet from a virtual network and update the virtual network</span></span>
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

<span data-ttu-id="b0db2-109">В этом примере создается группа ресурсов и виртуальная сеть с двумя подсетями.</span><span class="sxs-lookup"><span data-stu-id="b0db2-109">This example creates a resource group and a virtual network with two subnets.</span></span> <span data-ttu-id="b0db2-110">Затем она использует команду Remove-AzVirtualNetworkSubnetConfig для удаления подсети сервера из представления виртуальной сети в памяти.</span><span class="sxs-lookup"><span data-stu-id="b0db2-110">It then uses the Remove-AzVirtualNetworkSubnetConfig command to remove the backend subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="b0db2-111">Set-AzVirtualNetwork вызывается, чтобы изменить виртуальную сеть на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="b0db2-111">Set-AzVirtualNetwork is then called to modify the virtual network on the server side.</span></span>

## <span data-ttu-id="b0db2-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b0db2-112">PARAMETERS</span></span>

### <span data-ttu-id="b0db2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0db2-113">-DefaultProfile</span></span>
<span data-ttu-id="b0db2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b0db2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0db2-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b0db2-115">-Name</span></span>
<span data-ttu-id="b0db2-116">Указывает имя конфигурации подсети, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="b0db2-116">Specifies the name of the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="b0db2-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b0db2-117">-VirtualNetwork</span></span>
<span data-ttu-id="b0db2-118">Указывает объект **VirtualNetwork** , содержащий конфигурацию подсети, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="b0db2-118">Specifies the **VirtualNetwork** object that contains the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="b0db2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0db2-119">CommonParameters</span></span>
<span data-ttu-id="b0db2-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b0db2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0db2-121">Дополнительные сведения можно найти в разделе [about_CommonParameters] ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0db2-121">For more information, see [about_CommonParameters] (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0db2-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b0db2-122">INPUTS</span></span>

### <span data-ttu-id="b0db2-123">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b0db2-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="b0db2-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0db2-124">OUTPUTS</span></span>

### <span data-ttu-id="b0db2-125">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b0db2-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="b0db2-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="b0db2-126">NOTES</span></span>

## <span data-ttu-id="b0db2-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b0db2-127">RELATED LINKS</span></span>

[<span data-ttu-id="b0db2-128">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b0db2-128">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b0db2-129">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b0db2-129">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b0db2-130">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b0db2-130">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b0db2-131">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b0db2-131">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


