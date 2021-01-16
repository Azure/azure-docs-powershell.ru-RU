---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 76cf9e2624c812d99702823b303e4e6427845670
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506873"
---
# <span data-ttu-id="45af5-101">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="45af5-101">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="45af5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45af5-102">SYNOPSIS</span></span>
<span data-ttu-id="45af5-103">Удаляет из балансиров нагрузки конфигурацию входящие правила NAT.</span><span class="sxs-lookup"><span data-stu-id="45af5-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

## <span data-ttu-id="45af5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="45af5-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45af5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45af5-105">DESCRIPTION</span></span>
<span data-ttu-id="45af5-106">Для балансиента загрузки Azure конфигурация правила перевода сетевых адресов (NAT) **Remove-AzLoadBalancerInboundNatRuleConfig** удаляется.</span><span class="sxs-lookup"><span data-stu-id="45af5-106">The **Remove-AzLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="45af5-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="45af5-107">EXAMPLES</span></span>

### <span data-ttu-id="45af5-108">1. Удаление входящий правила NAT из балансиров нагрузки Azure</span><span class="sxs-lookup"><span data-stu-id="45af5-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="45af5-109">Первая команда загружает уже существующий баланс нагрузки "mylb" и сохраняет его в переменной $load балансе.</span><span class="sxs-lookup"><span data-stu-id="45af5-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="45af5-110">Вторая команда удаляет правило NAT, связанное с этим балансировом нагрузки.</span><span class="sxs-lookup"><span data-stu-id="45af5-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="45af5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45af5-111">PARAMETERS</span></span>

### <span data-ttu-id="45af5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45af5-112">-DefaultProfile</span></span>
<span data-ttu-id="45af5-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="45af5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45af5-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="45af5-114">-LoadBalancer</span></span>
<span data-ttu-id="45af5-115">Определяет объект **LoadBalancer,** который содержит конфигурацию правила NAT для входящий сообщений, удаляемую этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45af5-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="45af5-116">-Name</span><span class="sxs-lookup"><span data-stu-id="45af5-116">-Name</span></span>
<span data-ttu-id="45af5-117">Указывает имя конфигурации правила NAT, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45af5-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="45af5-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45af5-118">-Confirm</span></span>
<span data-ttu-id="45af5-119">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45af5-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45af5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45af5-120">-WhatIf</span></span>
<span data-ttu-id="45af5-121">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45af5-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45af5-122">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="45af5-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45af5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45af5-123">CommonParameters</span></span>
<span data-ttu-id="45af5-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45af5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45af5-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45af5-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45af5-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="45af5-126">INPUTS</span></span>

### <span data-ttu-id="45af5-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="45af5-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="45af5-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="45af5-128">OUTPUTS</span></span>

### <span data-ttu-id="45af5-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="45af5-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="45af5-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="45af5-130">NOTES</span></span>

## <span data-ttu-id="45af5-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45af5-131">RELATED LINKS</span></span>

[<span data-ttu-id="45af5-132">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="45af5-132">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="45af5-133">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="45af5-133">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="45af5-134">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="45af5-134">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="45af5-135">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="45af5-135">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


