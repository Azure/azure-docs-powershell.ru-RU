---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 87329e4864e4fd91d1a8aec09183fe02d8c498ff
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078922"
---
# <span data-ttu-id="4ced2-101">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ced2-101">Get-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="4ced2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4ced2-102">SYNOPSIS</span></span>
<span data-ttu-id="4ced2-103">Получает конфигурацию правила для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4ced2-103">Gets the rule configuration for a load balancer.</span></span>

## <span data-ttu-id="4ced2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4ced2-104">SYNTAX</span></span>

```
Get-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ced2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ced2-105">DESCRIPTION</span></span>
<span data-ttu-id="4ced2-106">Командлет **Get-AzLoadBalancerRuleConfig** получает одну или несколько конфигураций для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4ced2-106">The **Get-AzLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="4ced2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4ced2-107">EXAMPLES</span></span>

### <span data-ttu-id="4ced2-108">Пример 1: получение конфигурации правила для подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="4ced2-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="4ced2-109">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="4ced2-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="4ced2-110">Вторая команда получает конфигурацию связанного правила с именем MyLBrulename из подсистемы балансировки нагрузки в $slb.</span><span class="sxs-lookup"><span data-stu-id="4ced2-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="4ced2-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4ced2-111">PARAMETERS</span></span>

### <span data-ttu-id="4ced2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ced2-112">-DefaultProfile</span></span>
<span data-ttu-id="4ced2-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ced2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ced2-114">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="4ced2-114">-LoadBalancer</span></span>
<span data-ttu-id="4ced2-115">Указывает подсистему балансировки нагрузки, связанную с конфигурацией правила, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="4ced2-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="4ced2-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4ced2-116">-Name</span></span>
<span data-ttu-id="4ced2-117">Указывает имя конфигурации правила, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="4ced2-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="4ced2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ced2-118">CommonParameters</span></span>
<span data-ttu-id="4ced2-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4ced2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ced2-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ced2-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ced2-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4ced2-121">INPUTS</span></span>

### <span data-ttu-id="4ced2-122">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4ced2-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4ced2-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ced2-123">OUTPUTS</span></span>

### <span data-ttu-id="4ced2-124">Microsoft. Azure. Commands. Network. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="4ced2-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="4ced2-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="4ced2-125">NOTES</span></span>

## <span data-ttu-id="4ced2-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ced2-126">RELATED LINKS</span></span>

[<span data-ttu-id="4ced2-127">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ced2-127">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="4ced2-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4ced2-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="4ced2-129">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ced2-129">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="4ced2-130">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ced2-130">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)

