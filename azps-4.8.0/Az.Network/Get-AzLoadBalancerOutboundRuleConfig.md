---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: b8683d461fe442ec0ad20098766d975b4cd6ae73
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078924"
---
# <span data-ttu-id="17562-101">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="17562-101">Get-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="17562-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="17562-102">SYNOPSIS</span></span>
<span data-ttu-id="17562-103">Получает конфигурацию исходящего правила в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="17562-103">Gets an outbound rule configuration in a load balancer.</span></span>

## <span data-ttu-id="17562-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="17562-104">SYNTAX</span></span>

```
Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17562-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="17562-105">DESCRIPTION</span></span>
<span data-ttu-id="17562-106">Командлет **Get-AzLoadBalancerOutboundRuleConfig** получает конфигурацию исходящего правила или список конфигураций исходящих правил в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="17562-106">The **Get-AzLoadBalancerOutboundRuleConfig** cmdlet gets an outbound rule configuration or a list of outbound rule configurations in a load balancer.</span></span>

## <span data-ttu-id="17562-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="17562-107">EXAMPLES</span></span>

### <span data-ttu-id="17562-108">Пример 1: получение конфигурации исходящего правила в подсистеме балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="17562-108">Example 1: Get an outbound rule configuration in a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

<span data-ttu-id="17562-109">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="17562-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="17562-110">Вторая команда получает конфигурацию исходящего правила с именем MyRule, связанную с этой подсистемой балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="17562-110">The second command gets the outbound rule configuration named MyRule associated with that load balancer.</span></span>

## <span data-ttu-id="17562-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="17562-111">PARAMETERS</span></span>

### <span data-ttu-id="17562-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17562-112">-DefaultProfile</span></span>
<span data-ttu-id="17562-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="17562-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17562-114">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="17562-114">-LoadBalancer</span></span>
<span data-ttu-id="17562-115">Ссылка на ресурс подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="17562-115">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="17562-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="17562-116">-Name</span></span>
<span data-ttu-id="17562-117">Имя правила исходящего трафика.</span><span class="sxs-lookup"><span data-stu-id="17562-117">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="17562-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17562-118">CommonParameters</span></span>
<span data-ttu-id="17562-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="17562-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17562-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17562-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17562-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="17562-121">INPUTS</span></span>

### <span data-ttu-id="17562-122">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="17562-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="17562-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="17562-123">OUTPUTS</span></span>

### <span data-ttu-id="17562-124">Microsoft. Azure. Commands. Network. Models. PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="17562-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="17562-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="17562-125">NOTES</span></span>

## <span data-ttu-id="17562-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="17562-126">RELATED LINKS</span></span>

[<span data-ttu-id="17562-127">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="17562-127">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="17562-128">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="17562-128">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="17562-129">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="17562-129">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="17562-130">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="17562-130">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
