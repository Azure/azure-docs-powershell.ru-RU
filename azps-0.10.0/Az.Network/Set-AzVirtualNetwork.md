---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 93D8A341-540A-43F1-8C62-28323EAA58E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetwork.md
ms.openlocfilehash: dc780e4b05b2f0ccb92f014f658a9b21aa1bd224
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911009"
---
# <span data-ttu-id="59744-101">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="59744-101">Set-AzVirtualNetwork</span></span>

## <span data-ttu-id="59744-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="59744-102">SYNOPSIS</span></span>
<span data-ttu-id="59744-103">Задает состояние цели для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="59744-103">Sets the goal state for a virtual network.</span></span>

## <span data-ttu-id="59744-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="59744-104">SYNTAX</span></span>

```
Set-AzVirtualNetwork -VirtualNetwork <PSVirtualNetwork> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59744-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59744-105">DESCRIPTION</span></span>
<span data-ttu-id="59744-106">Командлет **Set-AzVirtualNetwork** задает состояние цели для виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="59744-106">The **Set-AzVirtualNetwork** cmdlet sets the goal state for an Azure virtual network.</span></span>

## <span data-ttu-id="59744-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="59744-107">EXAMPLES</span></span>

### <span data-ttu-id="59744-108">1: создание виртуальной сети и удаление одной из ее подсетей.</span><span class="sxs-lookup"><span data-stu-id="59744-108">1: Creates a virtual network and removes one of its subnets</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix "10.0.2.0/24"

$virtualNetwork = New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

Remove-AzVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork $virtualNetwork

$virtualNetwork | Set-AzVirtualNetwork
```

<span data-ttu-id="59744-109">В этом примере создается виртуальная сеть с двумя подсетями.</span><span class="sxs-lookup"><span data-stu-id="59744-109">This example creates a virtual network with two subnets.</span></span> <span data-ttu-id="59744-110">Затем она удаляет одну подсеть из представления виртуальной сети в памяти.</span><span class="sxs-lookup"><span data-stu-id="59744-110">Then it removes one subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="59744-111">Затем командлет Set-AzVirtualNetwork используется для записи измененного состояния виртуальной сети на стороне службы.</span><span class="sxs-lookup"><span data-stu-id="59744-111">The Set-AzVirtualNetwork cmdlet is then used to write the modified virtual network state on the service side.</span></span>

## <span data-ttu-id="59744-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="59744-112">PARAMETERS</span></span>

### <span data-ttu-id="59744-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59744-113">-AsJob</span></span>
<span data-ttu-id="59744-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="59744-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59744-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59744-115">-DefaultProfile</span></span>
<span data-ttu-id="59744-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="59744-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59744-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="59744-117">-VirtualNetwork</span></span>
<span data-ttu-id="59744-118">Указывает объект **VirtualNetwork** , который представляет состояние цели.</span><span class="sxs-lookup"><span data-stu-id="59744-118">Specifies a **VirtualNetwork** object that represents the goal state.</span></span>

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

### <span data-ttu-id="59744-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59744-119">CommonParameters</span></span>
<span data-ttu-id="59744-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="59744-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59744-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59744-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59744-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="59744-122">INPUTS</span></span>

### <span data-ttu-id="59744-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="59744-123">PSVirtualNetwork</span></span>
<span data-ttu-id="59744-124">Параметр "VirtualNetwork" принимает значение типа "PSVirtualNetwork" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="59744-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="59744-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="59744-125">OUTPUTS</span></span>

### <span data-ttu-id="59744-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="59744-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="59744-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="59744-127">NOTES</span></span>

## <span data-ttu-id="59744-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59744-128">RELATED LINKS</span></span>

[<span data-ttu-id="59744-129">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="59744-129">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="59744-130">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="59744-130">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="59744-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="59744-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="59744-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="59744-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)


