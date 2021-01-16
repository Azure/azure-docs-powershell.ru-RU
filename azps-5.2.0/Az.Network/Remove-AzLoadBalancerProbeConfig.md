---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 341bd8df76870de638db949fb844ac7187776509
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396303"
---
# <span data-ttu-id="d62e5-101">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d62e5-101">Remove-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="d62e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d62e5-102">SYNOPSIS</span></span>
<span data-ttu-id="d62e5-103">Удаление конфигурации из балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="d62e5-103">Removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="d62e5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d62e5-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d62e5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d62e5-105">DESCRIPTION</span></span>
<span data-ttu-id="d62e5-106">Для **этого из балансиров нагрузки** удаляется конфигурация загромождения.</span><span class="sxs-lookup"><span data-stu-id="d62e5-106">The **Remove-AzLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="d62e5-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d62e5-107">EXAMPLES</span></span>

### <span data-ttu-id="d62e5-108">Пример 1. Удаление конфигурации из балансиров нагрузки</span><span class="sxs-lookup"><span data-stu-id="d62e5-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="d62e5-109">Первая команда получает балансировку нагрузки MyLoadBalancer, а затем сохраняет его в переменной $loadbalancer загрузки.</span><span class="sxs-lookup"><span data-stu-id="d62e5-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="d62e5-110">Вторая команда удаляет конфигурацию MyProbe из балансира нагрузки в $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="d62e5-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="d62e5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d62e5-111">PARAMETERS</span></span>

### <span data-ttu-id="d62e5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d62e5-112">-DefaultProfile</span></span>
<span data-ttu-id="d62e5-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d62e5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d62e5-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d62e5-114">-LoadBalancer</span></span>
<span data-ttu-id="d62e5-115">Определяет балансировую нагрузку, которая содержит конфигурацию, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d62e5-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d62e5-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d62e5-116">-Name</span></span>
<span data-ttu-id="d62e5-117">Указывает имя конфигурации, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d62e5-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d62e5-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d62e5-118">-Confirm</span></span>
<span data-ttu-id="d62e5-119">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d62e5-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d62e5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d62e5-120">-WhatIf</span></span>
<span data-ttu-id="d62e5-121">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d62e5-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d62e5-122">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d62e5-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d62e5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d62e5-123">CommonParameters</span></span>
<span data-ttu-id="d62e5-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d62e5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d62e5-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d62e5-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d62e5-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d62e5-126">INPUTS</span></span>

### <span data-ttu-id="d62e5-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d62e5-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d62e5-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d62e5-128">OUTPUTS</span></span>

### <span data-ttu-id="d62e5-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d62e5-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d62e5-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d62e5-130">NOTES</span></span>

## <span data-ttu-id="d62e5-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d62e5-131">RELATED LINKS</span></span>

[<span data-ttu-id="d62e5-132">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d62e5-132">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="d62e5-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d62e5-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="d62e5-134">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d62e5-134">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="d62e5-135">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d62e5-135">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="d62e5-136">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d62e5-136">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


