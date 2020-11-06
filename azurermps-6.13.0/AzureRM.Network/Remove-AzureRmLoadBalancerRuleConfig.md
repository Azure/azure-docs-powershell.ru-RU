---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: b51c7300296644ffeda75d1fb9e4cf695ff61def
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560047"
---
# <span data-ttu-id="0d287-101">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0d287-101">Remove-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="0d287-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d287-102">SYNOPSIS</span></span>
<span data-ttu-id="0d287-103">Удаление конфигурации правила для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="0d287-103">Removes a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d287-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d287-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d287-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d287-105">DESCRIPTION</span></span>
<span data-ttu-id="0d287-106">Командлет **Remove-AzureRmLoadBalancerRuleConfig** удаляет конфигурацию правила для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="0d287-106">The **Remove-AzureRmLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="0d287-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d287-107">EXAMPLES</span></span>

### <span data-ttu-id="0d287-108">Пример 1: Удаление конфигурации правила из подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="0d287-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="0d287-109">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="0d287-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="0d287-110">Вторая команда удаляет конфигурацию правила с именем MyLBruleName из подсистемы балансировки нагрузки в $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="0d287-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="0d287-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d287-111">PARAMETERS</span></span>

### <span data-ttu-id="0d287-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d287-112">-DefaultProfile</span></span>
<span data-ttu-id="0d287-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0d287-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d287-114">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="0d287-114">-LoadBalancer</span></span>
<span data-ttu-id="0d287-115">Указывает объект подсистемы **балансировки** , который содержит конфигурацию правила, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0d287-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0d287-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0d287-116">-Name</span></span>
<span data-ttu-id="0d287-117">Указывает имя конфигурации правила подсистемы балансировки нагрузки, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0d287-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0d287-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d287-118">-Confirm</span></span>
<span data-ttu-id="0d287-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0d287-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d287-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d287-120">-WhatIf</span></span>
<span data-ttu-id="0d287-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0d287-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d287-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0d287-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d287-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d287-123">CommonParameters</span></span>
<span data-ttu-id="0d287-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d287-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d287-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d287-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d287-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d287-126">INPUTS</span></span>

### <span data-ttu-id="0d287-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0d287-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="0d287-128">Параметры: подсистема балансировки (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0d287-128">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="0d287-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d287-129">OUTPUTS</span></span>

### <span data-ttu-id="0d287-130">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0d287-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0d287-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d287-131">NOTES</span></span>

## <span data-ttu-id="0d287-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d287-132">RELATED LINKS</span></span>

[<span data-ttu-id="0d287-133">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0d287-133">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="0d287-134">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0d287-134">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="0d287-135">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0d287-135">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="0d287-136">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0d287-136">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="0d287-137">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0d287-137">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


