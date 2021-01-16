---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancer.md
ms.openlocfilehash: 049b99ee0d019ae7f845e5e7578d9982e41a7a4b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414988"
---
# <span data-ttu-id="e0c3a-101">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e0c3a-101">Set-AzLoadBalancer</span></span>

## <span data-ttu-id="e0c3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0c3a-102">SYNOPSIS</span></span>
<span data-ttu-id="e0c3a-103">Обновляет балансировку нагрузки.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-103">Updates a load balancer.</span></span>

## <span data-ttu-id="e0c3a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e0c3a-104">SYNTAX</span></span>

```
Set-AzLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0c3a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0c3a-105">DESCRIPTION</span></span>
<span data-ttu-id="e0c3a-106">Для **балансиров нагрузки обновляется cmdlet Set-AzLoadBalancer.**</span><span class="sxs-lookup"><span data-stu-id="e0c3a-106">The **Set-AzLoadBalancer** cmdlet updates a load balancer.</span></span>

## <span data-ttu-id="e0c3a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e0c3a-107">EXAMPLES</span></span>

### <span data-ttu-id="e0c3a-108">Пример 1. Изменение балансиров нагрузки</span><span class="sxs-lookup"><span data-stu-id="e0c3a-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="e0c3a-109">Первая команда получает баланс нагрузки с именем NRPLB, а затем сохраняет его в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="e0c3a-110">Вторая команда передает балансиру нагрузки в $slb add-AzLoadBalancerInboundNatRuleConfig, который добавляет входящий правило NAT с именем NewRule.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>
<span data-ttu-id="e0c3a-111">Третья команда передает баланс загрузки в **Set-AzLoadBalancer,** который обновляет конфигурацию балансиров нагрузки и сохраняет ее.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-111">The third command passes the load balancer to **Set-AzLoadBalancer**, which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="e0c3a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0c3a-112">PARAMETERS</span></span>

### <span data-ttu-id="e0c3a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0c3a-113">-AsJob</span></span>
<span data-ttu-id="e0c3a-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e0c3a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e0c3a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0c3a-115">-DefaultProfile</span></span>
<span data-ttu-id="e0c3a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0c3a-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e0c3a-117">-LoadBalancer</span></span>
<span data-ttu-id="e0c3a-118">Определяет объект балансиров нагрузки, представляющий состояние, в котором должен быть установлен баланс загрузки.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-118">Specifies a load balancer object representing the state to which the load balancer should be set.</span></span>

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

### <span data-ttu-id="e0c3a-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0c3a-119">-Confirm</span></span>
<span data-ttu-id="e0c3a-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0c3a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0c3a-121">-WhatIf</span></span>
<span data-ttu-id="e0c3a-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0c3a-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0c3a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0c3a-124">CommonParameters</span></span>
<span data-ttu-id="e0c3a-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0c3a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0c3a-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0c3a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0c3a-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e0c3a-127">INPUTS</span></span>

### <span data-ttu-id="e0c3a-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e0c3a-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e0c3a-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e0c3a-129">OUTPUTS</span></span>

### <span data-ttu-id="e0c3a-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e0c3a-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e0c3a-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e0c3a-131">NOTES</span></span>

## <span data-ttu-id="e0c3a-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0c3a-132">RELATED LINKS</span></span>

[<span data-ttu-id="e0c3a-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e0c3a-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="e0c3a-134">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e0c3a-134">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="e0c3a-135">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e0c3a-135">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)


