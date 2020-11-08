---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: cf8afee04e8aaf1a8909988465dc4371575b4309
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074035"
---
# <span data-ttu-id="800de-101">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="800de-101">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="800de-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="800de-102">SYNOPSIS</span></span>
<span data-ttu-id="800de-103">Удаляет конфигурацию входящего пула NAT из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="800de-103">Removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="800de-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="800de-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="800de-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="800de-105">DESCRIPTION</span></span>
<span data-ttu-id="800de-106">Командлет **Remove-AzLoadBalancerInboundNatPoolConfig** удаляет конфигурацию ВХОДЯЩЕГО пула NAT из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="800de-106">The **Remove-AzLoadBalancerInboundNatPoolConfig** cmdlet removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="800de-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="800de-107">EXAMPLES</span></span>

### <span data-ttu-id="800de-108">1: удаление</span><span class="sxs-lookup"><span data-stu-id="800de-108">1: Remove</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzLoadBalancerInboundNatPoolConfig -Name myinboundnatpool -LoadBalancer $slb
```

## <span data-ttu-id="800de-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="800de-109">PARAMETERS</span></span>

### <span data-ttu-id="800de-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="800de-110">-DefaultProfile</span></span>
<span data-ttu-id="800de-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="800de-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="800de-112">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="800de-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="800de-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="800de-113">-Name</span></span>
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

### <span data-ttu-id="800de-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="800de-114">-Confirm</span></span>
<span data-ttu-id="800de-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="800de-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="800de-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="800de-116">-WhatIf</span></span>
<span data-ttu-id="800de-117">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="800de-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="800de-118">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="800de-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="800de-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="800de-119">CommonParameters</span></span>
<span data-ttu-id="800de-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="800de-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="800de-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="800de-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="800de-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="800de-122">INPUTS</span></span>

### <span data-ttu-id="800de-123">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="800de-123">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="800de-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="800de-124">OUTPUTS</span></span>

### <span data-ttu-id="800de-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="800de-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="800de-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="800de-126">NOTES</span></span>

## <span data-ttu-id="800de-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="800de-127">RELATED LINKS</span></span>

[<span data-ttu-id="800de-128">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="800de-128">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="800de-129">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="800de-129">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="800de-130">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="800de-130">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="800de-131">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="800de-131">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
