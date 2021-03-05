---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdndeliveryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRule.md
ms.openlocfilehash: a2143e0363d08a06ac72ee7c5207ef93f5c3a509
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001832"
---
# <span data-ttu-id="4eb35-101">New-AzCdnDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="4eb35-101">New-AzCdnDeliveryRule</span></span>

## <span data-ttu-id="4eb35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4eb35-102">SYNOPSIS</span></span>
<span data-ttu-id="4eb35-103">Создает правило доставки.</span><span class="sxs-lookup"><span data-stu-id="4eb35-103">Creates a delivery rule.</span></span>

## <span data-ttu-id="4eb35-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4eb35-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRule [-Name <String>] -Order <Int32> [-Condition <PSDeliveryRuleCondition[]>]
 -Action <PSDeliveryRuleAction[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4eb35-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4eb35-105">DESCRIPTION</span></span>
<span data-ttu-id="4eb35-106">Для создания конечной точки CDN создается правило доставки для **new-AzCdnDeliveryRule.**</span><span class="sxs-lookup"><span data-stu-id="4eb35-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="4eb35-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4eb35-107">EXAMPLES</span></span>

### <span data-ttu-id="4eb35-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4eb35-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRule -Name "rule1" -Order 1 -Condition $cond1 -Action $action1

Name  Order Actions           Conditions
----  ----- -------           ----------
rule1     1 {Accept-Encoding} {Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition}
```

<span data-ttu-id="4eb35-109">Создайте простое правило.</span><span class="sxs-lookup"><span data-stu-id="4eb35-109">Create a simple rule.</span></span>

## <span data-ttu-id="4eb35-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4eb35-110">PARAMETERS</span></span>

### <span data-ttu-id="4eb35-111">-Action</span><span class="sxs-lookup"><span data-stu-id="4eb35-111">-Action</span></span>
<span data-ttu-id="4eb35-112">Список действий, которые выполняются при выполнении всех условий правила.</span><span class="sxs-lookup"><span data-stu-id="4eb35-112">A list of actions that are executed when all the conditions of a rule are satisfied.</span></span>

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

### <span data-ttu-id="4eb35-113">-Condition</span><span class="sxs-lookup"><span data-stu-id="4eb35-113">-Condition</span></span>
<span data-ttu-id="4eb35-114">Список условий, которые должны соответствовать для выполнения действий.</span><span class="sxs-lookup"><span data-stu-id="4eb35-114">A list of conditions that must be matched for the actions to be executed.</span></span>

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

### <span data-ttu-id="4eb35-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eb35-115">-DefaultProfile</span></span>
<span data-ttu-id="4eb35-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4eb35-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4eb35-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4eb35-117">-Name</span></span>
<span data-ttu-id="4eb35-118">Имя правила</span><span class="sxs-lookup"><span data-stu-id="4eb35-118">Name of the rule</span></span>

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

### <span data-ttu-id="4eb35-119">-Порядок</span><span class="sxs-lookup"><span data-stu-id="4eb35-119">-Order</span></span>
<span data-ttu-id="4eb35-120">Порядок правила</span><span class="sxs-lookup"><span data-stu-id="4eb35-120">Order of the rule</span></span>

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

### <span data-ttu-id="4eb35-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eb35-121">CommonParameters</span></span>
<span data-ttu-id="4eb35-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4eb35-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eb35-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4eb35-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eb35-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4eb35-124">INPUTS</span></span>

### <span data-ttu-id="4eb35-125">Нет</span><span class="sxs-lookup"><span data-stu-id="4eb35-125">None</span></span>

## <span data-ttu-id="4eb35-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4eb35-126">OUTPUTS</span></span>

### <span data-ttu-id="4eb35-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span><span class="sxs-lookup"><span data-stu-id="4eb35-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRule</span></span>

## <span data-ttu-id="4eb35-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4eb35-128">NOTES</span></span>

## <span data-ttu-id="4eb35-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4eb35-129">RELATED LINKS</span></span>
