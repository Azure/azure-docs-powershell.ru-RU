---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7688CE56-0A25-4409-9676-BF1B67C3F05F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 494c496a9f01b41fde2df07f804f9f0c851c5f61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569303"
---
# <span data-ttu-id="87e6a-101">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="87e6a-101">Get-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="87e6a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="87e6a-102">SYNOPSIS</span></span>
<span data-ttu-id="87e6a-103">Получает подсеть в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="87e6a-103">Gets a subnet in a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87e6a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="87e6a-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87e6a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87e6a-105">DESCRIPTION</span></span>
<span data-ttu-id="87e6a-106">Командлет **Get-AzureRmVirtualNetworkSubnetConfig** получает одну или несколько конфигураций подсети в виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="87e6a-106">The **Get-AzureRmVirtualNetworkSubnetConfig** cmdlet gets one or more subnet configurations in an Azure virtual network.</span></span>

## <span data-ttu-id="87e6a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="87e6a-107">EXAMPLES</span></span>

### <span data-ttu-id="87e6a-108">1: получение подсети в виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="87e6a-108">1: Get a subnet in a virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
    Get-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -VirtualNetwork $virtualNetwork
```

<span data-ttu-id="87e6a-109">В этом примере создается группа ресурсов и виртуальная сеть с единственной подсетью в этой группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="87e6a-109">This example creates a resource group and a virtual network with a single subnet in that resource group.</span></span> <span data-ttu-id="87e6a-110">Затем извлекаются данные об этой подсети.</span><span class="sxs-lookup"><span data-stu-id="87e6a-110">It then retrieves data about that subnet.</span></span>

## <span data-ttu-id="87e6a-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="87e6a-111">PARAMETERS</span></span>

### <span data-ttu-id="87e6a-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="87e6a-112">-Name</span></span>
<span data-ttu-id="87e6a-113">Указывает имя конфигурации подсети, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="87e6a-113">Specifies the name of the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="87e6a-114">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="87e6a-114">-VirtualNetwork</span></span>
<span data-ttu-id="87e6a-115">Указывает объект **VirtualNetwork** , который содержит конфигурацию подсети, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="87e6a-115">Specifies the **VirtualNetwork** object that contains the subnet configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="87e6a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87e6a-116">-DefaultProfile</span></span>
<span data-ttu-id="87e6a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="87e6a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87e6a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87e6a-118">CommonParameters</span></span>
<span data-ttu-id="87e6a-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="87e6a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87e6a-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87e6a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87e6a-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="87e6a-121">INPUTS</span></span>

### <span data-ttu-id="87e6a-122">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="87e6a-122">PSVirtualNetwork</span></span>
<span data-ttu-id="87e6a-123">Параметр "VirtualNetwork" принимает значение типа "PSVirtualNetwork" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="87e6a-123">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="87e6a-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="87e6a-124">OUTPUTS</span></span>

### <span data-ttu-id="87e6a-125">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="87e6a-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="87e6a-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="87e6a-126">NOTES</span></span>

## <span data-ttu-id="87e6a-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87e6a-127">RELATED LINKS</span></span>

[<span data-ttu-id="87e6a-128">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="87e6a-128">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="87e6a-129">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="87e6a-129">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="87e6a-130">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="87e6a-130">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>](./Remove-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="87e6a-131">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="87e6a-131">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


