---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancer.md
ms.openlocfilehash: 17af7cc61ec3d254133dd0563e8ea09fc0e3043f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911048"
---
# <span data-ttu-id="77b86-101">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="77b86-101">Set-AzLoadBalancer</span></span>

## <span data-ttu-id="77b86-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="77b86-102">SYNOPSIS</span></span>
<span data-ttu-id="77b86-103">Задает состояние цели для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="77b86-103">Sets the goal state for a load balancer.</span></span>

## <span data-ttu-id="77b86-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="77b86-104">SYNTAX</span></span>

```
Set-AzLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="77b86-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77b86-105">DESCRIPTION</span></span>
<span data-ttu-id="77b86-106">Командлет **Set-AzLoadBalancer** задает состояние цели для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="77b86-106">The **Set-AzLoadBalancer** cmdlet sets the goal state for an Azure load balancer.</span></span>

## <span data-ttu-id="77b86-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="77b86-107">EXAMPLES</span></span>

### <span data-ttu-id="77b86-108">Пример 1: изменение подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="77b86-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="77b86-109">Первая команда получает подсистему балансировки нагрузки с именем NRPLB и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="77b86-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="77b86-110">Вторая команда использует оператор Pipeline для передачи балансировщика нагрузки в $slb на Add-AzLoadBalancerInboundNatRuleConfig, который добавляет правило входящего NAT с именем NewRule.</span><span class="sxs-lookup"><span data-stu-id="77b86-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>

<span data-ttu-id="77b86-111">Третья команда передает подсистему балансировки нагрузки в **Set-AzLoadBalancer** , которая обновляет конфигурацию подсистемы балансировки нагрузки и сохраняет ее.</span><span class="sxs-lookup"><span data-stu-id="77b86-111">The third command passes the load balancer to **Set-AzLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="77b86-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="77b86-112">PARAMETERS</span></span>

### <span data-ttu-id="77b86-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77b86-113">-AsJob</span></span>
<span data-ttu-id="77b86-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="77b86-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b86-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77b86-115">-DefaultProfile</span></span>
<span data-ttu-id="77b86-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="77b86-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77b86-117">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="77b86-117">-LoadBalancer</span></span>
<span data-ttu-id="77b86-118">Указывает на подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="77b86-118">Specifies a load balancer.</span></span>
<span data-ttu-id="77b86-119">Этот командлет задает состояние цели для подсистемы балансировки нагрузки, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="77b86-119">This cmdlet sets the goal state for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="77b86-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77b86-120">CommonParameters</span></span>
<span data-ttu-id="77b86-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="77b86-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77b86-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77b86-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77b86-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="77b86-123">INPUTS</span></span>

### <span data-ttu-id="77b86-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="77b86-124">PSLoadBalancer</span></span>
<span data-ttu-id="77b86-125">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="77b86-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="77b86-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="77b86-126">OUTPUTS</span></span>

### <span data-ttu-id="77b86-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="77b86-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="77b86-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="77b86-128">NOTES</span></span>

## <span data-ttu-id="77b86-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77b86-129">RELATED LINKS</span></span>

[<span data-ttu-id="77b86-130">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="77b86-130">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="77b86-131">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="77b86-131">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="77b86-132">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="77b86-132">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)


