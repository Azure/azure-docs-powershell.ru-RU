---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47FE9EF4-6000-4096-8F04-26A0C6661FDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 92550eb08fb6abf704d450f323e3fd0b724d9942
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730096"
---
# <span data-ttu-id="9630c-101">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9630c-101">Remove-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="9630c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9630c-102">SYNOPSIS</span></span>
<span data-ttu-id="9630c-103">Удаление конфигурации подсети из виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="9630c-103">Removes a subnet configuration from a virtual network.</span></span>

## <span data-ttu-id="9630c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9630c-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9630c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9630c-105">DESCRIPTION</span></span>
<span data-ttu-id="9630c-106">Командлет **Remove-AzVirtualNetworkSubnetConfig** удаляет подсеть из виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="9630c-106">The **Remove-AzVirtualNetworkSubnetConfig** cmdlet removes a subnet from an Azure virtual network.</span></span>

## <span data-ttu-id="9630c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9630c-107">EXAMPLES</span></span>

### <span data-ttu-id="9630c-108">1: удалите подсеть из виртуальной сети и обновите виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="9630c-108">1: Remove a subnet from a virtual network and update the virtual network</span></span>
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

<span data-ttu-id="9630c-109">В этом примере создается группа ресурсов и виртуальная сеть с двумя подсетями.</span><span class="sxs-lookup"><span data-stu-id="9630c-109">This example creates a resource group and a virtual network with two subnets.</span></span> <span data-ttu-id="9630c-110">Затем она использует команду Remove-AzVirtualNetworkSubnetConfig для удаления подсети сервера из представления виртуальной сети в памяти.</span><span class="sxs-lookup"><span data-stu-id="9630c-110">It then uses the Remove-AzVirtualNetworkSubnetConfig command to remove the backend subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="9630c-111">Set-AzVirtualNetwork вызывается, чтобы изменить виртуальную сеть на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="9630c-111">Set-AzVirtualNetwork is then called to modify the virtual network on the server side.</span></span>

## <span data-ttu-id="9630c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9630c-112">PARAMETERS</span></span>

### <span data-ttu-id="9630c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9630c-113">-DefaultProfile</span></span>
<span data-ttu-id="9630c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9630c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9630c-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9630c-115">-Name</span></span>
<span data-ttu-id="9630c-116">Указывает имя конфигурации подсети, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="9630c-116">Specifies the name of the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="9630c-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9630c-117">-VirtualNetwork</span></span>
<span data-ttu-id="9630c-118">Указывает объект **VirtualNetwork** , содержащий конфигурацию подсети, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="9630c-118">Specifies the **VirtualNetwork** object that contains the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="9630c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9630c-119">CommonParameters</span></span>
<span data-ttu-id="9630c-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9630c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9630c-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9630c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9630c-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9630c-122">INPUTS</span></span>

### <span data-ttu-id="9630c-123">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9630c-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="9630c-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9630c-124">OUTPUTS</span></span>

### <span data-ttu-id="9630c-125">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9630c-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="9630c-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="9630c-126">NOTES</span></span>

## <span data-ttu-id="9630c-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9630c-127">RELATED LINKS</span></span>

[<span data-ttu-id="9630c-128">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9630c-128">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9630c-129">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9630c-129">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9630c-130">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9630c-130">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9630c-131">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9630c-131">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


