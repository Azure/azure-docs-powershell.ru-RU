---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: d5782ea85a97df723967d73cf2716d837477f01d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006424"
---
# <span data-ttu-id="5777e-101">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5777e-101">Get-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="5777e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5777e-102">SYNOPSIS</span></span>
<span data-ttu-id="5777e-103">Получает конфигурацию правил для балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="5777e-103">Gets the rule configuration for a load balancer.</span></span>

## <span data-ttu-id="5777e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5777e-104">SYNTAX</span></span>

```
Get-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5777e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5777e-105">DESCRIPTION</span></span>
<span data-ttu-id="5777e-106">Для балансиров нагрузки с его стороны возвращается одна или несколько конфигураций правил для **get-AzLoadBalancerRuleConfig.**</span><span class="sxs-lookup"><span data-stu-id="5777e-106">The **Get-AzLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="5777e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5777e-107">EXAMPLES</span></span>

### <span data-ttu-id="5777e-108">Пример 1. Настройка правил для балансиров нагрузки</span><span class="sxs-lookup"><span data-stu-id="5777e-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="5777e-109">Первая команда получает балансировку нагрузки MyLoadBalancer, а затем сохраняет его в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="5777e-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="5777e-110">Вторая команда получает имя связанного правила MyLBru из балансира нагрузки в $slb.</span><span class="sxs-lookup"><span data-stu-id="5777e-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="5777e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5777e-111">PARAMETERS</span></span>

### <span data-ttu-id="5777e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5777e-112">-DefaultProfile</span></span>
<span data-ttu-id="5777e-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5777e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5777e-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5777e-114">-LoadBalancer</span></span>
<span data-ttu-id="5777e-115">Определяет балансировку нагрузки, связанную с конфигурацией правил, которую нужно получить.</span><span class="sxs-lookup"><span data-stu-id="5777e-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="5777e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="5777e-116">-Name</span></span>
<span data-ttu-id="5777e-117">Указывает имя нужной конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="5777e-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="5777e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5777e-118">CommonParameters</span></span>
<span data-ttu-id="5777e-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5777e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5777e-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5777e-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5777e-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5777e-121">INPUTS</span></span>

### <span data-ttu-id="5777e-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5777e-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="5777e-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5777e-123">OUTPUTS</span></span>

### <span data-ttu-id="5777e-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="5777e-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="5777e-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5777e-125">NOTES</span></span>

## <span data-ttu-id="5777e-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5777e-126">RELATED LINKS</span></span>

[<span data-ttu-id="5777e-127">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5777e-127">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="5777e-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5777e-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="5777e-129">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5777e-129">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="5777e-130">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5777e-130">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


