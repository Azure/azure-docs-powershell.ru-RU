---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancer
schema: 2.0.0
ms.openlocfilehash: 7719847f578b540fd2c8bba93a378c4377fecab8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914798"
---
# <span data-ttu-id="d3e88-101">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d3e88-101">Set-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="d3e88-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d3e88-102">SYNOPSIS</span></span>
<span data-ttu-id="d3e88-103">Задает состояние цели для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="d3e88-103">Sets the goal state for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3e88-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d3e88-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d3e88-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3e88-105">DESCRIPTION</span></span>
<span data-ttu-id="d3e88-106">Командлет **Set-AzureRmLoadBalancer** задает состояние цели для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="d3e88-106">The **Set-AzureRmLoadBalancer** cmdlet sets the goal state for an Azure load balancer.</span></span>

## <span data-ttu-id="d3e88-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d3e88-107">EXAMPLES</span></span>

### <span data-ttu-id="d3e88-108">Пример 1: изменение подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="d3e88-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzureRmLoadBalancer
```

<span data-ttu-id="d3e88-109">Первая команда получает подсистему балансировки нагрузки с именем NRPLB и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="d3e88-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="d3e88-110">Вторая команда использует оператор Pipeline для передачи балансировщика нагрузки в $slb на Add-AzureRmLoadBalancerInboundNatRuleConfig, который добавляет правило входящего NAT с именем NewRule.</span><span class="sxs-lookup"><span data-stu-id="d3e88-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>

<span data-ttu-id="d3e88-111">Третья команда передает подсистему балансировки нагрузки в **Set-AzureRmLoadBalancer** , которая обновляет конфигурацию подсистемы балансировки нагрузки и сохраняет ее.</span><span class="sxs-lookup"><span data-stu-id="d3e88-111">The third command passes the load balancer to **Set-AzureRmLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="d3e88-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d3e88-112">PARAMETERS</span></span>

### <span data-ttu-id="d3e88-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3e88-113">-AsJob</span></span>
<span data-ttu-id="d3e88-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d3e88-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3e88-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3e88-115">-DefaultProfile</span></span>
<span data-ttu-id="d3e88-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d3e88-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3e88-117">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="d3e88-117">-LoadBalancer</span></span>
<span data-ttu-id="d3e88-118">Указывает на подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="d3e88-118">Specifies a load balancer.</span></span>
<span data-ttu-id="d3e88-119">Этот командлет задает состояние цели для подсистемы балансировки нагрузки, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="d3e88-119">This cmdlet sets the goal state for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="d3e88-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3e88-120">CommonParameters</span></span>
<span data-ttu-id="d3e88-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d3e88-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3e88-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3e88-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3e88-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d3e88-123">INPUTS</span></span>

### <span data-ttu-id="d3e88-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d3e88-124">PSLoadBalancer</span></span>
<span data-ttu-id="d3e88-125">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="d3e88-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="d3e88-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3e88-126">OUTPUTS</span></span>

### <span data-ttu-id="d3e88-127">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d3e88-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d3e88-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="d3e88-128">NOTES</span></span>

## <span data-ttu-id="d3e88-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3e88-129">RELATED LINKS</span></span>

[<span data-ttu-id="d3e88-130">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d3e88-130">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="d3e88-131">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d3e88-131">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="d3e88-132">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d3e88-132">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)


