---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 824675d331d37c93e6bcf3bb3d5da0fa8cbde78b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393124"
---
# <span data-ttu-id="7ea89-101">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7ea89-101">Remove-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="7ea89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ea89-102">SYNOPSIS</span></span>
<span data-ttu-id="7ea89-103">Удаляет конфигурацию исходящие правила из балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="7ea89-103">Removes an outbound rule configuration from a load balancer.</span></span>

## <span data-ttu-id="7ea89-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7ea89-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ea89-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ea89-105">DESCRIPTION</span></span>
<span data-ttu-id="7ea89-106">При **этом из балансиров** нагрузки Azure удаляется конфигурация исходящие правил.</span><span class="sxs-lookup"><span data-stu-id="7ea89-106">The **Remove-AzLoadBalancerOutboundRuleConfig** cmdlet removes an outbound rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="7ea89-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7ea89-107">EXAMPLES</span></span>

### <span data-ttu-id="7ea89-108">Пример 1. Удаление правила исходящие сообщения из балансиров нагрузки Azure</span><span class="sxs-lookup"><span data-stu-id="7ea89-108">Example 1: Delete an outbound rule from an Azure load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Remove-AzLoadBalancerOutboundRuleConfig -Name "RuleName" -LoadBalancer $slb
PS C:\>Set-AzLoadBalancer -LoadBalancer $slb
```

<span data-ttu-id="7ea89-109">Первая команда получает балансировку нагрузки, связанную с конфигурацией правил исходящие, которую вы хотите удалить, и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="7ea89-109">The first command gets the load balancer that is associated with the outbound rule configuration you want to remove, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="7ea89-110">Вторая команда удаляет из балансиров нагрузки связанную конфигурацию исходящие правила.</span><span class="sxs-lookup"><span data-stu-id="7ea89-110">The second command removes the associated outbound rule configuration from the load balancer.</span></span>
<span data-ttu-id="7ea89-111">Третья команда обновляет баланс нагрузки.</span><span class="sxs-lookup"><span data-stu-id="7ea89-111">The third command updates the load balancer.</span></span>

## <span data-ttu-id="7ea89-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ea89-112">PARAMETERS</span></span>

### <span data-ttu-id="7ea89-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ea89-113">-DefaultProfile</span></span>
<span data-ttu-id="7ea89-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7ea89-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ea89-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7ea89-115">-LoadBalancer</span></span>
<span data-ttu-id="7ea89-116">Ссылка на ресурс балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="7ea89-116">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="7ea89-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7ea89-117">-Name</span></span>
<span data-ttu-id="7ea89-118">Имя правила исходящие</span><span class="sxs-lookup"><span data-stu-id="7ea89-118">The Name of outbound rule</span></span>

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

### <span data-ttu-id="7ea89-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ea89-119">-Confirm</span></span>
<span data-ttu-id="7ea89-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ea89-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ea89-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ea89-121">-WhatIf</span></span>
<span data-ttu-id="7ea89-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ea89-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ea89-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7ea89-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ea89-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ea89-124">CommonParameters</span></span>
<span data-ttu-id="7ea89-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ea89-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ea89-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ea89-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ea89-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7ea89-127">INPUTS</span></span>

### <span data-ttu-id="7ea89-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7ea89-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7ea89-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7ea89-129">OUTPUTS</span></span>

### <span data-ttu-id="7ea89-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7ea89-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7ea89-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7ea89-131">NOTES</span></span>

## <span data-ttu-id="7ea89-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7ea89-132">RELATED LINKS</span></span>

[<span data-ttu-id="7ea89-133">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7ea89-133">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="7ea89-134">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7ea89-134">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="7ea89-135">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7ea89-135">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="7ea89-136">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7ea89-136">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
