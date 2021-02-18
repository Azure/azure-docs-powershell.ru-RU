---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: b8683d461fe442ec0ad20098766d975b4cd6ae73
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100227924"
---
# <span data-ttu-id="6b83a-101">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6b83a-101">Get-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="6b83a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b83a-102">SYNOPSIS</span></span>
<span data-ttu-id="6b83a-103">Возвращает конфигурацию исходящие правила в балансе нагрузки.</span><span class="sxs-lookup"><span data-stu-id="6b83a-103">Gets an outbound rule configuration in a load balancer.</span></span>

## <span data-ttu-id="6b83a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6b83a-104">SYNTAX</span></span>

```
Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b83a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b83a-105">DESCRIPTION</span></span>
<span data-ttu-id="6b83a-106">Для **этого можно** получить конфигурацию исходящие правил или список конфигураций правил исходящие в балансе нагрузки.</span><span class="sxs-lookup"><span data-stu-id="6b83a-106">The **Get-AzLoadBalancerOutboundRuleConfig** cmdlet gets an outbound rule configuration or a list of outbound rule configurations in a load balancer.</span></span>

## <span data-ttu-id="6b83a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6b83a-107">EXAMPLES</span></span>

### <span data-ttu-id="6b83a-108">Пример 1. Настройка исходящие правил в балансире нагрузки</span><span class="sxs-lookup"><span data-stu-id="6b83a-108">Example 1: Get an outbound rule configuration in a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

<span data-ttu-id="6b83a-109">Первая команда получает балансировку нагрузки MyLoadBalancer, а затем сохраняет его в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="6b83a-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="6b83a-110">Вторая команда получает конфигурацию исходящие правила MyRule, связанную с этим балансировом нагрузки.</span><span class="sxs-lookup"><span data-stu-id="6b83a-110">The second command gets the outbound rule configuration named MyRule associated with that load balancer.</span></span>

## <span data-ttu-id="6b83a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b83a-111">PARAMETERS</span></span>

### <span data-ttu-id="6b83a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b83a-112">-DefaultProfile</span></span>
<span data-ttu-id="6b83a-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6b83a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b83a-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6b83a-114">-LoadBalancer</span></span>
<span data-ttu-id="6b83a-115">Ссылка на ресурс балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="6b83a-115">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="6b83a-116">-Name</span><span class="sxs-lookup"><span data-stu-id="6b83a-116">-Name</span></span>
<span data-ttu-id="6b83a-117">Имя правила исходящие.</span><span class="sxs-lookup"><span data-stu-id="6b83a-117">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="6b83a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b83a-118">CommonParameters</span></span>
<span data-ttu-id="6b83a-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b83a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b83a-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b83a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b83a-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b83a-121">INPUTS</span></span>

### <span data-ttu-id="6b83a-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6b83a-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6b83a-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6b83a-123">OUTPUTS</span></span>

### <span data-ttu-id="6b83a-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="6b83a-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="6b83a-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6b83a-125">NOTES</span></span>

## <span data-ttu-id="6b83a-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b83a-126">RELATED LINKS</span></span>

[<span data-ttu-id="6b83a-127">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6b83a-127">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="6b83a-128">New-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6b83a-128">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="6b83a-129">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6b83a-129">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="6b83a-130">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6b83a-130">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
