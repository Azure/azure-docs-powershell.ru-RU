---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 1bcaab526ac2fbb82d696db7197bbc8d69c0078f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735100"
---
# <span data-ttu-id="cff23-101">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cff23-101">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="cff23-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cff23-102">SYNOPSIS</span></span>
<span data-ttu-id="cff23-103">Получает конфигурацию исходящего правила в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="cff23-103">Gets an outbound rule configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cff23-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cff23-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cff23-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cff23-105">DESCRIPTION</span></span>
<span data-ttu-id="cff23-106">Командлет **Get-AzureRmLoadBalancerOutboundRuleConfig** получает конфигурацию исходящего правила или список конфигураций исходящих правил в подсистеме балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="cff23-106">The **Get-AzureRmLoadBalancerOutboundRuleConfig** cmdlet gets an outbound rule configuration or a list of outbound rule configurations in a load balancer.</span></span>

## <span data-ttu-id="cff23-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cff23-107">EXAMPLES</span></span>

### <span data-ttu-id="cff23-108">Пример 1: получение конфигурации исходящего правила в подсистеме балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="cff23-108">Example 1: Get an outbound rule configuration in a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzureRmLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

<span data-ttu-id="cff23-109">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="cff23-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="cff23-110">Вторая команда получает конфигурацию исходящего правила с именем MyRule, связанную с этой подсистемой балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="cff23-110">The second command gets the outbound rule configuration named MyRule associated with that load balancer.</span></span>

## <span data-ttu-id="cff23-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cff23-111">PARAMETERS</span></span>

### <span data-ttu-id="cff23-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cff23-112">-DefaultProfile</span></span>
<span data-ttu-id="cff23-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cff23-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cff23-114">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="cff23-114">-LoadBalancer</span></span>
<span data-ttu-id="cff23-115">Ссылка на ресурс подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="cff23-115">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="cff23-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cff23-116">-Name</span></span>
<span data-ttu-id="cff23-117">Имя правила исходящего трафика.</span><span class="sxs-lookup"><span data-stu-id="cff23-117">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="cff23-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cff23-118">CommonParameters</span></span>
<span data-ttu-id="cff23-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cff23-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cff23-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cff23-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cff23-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cff23-121">INPUTS</span></span>

### <span data-ttu-id="cff23-122">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cff23-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="cff23-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cff23-123">OUTPUTS</span></span>

### <span data-ttu-id="cff23-124">Microsoft. Azure. Commands. Network. Models. PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="cff23-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="cff23-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="cff23-125">NOTES</span></span>

## <span data-ttu-id="cff23-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cff23-126">RELATED LINKS</span></span>
