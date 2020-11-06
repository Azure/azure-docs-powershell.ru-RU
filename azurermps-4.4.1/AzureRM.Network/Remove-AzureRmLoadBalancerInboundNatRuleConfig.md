---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: ee831cf3f2b6441bde55dc458d6b9af33f4b42e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557739"
---
# <span data-ttu-id="d0475-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d0475-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="d0475-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d0475-102">SYNOPSIS</span></span>
<span data-ttu-id="d0475-103">Удаление конфигурации правила входящего трафика NAT из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="d0475-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0475-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d0475-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0475-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0475-105">DESCRIPTION</span></span>
<span data-ttu-id="d0475-106">Командлет **Remove-AzureRmLoadBalancerInboundNatRuleConfig** удаляет конфигурацию правила трансляции сетевых адресов (NAT) из подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="d0475-106">The **Remove-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="d0475-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d0475-107">EXAMPLES</span></span>

### <span data-ttu-id="d0475-108">1: Удаление правила входящего NAT из подсистемы балансировки нагрузки для Azure</span><span class="sxs-lookup"><span data-stu-id="d0475-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzureRmLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzureRmLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="d0475-109">Первая команда загружает уже существующий подсистему балансировки нагрузки под названием "mylb" и сохраняет его в подсистеме балансировки $load.</span><span class="sxs-lookup"><span data-stu-id="d0475-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="d0475-110">Вторая команда удаляет правило входящего NAT, связанное с этой подсистемой балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="d0475-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="d0475-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d0475-111">PARAMETERS</span></span>

### <span data-ttu-id="d0475-112">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="d0475-112">-LoadBalancer</span></span>
<span data-ttu-id="d0475-113">Указывает объект подсистемы **балансировки** , который содержит конфигурацию правила входящего NAT, которая удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="d0475-113">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d0475-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d0475-114">-Name</span></span>
<span data-ttu-id="d0475-115">Указывает имя конфигурации правила входящего NAT, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d0475-115">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d0475-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0475-116">-DefaultProfile</span></span>
<span data-ttu-id="d0475-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d0475-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0475-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0475-118">CommonParameters</span></span>
<span data-ttu-id="d0475-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d0475-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0475-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0475-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0475-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d0475-121">INPUTS</span></span>

### <span data-ttu-id="d0475-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d0475-122">PSLoadBalancer</span></span>
<span data-ttu-id="d0475-123">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="d0475-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="d0475-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0475-124">OUTPUTS</span></span>

### <span data-ttu-id="d0475-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d0475-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d0475-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="d0475-126">NOTES</span></span>

## <span data-ttu-id="d0475-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d0475-127">RELATED LINKS</span></span>

[<span data-ttu-id="d0475-128">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d0475-128">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d0475-129">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d0475-129">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d0475-130">New-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d0475-130">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="d0475-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d0475-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


