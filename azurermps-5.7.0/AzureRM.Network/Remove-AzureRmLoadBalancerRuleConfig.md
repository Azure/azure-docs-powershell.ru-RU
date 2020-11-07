---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 25340322c7d5f74eb8f277db9f7693c938007840
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734698"
---
# <span data-ttu-id="9944d-101">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9944d-101">Remove-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="9944d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9944d-102">SYNOPSIS</span></span>
<span data-ttu-id="9944d-103">Удаление конфигурации правила для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="9944d-103">Removes a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9944d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9944d-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9944d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9944d-105">DESCRIPTION</span></span>
<span data-ttu-id="9944d-106">Командлет **Remove-AzureRmLoadBalancerRuleConfig** удаляет конфигурацию правила для подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="9944d-106">The **Remove-AzureRmLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="9944d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9944d-107">EXAMPLES</span></span>

### <span data-ttu-id="9944d-108">Пример 1: Удаление конфигурации правила из подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="9944d-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="9944d-109">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="9944d-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="9944d-110">Вторая команда удаляет конфигурацию правила с именем MyLBruleName из подсистемы балансировки нагрузки в $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="9944d-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="9944d-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9944d-111">PARAMETERS</span></span>

### <span data-ttu-id="9944d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9944d-112">-DefaultProfile</span></span>
<span data-ttu-id="9944d-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9944d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9944d-114">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="9944d-114">-LoadBalancer</span></span>
<span data-ttu-id="9944d-115">Указывает объект подсистемы **балансировки** , который содержит конфигурацию правила, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9944d-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9944d-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9944d-116">-Name</span></span>
<span data-ttu-id="9944d-117">Указывает имя конфигурации правила подсистемы балансировки нагрузки, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9944d-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9944d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9944d-118">CommonParameters</span></span>
<span data-ttu-id="9944d-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9944d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9944d-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9944d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9944d-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9944d-121">INPUTS</span></span>

### <span data-ttu-id="9944d-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9944d-122">PSLoadBalancer</span></span>
<span data-ttu-id="9944d-123">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="9944d-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="9944d-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9944d-124">OUTPUTS</span></span>

### <span data-ttu-id="9944d-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9944d-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="9944d-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="9944d-126">NOTES</span></span>

## <span data-ttu-id="9944d-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9944d-127">RELATED LINKS</span></span>

[<span data-ttu-id="9944d-128">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9944d-128">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="9944d-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="9944d-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="9944d-130">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9944d-130">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="9944d-131">New-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9944d-131">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="9944d-132">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9944d-132">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


