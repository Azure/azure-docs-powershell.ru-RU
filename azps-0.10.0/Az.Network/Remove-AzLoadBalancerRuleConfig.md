---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 9c50452acd832c7ac7ca0c4bc2827b8f320115b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909477"
---
# <span data-ttu-id="4921b-101">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4921b-101">Remove-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="4921b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4921b-102">SYNOPSIS</span></span>
<span data-ttu-id="4921b-103">Удаление конфигурации правила для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="4921b-103">Removes a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="4921b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4921b-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4921b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4921b-105">DESCRIPTION</span></span>
<span data-ttu-id="4921b-106">Командлет **Remove-AzLoadBalancerRuleConfig** удаляет конфигурацию правила для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="4921b-106">The **Remove-AzLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="4921b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4921b-107">EXAMPLES</span></span>

### <span data-ttu-id="4921b-108">Пример 1: Удаление конфигурации правила из подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="4921b-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="4921b-109">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="4921b-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="4921b-110">Вторая команда удаляет конфигурацию правила с именем MyLBruleName из подсистемы балансировки нагрузки в $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="4921b-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="4921b-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4921b-111">PARAMETERS</span></span>

### <span data-ttu-id="4921b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4921b-112">-DefaultProfile</span></span>
<span data-ttu-id="4921b-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4921b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4921b-114">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="4921b-114">-LoadBalancer</span></span>
<span data-ttu-id="4921b-115">Указывает объект подсистемы **балансировки** , который содержит конфигурацию правила, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4921b-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4921b-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4921b-116">-Name</span></span>
<span data-ttu-id="4921b-117">Указывает имя конфигурации правила подсистемы балансировки нагрузки, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4921b-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4921b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4921b-118">CommonParameters</span></span>
<span data-ttu-id="4921b-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4921b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4921b-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4921b-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4921b-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4921b-121">INPUTS</span></span>

### <span data-ttu-id="4921b-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4921b-122">PSLoadBalancer</span></span>
<span data-ttu-id="4921b-123">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="4921b-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="4921b-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4921b-124">OUTPUTS</span></span>

### <span data-ttu-id="4921b-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4921b-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4921b-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="4921b-126">NOTES</span></span>

## <span data-ttu-id="4921b-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4921b-127">RELATED LINKS</span></span>

[<span data-ttu-id="4921b-128">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4921b-128">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="4921b-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4921b-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="4921b-130">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4921b-130">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="4921b-131">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4921b-131">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="4921b-132">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4921b-132">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


