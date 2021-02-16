---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
ms.openlocfilehash: 7d7d15fdbaac3de1a212c13fb35dee134dde5381
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211937"
---
# <span data-ttu-id="77a51-101">New-AzCdnDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="77a51-101">New-AzCdnDeliveryRuleCondition</span></span>

## <span data-ttu-id="77a51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77a51-102">SYNOPSIS</span></span>
<span data-ttu-id="77a51-103">Создает условие правила доставки.</span><span class="sxs-lookup"><span data-stu-id="77a51-103">Creates a delivery rule condition.</span></span>

## <span data-ttu-id="77a51-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="77a51-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRuleCondition -MatchVariable <String> -Operator <String> [-Selector <String>]
 -MatchValue <String[]> [-Transform <String>] [-NegateCondition] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="77a51-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77a51-105">DESCRIPTION</span></span>
<span data-ttu-id="77a51-106">Для создания конечной точки CDN создается правило доставки для **new-AzCdnDeliveryRule.**</span><span class="sxs-lookup"><span data-stu-id="77a51-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="77a51-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="77a51-107">EXAMPLES</span></span>

### <span data-ttu-id="77a51-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="77a51-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleCondition -MatchVariable UrlPath -Operator Equal -MatchValue "abc"

MatchVariable   : UrlPath
Operator        : Equal
Selector        :
MatchValue      : {abc}
NegateCondition : False
Transfroms      :
```

<span data-ttu-id="77a51-109">Создайте простое условие.</span><span class="sxs-lookup"><span data-stu-id="77a51-109">Create a simple condition.</span></span>

## <span data-ttu-id="77a51-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77a51-110">PARAMETERS</span></span>

### <span data-ttu-id="77a51-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77a51-111">-DefaultProfile</span></span>
<span data-ttu-id="77a51-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="77a51-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77a51-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="77a51-113">-MatchValue</span></span>
<span data-ttu-id="77a51-114">Список возможных значений совпадений.</span><span class="sxs-lookup"><span data-stu-id="77a51-114">List of possible match values.</span></span>

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

### <span data-ttu-id="77a51-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="77a51-115">-MatchVariable</span></span>
<span data-ttu-id="77a51-116">Соответствует переменной условия.</span><span class="sxs-lookup"><span data-stu-id="77a51-116">Match variable of the condition.</span></span>

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

### <span data-ttu-id="77a51-117">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="77a51-117">-NegateCondition</span></span>
<span data-ttu-id="77a51-118">В нем описывается, следует ли ото всех результатов этого условия отрицать.</span><span class="sxs-lookup"><span data-stu-id="77a51-118">Describes if the result of this condition should be negated.</span></span>

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

### <span data-ttu-id="77a51-119">-Operator</span><span class="sxs-lookup"><span data-stu-id="77a51-119">-Operator</span></span>
<span data-ttu-id="77a51-120">Оператор для совпадения</span><span class="sxs-lookup"><span data-stu-id="77a51-120">Describes operator to be matched</span></span>

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

### <span data-ttu-id="77a51-121">-Selector</span><span class="sxs-lookup"><span data-stu-id="77a51-121">-Selector</span></span>
<span data-ttu-id="77a51-122">Имя области выбора, которая должна быть совме же</span><span class="sxs-lookup"><span data-stu-id="77a51-122">Name of Selector to be matched</span></span>

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

### <span data-ttu-id="77a51-123">-Transform</span><span class="sxs-lookup"><span data-stu-id="77a51-123">-Transform</span></span>
<span data-ttu-id="77a51-124">Преобразуются для применения перед соответствием.</span><span class="sxs-lookup"><span data-stu-id="77a51-124">Transform to apply before matching.</span></span>
<span data-ttu-id="77a51-125">Возможные значения: нижний и верхний регистры</span><span class="sxs-lookup"><span data-stu-id="77a51-125">Possible values are Lowercase and Uppercase</span></span>

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

### <span data-ttu-id="77a51-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77a51-126">CommonParameters</span></span>
<span data-ttu-id="77a51-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77a51-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77a51-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="77a51-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77a51-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="77a51-129">INPUTS</span></span>

### <span data-ttu-id="77a51-130">Нет</span><span class="sxs-lookup"><span data-stu-id="77a51-130">None</span></span>

## <span data-ttu-id="77a51-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="77a51-131">OUTPUTS</span></span>

### <span data-ttu-id="77a51-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="77a51-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span></span>

## <span data-ttu-id="77a51-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="77a51-133">NOTES</span></span>

## <span data-ttu-id="77a51-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77a51-134">RELATED LINKS</span></span>
