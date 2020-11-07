---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
ms.openlocfilehash: d16e0579224907885a2239aa0669ae865ed19dd6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730012"
---
# <span data-ttu-id="5bb91-101">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5bb91-101">Set-AzLoadBalancer</span></span>

## <span data-ttu-id="5bb91-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5bb91-102">SYNOPSIS</span></span>
<span data-ttu-id="5bb91-103">Обновляет подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="5bb91-103">Updates a load balancer.</span></span>

## <span data-ttu-id="5bb91-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5bb91-104">SYNTAX</span></span>

```
Set-AzLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bb91-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5bb91-105">DESCRIPTION</span></span>
<span data-ttu-id="5bb91-106">Командлет **Set-AzLoadBalancer** обновляет подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="5bb91-106">The **Set-AzLoadBalancer** cmdlet updates a load balancer.</span></span>

## <span data-ttu-id="5bb91-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5bb91-107">EXAMPLES</span></span>

### <span data-ttu-id="5bb91-108">Пример 1: изменение подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="5bb91-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="5bb91-109">Первая команда получает подсистему балансировки нагрузки с именем NRPLB и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="5bb91-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="5bb91-110">Вторая команда использует оператор Pipeline для передачи балансировщика нагрузки в $slb на Add-AzLoadBalancerInboundNatRuleConfig, который добавляет правило входящего NAT с именем NewRule.</span><span class="sxs-lookup"><span data-stu-id="5bb91-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>
<span data-ttu-id="5bb91-111">Третья команда передает подсистему балансировки нагрузки в **Set-AzLoadBalancer** , которая обновляет конфигурацию подсистемы балансировки нагрузки и сохраняет ее.</span><span class="sxs-lookup"><span data-stu-id="5bb91-111">The third command passes the load balancer to **Set-AzLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="5bb91-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5bb91-112">PARAMETERS</span></span>

### <span data-ttu-id="5bb91-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5bb91-113">-AsJob</span></span>
<span data-ttu-id="5bb91-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5bb91-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5bb91-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bb91-115">-DefaultProfile</span></span>
<span data-ttu-id="5bb91-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5bb91-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bb91-117">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="5bb91-117">-LoadBalancer</span></span>
<span data-ttu-id="5bb91-118">Указывает объект подсистемы балансировки нагрузки, представляющий состояние, в которое следует установить подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="5bb91-118">Specifies a load balancer object representing the state to which the load balancer should be set.</span></span>

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

### <span data-ttu-id="5bb91-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5bb91-119">-Confirm</span></span>
<span data-ttu-id="5bb91-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5bb91-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bb91-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bb91-121">-WhatIf</span></span>
<span data-ttu-id="5bb91-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5bb91-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5bb91-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5bb91-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bb91-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bb91-124">CommonParameters</span></span>
<span data-ttu-id="5bb91-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5bb91-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bb91-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bb91-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bb91-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5bb91-127">INPUTS</span></span>

### <span data-ttu-id="5bb91-128">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5bb91-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="5bb91-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5bb91-129">OUTPUTS</span></span>

### <span data-ttu-id="5bb91-130">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5bb91-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="5bb91-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="5bb91-131">NOTES</span></span>

## <span data-ttu-id="5bb91-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5bb91-132">RELATED LINKS</span></span>

[<span data-ttu-id="5bb91-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5bb91-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="5bb91-134">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5bb91-134">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="5bb91-135">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5bb91-135">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)


