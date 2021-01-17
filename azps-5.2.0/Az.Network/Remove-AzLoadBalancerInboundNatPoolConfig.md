---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: cf8afee04e8aaf1a8909988465dc4371575b4309
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399607"
---
# <span data-ttu-id="f8345-101">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f8345-101">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="f8345-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8345-102">SYNOPSIS</span></span>
<span data-ttu-id="f8345-103">Удаляет конфигурацию входящий пул NAT из балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f8345-103">Removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="f8345-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f8345-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8345-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8345-105">DESCRIPTION</span></span>
<span data-ttu-id="f8345-106">Из балансиров нагрузки удаляется конфигурация входящий пул NAT для **Remove-AzLoadBalancerInboundNatPoolConfig.**</span><span class="sxs-lookup"><span data-stu-id="f8345-106">The **Remove-AzLoadBalancerInboundNatPoolConfig** cmdlet removes an inbound NAT pool configuration from a load balancer.</span></span>

## <span data-ttu-id="f8345-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f8345-107">EXAMPLES</span></span>

### <span data-ttu-id="f8345-108">1. Удаление</span><span class="sxs-lookup"><span data-stu-id="f8345-108">1: Remove</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzLoadBalancerInboundNatPoolConfig -Name myinboundnatpool -LoadBalancer $slb
```

## <span data-ttu-id="f8345-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8345-109">PARAMETERS</span></span>

### <span data-ttu-id="f8345-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8345-110">-DefaultProfile</span></span>
<span data-ttu-id="f8345-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f8345-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8345-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f8345-112">-LoadBalancer</span></span>
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

### <span data-ttu-id="f8345-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f8345-113">-Name</span></span>
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

### <span data-ttu-id="f8345-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8345-114">-Confirm</span></span>
<span data-ttu-id="f8345-115">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8345-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8345-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8345-116">-WhatIf</span></span>
<span data-ttu-id="f8345-117">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8345-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f8345-118">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f8345-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8345-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8345-119">CommonParameters</span></span>
<span data-ttu-id="f8345-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8345-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8345-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8345-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8345-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f8345-122">INPUTS</span></span>

### <span data-ttu-id="f8345-123">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f8345-123">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f8345-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f8345-124">OUTPUTS</span></span>

### <span data-ttu-id="f8345-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f8345-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f8345-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f8345-126">NOTES</span></span>

## <span data-ttu-id="f8345-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8345-127">RELATED LINKS</span></span>

[<span data-ttu-id="f8345-128">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f8345-128">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="f8345-129">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f8345-129">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="f8345-130">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f8345-130">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="f8345-131">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f8345-131">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
