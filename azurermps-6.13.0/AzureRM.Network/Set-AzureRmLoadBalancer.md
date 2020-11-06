---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
ms.openlocfilehash: 5090d97157e608b2c3f6ef52d6eafa932ae4be50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566441"
---
# <span data-ttu-id="a9c22-101">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a9c22-101">Set-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="a9c22-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a9c22-102">SYNOPSIS</span></span>
<span data-ttu-id="a9c22-103">Задает состояние цели для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a9c22-103">Sets the goal state for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9c22-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a9c22-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9c22-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9c22-105">DESCRIPTION</span></span>
<span data-ttu-id="a9c22-106">Командлет **Set-AzureRmLoadBalancer** задает состояние цели для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="a9c22-106">The **Set-AzureRmLoadBalancer** cmdlet sets the goal state for an Azure load balancer.</span></span>

## <span data-ttu-id="a9c22-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a9c22-107">EXAMPLES</span></span>

### <span data-ttu-id="a9c22-108">Пример 1: изменение подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="a9c22-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzureRmLoadBalancer
```

<span data-ttu-id="a9c22-109">Первая команда получает подсистему балансировки нагрузки с именем NRPLB и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="a9c22-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="a9c22-110">Вторая команда использует оператор Pipeline для передачи балансировщика нагрузки в $slb на Add-AzureRmLoadBalancerInboundNatRuleConfig, который добавляет правило входящего NAT с именем NewRule.</span><span class="sxs-lookup"><span data-stu-id="a9c22-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>
<span data-ttu-id="a9c22-111">Третья команда передает подсистему балансировки нагрузки в **Set-AzureRmLoadBalancer** , которая обновляет конфигурацию подсистемы балансировки нагрузки и сохраняет ее.</span><span class="sxs-lookup"><span data-stu-id="a9c22-111">The third command passes the load balancer to **Set-AzureRmLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="a9c22-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a9c22-112">PARAMETERS</span></span>

### <span data-ttu-id="a9c22-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9c22-113">-AsJob</span></span>
<span data-ttu-id="a9c22-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a9c22-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a9c22-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9c22-115">-DefaultProfile</span></span>
<span data-ttu-id="a9c22-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a9c22-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9c22-117">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="a9c22-117">-LoadBalancer</span></span>
<span data-ttu-id="a9c22-118">Указывает на подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a9c22-118">Specifies a load balancer.</span></span>
<span data-ttu-id="a9c22-119">Этот командлет задает состояние цели для подсистемы балансировки нагрузки, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="a9c22-119">This cmdlet sets the goal state for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="a9c22-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a9c22-120">-Confirm</span></span>
<span data-ttu-id="a9c22-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a9c22-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9c22-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9c22-122">-WhatIf</span></span>
<span data-ttu-id="a9c22-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a9c22-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9c22-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a9c22-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9c22-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9c22-125">CommonParameters</span></span>
<span data-ttu-id="a9c22-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a9c22-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9c22-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9c22-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9c22-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a9c22-128">INPUTS</span></span>

### <span data-ttu-id="a9c22-129">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a9c22-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="a9c22-130">Параметры: подсистема балансировки (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a9c22-130">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="a9c22-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9c22-131">OUTPUTS</span></span>

### <span data-ttu-id="a9c22-132">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a9c22-132">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a9c22-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="a9c22-133">NOTES</span></span>

## <span data-ttu-id="a9c22-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a9c22-134">RELATED LINKS</span></span>

[<span data-ttu-id="a9c22-135">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a9c22-135">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="a9c22-136">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a9c22-136">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="a9c22-137">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a9c22-137">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)


