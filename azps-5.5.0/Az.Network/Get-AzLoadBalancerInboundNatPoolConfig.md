---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 444db99b21289f3c46c2f73a726e44dad8635d39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236996"
---
# <span data-ttu-id="b08fb-101">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b08fb-101">Get-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="b08fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b08fb-102">SYNOPSIS</span></span>
<span data-ttu-id="b08fb-103">Получает одну или несколько конфигураций пула NAT для входящий остаток на балансе нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b08fb-103">Gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="b08fb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b08fb-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b08fb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b08fb-105">DESCRIPTION</span></span>
<span data-ttu-id="b08fb-106">Для **этого вы** можете получить одну или несколько конфигураций пула NAT для входящий остаток на счете нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b08fb-106">The **Get-AzLoadBalancerInboundNatPoolConfig** cmdlet gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="b08fb-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b08fb-107">EXAMPLES</span></span>

### <span data-ttu-id="b08fb-108">1. Получить</span><span class="sxs-lookup"><span data-stu-id="b08fb-108">1: Get</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Get-AzLoadBalancerInboundNatPoolConfig -Name myInboundNatPool
```

## <span data-ttu-id="b08fb-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b08fb-109">PARAMETERS</span></span>

### <span data-ttu-id="b08fb-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b08fb-110">-DefaultProfile</span></span>
<span data-ttu-id="b08fb-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b08fb-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b08fb-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b08fb-112">-LoadBalancer</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b08fb-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b08fb-113">-Name</span></span>
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

### <span data-ttu-id="b08fb-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b08fb-114">CommonParameters</span></span>
<span data-ttu-id="b08fb-115">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b08fb-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b08fb-116">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b08fb-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b08fb-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b08fb-117">INPUTS</span></span>

### <span data-ttu-id="b08fb-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b08fb-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b08fb-119">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b08fb-119">OUTPUTS</span></span>

### <span data-ttu-id="b08fb-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="b08fb-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="b08fb-121">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b08fb-121">NOTES</span></span>

## <span data-ttu-id="b08fb-122">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b08fb-122">RELATED LINKS</span></span>

[<span data-ttu-id="b08fb-123">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b08fb-123">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="b08fb-124">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b08fb-124">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="b08fb-125">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b08fb-125">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="b08fb-126">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b08fb-126">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
