---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 444db99b21289f3c46c2f73a726e44dad8635d39
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078935"
---
# <span data-ttu-id="a481c-101">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a481c-101">Get-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="a481c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a481c-102">SYNOPSIS</span></span>
<span data-ttu-id="a481c-103">Возвращает один или несколько конфигураций входящего пула NAT из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a481c-103">Gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="a481c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a481c-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a481c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a481c-105">DESCRIPTION</span></span>
<span data-ttu-id="a481c-106">Командлет **Get-AzLoadBalancerInboundNatPoolConfig** получает один или несколько конфигураций ВХОДЯЩЕГО пула NAT из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a481c-106">The **Get-AzLoadBalancerInboundNatPoolConfig** cmdlet gets one or more inbound NAT pool configurations from a load balancer.</span></span>

## <span data-ttu-id="a481c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a481c-107">EXAMPLES</span></span>

### <span data-ttu-id="a481c-108">1: Get</span><span class="sxs-lookup"><span data-stu-id="a481c-108">1: Get</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Get-AzLoadBalancerInboundNatPoolConfig -Name myInboundNatPool
```

## <span data-ttu-id="a481c-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a481c-109">PARAMETERS</span></span>

### <span data-ttu-id="a481c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a481c-110">-DefaultProfile</span></span>
<span data-ttu-id="a481c-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a481c-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a481c-112">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="a481c-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="a481c-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a481c-113">-Name</span></span>
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

### <span data-ttu-id="a481c-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a481c-114">CommonParameters</span></span>
<span data-ttu-id="a481c-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a481c-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a481c-116">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a481c-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a481c-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a481c-117">INPUTS</span></span>

### <span data-ttu-id="a481c-118">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a481c-118">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a481c-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a481c-119">OUTPUTS</span></span>

### <span data-ttu-id="a481c-120">Microsoft. Azure. Commands. Network. Models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="a481c-120">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="a481c-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="a481c-121">NOTES</span></span>

## <span data-ttu-id="a481c-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a481c-122">RELATED LINKS</span></span>

[<span data-ttu-id="a481c-123">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a481c-123">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="a481c-124">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a481c-124">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="a481c-125">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a481c-125">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="a481c-126">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="a481c-126">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)