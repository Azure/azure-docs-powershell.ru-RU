---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 87329e4864e4fd91d1a8aec09183fe02d8c498ff
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246219"
---
# <span data-ttu-id="098d9-101">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="098d9-101">Get-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="098d9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="098d9-102">SYNOPSIS</span></span>
<span data-ttu-id="098d9-103">Получает конфигурацию правила для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="098d9-103">Gets the rule configuration for a load balancer.</span></span>

## <span data-ttu-id="098d9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="098d9-104">SYNTAX</span></span>

```
Get-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="098d9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="098d9-105">DESCRIPTION</span></span>
<span data-ttu-id="098d9-106">Командлет **Get-AzLoadBalancerRuleConfig** получает одну или несколько конфигураций для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="098d9-106">The **Get-AzLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="098d9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="098d9-107">EXAMPLES</span></span>

### <span data-ttu-id="098d9-108">Пример 1: получение конфигурации правила для подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="098d9-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="098d9-109">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="098d9-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="098d9-110">Вторая команда получает конфигурацию связанного правила с именем MyLBrulename из подсистемы балансировки нагрузки в $slb.</span><span class="sxs-lookup"><span data-stu-id="098d9-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="098d9-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="098d9-111">PARAMETERS</span></span>

### <span data-ttu-id="098d9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="098d9-112">-DefaultProfile</span></span>
<span data-ttu-id="098d9-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="098d9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="098d9-114">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="098d9-114">-LoadBalancer</span></span>
<span data-ttu-id="098d9-115">Указывает подсистему балансировки нагрузки, связанную с конфигурацией правила, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="098d9-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="098d9-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="098d9-116">-Name</span></span>
<span data-ttu-id="098d9-117">Указывает имя конфигурации правила, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="098d9-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="098d9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="098d9-118">CommonParameters</span></span>
<span data-ttu-id="098d9-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="098d9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="098d9-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="098d9-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="098d9-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="098d9-121">INPUTS</span></span>

### <span data-ttu-id="098d9-122">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="098d9-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="098d9-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="098d9-123">OUTPUTS</span></span>

### <span data-ttu-id="098d9-124">Microsoft. Azure. Commands. Network. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="098d9-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="098d9-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="098d9-125">NOTES</span></span>

## <span data-ttu-id="098d9-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="098d9-126">RELATED LINKS</span></span>

[<span data-ttu-id="098d9-127">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="098d9-127">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="098d9-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="098d9-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="098d9-129">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="098d9-129">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="098d9-130">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="098d9-130">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)

