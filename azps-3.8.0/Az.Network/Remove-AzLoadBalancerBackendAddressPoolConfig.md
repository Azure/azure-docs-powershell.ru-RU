---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 26f7e0dde825305e888d598a23af0b2fbaff81cd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074037"
---
# <span data-ttu-id="52858-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="52858-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="52858-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="52858-102">SYNOPSIS</span></span>
<span data-ttu-id="52858-103">Удаляет конфигурацию пула адресных адресов из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="52858-103">Removes a backend address pool configuration from a load balancer.</span></span>

## <span data-ttu-id="52858-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="52858-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52858-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="52858-105">DESCRIPTION</span></span>
<span data-ttu-id="52858-106">Командлет **Remove-AzLoadBalancerBackendAddressPoolConfig** удаляет пул серверных адресов из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="52858-106">The **Remove-AzLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="52858-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="52858-107">EXAMPLES</span></span>

### <span data-ttu-id="52858-108">Пример 1: Удаление конфигурации пула адресов серверной части из подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="52858-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="52858-109">Эта команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и передает ее в **Remove-AzLoadBalancerBackendAddressPoolConfig** , удаляя конфигурацию BackendAddressPool02 из MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="52858-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="52858-110">Наконец, командлет Set-AzLoadBalancer обновляет MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="52858-110">Finally, the Set-AzLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="52858-111">Обратите внимание, что конфигурация пула адресных адресов сервера должна существовать, прежде чем ее можно будет удалить.</span><span class="sxs-lookup"><span data-stu-id="52858-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="52858-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="52858-112">PARAMETERS</span></span>

### <span data-ttu-id="52858-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52858-113">-DefaultProfile</span></span>
<span data-ttu-id="52858-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="52858-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52858-115">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="52858-115">-LoadBalancer</span></span>
<span data-ttu-id="52858-116">Указывает подсистему балансировки нагрузки, которая содержит пул серверных адресов, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="52858-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="52858-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="52858-117">-Name</span></span>
<span data-ttu-id="52858-118">Указывает имя пула адресных адресов серверной платформы, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="52858-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="52858-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52858-119">-Confirm</span></span>
<span data-ttu-id="52858-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="52858-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52858-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52858-121">-WhatIf</span></span>
<span data-ttu-id="52858-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="52858-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52858-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="52858-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52858-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52858-124">CommonParameters</span></span>
<span data-ttu-id="52858-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="52858-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52858-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52858-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52858-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="52858-127">INPUTS</span></span>

### <span data-ttu-id="52858-128">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="52858-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="52858-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="52858-129">OUTPUTS</span></span>

### <span data-ttu-id="52858-130">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="52858-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="52858-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="52858-131">NOTES</span></span>

## <span data-ttu-id="52858-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="52858-132">RELATED LINKS</span></span>

[<span data-ttu-id="52858-133">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="52858-133">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="52858-134">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="52858-134">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="52858-135">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="52858-135">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="52858-136">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="52858-136">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)


