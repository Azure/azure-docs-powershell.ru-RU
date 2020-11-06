---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
ms.openlocfilehash: a5158b1c2d1439286295a2f84f7273b37d608161
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569287"
---
# <span data-ttu-id="81e1f-101">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="81e1f-101">Set-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="81e1f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="81e1f-102">SYNOPSIS</span></span>
<span data-ttu-id="81e1f-103">Задает состояние цели для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="81e1f-103">Sets the goal state for a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81e1f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="81e1f-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="81e1f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="81e1f-105">DESCRIPTION</span></span>
<span data-ttu-id="81e1f-106">Командлет **Set-AzureRmVirtualNetwork** задает состояние цели для виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="81e1f-106">The **Set-AzureRmVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="81e1f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="81e1f-107">EXAMPLES</span></span>

### <span data-ttu-id="81e1f-108">1: создание виртуальной сети и удаление одной из ее подсетей.</span><span class="sxs-lookup"><span data-stu-id="81e1f-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork

$virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="81e1f-109">В этом примере создается виртуальная сеть с двумя подсетями.</span><span class="sxs-lookup"><span data-stu-id="81e1f-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="81e1f-110">Затем она удаляет одну подсеть из представления виртуальной сети в памяти.</span><span class="sxs-lookup"><span data-stu-id="81e1f-110">Then it removes one subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="81e1f-111">Затем командлет Set-AzureRmVirtualNetwork используется для записи измененного состояния виртуальной сети на стороне службы.</span><span class="sxs-lookup"><span data-stu-id="81e1f-111">The Set-AzureRmVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span>

## <span data-ttu-id="81e1f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="81e1f-112">PARAMETERS</span></span>

### <span data-ttu-id="81e1f-113">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="81e1f-113">-VirtualNetwork</span></span>
<span data-ttu-id="81e1f-114">Указывает объект **VirtualNetwork** , который представляет состояние цели.</span><span class="sxs-lookup"><span data-stu-id="81e1f-114">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

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

### <span data-ttu-id="81e1f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81e1f-115">-DefaultProfile</span></span>
<span data-ttu-id="81e1f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="81e1f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81e1f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81e1f-117">CommonParameters</span></span>
<span data-ttu-id="81e1f-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="81e1f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81e1f-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81e1f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81e1f-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="81e1f-120">INPUTS</span></span>

### <span data-ttu-id="81e1f-121">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="81e1f-121">PSVirtualNetwork</span></span>
<span data-ttu-id="81e1f-122">Параметр "VirtualNetwork" принимает значение типа "PSVirtualNetwork" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="81e1f-122">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="81e1f-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="81e1f-123">OUTPUTS</span></span>

### <span data-ttu-id="81e1f-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="81e1f-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="81e1f-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="81e1f-125">NOTES</span></span>

## <span data-ttu-id="81e1f-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="81e1f-126">RELATED LINKS</span></span>

[<span data-ttu-id="81e1f-127">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="81e1f-127">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="81e1f-128">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="81e1f-128">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="81e1f-129">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="81e1f-129">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="81e1f-130">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="81e1f-130">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)


