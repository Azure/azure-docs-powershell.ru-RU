---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: 3d3667e73988b50e5c7cab09d07c6ba1a32d072b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904373"
---
# <span data-ttu-id="df0e3-101">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="df0e3-101">Set-AzVirtualNetwork</span></span>

## <span data-ttu-id="df0e3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="df0e3-102">SYNOPSIS</span></span>
<span data-ttu-id="df0e3-103">Обновляет виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="df0e3-103">Updates a virtual network.</span></span>

## <span data-ttu-id="df0e3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="df0e3-104">SYNTAX</span></span>

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df0e3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="df0e3-105">DESCRIPTION</span></span>
<span data-ttu-id="df0e3-106">Командлет **Set-AzVirtualNetwork** обновляет виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="df0e3-106">The **Set-AzVirtualNetwork** cmdlet updates a virtual network.</span></span>

## <span data-ttu-id="df0e3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="df0e3-107">EXAMPLES</span></span>

### <span data-ttu-id="df0e3-108">1: создание виртуальной сети и удаление одной из ее подсетей.</span><span class="sxs-lookup"><span data-stu-id="df0e3-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create resource group
$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzVirtualNetwork ## Remove subnet from virtual network
```

<span data-ttu-id="df0e3-109">В этом примере создается виртуальная сеть под названием TestResourceGroup с двумя подсетями: frontendSubnet и backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="df0e3-109">This example creates a virtual network called TestResourceGroup with two subnets: frontendSubnet and backendSubnet.</span></span> <span data-ttu-id="df0e3-110">После этого она удаляет подсеть backendSubnet из представления виртуальной сети в памяти.</span><span class="sxs-lookup"><span data-stu-id="df0e3-110">Then it removes backendSubnet subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="df0e3-111">Затем командлет Set-AzVirtualNetwork используется для записи измененного состояния виртуальной сети на стороне службы.</span><span class="sxs-lookup"><span data-stu-id="df0e3-111">The Set-AzVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span> <span data-ttu-id="df0e3-112">При выполнении командлета Set-AzVirtualNetwork удаляется backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="df0e3-112">When the Set-AzVirtualNetwork cmdlet is executed, the backendSubnet is removed.</span></span>

## <span data-ttu-id="df0e3-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="df0e3-113">PARAMETERS</span></span>

### <span data-ttu-id="df0e3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df0e3-114">-AsJob</span></span>
<span data-ttu-id="df0e3-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="df0e3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="df0e3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df0e3-116">-DefaultProfile</span></span>
<span data-ttu-id="df0e3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="df0e3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df0e3-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="df0e3-118">-VirtualNetwork</span></span>
<span data-ttu-id="df0e3-119">Указывает объект виртуальной сети, представляющий состояние, в котором следует настроить виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="df0e3-119">Specifies a virtual network object representing the state to which the virtual network should be set.</span></span>

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

### <span data-ttu-id="df0e3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df0e3-120">CommonParameters</span></span>
<span data-ttu-id="df0e3-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="df0e3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df0e3-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df0e3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df0e3-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="df0e3-123">INPUTS</span></span>

### <span data-ttu-id="df0e3-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="df0e3-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="df0e3-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="df0e3-125">OUTPUTS</span></span>

### <span data-ttu-id="df0e3-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="df0e3-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="df0e3-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="df0e3-127">NOTES</span></span>

## <span data-ttu-id="df0e3-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="df0e3-128">RELATED LINKS</span></span>

[<span data-ttu-id="df0e3-129">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="df0e3-129">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="df0e3-130">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="df0e3-130">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="df0e3-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="df0e3-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="df0e3-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="df0e3-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)


