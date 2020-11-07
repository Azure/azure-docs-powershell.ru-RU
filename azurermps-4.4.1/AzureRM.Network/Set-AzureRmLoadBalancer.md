---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
ms.openlocfilehash: be09bb6592ebf950c2fb3de6b4a512235fd0feab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733349"
---
# <span data-ttu-id="f4b5d-101">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f4b5d-101">Set-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="f4b5d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f4b5d-102">SYNOPSIS</span></span>
<span data-ttu-id="f4b5d-103">Задает состояние цели для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f4b5d-103">Sets the goal state for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4b5d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f4b5d-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancer -LoadBalancer <PSLoadBalancer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4b5d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4b5d-105">DESCRIPTION</span></span>
<span data-ttu-id="f4b5d-106">Командлет **Set-AzureRmLoadBalancer** задает состояние цели для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="f4b5d-106">The **Set-AzureRmLoadBalancer** cmdlet sets the goal state for an Azure load balancer.</span></span>

## <span data-ttu-id="f4b5d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f4b5d-107">EXAMPLES</span></span>

### <span data-ttu-id="f4b5d-108">Пример 1: изменение подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="f4b5d-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzureRmLoadBalancer
```

<span data-ttu-id="f4b5d-109">Первая команда получает подсистему балансировки нагрузки с именем NRPLB и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="f4b5d-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="f4b5d-110">Вторая команда использует оператор Pipeline для передачи балансировщика нагрузки в $slb на Add-AzureRmLoadBalancerInboundNatRuleConfig, который добавляет правило входящего NAT с именем NewRule.</span><span class="sxs-lookup"><span data-stu-id="f4b5d-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>

<span data-ttu-id="f4b5d-111">Третья команда передает подсистему балансировки нагрузки в **Set-AzureRmLoadBalancer** , которая обновляет конфигурацию подсистемы балансировки нагрузки и сохраняет ее.</span><span class="sxs-lookup"><span data-stu-id="f4b5d-111">The third command passes the load balancer to **Set-AzureRmLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="f4b5d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f4b5d-112">PARAMETERS</span></span>

### <span data-ttu-id="f4b5d-113">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="f4b5d-113">-LoadBalancer</span></span>
<span data-ttu-id="f4b5d-114">Указывает на подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="f4b5d-114">Specifies a load balancer.</span></span>
<span data-ttu-id="f4b5d-115">Этот командлет задает состояние цели для подсистемы балансировки нагрузки, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f4b5d-115">This cmdlet sets the goal state for the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4b5d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4b5d-116">-DefaultProfile</span></span>
<span data-ttu-id="f4b5d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4b5d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4b5d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4b5d-118">CommonParameters</span></span>
<span data-ttu-id="f4b5d-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f4b5d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4b5d-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4b5d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4b5d-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f4b5d-121">INPUTS</span></span>

### <span data-ttu-id="f4b5d-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f4b5d-122">PSLoadBalancer</span></span>
<span data-ttu-id="f4b5d-123">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="f4b5d-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="f4b5d-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4b5d-124">OUTPUTS</span></span>

### <span data-ttu-id="f4b5d-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f4b5d-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="f4b5d-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="f4b5d-126">NOTES</span></span>

## <span data-ttu-id="f4b5d-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4b5d-127">RELATED LINKS</span></span>

[<span data-ttu-id="f4b5d-128">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f4b5d-128">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="f4b5d-129">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f4b5d-129">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="f4b5d-130">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f4b5d-130">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)


