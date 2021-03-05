---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 3e7433c8c779c078ab1b264e6b724d06cd884bab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993667"
---
# <span data-ttu-id="dcca2-101">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="dcca2-101">Remove-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="dcca2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcca2-102">SYNOPSIS</span></span>
<span data-ttu-id="dcca2-103">Удаление конфигурации из балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="dcca2-103">Removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="dcca2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dcca2-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcca2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcca2-105">DESCRIPTION</span></span>
<span data-ttu-id="dcca2-106">Для этого из балансиров нагрузки удаляется конфигурация формы **Remove-AzLoadBalancerProbeConfig.**</span><span class="sxs-lookup"><span data-stu-id="dcca2-106">The **Remove-AzLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="dcca2-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dcca2-107">EXAMPLES</span></span>

### <span data-ttu-id="dcca2-108">Пример 1. Удаление конфигурации из балансиров нагрузки</span><span class="sxs-lookup"><span data-stu-id="dcca2-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="dcca2-109">Первая команда получает балансировку нагрузки MyLoadBalancer, а затем сохраняет его в переменной $loadbalancer загрузки.</span><span class="sxs-lookup"><span data-stu-id="dcca2-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="dcca2-110">Вторая команда удаляет конфигурацию MyProbe из балансира нагрузки в $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="dcca2-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="dcca2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dcca2-111">PARAMETERS</span></span>

### <span data-ttu-id="dcca2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcca2-112">-DefaultProfile</span></span>
<span data-ttu-id="dcca2-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dcca2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcca2-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dcca2-114">-LoadBalancer</span></span>
<span data-ttu-id="dcca2-115">Указывает балансировую нагрузку, которая содержит конфигурацию, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcca2-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dcca2-116">-Name</span><span class="sxs-lookup"><span data-stu-id="dcca2-116">-Name</span></span>
<span data-ttu-id="dcca2-117">Указывает имя конфигурации, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcca2-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dcca2-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dcca2-118">-Confirm</span></span>
<span data-ttu-id="dcca2-119">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="dcca2-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcca2-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcca2-120">-WhatIf</span></span>
<span data-ttu-id="dcca2-121">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcca2-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dcca2-122">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dcca2-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcca2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcca2-123">CommonParameters</span></span>
<span data-ttu-id="dcca2-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcca2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcca2-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcca2-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcca2-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dcca2-126">INPUTS</span></span>

### <span data-ttu-id="dcca2-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dcca2-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="dcca2-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dcca2-128">OUTPUTS</span></span>

### <span data-ttu-id="dcca2-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dcca2-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="dcca2-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dcca2-130">NOTES</span></span>

## <span data-ttu-id="dcca2-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dcca2-131">RELATED LINKS</span></span>

[<span data-ttu-id="dcca2-132">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="dcca2-132">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="dcca2-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dcca2-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="dcca2-134">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="dcca2-134">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="dcca2-135">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="dcca2-135">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="dcca2-136">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="dcca2-136">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


