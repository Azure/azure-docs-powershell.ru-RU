---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 93b7c79544f79a528fc09203fdae77f8ee76474a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909826"
---
# <span data-ttu-id="ce6dd-101">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ce6dd-101">Get-AzVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="ce6dd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ce6dd-102">SYNOPSIS</span></span>
<span data-ttu-id="ce6dd-103">Получает подсеть в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ce6dd-103">Gets a subnet in a virtual network.</span></span>

## <span data-ttu-id="ce6dd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ce6dd-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce6dd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce6dd-105">DESCRIPTION</span></span>
<span data-ttu-id="ce6dd-106">Командлет **Get-AzVirtualNetworkSubnetConfig** получает одну или несколько конфигураций подсети в виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="ce6dd-106">The **Get-AzVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="ce6dd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ce6dd-107">EXAMPLES</span></span>

### <span data-ttu-id="ce6dd-108">1: получение подсети в виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="ce6dd-108">1: Get a subnet in a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="ce6dd-109">В этом примере создается группа ресурсов и виртуальная сеть с единственной подсетью в этой группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ce6dd-109">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="ce6dd-110">Затем извлекаются данные об этой подсети.</span><span class="sxs-lookup"><span data-stu-id="ce6dd-110">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="ce6dd-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ce6dd-111">PARAMETERS</span></span>

### <span data-ttu-id="ce6dd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce6dd-112">-DefaultProfile</span></span>
<span data-ttu-id="ce6dd-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ce6dd-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce6dd-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ce6dd-114">-Name</span></span>
<span data-ttu-id="ce6dd-115">Указывает имя конфигурации подсети, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ce6dd-115">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce6dd-116">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ce6dd-116">-VirtualNetwork</span></span>
<span data-ttu-id="ce6dd-117">Указывает объект **VirtualNetwork** , который содержит конфигурацию подсети, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ce6dd-117">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce6dd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce6dd-118">CommonParameters</span></span>
<span data-ttu-id="ce6dd-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ce6dd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce6dd-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce6dd-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce6dd-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ce6dd-121">INPUTS</span></span>

### <span data-ttu-id="ce6dd-122">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ce6dd-122">PSVirtualNetwork</span></span>
<span data-ttu-id="ce6dd-123">Параметр "VirtualNetwork" принимает значение типа "PSVirtualNetwork" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="ce6dd-123">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="ce6dd-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce6dd-124">OUTPUTS</span></span>

### <span data-ttu-id="ce6dd-125">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="ce6dd-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="ce6dd-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="ce6dd-126">NOTES</span></span>

## <span data-ttu-id="ce6dd-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ce6dd-127">RELATED LINKS</span></span>

[<span data-ttu-id="ce6dd-128">Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ce6dd-128">Add-AzVirtualNetworkSubnetConfig</span></span>](./Add-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="ce6dd-129">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ce6dd-129">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="ce6dd-130">Remove-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ce6dd-130">Remove-AzVirtualNetworkSubnetConfig</span></span>](./Remove-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="ce6dd-131">Set-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ce6dd-131">Set-AzVirtualNetworkSubnetConfig</span></span>](./Set-AzVirtualNetworkSubnetConfig.md)


