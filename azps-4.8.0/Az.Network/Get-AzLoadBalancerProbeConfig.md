---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 5b6031657438bfc28ce76519c8489e041a060965
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078923"
---
# <span data-ttu-id="e89a7-101">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e89a7-101">Get-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="e89a7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e89a7-102">SYNOPSIS</span></span>
<span data-ttu-id="e89a7-103">Возвращает конфигурацию зонда для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="e89a7-103">Gets a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="e89a7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e89a7-104">SYNTAX</span></span>

```
Get-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e89a7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e89a7-105">DESCRIPTION</span></span>
<span data-ttu-id="e89a7-106">Командлет **Get-AzLoadBalancerProbeConfig** получает одну или несколько пробных конфигураций для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="e89a7-106">The **Get-AzLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="e89a7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e89a7-107">EXAMPLES</span></span>

### <span data-ttu-id="e89a7-108">Пример 1: получение конфигурации пробной подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="e89a7-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="e89a7-109">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="e89a7-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="e89a7-110">Вторая команда получает соответствующую конфигурацию пробной проверки с именем MyProbe из подсистемы балансировки нагрузки в $slb.</span><span class="sxs-lookup"><span data-stu-id="e89a7-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="e89a7-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e89a7-111">PARAMETERS</span></span>

### <span data-ttu-id="e89a7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e89a7-112">-DefaultProfile</span></span>
<span data-ttu-id="e89a7-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e89a7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e89a7-114">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="e89a7-114">-LoadBalancer</span></span>
<span data-ttu-id="e89a7-115">Определяет подсистему балансировки нагрузки, связанную с конфигурацией зонда, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="e89a7-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

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

### <span data-ttu-id="e89a7-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e89a7-116">-Name</span></span>
<span data-ttu-id="e89a7-117">Указывает имя конфигурации зонда, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="e89a7-117">Specifies the name of the probe configuration to get.</span></span>

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

### <span data-ttu-id="e89a7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e89a7-118">CommonParameters</span></span>
<span data-ttu-id="e89a7-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e89a7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e89a7-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e89a7-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e89a7-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e89a7-121">INPUTS</span></span>

### <span data-ttu-id="e89a7-122">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e89a7-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e89a7-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e89a7-123">OUTPUTS</span></span>

### <span data-ttu-id="e89a7-124">Microsoft. Azure. Commands. Network. Models. PSProbe</span><span class="sxs-lookup"><span data-stu-id="e89a7-124">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="e89a7-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="e89a7-125">NOTES</span></span>

## <span data-ttu-id="e89a7-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e89a7-126">RELATED LINKS</span></span>

[<span data-ttu-id="e89a7-127">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e89a7-127">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="e89a7-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e89a7-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="e89a7-129">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e89a7-129">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="e89a7-130">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e89a7-130">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="e89a7-131">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e89a7-131">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)

