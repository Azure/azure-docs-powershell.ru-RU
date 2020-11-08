---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 824675d331d37c93e6bcf3bb3d5da0fa8cbde78b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248242"
---
# <span data-ttu-id="1a8ef-101">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1a8ef-101">Remove-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="1a8ef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1a8ef-102">SYNOPSIS</span></span>
<span data-ttu-id="1a8ef-103">Удаляет конфигурацию исходящего правила из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="1a8ef-103">Removes an outbound rule configuration from a load balancer.</span></span>

## <span data-ttu-id="1a8ef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1a8ef-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a8ef-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a8ef-105">DESCRIPTION</span></span>
<span data-ttu-id="1a8ef-106">Командлет **Remove-AzLoadBalancerOutboundRuleConfig** удаляет конфигурацию исходящего правила из подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="1a8ef-106">The **Remove-AzLoadBalancerOutboundRuleConfig** cmdlet removes an outbound rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="1a8ef-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1a8ef-107">EXAMPLES</span></span>

### <span data-ttu-id="1a8ef-108">Пример 1: удаление исходящего правила из подсистемы балансировки нагрузки для Azure</span><span class="sxs-lookup"><span data-stu-id="1a8ef-108">Example 1: Delete an outbound rule from an Azure load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Remove-AzLoadBalancerOutboundRuleConfig -Name "RuleName" -LoadBalancer $slb
PS C:\>Set-AzLoadBalancer -LoadBalancer $slb
```

<span data-ttu-id="1a8ef-109">Первая команда получает подсистему балансировки нагрузки, связанную с конфигурацией исходящего правила, которую вы хотите удалить, и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="1a8ef-109">The first command gets the load balancer that is associated with the outbound rule configuration you want to remove, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="1a8ef-110">Вторая команда удаляет соответствующую конфигурацию исходящего правила из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="1a8ef-110">The second command removes the associated outbound rule configuration from the load balancer.</span></span>
<span data-ttu-id="1a8ef-111">Третья команда обновляет подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="1a8ef-111">The third command updates the load balancer.</span></span>

## <span data-ttu-id="1a8ef-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1a8ef-112">PARAMETERS</span></span>

### <span data-ttu-id="1a8ef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a8ef-113">-DefaultProfile</span></span>
<span data-ttu-id="1a8ef-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1a8ef-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a8ef-115">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="1a8ef-115">-LoadBalancer</span></span>
<span data-ttu-id="1a8ef-116">Ссылка на ресурс подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="1a8ef-116">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="1a8ef-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1a8ef-117">-Name</span></span>
<span data-ttu-id="1a8ef-118">Имя правила для исходящих подключений</span><span class="sxs-lookup"><span data-stu-id="1a8ef-118">The Name of outbound rule</span></span>

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

### <span data-ttu-id="1a8ef-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a8ef-119">-Confirm</span></span>
<span data-ttu-id="1a8ef-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1a8ef-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a8ef-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a8ef-121">-WhatIf</span></span>
<span data-ttu-id="1a8ef-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1a8ef-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a8ef-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1a8ef-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a8ef-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a8ef-124">CommonParameters</span></span>
<span data-ttu-id="1a8ef-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1a8ef-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a8ef-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a8ef-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a8ef-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1a8ef-127">INPUTS</span></span>

### <span data-ttu-id="1a8ef-128">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1a8ef-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="1a8ef-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a8ef-129">OUTPUTS</span></span>

### <span data-ttu-id="1a8ef-130">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1a8ef-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="1a8ef-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="1a8ef-131">NOTES</span></span>

## <span data-ttu-id="1a8ef-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a8ef-132">RELATED LINKS</span></span>

[<span data-ttu-id="1a8ef-133">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1a8ef-133">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="1a8ef-134">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1a8ef-134">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="1a8ef-135">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1a8ef-135">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="1a8ef-136">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1a8ef-136">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
