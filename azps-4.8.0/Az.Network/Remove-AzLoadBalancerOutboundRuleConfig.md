---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 824675d331d37c93e6bcf3bb3d5da0fa8cbde78b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234948"
---
# <span data-ttu-id="c6261-101">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c6261-101">Remove-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="c6261-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c6261-102">SYNOPSIS</span></span>
<span data-ttu-id="c6261-103">Удаляет конфигурацию исходящего правила из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="c6261-103">Removes an outbound rule configuration from a load balancer.</span></span>

## <span data-ttu-id="c6261-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c6261-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6261-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6261-105">DESCRIPTION</span></span>
<span data-ttu-id="c6261-106">Командлет **Remove-AzLoadBalancerOutboundRuleConfig** удаляет конфигурацию исходящего правила из подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="c6261-106">The **Remove-AzLoadBalancerOutboundRuleConfig** cmdlet removes an outbound rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="c6261-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c6261-107">EXAMPLES</span></span>

### <span data-ttu-id="c6261-108">Пример 1: удаление исходящего правила из подсистемы балансировки нагрузки для Azure</span><span class="sxs-lookup"><span data-stu-id="c6261-108">Example 1: Delete an outbound rule from an Azure load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Remove-AzLoadBalancerOutboundRuleConfig -Name "RuleName" -LoadBalancer $slb
PS C:\>Set-AzLoadBalancer -LoadBalancer $slb
```

<span data-ttu-id="c6261-109">Первая команда получает подсистему балансировки нагрузки, связанную с конфигурацией исходящего правила, которую вы хотите удалить, и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="c6261-109">The first command gets the load balancer that is associated with the outbound rule configuration you want to remove, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="c6261-110">Вторая команда удаляет соответствующую конфигурацию исходящего правила из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="c6261-110">The second command removes the associated outbound rule configuration from the load balancer.</span></span>
<span data-ttu-id="c6261-111">Третья команда обновляет подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="c6261-111">The third command updates the load balancer.</span></span>

## <span data-ttu-id="c6261-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c6261-112">PARAMETERS</span></span>

### <span data-ttu-id="c6261-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6261-113">-DefaultProfile</span></span>
<span data-ttu-id="c6261-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c6261-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6261-115">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="c6261-115">-LoadBalancer</span></span>
<span data-ttu-id="c6261-116">Ссылка на ресурс подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="c6261-116">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="c6261-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c6261-117">-Name</span></span>
<span data-ttu-id="c6261-118">Имя правила для исходящих подключений</span><span class="sxs-lookup"><span data-stu-id="c6261-118">The Name of outbound rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6261-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6261-119">-Confirm</span></span>
<span data-ttu-id="c6261-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c6261-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6261-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6261-121">-WhatIf</span></span>
<span data-ttu-id="c6261-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c6261-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6261-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c6261-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6261-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6261-124">CommonParameters</span></span>
<span data-ttu-id="c6261-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c6261-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6261-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6261-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6261-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c6261-127">INPUTS</span></span>

### <span data-ttu-id="c6261-128">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c6261-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c6261-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6261-129">OUTPUTS</span></span>

### <span data-ttu-id="c6261-130">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c6261-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c6261-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="c6261-131">NOTES</span></span>

## <span data-ttu-id="c6261-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c6261-132">RELATED LINKS</span></span>

[<span data-ttu-id="c6261-133">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c6261-133">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="c6261-134">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c6261-134">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="c6261-135">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c6261-135">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="c6261-136">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c6261-136">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
