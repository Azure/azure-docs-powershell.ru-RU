---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
ms.openlocfilehash: 049b99ee0d019ae7f845e5e7578d9982e41a7a4b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235990"
---
# <span data-ttu-id="b3de9-101">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b3de9-101">Set-AzLoadBalancer</span></span>

## <span data-ttu-id="b3de9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b3de9-102">SYNOPSIS</span></span>
<span data-ttu-id="b3de9-103">Обновляет подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b3de9-103">Updates a load balancer.</span></span>

## <span data-ttu-id="b3de9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b3de9-104">SYNTAX</span></span>

```
Set-AzLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3de9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3de9-105">DESCRIPTION</span></span>
<span data-ttu-id="b3de9-106">Командлет **Set-AzLoadBalancer** обновляет подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b3de9-106">The **Set-AzLoadBalancer** cmdlet updates a load balancer.</span></span>

## <span data-ttu-id="b3de9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b3de9-107">EXAMPLES</span></span>

### <span data-ttu-id="b3de9-108">Пример 1: изменение подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="b3de9-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="b3de9-109">Первая команда получает подсистему балансировки нагрузки с именем NRPLB и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="b3de9-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="b3de9-110">Вторая команда использует оператор Pipeline для передачи балансировщика нагрузки в $slb на Add-AzLoadBalancerInboundNatRuleConfig, который добавляет правило входящего NAT с именем NewRule.</span><span class="sxs-lookup"><span data-stu-id="b3de9-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>
<span data-ttu-id="b3de9-111">Третья команда передает подсистему балансировки нагрузки в **Set-AzLoadBalancer** , которая обновляет конфигурацию подсистемы балансировки нагрузки и сохраняет ее.</span><span class="sxs-lookup"><span data-stu-id="b3de9-111">The third command passes the load balancer to **Set-AzLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="b3de9-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b3de9-112">PARAMETERS</span></span>

### <span data-ttu-id="b3de9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3de9-113">-AsJob</span></span>
<span data-ttu-id="b3de9-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b3de9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b3de9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3de9-115">-DefaultProfile</span></span>
<span data-ttu-id="b3de9-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b3de9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3de9-117">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="b3de9-117">-LoadBalancer</span></span>
<span data-ttu-id="b3de9-118">Указывает объект подсистемы балансировки нагрузки, представляющий состояние, в которое следует установить подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b3de9-118">Specifies a load balancer object representing the state to which the load balancer should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3de9-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3de9-119">-Confirm</span></span>
<span data-ttu-id="b3de9-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b3de9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3de9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3de9-121">-WhatIf</span></span>
<span data-ttu-id="b3de9-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b3de9-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b3de9-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b3de9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3de9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3de9-124">CommonParameters</span></span>
<span data-ttu-id="b3de9-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b3de9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3de9-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3de9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3de9-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b3de9-127">INPUTS</span></span>

### <span data-ttu-id="b3de9-128">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b3de9-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b3de9-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3de9-129">OUTPUTS</span></span>

### <span data-ttu-id="b3de9-130">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b3de9-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b3de9-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="b3de9-131">NOTES</span></span>

## <span data-ttu-id="b3de9-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3de9-132">RELATED LINKS</span></span>

[<span data-ttu-id="b3de9-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b3de9-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="b3de9-134">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b3de9-134">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="b3de9-135">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b3de9-135">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)


