---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdndeliveryrulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
ms.openlocfilehash: 6367910117ff00219c3194a06bb51754913df063
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009219"
---
# <span data-ttu-id="2dbef-101">New-AzCdnDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="2dbef-101">New-AzCdnDeliveryRuleCondition</span></span>

## <span data-ttu-id="2dbef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2dbef-102">SYNOPSIS</span></span>
<span data-ttu-id="2dbef-103">Создает условие правила доставки.</span><span class="sxs-lookup"><span data-stu-id="2dbef-103">Creates a delivery rule condition.</span></span>

## <span data-ttu-id="2dbef-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2dbef-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRuleCondition -MatchVariable <String> -Operator <String> [-Selector <String>]
 -MatchValue <String[]> [-Transform <String>] [-NegateCondition] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2dbef-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2dbef-105">DESCRIPTION</span></span>
<span data-ttu-id="2dbef-106">Для создания конечной точки CDN создается правило доставки для **new-AzCdnDeliveryRule.**</span><span class="sxs-lookup"><span data-stu-id="2dbef-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="2dbef-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2dbef-107">EXAMPLES</span></span>

### <span data-ttu-id="2dbef-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2dbef-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleCondition -MatchVariable UrlPath -Operator Equal -MatchValue "abc"

MatchVariable   : UrlPath
Operator        : Equal
Selector        :
MatchValue      : {abc}
NegateCondition : False
Transfroms      :
```

<span data-ttu-id="2dbef-109">Создайте простое условие.</span><span class="sxs-lookup"><span data-stu-id="2dbef-109">Create a simple condition.</span></span>

## <span data-ttu-id="2dbef-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2dbef-110">PARAMETERS</span></span>

### <span data-ttu-id="2dbef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dbef-111">-DefaultProfile</span></span>
<span data-ttu-id="2dbef-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2dbef-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dbef-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="2dbef-113">-MatchValue</span></span>
<span data-ttu-id="2dbef-114">Список возможных значений совпадений.</span><span class="sxs-lookup"><span data-stu-id="2dbef-114">List of possible match values.</span></span>

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

### <span data-ttu-id="2dbef-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="2dbef-115">-MatchVariable</span></span>
<span data-ttu-id="2dbef-116">Соответствует переменной условия.</span><span class="sxs-lookup"><span data-stu-id="2dbef-116">Match variable of the condition.</span></span>

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

### <span data-ttu-id="2dbef-117">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="2dbef-117">-NegateCondition</span></span>
<span data-ttu-id="2dbef-118">В нем описывается, следует ли ото всех результатов этого условия отрицать.</span><span class="sxs-lookup"><span data-stu-id="2dbef-118">Describes if the result of this condition should be negated.</span></span>

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

### <span data-ttu-id="2dbef-119">-Operator</span><span class="sxs-lookup"><span data-stu-id="2dbef-119">-Operator</span></span>
<span data-ttu-id="2dbef-120">Оператор для совпадения</span><span class="sxs-lookup"><span data-stu-id="2dbef-120">Describes operator to be matched</span></span>

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

### <span data-ttu-id="2dbef-121">-Selector</span><span class="sxs-lookup"><span data-stu-id="2dbef-121">-Selector</span></span>
<span data-ttu-id="2dbef-122">Имя области выбора, которая должна быть совме же</span><span class="sxs-lookup"><span data-stu-id="2dbef-122">Name of Selector to be matched</span></span>

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

### <span data-ttu-id="2dbef-123">-Transform</span><span class="sxs-lookup"><span data-stu-id="2dbef-123">-Transform</span></span>
<span data-ttu-id="2dbef-124">Преобразуются для применения перед соответствием.</span><span class="sxs-lookup"><span data-stu-id="2dbef-124">Transform to apply before matching.</span></span>
<span data-ttu-id="2dbef-125">Возможные значения: нижний и верхний регистры</span><span class="sxs-lookup"><span data-stu-id="2dbef-125">Possible values are Lowercase and Uppercase</span></span>

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

### <span data-ttu-id="2dbef-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dbef-126">CommonParameters</span></span>
<span data-ttu-id="2dbef-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dbef-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dbef-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2dbef-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dbef-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2dbef-129">INPUTS</span></span>

### <span data-ttu-id="2dbef-130">Нет</span><span class="sxs-lookup"><span data-stu-id="2dbef-130">None</span></span>

## <span data-ttu-id="2dbef-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2dbef-131">OUTPUTS</span></span>

### <span data-ttu-id="2dbef-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="2dbef-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span></span>

## <span data-ttu-id="2dbef-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2dbef-133">NOTES</span></span>

## <span data-ttu-id="2dbef-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2dbef-134">RELATED LINKS</span></span>
