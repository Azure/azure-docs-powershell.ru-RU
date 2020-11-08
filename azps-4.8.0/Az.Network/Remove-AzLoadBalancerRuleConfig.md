---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 5ba865b5059e69ae9fb89936a45e432ddff7fb9a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234942"
---
# <span data-ttu-id="35d5c-101">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="35d5c-101">Remove-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="35d5c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="35d5c-102">SYNOPSIS</span></span>
<span data-ttu-id="35d5c-103">Удаление конфигурации правила для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="35d5c-103">Removes a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="35d5c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="35d5c-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35d5c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35d5c-105">DESCRIPTION</span></span>
<span data-ttu-id="35d5c-106">Командлет **Remove-AzLoadBalancerRuleConfig** удаляет конфигурацию правила для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="35d5c-106">The **Remove-AzLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="35d5c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="35d5c-107">EXAMPLES</span></span>

### <span data-ttu-id="35d5c-108">Пример 1: Удаление конфигурации правила из подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="35d5c-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="35d5c-109">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="35d5c-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="35d5c-110">Вторая команда удаляет конфигурацию правила с именем MyLBruleName из подсистемы балансировки нагрузки в $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="35d5c-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="35d5c-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="35d5c-111">PARAMETERS</span></span>

### <span data-ttu-id="35d5c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35d5c-112">-DefaultProfile</span></span>
<span data-ttu-id="35d5c-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35d5c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35d5c-114">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="35d5c-114">-LoadBalancer</span></span>
<span data-ttu-id="35d5c-115">Указывает объект подсистемы **балансировки** , который содержит конфигурацию правила, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="35d5c-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="35d5c-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="35d5c-116">-Name</span></span>
<span data-ttu-id="35d5c-117">Указывает имя конфигурации правила подсистемы балансировки нагрузки, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="35d5c-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="35d5c-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35d5c-118">-Confirm</span></span>
<span data-ttu-id="35d5c-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="35d5c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35d5c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35d5c-120">-WhatIf</span></span>
<span data-ttu-id="35d5c-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="35d5c-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35d5c-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="35d5c-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35d5c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35d5c-123">CommonParameters</span></span>
<span data-ttu-id="35d5c-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="35d5c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35d5c-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35d5c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35d5c-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="35d5c-126">INPUTS</span></span>

### <span data-ttu-id="35d5c-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="35d5c-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="35d5c-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="35d5c-128">OUTPUTS</span></span>

### <span data-ttu-id="35d5c-129">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="35d5c-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="35d5c-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="35d5c-130">NOTES</span></span>

## <span data-ttu-id="35d5c-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35d5c-131">RELATED LINKS</span></span>

[<span data-ttu-id="35d5c-132">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="35d5c-132">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="35d5c-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="35d5c-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="35d5c-134">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="35d5c-134">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="35d5c-135">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="35d5c-135">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="35d5c-136">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="35d5c-136">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)

