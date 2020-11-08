---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryrulecondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleCondition.md
ms.openlocfilehash: 7d7d15fdbaac3de1a212c13fb35dee134dde5381
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236243"
---
# <span data-ttu-id="44527-101">New-AzCdnDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="44527-101">New-AzCdnDeliveryRuleCondition</span></span>

## <span data-ttu-id="44527-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="44527-102">SYNOPSIS</span></span>
<span data-ttu-id="44527-103">Создание условия для правила доставки.</span><span class="sxs-lookup"><span data-stu-id="44527-103">Creates a delivery rule condition.</span></span>

## <span data-ttu-id="44527-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="44527-104">SYNTAX</span></span>

```
New-AzCdnDeliveryRuleCondition -MatchVariable <String> -Operator <String> [-Selector <String>]
 -MatchValue <String[]> [-Transform <String>] [-NegateCondition] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="44527-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="44527-105">DESCRIPTION</span></span>
<span data-ttu-id="44527-106">Командлет **New-AzCdnDeliveryRule** создает правило доставки для создания КОНЕЧНОЙ точки CDN.</span><span class="sxs-lookup"><span data-stu-id="44527-106">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="44527-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="44527-107">EXAMPLES</span></span>

### <span data-ttu-id="44527-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="44527-108">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleCondition -MatchVariable UrlPath -Operator Equal -MatchValue "abc"

MatchVariable   : UrlPath
Operator        : Equal
Selector        :
MatchValue      : {abc}
NegateCondition : False
Transfroms      :
```

<span data-ttu-id="44527-109">Создание простого условия.</span><span class="sxs-lookup"><span data-stu-id="44527-109">Create a simple condition.</span></span>

## <span data-ttu-id="44527-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="44527-110">PARAMETERS</span></span>

### <span data-ttu-id="44527-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44527-111">-DefaultProfile</span></span>
<span data-ttu-id="44527-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="44527-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44527-113">-MatchValue</span><span class="sxs-lookup"><span data-stu-id="44527-113">-MatchValue</span></span>
<span data-ttu-id="44527-114">Список возможных значений соответствия.</span><span class="sxs-lookup"><span data-stu-id="44527-114">List of possible match values.</span></span>

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

### <span data-ttu-id="44527-115">-MatchVariable</span><span class="sxs-lookup"><span data-stu-id="44527-115">-MatchVariable</span></span>
<span data-ttu-id="44527-116">Соответствует переменной условия.</span><span class="sxs-lookup"><span data-stu-id="44527-116">Match variable of the condition.</span></span>

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

### <span data-ttu-id="44527-117">-NegateCondition</span><span class="sxs-lookup"><span data-stu-id="44527-117">-NegateCondition</span></span>
<span data-ttu-id="44527-118">Указывает, следует ли инвертировать результат этого условия.</span><span class="sxs-lookup"><span data-stu-id="44527-118">Describes if the result of this condition should be negated.</span></span>

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

### <span data-ttu-id="44527-119">-Operator</span><span class="sxs-lookup"><span data-stu-id="44527-119">-Operator</span></span>
<span data-ttu-id="44527-120">Описывает оператор для сопоставления</span><span class="sxs-lookup"><span data-stu-id="44527-120">Describes operator to be matched</span></span>

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

### <span data-ttu-id="44527-121">-Selector</span><span class="sxs-lookup"><span data-stu-id="44527-121">-Selector</span></span>
<span data-ttu-id="44527-122">Имя средства выбора для сопоставления</span><span class="sxs-lookup"><span data-stu-id="44527-122">Name of Selector to be matched</span></span>

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

### <span data-ttu-id="44527-123">-Transform</span><span class="sxs-lookup"><span data-stu-id="44527-123">-Transform</span></span>
<span data-ttu-id="44527-124">Преобразование для применения перед совпадением.</span><span class="sxs-lookup"><span data-stu-id="44527-124">Transform to apply before matching.</span></span>
<span data-ttu-id="44527-125">Допустимые значения — строчные и прописные</span><span class="sxs-lookup"><span data-stu-id="44527-125">Possible values are Lowercase and Uppercase</span></span>

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

### <span data-ttu-id="44527-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44527-126">CommonParameters</span></span>
<span data-ttu-id="44527-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="44527-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44527-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44527-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44527-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="44527-129">INPUTS</span></span>

### <span data-ttu-id="44527-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="44527-130">None</span></span>

## <span data-ttu-id="44527-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="44527-131">OUTPUTS</span></span>

### <span data-ttu-id="44527-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span><span class="sxs-lookup"><span data-stu-id="44527-132">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleCondition</span></span>

## <span data-ttu-id="44527-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="44527-133">NOTES</span></span>

## <span data-ttu-id="44527-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="44527-134">RELATED LINKS</span></span>
