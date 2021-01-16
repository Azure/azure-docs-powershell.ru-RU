---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 9304471b12f33d677f493a3ee6803a1219d9f977
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410135"
---
# <span data-ttu-id="e12ea-101">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e12ea-101">Get-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="e12ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e12ea-102">SYNOPSIS</span></span>
<span data-ttu-id="e12ea-103">Возвращает конфигурацию входящие правила NAT для балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="e12ea-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="e12ea-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e12ea-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e12ea-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e12ea-105">DESCRIPTION</span></span>
<span data-ttu-id="e12ea-106">Для **получения одного или** более правил перевода сетевых адресов (NAT) в балансе нагрузки Azure возвращается одно или несколько правил перевода сетевых адресов (NAT).</span><span class="sxs-lookup"><span data-stu-id="e12ea-106">The **Get-AzLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="e12ea-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e12ea-107">EXAMPLES</span></span>

### <span data-ttu-id="e12ea-108">Пример 1. Настройка входящие правила NAT</span><span class="sxs-lookup"><span data-stu-id="e12ea-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="e12ea-109">Первая команда получает балансировку нагрузки MyLoadBalancer и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="e12ea-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>
<span data-ttu-id="e12ea-110">Вторая команда получает связанное правило NAT myInboundNatRule1 из балансира нагрузки в $slb.</span><span class="sxs-lookup"><span data-stu-id="e12ea-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="e12ea-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e12ea-111">PARAMETERS</span></span>

### <span data-ttu-id="e12ea-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e12ea-112">-DefaultProfile</span></span>
<span data-ttu-id="e12ea-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e12ea-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e12ea-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e12ea-114">-LoadBalancer</span></span>
<span data-ttu-id="e12ea-115">Определяет балансировку нагрузки, связанную с конфигурацией правила NAT для входящий сообщений.</span><span class="sxs-lookup"><span data-stu-id="e12ea-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="e12ea-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e12ea-116">-Name</span></span>
<span data-ttu-id="e12ea-117">Указывает имя конфигурации входящие правила NAT, которые нужно получить.</span><span class="sxs-lookup"><span data-stu-id="e12ea-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="e12ea-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e12ea-118">CommonParameters</span></span>
<span data-ttu-id="e12ea-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e12ea-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e12ea-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e12ea-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e12ea-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e12ea-121">INPUTS</span></span>

### <span data-ttu-id="e12ea-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e12ea-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e12ea-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e12ea-123">OUTPUTS</span></span>

### <span data-ttu-id="e12ea-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="e12ea-124">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="e12ea-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e12ea-125">NOTES</span></span>

## <span data-ttu-id="e12ea-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e12ea-126">RELATED LINKS</span></span>

[<span data-ttu-id="e12ea-127">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e12ea-127">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="e12ea-128">New-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e12ea-128">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="e12ea-129">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e12ea-129">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="e12ea-130">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="e12ea-130">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


