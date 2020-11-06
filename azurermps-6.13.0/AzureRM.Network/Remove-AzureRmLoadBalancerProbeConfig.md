---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: c52546ba0477a2911ac34533060d7a47df0b0698
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560051"
---
# <span data-ttu-id="6d609-101">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6d609-101">Remove-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="6d609-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6d609-102">SYNOPSIS</span></span>
<span data-ttu-id="6d609-103">Удаляет конфигурацию зонда из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="6d609-103">Removes a probe configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d609-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6d609-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d609-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d609-105">DESCRIPTION</span></span>
<span data-ttu-id="6d609-106">Командлет **Remove-AzureRmLoadBalancerProbeConfig** удаляет конфигурацию зонда из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="6d609-106">The **Remove-AzureRmLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="6d609-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6d609-107">EXAMPLES</span></span>

### <span data-ttu-id="6d609-108">Пример 1: Удаление конфигурации зонда из подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="6d609-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="6d609-109">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="6d609-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="6d609-110">Вторая команда удаляет конфигурацию с именем MyProbe из подсистемы балансировки нагрузки в $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="6d609-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="6d609-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6d609-111">PARAMETERS</span></span>

### <span data-ttu-id="6d609-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d609-112">-DefaultProfile</span></span>
<span data-ttu-id="6d609-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6d609-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d609-114">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="6d609-114">-LoadBalancer</span></span>
<span data-ttu-id="6d609-115">Указывает подсистему балансировки нагрузки, которая содержит конфигурацию зонда, которая удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="6d609-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6d609-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6d609-116">-Name</span></span>
<span data-ttu-id="6d609-117">Указывает имя конфигурации зонда, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6d609-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6d609-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d609-118">-Confirm</span></span>
<span data-ttu-id="6d609-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6d609-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d609-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d609-120">-WhatIf</span></span>
<span data-ttu-id="6d609-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6d609-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6d609-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6d609-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d609-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d609-123">CommonParameters</span></span>
<span data-ttu-id="6d609-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6d609-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d609-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d609-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d609-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6d609-126">INPUTS</span></span>

### <span data-ttu-id="6d609-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6d609-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="6d609-128">Параметры: подсистема балансировки (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6d609-128">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="6d609-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d609-129">OUTPUTS</span></span>

### <span data-ttu-id="6d609-130">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6d609-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6d609-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="6d609-131">NOTES</span></span>

## <span data-ttu-id="6d609-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d609-132">RELATED LINKS</span></span>

[<span data-ttu-id="6d609-133">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6d609-133">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="6d609-134">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6d609-134">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="6d609-135">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6d609-135">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="6d609-136">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6d609-136">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="6d609-137">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6d609-137">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


