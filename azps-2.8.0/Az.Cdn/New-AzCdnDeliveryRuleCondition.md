---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
ms.openlocfilehash: 830b561a3d46e23f083d77dcac627b28f7dbb94e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727582"
---
# <span data-ttu-id="e6de9-101">New-AzCdnDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="e6de9-101">New-AzCdnDeliveryRuleCondition</span></span>

## <span data-ttu-id="e6de9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e6de9-102">SYNOPSIS</span></span>
<span data-ttu-id="e6de9-103">Создание условия для правила доставки.</span><span class="sxs-lookup"><span data-stu-id="e6de9-103">Creates a delivery rule condition.</span></span>

## <span data-ttu-id="e6de9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e6de9-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRuleCondition -MatchVariable <String> -Operator <String> -MatchValue <String[]>
 [-Transform <String>] [-NegateCondition] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6de9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6de9-105">DESCRIPTION</span></span>
<span data-ttu-id="e6de9-106">Командлет **New-AzCdnDeliveryRule** создает правило доставки для создания КОНЕЧНОЙ точки CDN.</span><span class="sxs-lookup"><span data-stu-id="e6de9-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="e6de9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e6de9-107">EXAMPLES</span></span>

### <span data-ttu-id="e6de9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e6de9-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleCondition -MatchVariable UrlPath -Operator Equal -MatchValue "abc"

MatchVariable   : UrlPath
Operator        : Equal
Selector        :
MatchValue      : {abc}
NegateCondition : False
Transfroms      :
```

<span data-ttu-id="e6de9-109">Создание простого условия.</span><span class="sxs-lookup"><span data-stu-id="e6de9-109">Create a simple condition.</span></span>

## <span data-ttu-id="e6de9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e6de9-110">PARAMETERS</span></span>

### <span data-ttu-id="e6de9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6de9-111">-DefaultProfile</span></span>
<span data-ttu-id="e6de9-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e6de9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6de9-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="e6de9-113">-MatchValue</span></span>
<span data-ttu-id="e6de9-114">Список возможных значений соответствия.</span><span class="sxs-lookup"><span data-stu-id="e6de9-114">List of possible match values.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6de9-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="e6de9-115">-MatchVariable</span></span>
<span data-ttu-id="e6de9-116">Соответствует переменной условия.</span><span class="sxs-lookup"><span data-stu-id="e6de9-116">Match variable of the condition.</span></span>

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

### <span data-ttu-id="e6de9-117">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="e6de9-117">-NegateCondition</span></span>
<span data-ttu-id="e6de9-118">Указывает, следует ли инвертировать результат этого условия.</span><span class="sxs-lookup"><span data-stu-id="e6de9-118">Describes if the result of this condition should be negated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6de9-119">-Operator</span><span class="sxs-lookup"><span data-stu-id="e6de9-119">-Operator</span></span>
<span data-ttu-id="e6de9-120">Описывает оператор для сопоставления</span><span class="sxs-lookup"><span data-stu-id="e6de9-120">Describes operator to be matched</span></span>

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

### <span data-ttu-id="e6de9-121">-Transform</span><span class="sxs-lookup"><span data-stu-id="e6de9-121">-Transform</span></span>
<span data-ttu-id="e6de9-122">Преобразование для применения перед совпадением.</span><span class="sxs-lookup"><span data-stu-id="e6de9-122">Transform to apply before matching.</span></span>
<span data-ttu-id="e6de9-123">Допустимые значения — строчные и прописные</span><span class="sxs-lookup"><span data-stu-id="e6de9-123">Possible values are Lowercase and Uppercase</span></span>

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

### <span data-ttu-id="e6de9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6de9-124">CommonParameters</span></span>
<span data-ttu-id="e6de9-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e6de9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6de9-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6de9-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6de9-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e6de9-127">INPUTS</span></span>

### <span data-ttu-id="e6de9-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="e6de9-128">None</span></span>

## <span data-ttu-id="e6de9-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6de9-129">OUTPUTS</span></span>

### <span data-ttu-id="e6de9-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="e6de9-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span></span>

## <span data-ttu-id="e6de9-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="e6de9-131">NOTES</span></span>

## <span data-ttu-id="e6de9-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6de9-132">RELATED LINKS</span></span>
