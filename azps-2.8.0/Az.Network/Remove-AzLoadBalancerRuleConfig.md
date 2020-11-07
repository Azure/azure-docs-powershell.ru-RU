---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 01e132dab83931a48254bb8483cc794d7c619a6e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903454"
---
# <span data-ttu-id="14887-101">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="14887-101">Remove-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="14887-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="14887-102">SYNOPSIS</span></span>
<span data-ttu-id="14887-103">Удаление конфигурации правила для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="14887-103">Removes a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="14887-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="14887-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14887-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14887-105">DESCRIPTION</span></span>
<span data-ttu-id="14887-106">Командлет **Remove-AzLoadBalancerRuleConfig** удаляет конфигурацию правила для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="14887-106">The **Remove-AzLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="14887-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="14887-107">EXAMPLES</span></span>

### <span data-ttu-id="14887-108">Пример 1: Удаление конфигурации правила из подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="14887-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="14887-109">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="14887-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="14887-110">Вторая команда удаляет конфигурацию правила с именем MyLBruleName из подсистемы балансировки нагрузки в $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="14887-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="14887-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="14887-111">PARAMETERS</span></span>

### <span data-ttu-id="14887-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14887-112">-DefaultProfile</span></span>
<span data-ttu-id="14887-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="14887-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14887-114">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="14887-114">-LoadBalancer</span></span>
<span data-ttu-id="14887-115">Указывает объект подсистемы **балансировки** , который содержит конфигурацию правила, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="14887-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="14887-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="14887-116">-Name</span></span>
<span data-ttu-id="14887-117">Указывает имя конфигурации правила подсистемы балансировки нагрузки, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="14887-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="14887-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14887-118">-Confirm</span></span>
<span data-ttu-id="14887-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="14887-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14887-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14887-120">-WhatIf</span></span>
<span data-ttu-id="14887-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="14887-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14887-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="14887-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14887-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14887-123">CommonParameters</span></span>
<span data-ttu-id="14887-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="14887-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14887-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14887-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14887-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="14887-126">INPUTS</span></span>

### <span data-ttu-id="14887-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="14887-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="14887-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="14887-128">OUTPUTS</span></span>

### <span data-ttu-id="14887-129">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="14887-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="14887-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="14887-130">NOTES</span></span>

## <span data-ttu-id="14887-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14887-131">RELATED LINKS</span></span>

[<span data-ttu-id="14887-132">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="14887-132">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="14887-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="14887-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="14887-134">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="14887-134">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="14887-135">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="14887-135">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="14887-136">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="14887-136">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


