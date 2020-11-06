---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetwork.md
ms.openlocfilehash: 2a81b7bf5420bdbf4fa5252d71c511c7152e47fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562779"
---
# <span data-ttu-id="46d4c-101">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="46d4c-101">Set-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="46d4c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="46d4c-102">SYNOPSIS</span></span>
<span data-ttu-id="46d4c-103">Задает состояние цели для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="46d4c-103">Sets the goal state for a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46d4c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="46d4c-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46d4c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46d4c-105">DESCRIPTION</span></span>
<span data-ttu-id="46d4c-106">Командлет **Set-AzureRmVirtualNetwork** задает состояние цели для виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="46d4c-106">The **Set-AzureRmVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="46d4c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="46d4c-107">EXAMPLES</span></span>

### <span data-ttu-id="46d4c-108">1: создание виртуальной сети и удаление одной из ее подсетей.</span><span class="sxs-lookup"><span data-stu-id="46d4c-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create resource group
$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzureRmVirtualNetwork ## Remove subnet from virtual network
```

<span data-ttu-id="46d4c-109">В этом примере создается виртуальная сеть под названием TestResourceGroup с двумя подсетями: frontendSubnet и backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="46d4c-109">This example creates a virtual network called TestResourceGroup with two subnets: frontendSubnet and backendSubnet.</span></span> <span data-ttu-id="46d4c-110">После этого она удаляет подсеть backendSubnet из представления виртуальной сети в памяти.</span><span class="sxs-lookup"><span data-stu-id="46d4c-110">Then it removes backendSubnet subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="46d4c-111">Затем командлет Set-AzureRmVirtualNetwork используется для записи измененного состояния виртуальной сети на стороне службы.</span><span class="sxs-lookup"><span data-stu-id="46d4c-111">The Set-AzureRmVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span> <span data-ttu-id="46d4c-112">При выполнении командлета Set-AzureRmVirtualNetwork удаляется backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="46d4c-112">When the Set-AzureRmVirtualNetwork cmdlet is executed, the backendSubnet is removed.</span></span>

## <span data-ttu-id="46d4c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="46d4c-113">PARAMETERS</span></span>

### <span data-ttu-id="46d4c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46d4c-114">-AsJob</span></span>
<span data-ttu-id="46d4c-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="46d4c-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d4c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46d4c-116">-DefaultProfile</span></span>
<span data-ttu-id="46d4c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="46d4c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46d4c-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="46d4c-118">-VirtualNetwork</span></span>
<span data-ttu-id="46d4c-119">Указывает объект **VirtualNetwork** , который представляет состояние цели.</span><span class="sxs-lookup"><span data-stu-id="46d4c-119">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

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

### <span data-ttu-id="46d4c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46d4c-120">CommonParameters</span></span>
<span data-ttu-id="46d4c-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="46d4c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46d4c-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46d4c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46d4c-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="46d4c-123">INPUTS</span></span>

### <span data-ttu-id="46d4c-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="46d4c-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>
<span data-ttu-id="46d4c-125">Параметры: VirtualNetwork (ByValue)</span><span class="sxs-lookup"><span data-stu-id="46d4c-125">Parameters: VirtualNetwork (ByValue)</span></span>

## <span data-ttu-id="46d4c-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="46d4c-126">OUTPUTS</span></span>

### <span data-ttu-id="46d4c-127">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="46d4c-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="46d4c-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="46d4c-128">NOTES</span></span>

## <span data-ttu-id="46d4c-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46d4c-129">RELATED LINKS</span></span>

[<span data-ttu-id="46d4c-130">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="46d4c-130">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="46d4c-131">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="46d4c-131">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="46d4c-132">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="46d4c-132">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="46d4c-133">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="46d4c-133">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)


