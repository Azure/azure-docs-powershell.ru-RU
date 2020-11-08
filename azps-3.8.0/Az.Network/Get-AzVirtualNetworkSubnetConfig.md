---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: dcc5e688838508e6917a6732b24d7de3b27b2737
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065838"
---
# <span data-ttu-id="9c8b9-101">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9c8b9-101">Get-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="9c8b9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9c8b9-102">SYNOPSIS</span></span>
<span data-ttu-id="9c8b9-103">Получает подсеть в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="9c8b9-103">Gets a subnet in a virtual network.</span></span>

## <span data-ttu-id="9c8b9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9c8b9-104">SYNTAX</span></span>

### <span data-ttu-id="9c8b9-105">GetByVirtualNetwork (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9c8b9-105">GetByVirtualNetwork (Default)</span></span>
```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c8b9-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9c8b9-106">GetByResourceId</span></span>
```
Get-AzVirtualNetworkSubnetConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c8b9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c8b9-107">DESCRIPTION</span></span>
<span data-ttu-id="9c8b9-108">Командлет **Get-AzVirtualNetworkSubnetConfig** получает одну или несколько конфигураций подсети в виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="9c8b9-108">The **Get-AzVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="9c8b9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9c8b9-109">EXAMPLES</span></span>

### <span data-ttu-id="9c8b9-110">1: получение подсети в виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="9c8b9-110">1: Get a subnet in a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="9c8b9-111">В этом примере создается группа ресурсов и виртуальная сеть с единственной подсетью в этой группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9c8b9-111">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="9c8b9-112">Затем извлекаются данные об этой подсети.</span><span class="sxs-lookup"><span data-stu-id="9c8b9-112">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="9c8b9-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9c8b9-113">PARAMETERS</span></span>

### <span data-ttu-id="9c8b9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c8b9-114">-DefaultProfile</span></span>
<span data-ttu-id="9c8b9-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9c8b9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c8b9-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9c8b9-116">-Name</span></span>
<span data-ttu-id="9c8b9-117">Указывает имя конфигурации подсети, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9c8b9-117">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByVirtualNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c8b9-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c8b9-118">-ResourceId</span></span>
<span data-ttu-id="9c8b9-119">Указывает идентификатор ресурса подсети, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9c8b9-119">Specifies the resource id of the subnet that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c8b9-120">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9c8b9-120">-VirtualNetwork</span></span>
<span data-ttu-id="9c8b9-121">Указывает объект **VirtualNetwork** , который содержит конфигурацию подсети, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9c8b9-121">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: GetByVirtualNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c8b9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c8b9-122">CommonParameters</span></span>
<span data-ttu-id="9c8b9-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9c8b9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c8b9-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c8b9-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c8b9-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9c8b9-125">INPUTS</span></span>

### <span data-ttu-id="9c8b9-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9c8b9-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

### <span data-ttu-id="9c8b9-127">System. String</span><span class="sxs-lookup"><span data-stu-id="9c8b9-127">System.String</span></span>

## <span data-ttu-id="9c8b9-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c8b9-128">OUTPUTS</span></span>

### <span data-ttu-id="9c8b9-129">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="9c8b9-129">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="9c8b9-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="9c8b9-130">NOTES</span></span>

## <span data-ttu-id="9c8b9-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c8b9-131">RELATED LINKS</span></span>

[<span data-ttu-id="9c8b9-132">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9c8b9-132">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9c8b9-133">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9c8b9-133">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9c8b9-134">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9c8b9-134">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="9c8b9-135">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="9c8b9-135">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)
