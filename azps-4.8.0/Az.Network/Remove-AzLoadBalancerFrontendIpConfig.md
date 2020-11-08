---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: bde16a6f3ecd68307574ae5eac7760a177101cc1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234953"
---
# <span data-ttu-id="94654-101">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="94654-101">Remove-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="94654-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="94654-102">SYNOPSIS</span></span>
<span data-ttu-id="94654-103">Удаляет интерфейсную конфигурацию IP из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="94654-103">Removes a front-end IP configuration from a load balancer.</span></span>

## <span data-ttu-id="94654-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="94654-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94654-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94654-105">DESCRIPTION</span></span>
<span data-ttu-id="94654-106">Командлет **Remove-AzLoadBalancerFrontendIpConfig** удаляет IP-конфигурацию интерфейсов из подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="94654-106">The **Remove-AzLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="94654-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="94654-107">EXAMPLES</span></span>

### <span data-ttu-id="94654-108">Пример 1: удаление интерфейсной конфигурации IP из подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="94654-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="94654-109">Первая команда получает подсистему балансировки нагрузки, связанную с интерфейсной IP-конфигурацией, которую вы хотите удалить, и сохраняет ее в переменной $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="94654-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="94654-110">Вторая команда удаляет связанную конфигурацию IP-интерфейсов из подсистемы балансировки нагрузки в $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="94654-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="94654-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="94654-111">PARAMETERS</span></span>

### <span data-ttu-id="94654-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94654-112">-DefaultProfile</span></span>
<span data-ttu-id="94654-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="94654-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94654-114">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="94654-114">-LoadBalancer</span></span>
<span data-ttu-id="94654-115">Указывает подсистему балансировки нагрузки, которая содержит интерфейсную конфигурацию IP-интерфейса, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="94654-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="94654-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="94654-116">-Name</span></span>
<span data-ttu-id="94654-117">Указывает имя удаляемой конфигурации переднего IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="94654-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="94654-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94654-118">-Confirm</span></span>
<span data-ttu-id="94654-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="94654-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94654-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94654-120">-WhatIf</span></span>
<span data-ttu-id="94654-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="94654-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94654-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="94654-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94654-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94654-123">CommonParameters</span></span>
<span data-ttu-id="94654-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="94654-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94654-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94654-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94654-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="94654-126">INPUTS</span></span>

### <span data-ttu-id="94654-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="94654-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="94654-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="94654-128">OUTPUTS</span></span>

### <span data-ttu-id="94654-129">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="94654-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="94654-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="94654-130">NOTES</span></span>

## <span data-ttu-id="94654-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94654-131">RELATED LINKS</span></span>

[<span data-ttu-id="94654-132">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="94654-132">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="94654-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="94654-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="94654-134">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="94654-134">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="94654-135">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="94654-135">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="94654-136">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="94654-136">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


