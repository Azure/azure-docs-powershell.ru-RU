---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 6a1e5f4de5ec98030cc9bd3300d9e9fd447f6f02
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901953"
---
# <span data-ttu-id="71169-101">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="71169-101">Remove-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="71169-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="71169-102">SYNOPSIS</span></span>
<span data-ttu-id="71169-103">Удаляет конфигурацию зонда из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="71169-103">Removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="71169-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="71169-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71169-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71169-105">DESCRIPTION</span></span>
<span data-ttu-id="71169-106">Командлет **Remove-AzLoadBalancerProbeConfig** удаляет конфигурацию зонда из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="71169-106">The **Remove-AzLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="71169-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="71169-107">EXAMPLES</span></span>

### <span data-ttu-id="71169-108">Пример 1: Удаление конфигурации зонда из подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="71169-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="71169-109">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="71169-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="71169-110">Вторая команда удаляет конфигурацию с именем MyProbe из подсистемы балансировки нагрузки в $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="71169-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="71169-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="71169-111">PARAMETERS</span></span>

### <span data-ttu-id="71169-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71169-112">-DefaultProfile</span></span>
<span data-ttu-id="71169-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="71169-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71169-114">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="71169-114">-LoadBalancer</span></span>
<span data-ttu-id="71169-115">Указывает подсистему балансировки нагрузки, которая содержит конфигурацию зонда, которая удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="71169-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="71169-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="71169-116">-Name</span></span>
<span data-ttu-id="71169-117">Указывает имя конфигурации зонда, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="71169-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="71169-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71169-118">-Confirm</span></span>
<span data-ttu-id="71169-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="71169-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71169-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71169-120">-WhatIf</span></span>
<span data-ttu-id="71169-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="71169-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71169-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="71169-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71169-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71169-123">CommonParameters</span></span>
<span data-ttu-id="71169-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="71169-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71169-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71169-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71169-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="71169-126">INPUTS</span></span>

### <span data-ttu-id="71169-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="71169-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="71169-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="71169-128">OUTPUTS</span></span>

### <span data-ttu-id="71169-129">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="71169-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="71169-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="71169-130">NOTES</span></span>

## <span data-ttu-id="71169-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71169-131">RELATED LINKS</span></span>

[<span data-ttu-id="71169-132">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="71169-132">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="71169-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="71169-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="71169-134">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="71169-134">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="71169-135">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="71169-135">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="71169-136">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="71169-136">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


