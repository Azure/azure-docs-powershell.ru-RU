---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 87329e4864e4fd91d1a8aec09183fe02d8c498ff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221193"
---
# <span data-ttu-id="059b1-101">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="059b1-101">Get-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="059b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="059b1-102">SYNOPSIS</span></span>
<span data-ttu-id="059b1-103">Получает конфигурацию правил для балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="059b1-103">Gets the rule configuration for a load balancer.</span></span>

## <span data-ttu-id="059b1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="059b1-104">SYNTAX</span></span>

```
Get-AzLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="059b1-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="059b1-105">DESCRIPTION</span></span>
<span data-ttu-id="059b1-106">Для балансиров нагрузки с его стороны возвращается одна или несколько конфигураций правил для **get-AzLoadBalancerRuleConfig.**</span><span class="sxs-lookup"><span data-stu-id="059b1-106">The **Get-AzLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="059b1-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="059b1-107">EXAMPLES</span></span>

### <span data-ttu-id="059b1-108">Пример 1. Настройка правил для балансиров нагрузки</span><span class="sxs-lookup"><span data-stu-id="059b1-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="059b1-109">Первая команда получает балансировку нагрузки MyLoadBalancer, а затем сохраняет его в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="059b1-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="059b1-110">Вторая команда получает имя связанного правила MyLBru из балансира нагрузки в $slb.</span><span class="sxs-lookup"><span data-stu-id="059b1-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="059b1-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="059b1-111">PARAMETERS</span></span>

### <span data-ttu-id="059b1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="059b1-112">-DefaultProfile</span></span>
<span data-ttu-id="059b1-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="059b1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="059b1-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="059b1-114">-LoadBalancer</span></span>
<span data-ttu-id="059b1-115">Определяет балансировку нагрузки, связанную с конфигурацией правил, которую нужно получить.</span><span class="sxs-lookup"><span data-stu-id="059b1-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="059b1-116">-Name</span><span class="sxs-lookup"><span data-stu-id="059b1-116">-Name</span></span>
<span data-ttu-id="059b1-117">Указывает имя нужной конфигурации правила.</span><span class="sxs-lookup"><span data-stu-id="059b1-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="059b1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="059b1-118">CommonParameters</span></span>
<span data-ttu-id="059b1-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="059b1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="059b1-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="059b1-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="059b1-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="059b1-121">INPUTS</span></span>

### <span data-ttu-id="059b1-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="059b1-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="059b1-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="059b1-123">OUTPUTS</span></span>

### <span data-ttu-id="059b1-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="059b1-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="059b1-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="059b1-125">NOTES</span></span>

## <span data-ttu-id="059b1-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="059b1-126">RELATED LINKS</span></span>

[<span data-ttu-id="059b1-127">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="059b1-127">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="059b1-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="059b1-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="059b1-129">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="059b1-129">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="059b1-130">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="059b1-130">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


