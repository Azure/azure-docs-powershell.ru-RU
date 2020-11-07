---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 2d47a3481772d846a65e3b0bc0d1eb1c62fa5cd5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730159"
---
# <span data-ttu-id="08709-101">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="08709-101">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="08709-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="08709-102">SYNOPSIS</span></span>
<span data-ttu-id="08709-103">Удаление конфигурации правила входящего трафика NAT из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="08709-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

## <span data-ttu-id="08709-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="08709-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08709-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="08709-105">DESCRIPTION</span></span>
<span data-ttu-id="08709-106">Командлет **Remove-AzLoadBalancerInboundNatRuleConfig** удаляет конфигурацию правила трансляции сетевых адресов (NAT) из подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="08709-106">The **Remove-AzLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="08709-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="08709-107">EXAMPLES</span></span>

### <span data-ttu-id="08709-108">1: Удаление правила входящего NAT из подсистемы балансировки нагрузки для Azure</span><span class="sxs-lookup"><span data-stu-id="08709-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="08709-109">Первая команда загружает уже существующий подсистему балансировки нагрузки под названием "mylb" и сохраняет его в подсистеме балансировки $load.</span><span class="sxs-lookup"><span data-stu-id="08709-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="08709-110">Вторая команда удаляет правило входящего NAT, связанное с этой подсистемой балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="08709-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="08709-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="08709-111">PARAMETERS</span></span>

### <span data-ttu-id="08709-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08709-112">-DefaultProfile</span></span>
<span data-ttu-id="08709-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="08709-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08709-114">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="08709-114">-LoadBalancer</span></span>
<span data-ttu-id="08709-115">Указывает объект подсистемы **балансировки** , который содержит конфигурацию правила входящего NAT, которая удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="08709-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="08709-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="08709-116">-Name</span></span>
<span data-ttu-id="08709-117">Указывает имя конфигурации правила входящего NAT, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="08709-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="08709-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="08709-118">-Confirm</span></span>
<span data-ttu-id="08709-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="08709-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08709-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08709-120">-WhatIf</span></span>
<span data-ttu-id="08709-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="08709-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="08709-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="08709-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08709-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08709-123">CommonParameters</span></span>
<span data-ttu-id="08709-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="08709-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08709-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08709-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08709-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="08709-126">INPUTS</span></span>

### <span data-ttu-id="08709-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="08709-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="08709-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="08709-128">OUTPUTS</span></span>

### <span data-ttu-id="08709-129">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="08709-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="08709-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="08709-130">NOTES</span></span>

## <span data-ttu-id="08709-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="08709-131">RELATED LINKS</span></span>

[<span data-ttu-id="08709-132">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="08709-132">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="08709-133">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="08709-133">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="08709-134">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="08709-134">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="08709-135">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="08709-135">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


