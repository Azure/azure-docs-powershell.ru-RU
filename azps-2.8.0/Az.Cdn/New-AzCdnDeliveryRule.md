---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
ms.openlocfilehash: 981447b1988dd750534a69529989d5d3480bc006
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727591"
---
# <span data-ttu-id="83072-101">New-AzCdnDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="83072-101">New-AzCdnDeliveryRule</span></span>

## <span data-ttu-id="83072-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="83072-102">SYNOPSIS</span></span>
<span data-ttu-id="83072-103">Создание правила доставки.</span><span class="sxs-lookup"><span data-stu-id="83072-103">Creates a delivery rule.</span></span>

## <span data-ttu-id="83072-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="83072-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRule [-Name <String>] -Order <Int32> [-Condition <PSDeliveryRuleCondition[]>]
 -Action <PSDeliveryRuleAction[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83072-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="83072-105">DESCRIPTION</span></span>
<span data-ttu-id="83072-106">Командлет **New-AzCdnDeliveryRule** создает правило доставки для создания КОНЕЧНОЙ точки CDN.</span><span class="sxs-lookup"><span data-stu-id="83072-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="83072-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="83072-107">EXAMPLES</span></span>

### <span data-ttu-id="83072-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="83072-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRule -Name "rule1" -Order 1 -Condition $cond1 -Action $action1

Name  Order Actions           Conditions
----  ----- -------           ----------
rule1     1 {Accept-Encoding} {Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition}
```

<span data-ttu-id="83072-109">Создание простого правила.</span><span class="sxs-lookup"><span data-stu-id="83072-109">Create a simple rule.</span></span>

## <span data-ttu-id="83072-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="83072-110">PARAMETERS</span></span>

### <span data-ttu-id="83072-111">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="83072-111">-Action</span></span>
<span data-ttu-id="83072-112">Список действий, выполняемых, если выполнены все условия правила.</span><span class="sxs-lookup"><span data-stu-id="83072-112">A list of actions that are executed when all the conditions of a rule are satisfied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83072-113">-Условие</span><span class="sxs-lookup"><span data-stu-id="83072-113">-Condition</span></span>
<span data-ttu-id="83072-114">Список условий, которые должны быть согласованы для выполняемых действий.</span><span class="sxs-lookup"><span data-stu-id="83072-114">A list of conditions that must be matched for the actions to be executed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83072-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83072-115">-DefaultProfile</span></span>
<span data-ttu-id="83072-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="83072-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83072-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="83072-117">-Name</span></span>
<span data-ttu-id="83072-118">Имя правила</span><span class="sxs-lookup"><span data-stu-id="83072-118">Name of the rule</span></span>

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

### <span data-ttu-id="83072-119">-Порядок</span><span class="sxs-lookup"><span data-stu-id="83072-119">-Order</span></span>
<span data-ttu-id="83072-120">Порядок правила</span><span class="sxs-lookup"><span data-stu-id="83072-120">Order of the rule</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83072-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83072-121">CommonParameters</span></span>
<span data-ttu-id="83072-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="83072-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83072-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83072-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83072-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="83072-124">INPUTS</span></span>

### <span data-ttu-id="83072-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="83072-125">None</span></span>

## <span data-ttu-id="83072-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="83072-126">OUTPUTS</span></span>

### <span data-ttu-id="83072-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="83072-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span></span>

## <span data-ttu-id="83072-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="83072-128">NOTES</span></span>

## <span data-ttu-id="83072-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="83072-129">RELATED LINKS</span></span>
