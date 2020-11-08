---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: cf8afee04e8aaf1a8909988465dc4371575b4309
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234950"
---
# <span data-ttu-id="664d2-101">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="664d2-101">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="664d2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="664d2-102">SYNOPSIS</span></span>
<span data-ttu-id="664d2-103">Удаляет конфигурацию входящего пула NAT из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="664d2-103">Removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="664d2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="664d2-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="664d2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="664d2-105">DESCRIPTION</span></span>
<span data-ttu-id="664d2-106">Командлет **Remove-AzLoadBalancerInboundNatPoolConfig** удаляет конфигурацию ВХОДЯЩЕГО пула NAT из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="664d2-106">The **Remove-AzLoadBalancerInboundNatPoolConfig** cmdlet removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="664d2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="664d2-107">EXAMPLES</span></span>

### <span data-ttu-id="664d2-108">1: удаление</span><span class="sxs-lookup"><span data-stu-id="664d2-108">1: Remove</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzLoadBalancerInboundNatPoolConfig -Name myinboundnatpool -LoadBalancer $slb
```

## <span data-ttu-id="664d2-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="664d2-109">PARAMETERS</span></span>

### <span data-ttu-id="664d2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="664d2-110">-DefaultProfile</span></span>
<span data-ttu-id="664d2-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="664d2-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="664d2-112">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="664d2-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="664d2-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="664d2-113">-Name</span></span>
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

### <span data-ttu-id="664d2-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="664d2-114">-Confirm</span></span>
<span data-ttu-id="664d2-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="664d2-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="664d2-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="664d2-116">-WhatIf</span></span>
<span data-ttu-id="664d2-117">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="664d2-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="664d2-118">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="664d2-118">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="664d2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="664d2-119">CommonParameters</span></span>
<span data-ttu-id="664d2-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="664d2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="664d2-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="664d2-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="664d2-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="664d2-122">INPUTS</span></span>

### <span data-ttu-id="664d2-123">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="664d2-123">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="664d2-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="664d2-124">OUTPUTS</span></span>

### <span data-ttu-id="664d2-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="664d2-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="664d2-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="664d2-126">NOTES</span></span>

## <span data-ttu-id="664d2-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="664d2-127">RELATED LINKS</span></span>

[<span data-ttu-id="664d2-128">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="664d2-128">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="664d2-129">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="664d2-129">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="664d2-130">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="664d2-130">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="664d2-131">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="664d2-131">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
