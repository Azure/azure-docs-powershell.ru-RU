---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
ms.openlocfilehash: c90332967621d4dad35594cc5080143d42a47693
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073100"
---
# <span data-ttu-id="f43a0-101">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f43a0-101">Set-AzPrivateEndpoint</span></span>

## <span data-ttu-id="f43a0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f43a0-102">SYNOPSIS</span></span>
<span data-ttu-id="f43a0-103">Обновляет частную конечную точку.</span><span class="sxs-lookup"><span data-stu-id="f43a0-103">Updates a private endpoint.</span></span>

## <span data-ttu-id="f43a0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f43a0-104">SYNTAX</span></span>

```
Set-AzPrivateEndpoint -PrivateEndpoint <PSPrivateEndpoint> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f43a0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f43a0-105">DESCRIPTION</span></span>
<span data-ttu-id="f43a0-106">Командлет **Set-AzPrivateEndpoint** обновляет частную конечную точку.</span><span class="sxs-lookup"><span data-stu-id="f43a0-106">The **Set-AzPrivateEndpoint** cmdlet updates a private endpoint.</span></span>

## <span data-ttu-id="f43a0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f43a0-107">EXAMPLES</span></span>

### <span data-ttu-id="f43a0-108">1: создает частную конечную точку и заменяет одну из ее подсетей на другую.</span><span class="sxs-lookup"><span data-stu-id="f43a0-108">1: Creates a private endpoint and replace one of its subnets to another</span></span>
```
$virtualNetwork = Get-AzVirtualNetwork -ResourceName MyVirtualNetwork -ResourceGroupName TestResourceGroup
$plsConnection= New-AzPrivateLinkServiceConnection -Name MyPLSConnections -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
$privateEndpoint = New-AzPrivateEndpoint -Name MyPrivateEndpoint -ResourceGroup TestResourceGroup -Location centralus -PirvateLinkServiceConnection $plsConnection -Subnet $virtualNetwork.Subnets[0]

$privateEndpoint.Subnet = $virtualNetwork.Subnet[1]

$privateEndpoint | Set-AzPrivateEndpoint
```

<span data-ttu-id="f43a0-109">В этом примере создается закрытая конечная точка с одной подсетью, после чего она заменяется на другую подсеть из представления виртуальной сети в памяти.</span><span class="sxs-lookup"><span data-stu-id="f43a0-109">This example creates a private endpoint with one subnet, then it replace to another subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="f43a0-110">Затем командлет Set-PrivateEndpoint используется для записи измененного состояния частной конечной точки на стороне службы.</span><span class="sxs-lookup"><span data-stu-id="f43a0-110">The Set-PrivateEndpoint cmdlet is then used to write the modified private endpoint state on the service side.</span></span> 

## <span data-ttu-id="f43a0-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f43a0-111">PARAMETERS</span></span>

### <span data-ttu-id="f43a0-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f43a0-112">-AsJob</span></span>
<span data-ttu-id="f43a0-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f43a0-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f43a0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f43a0-114">-DefaultProfile</span></span>
<span data-ttu-id="f43a0-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f43a0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f43a0-116">-PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f43a0-116">-PrivateEndpoint</span></span>
<span data-ttu-id="f43a0-117">Указывает частный объект конечной точки, представляющий состояние, для которого нужно задать частную конечную точку.</span><span class="sxs-lookup"><span data-stu-id="f43a0-117">Specifies a private endpoint object representing the state to which the private endpoint should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f43a0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f43a0-118">CommonParameters</span></span>
<span data-ttu-id="f43a0-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f43a0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f43a0-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f43a0-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f43a0-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f43a0-121">INPUTS</span></span>

### <span data-ttu-id="f43a0-122">Microsoft. Azure. Commands. Network. Models. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f43a0-122">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="f43a0-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f43a0-123">OUTPUTS</span></span>

### <span data-ttu-id="f43a0-124">Microsoft. Azure. Commands. Network. Models. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f43a0-124">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="f43a0-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="f43a0-125">NOTES</span></span>

## <span data-ttu-id="f43a0-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f43a0-126">RELATED LINKS</span></span>

[<span data-ttu-id="f43a0-127">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f43a0-127">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="f43a0-128">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f43a0-128">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="f43a0-129">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f43a0-129">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)


