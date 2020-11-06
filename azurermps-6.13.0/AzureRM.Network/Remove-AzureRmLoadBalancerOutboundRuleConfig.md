---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: cc9a79b424d6ad81804aaed0d941ca017463abba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565852"
---
# <span data-ttu-id="a3ac1-101">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a3ac1-101">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="a3ac1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a3ac1-102">SYNOPSIS</span></span>
<span data-ttu-id="a3ac1-103">Удаляет конфигурацию исходящего правила из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a3ac1-103">Removes an outbound rule configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3ac1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a3ac1-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3ac1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3ac1-105">DESCRIPTION</span></span>
<span data-ttu-id="a3ac1-106">Командлет **Remove-AzureRmLoadBalancerOutboundRuleConfig** удаляет конфигурацию исходящего правила из подсистемы балансировки нагрузки Azure.</span><span class="sxs-lookup"><span data-stu-id="a3ac1-106">The **Remove-AzureRmLoadBalancerOutboundRuleConfig** cmdlet removes an outbound rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="a3ac1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a3ac1-107">EXAMPLES</span></span>

### <span data-ttu-id="a3ac1-108">Пример 1: удаление исходящего правила из подсистемы балансировки нагрузки для Azure</span><span class="sxs-lookup"><span data-stu-id="a3ac1-108">Example 1: Delete an outbound rule from an Azure load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzureRmLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Remove-AzureRmLoadBalancerOutboundRuleConfig -Name "RuleName" -LoadBalancer $slb
PS C:\>Set-AzureRmLoadBalancer -LoadBalancer $slb
```

<span data-ttu-id="a3ac1-109">Первая команда получает подсистему балансировки нагрузки, связанную с конфигурацией исходящего правила, которую вы хотите удалить, и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="a3ac1-109">The first command gets the load balancer that is associated with the outbound rule configuration you want to remove, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="a3ac1-110">Вторая команда удаляет соответствующую конфигурацию исходящего правила из подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a3ac1-110">The second command removes the associated outbound rule configuration from the load balancer.</span></span>
<span data-ttu-id="a3ac1-111">Третья команда обновляет подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a3ac1-111">The third command updates the load balancer.</span></span>

## <span data-ttu-id="a3ac1-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a3ac1-112">PARAMETERS</span></span>

### <span data-ttu-id="a3ac1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3ac1-113">-DefaultProfile</span></span>
<span data-ttu-id="a3ac1-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a3ac1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3ac1-115">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="a3ac1-115">-LoadBalancer</span></span>
<span data-ttu-id="a3ac1-116">Ссылка на ресурс подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a3ac1-116">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="a3ac1-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a3ac1-117">-Name</span></span>
<span data-ttu-id="a3ac1-118">Имя правила для исходящих подключений</span><span class="sxs-lookup"><span data-stu-id="a3ac1-118">The Name of outbound rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3ac1-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3ac1-119">-Confirm</span></span>
<span data-ttu-id="a3ac1-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a3ac1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3ac1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3ac1-121">-WhatIf</span></span>
<span data-ttu-id="a3ac1-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a3ac1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3ac1-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a3ac1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3ac1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3ac1-124">CommonParameters</span></span>
<span data-ttu-id="a3ac1-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a3ac1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3ac1-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3ac1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3ac1-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a3ac1-127">INPUTS</span></span>

### <span data-ttu-id="a3ac1-128">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a3ac1-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a3ac1-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3ac1-129">OUTPUTS</span></span>

### <span data-ttu-id="a3ac1-130">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a3ac1-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a3ac1-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="a3ac1-131">NOTES</span></span>

## <span data-ttu-id="a3ac1-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a3ac1-132">RELATED LINKS</span></span>
