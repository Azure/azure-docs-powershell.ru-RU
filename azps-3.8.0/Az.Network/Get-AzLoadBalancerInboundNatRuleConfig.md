---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 9304471b12f33d677f493a3ee6803a1219d9f977
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073334"
---
# <span data-ttu-id="0e0b7-101">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0e0b7-101">Get-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="0e0b7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0e0b7-102">SYNOPSIS</span></span>
<span data-ttu-id="0e0b7-103">Получает конфигурацию правила NAT для входящего трафика для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="0e0b7-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="0e0b7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0e0b7-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e0b7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e0b7-105">DESCRIPTION</span></span>
<span data-ttu-id="0e0b7-106">Командлет **Get-AzLoadBalancerInboundNatRuleConfig** получает одно или несколько правил трансляции сетевых адресов (NAT) для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="0e0b7-106">The **Get-AzLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="0e0b7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0e0b7-107">EXAMPLES</span></span>

### <span data-ttu-id="0e0b7-108">Пример 1: получение конфигурации правила входящего NAT</span><span class="sxs-lookup"><span data-stu-id="0e0b7-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="0e0b7-109">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в $slb переменной.</span><span class="sxs-lookup"><span data-stu-id="0e0b7-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>
<span data-ttu-id="0e0b7-110">Вторая команда получает соответствующее правило NAT с именем MyInboundNatRule1 из подсистемы балансировки нагрузки в $slb.</span><span class="sxs-lookup"><span data-stu-id="0e0b7-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="0e0b7-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0e0b7-111">PARAMETERS</span></span>

### <span data-ttu-id="0e0b7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e0b7-112">-DefaultProfile</span></span>
<span data-ttu-id="0e0b7-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0e0b7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e0b7-114">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="0e0b7-114">-LoadBalancer</span></span>
<span data-ttu-id="0e0b7-115">Указывает подсистему балансировки нагрузки, связанную с конфигурацией правила входящего NAT для получения.</span><span class="sxs-lookup"><span data-stu-id="0e0b7-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="0e0b7-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0e0b7-116">-Name</span></span>
<span data-ttu-id="0e0b7-117">Указывает имя конфигурации правила входящего NAT, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="0e0b7-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="0e0b7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e0b7-118">CommonParameters</span></span>
<span data-ttu-id="0e0b7-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0e0b7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e0b7-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e0b7-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e0b7-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0e0b7-121">INPUTS</span></span>

### <span data-ttu-id="0e0b7-122">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0e0b7-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0e0b7-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e0b7-123">OUTPUTS</span></span>

### <span data-ttu-id="0e0b7-124">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="0e0b7-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="0e0b7-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="0e0b7-125">NOTES</span></span>

## <span data-ttu-id="0e0b7-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0e0b7-126">RELATED LINKS</span></span>

[<span data-ttu-id="0e0b7-127">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0e0b7-127">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="0e0b7-128">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0e0b7-128">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="0e0b7-129">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0e0b7-129">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="0e0b7-130">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0e0b7-130">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


