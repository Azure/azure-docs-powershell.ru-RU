---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpoint.md
ms.openlocfilehash: 5bacd7c1b98bf7996ee8e6a8f7b188d67cf32073
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016168"
---
# <span data-ttu-id="f8b99-101">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f8b99-101">Set-AzPrivateEndpoint</span></span>

## <span data-ttu-id="f8b99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8b99-102">SYNOPSIS</span></span>
<span data-ttu-id="f8b99-103">Обновляет частную конечную точку.</span><span class="sxs-lookup"><span data-stu-id="f8b99-103">Updates a private endpoint.</span></span>

## <span data-ttu-id="f8b99-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f8b99-104">SYNTAX</span></span>

```
Set-AzPrivateEndpoint -PrivateEndpoint <PSPrivateEndpoint> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f8b99-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8b99-105">DESCRIPTION</span></span>
<span data-ttu-id="f8b99-106">Для личной конечной точки обновляется **cmdlet Set-AzPrivateEndpoint.**</span><span class="sxs-lookup"><span data-stu-id="f8b99-106">The **Set-AzPrivateEndpoint** cmdlet updates a private endpoint.</span></span>

## <span data-ttu-id="f8b99-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f8b99-107">EXAMPLES</span></span>

### <span data-ttu-id="f8b99-108">1. Создание закрытой конечной точки и замена одной из ее подсетей на другую</span><span class="sxs-lookup"><span data-stu-id="f8b99-108">1: Creates a private endpoint and replace one of its subnets to another</span></span>
```
$virtualNetwork = Get-AzVirtualNetwork -ResourceName MyVirtualNetwork -ResourceGroupName TestResourceGroup
$plsConnection= New-AzPrivateLinkServiceConnection -Name MyPLSConnections -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
$privateEndpoint = New-AzPrivateEndpoint -Name MyPrivateEndpoint -ResourceGroup TestResourceGroup -Location centralus -PirvateLinkServiceConnection $plsConnection -Subnet $virtualNetwork.Subnets[0]

$privateEndpoint.Subnet = $virtualNetwork.Subnet[1]

$privateEndpoint | Set-AzPrivateEndpoint
```

<span data-ttu-id="f8b99-109">В этом примере создается частная конечная точка с одной подсетей, которая затем заменяется другой подсетей из представления виртуальной сети в памяти.</span><span class="sxs-lookup"><span data-stu-id="f8b99-109">This example creates a private endpoint with one subnet, then it replace to another subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="f8b99-110">Затем Set-PrivateEndpoint записи измененного состояния закрытой конечной точки на стороне службы.</span><span class="sxs-lookup"><span data-stu-id="f8b99-110">The Set-PrivateEndpoint cmdlet is then used to write the modified private endpoint state on the service side.</span></span> 

## <span data-ttu-id="f8b99-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8b99-111">PARAMETERS</span></span>

### <span data-ttu-id="f8b99-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8b99-112">-AsJob</span></span>
<span data-ttu-id="f8b99-113">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f8b99-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8b99-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8b99-114">-DefaultProfile</span></span>
<span data-ttu-id="f8b99-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f8b99-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8b99-116">-PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f8b99-116">-PrivateEndpoint</span></span>
<span data-ttu-id="f8b99-117">Указывает частный конечный объект, представляющий состояние, в котором должна быть установлена частная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="f8b99-117">Specifies a private endpoint object representing the state to which the private endpoint should be set.</span></span>

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

### <span data-ttu-id="f8b99-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8b99-118">CommonParameters</span></span>
<span data-ttu-id="f8b99-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8b99-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8b99-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8b99-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8b99-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f8b99-121">INPUTS</span></span>

### <span data-ttu-id="f8b99-122">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f8b99-122">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="f8b99-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f8b99-123">OUTPUTS</span></span>

### <span data-ttu-id="f8b99-124">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f8b99-124">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="f8b99-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f8b99-125">NOTES</span></span>

## <span data-ttu-id="f8b99-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8b99-126">RELATED LINKS</span></span>

[<span data-ttu-id="f8b99-127">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f8b99-127">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="f8b99-128">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f8b99-128">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)

[<span data-ttu-id="f8b99-129">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="f8b99-129">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)


