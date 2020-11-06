---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 3a11b6435c263b5460258a63adb9b72d7ac9f02c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569939"
---
# <span data-ttu-id="cfa3c-101">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cfa3c-101">Get-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="cfa3c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cfa3c-102">SYNOPSIS</span></span>
<span data-ttu-id="cfa3c-103">Получает конфигурацию правила для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="cfa3c-103">Gets the rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfa3c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cfa3c-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfa3c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cfa3c-105">DESCRIPTION</span></span>
<span data-ttu-id="cfa3c-106">Командлет **Get-AzureRmLoadBalancerRuleConfig** получает одну или несколько конфигураций для подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="cfa3c-106">The **Get-AzureRmLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="cfa3c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cfa3c-107">EXAMPLES</span></span>

### <span data-ttu-id="cfa3c-108">Пример 1: получение конфигурации правила для подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="cfa3c-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="cfa3c-109">Первая команда получает подсистему балансировки нагрузки с именем MyLoadBalancer и сохраняет ее в переменной $slb.</span><span class="sxs-lookup"><span data-stu-id="cfa3c-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="cfa3c-110">Вторая команда получает конфигурацию связанного правила с именем MyLBrulename из подсистемы балансировки нагрузки в $slb.</span><span class="sxs-lookup"><span data-stu-id="cfa3c-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="cfa3c-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cfa3c-111">PARAMETERS</span></span>

### <span data-ttu-id="cfa3c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfa3c-112">-DefaultProfile</span></span>
<span data-ttu-id="cfa3c-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa3c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfa3c-114">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="cfa3c-114">-LoadBalancer</span></span>
<span data-ttu-id="cfa3c-115">Указывает подсистему балансировки нагрузки, связанную с конфигурацией правила, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="cfa3c-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="cfa3c-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cfa3c-116">-Name</span></span>
<span data-ttu-id="cfa3c-117">Указывает имя конфигурации правила, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="cfa3c-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="cfa3c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfa3c-118">CommonParameters</span></span>
<span data-ttu-id="cfa3c-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cfa3c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfa3c-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfa3c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfa3c-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cfa3c-121">INPUTS</span></span>

### <span data-ttu-id="cfa3c-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cfa3c-122">PSLoadBalancer</span></span>
<span data-ttu-id="cfa3c-123">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="cfa3c-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="cfa3c-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cfa3c-124">OUTPUTS</span></span>

### <span data-ttu-id="cfa3c-125">Microsoft. Azure. Commands. Network. Models. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="cfa3c-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="cfa3c-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="cfa3c-126">NOTES</span></span>

## <span data-ttu-id="cfa3c-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cfa3c-127">RELATED LINKS</span></span>

[<span data-ttu-id="cfa3c-128">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cfa3c-128">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="cfa3c-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cfa3c-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="cfa3c-130">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cfa3c-130">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="cfa3c-131">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cfa3c-131">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


