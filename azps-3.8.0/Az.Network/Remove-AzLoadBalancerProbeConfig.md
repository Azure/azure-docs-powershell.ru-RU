---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 341bd8df76870de638db949fb844ac7187776509
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074030"
---
# <span data-ttu-id="a1db1-101">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a1db1-101">Remove-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="a1db1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a1db1-102">SYNOPSIS</span></span>
<span data-ttu-id="a1db1-103">Удаляет конфигурацию зонда из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a1db1-103">Removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="a1db1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a1db1-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1db1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1db1-105">DESCRIPTION</span></span>
<span data-ttu-id="a1db1-106">Командлет **Remove-AzLoadBalancerProbeConfig** удаляет конфигурацию зонда из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a1db1-106">The **Remove-AzLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="a1db1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a1db1-107">EXAMPLES</span></span>

### <span data-ttu-id="a1db1-108">Пример 1: Удаление конфигурации зонда из подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="a1db1-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="a1db1-109">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="a1db1-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="a1db1-110">Вторая команда удаляет конфигурацию с именем MyProbe из подсистемы балансировки нагрузки в $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="a1db1-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="a1db1-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a1db1-111">PARAMETERS</span></span>

### <span data-ttu-id="a1db1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1db1-112">-DefaultProfile</span></span>
<span data-ttu-id="a1db1-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a1db1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1db1-114">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="a1db1-114">-LoadBalancer</span></span>
<span data-ttu-id="a1db1-115">Указывает подсистему балансировки нагрузки, которая содержит конфигурацию зонда, которая удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="a1db1-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a1db1-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a1db1-116">-Name</span></span>
<span data-ttu-id="a1db1-117">Указывает имя конфигурации зонда, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a1db1-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a1db1-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1db1-118">-Confirm</span></span>
<span data-ttu-id="a1db1-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a1db1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1db1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1db1-120">-WhatIf</span></span>
<span data-ttu-id="a1db1-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a1db1-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1db1-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a1db1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1db1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1db1-123">CommonParameters</span></span>
<span data-ttu-id="a1db1-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a1db1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1db1-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1db1-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1db1-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a1db1-126">INPUTS</span></span>

### <span data-ttu-id="a1db1-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a1db1-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a1db1-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1db1-128">OUTPUTS</span></span>

### <span data-ttu-id="a1db1-129">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a1db1-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a1db1-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="a1db1-130">NOTES</span></span>

## <span data-ttu-id="a1db1-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1db1-131">RELATED LINKS</span></span>

[<span data-ttu-id="a1db1-132">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a1db1-132">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="a1db1-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a1db1-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="a1db1-134">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a1db1-134">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="a1db1-135">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a1db1-135">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="a1db1-136">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a1db1-136">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


