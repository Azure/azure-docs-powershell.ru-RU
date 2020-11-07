---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 11de4e8966b5e57e817b6c5d829536deacf229f8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909482"
---
# <span data-ttu-id="5909b-101">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5909b-101">Remove-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="5909b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5909b-102">SYNOPSIS</span></span>
<span data-ttu-id="5909b-103">Удаляет конфигурацию зонда из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="5909b-103">Removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="5909b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5909b-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5909b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5909b-105">DESCRIPTION</span></span>
<span data-ttu-id="5909b-106">Командлет **Remove-AzLoadBalancerProbeConfig** удаляет конфигурацию зонда из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="5909b-106">The **Remove-AzLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="5909b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5909b-107">EXAMPLES</span></span>

### <span data-ttu-id="5909b-108">Пример 1: Удаление конфигурации зонда из подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="5909b-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="5909b-109">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="5909b-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="5909b-110">Вторая команда удаляет конфигурацию с именем MyProbe из подсистемы балансировки нагрузки в $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="5909b-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="5909b-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5909b-111">PARAMETERS</span></span>

### <span data-ttu-id="5909b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5909b-112">-DefaultProfile</span></span>
<span data-ttu-id="5909b-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5909b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5909b-114">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="5909b-114">-LoadBalancer</span></span>
<span data-ttu-id="5909b-115">Указывает подсистему балансировки нагрузки, которая содержит конфигурацию зонда, которая удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="5909b-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5909b-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5909b-116">-Name</span></span>
<span data-ttu-id="5909b-117">Указывает имя конфигурации зонда, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5909b-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5909b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5909b-118">CommonParameters</span></span>
<span data-ttu-id="5909b-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5909b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5909b-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5909b-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5909b-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5909b-121">INPUTS</span></span>

### <span data-ttu-id="5909b-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5909b-122">PSLoadBalancer</span></span>
<span data-ttu-id="5909b-123">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="5909b-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="5909b-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5909b-124">OUTPUTS</span></span>

### <span data-ttu-id="5909b-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5909b-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="5909b-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="5909b-126">NOTES</span></span>

## <span data-ttu-id="5909b-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5909b-127">RELATED LINKS</span></span>

[<span data-ttu-id="5909b-128">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5909b-128">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="5909b-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5909b-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="5909b-130">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5909b-130">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="5909b-131">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5909b-131">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="5909b-132">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5909b-132">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


