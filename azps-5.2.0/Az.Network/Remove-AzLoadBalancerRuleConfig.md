---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 5ba865b5059e69ae9fb89936a45e432ddff7fb9a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405164"
---
# <span data-ttu-id="203a8-101">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="203a8-101">Remove-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="203a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="203a8-102">SYNOPSIS</span></span>
<span data-ttu-id="203a8-103">Удаляет конфигурацию правил для балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="203a8-103">Removes a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="203a8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="203a8-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="203a8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="203a8-105">DESCRIPTION</span></span>
<span data-ttu-id="203a8-106">Для балансиров нагрузки Azure конфигурация правил удаляется с использованием **cmdlet Remove-AzLoadBalancerRuleConfig.**</span><span class="sxs-lookup"><span data-stu-id="203a8-106">The **Remove-AzLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="203a8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="203a8-107">EXAMPLES</span></span>

### <span data-ttu-id="203a8-108">Пример 1. Удаление конфигурации правил из балансиров нагрузки</span><span class="sxs-lookup"><span data-stu-id="203a8-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="203a8-109">Первая команда получает балансировку нагрузки MyLoadBalancer, а затем сохраняет его в переменной $loadbalancer загрузки.</span><span class="sxs-lookup"><span data-stu-id="203a8-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="203a8-110">Вторая команда удаляет конфигурацию правила MyLBruleName из балансироса нагрузки в $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="203a8-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="203a8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="203a8-111">PARAMETERS</span></span>

### <span data-ttu-id="203a8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="203a8-112">-DefaultProfile</span></span>
<span data-ttu-id="203a8-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="203a8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="203a8-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="203a8-114">-LoadBalancer</span></span>
<span data-ttu-id="203a8-115">Определяет объект **LoadBalancer,** который содержит конфигурацию правил, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="203a8-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="203a8-116">-Name</span><span class="sxs-lookup"><span data-stu-id="203a8-116">-Name</span></span>
<span data-ttu-id="203a8-117">Указывает имя конфигурации правила балансиров нагрузки, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="203a8-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="203a8-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="203a8-118">-Confirm</span></span>
<span data-ttu-id="203a8-119">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="203a8-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="203a8-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="203a8-120">-WhatIf</span></span>
<span data-ttu-id="203a8-121">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="203a8-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="203a8-122">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="203a8-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="203a8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="203a8-123">CommonParameters</span></span>
<span data-ttu-id="203a8-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="203a8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="203a8-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="203a8-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="203a8-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="203a8-126">INPUTS</span></span>

### <span data-ttu-id="203a8-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="203a8-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="203a8-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="203a8-128">OUTPUTS</span></span>

### <span data-ttu-id="203a8-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="203a8-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="203a8-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="203a8-130">NOTES</span></span>

## <span data-ttu-id="203a8-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="203a8-131">RELATED LINKS</span></span>

[<span data-ttu-id="203a8-132">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="203a8-132">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="203a8-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="203a8-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="203a8-134">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="203a8-134">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="203a8-135">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="203a8-135">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="203a8-136">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="203a8-136">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


