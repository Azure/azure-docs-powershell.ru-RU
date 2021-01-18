---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: 822b982b2c1714e2c0331cc9b64fe2c1753044f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506066"
---
# <span data-ttu-id="bb162-101">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bb162-101">Set-AzVirtualNetwork</span></span>

## <span data-ttu-id="bb162-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb162-102">SYNOPSIS</span></span>
<span data-ttu-id="bb162-103">Обновляет виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="bb162-103">Updates a virtual network.</span></span>

## <span data-ttu-id="bb162-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bb162-104">SYNTAX</span></span>

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb162-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb162-105">DESCRIPTION</span></span>
<span data-ttu-id="bb162-106">Командлет **Set-AzVirtualNetwork** обновляет виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="bb162-106">The **Set-AzVirtualNetwork** cmdlet updates a virtual network.</span></span>

## <span data-ttu-id="bb162-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bb162-107">EXAMPLES</span></span>

### <span data-ttu-id="bb162-108">1. Создание виртуальной сети и удаление одной из ее подсетей</span><span class="sxs-lookup"><span data-stu-id="bb162-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" ## Create resource group
$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24" ## Create backend subnet

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet ## Create virtual network

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork ## Remove subnet from in memory representation of virtual network

$virtualNetwork | Set-AzVirtualNetwork ## Remove subnet from virtual network
```

<span data-ttu-id="bb162-109">В этом примере создается виртуальная сеть TestResourceGroup с двумя подсетями: frontendSubnet и backendSubnet.</span><span class="sxs-lookup"><span data-stu-id="bb162-109">This example creates a virtual network called TestResourceGroup with two subnets: frontendSubnet and backendSubnet.</span></span> <span data-ttu-id="bb162-110">Затем она удаляет подсеть backendSubnet из представления виртуальной сети в памяти.</span><span class="sxs-lookup"><span data-stu-id="bb162-110">Then it removes backendSubnet subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="bb162-111">Затем Set-AzVirtualNetwork записи измененного состояния виртуальной сети на стороне службы.</span><span class="sxs-lookup"><span data-stu-id="bb162-111">The Set-AzVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span> <span data-ttu-id="bb162-112">При Set-AzVirtualNetwork выполняется, backendSubnet удаляется.</span><span class="sxs-lookup"><span data-stu-id="bb162-112">When the Set-AzVirtualNetwork cmdlet is executed, the backendSubnet is removed.</span></span>

## <span data-ttu-id="bb162-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb162-113">PARAMETERS</span></span>

### <span data-ttu-id="bb162-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb162-114">-AsJob</span></span>
<span data-ttu-id="bb162-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="bb162-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bb162-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb162-116">-DefaultProfile</span></span>
<span data-ttu-id="bb162-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bb162-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb162-118">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bb162-118">-VirtualNetwork</span></span>
<span data-ttu-id="bb162-119">Определяет виртуальный объект сети, представляющий состояние, в котором должна быть установлена виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="bb162-119">Specifies a virtual network object representing the state to which the virtual network should be set.</span></span>

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

### <span data-ttu-id="bb162-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb162-120">CommonParameters</span></span>
<span data-ttu-id="bb162-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb162-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb162-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb162-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb162-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bb162-123">INPUTS</span></span>

### <span data-ttu-id="bb162-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bb162-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="bb162-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bb162-125">OUTPUTS</span></span>

### <span data-ttu-id="bb162-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bb162-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="bb162-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bb162-127">NOTES</span></span>

## <span data-ttu-id="bb162-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb162-128">RELATED LINKS</span></span>

[<span data-ttu-id="bb162-129">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bb162-129">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="bb162-130">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bb162-130">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="bb162-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bb162-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="bb162-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bb162-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)


