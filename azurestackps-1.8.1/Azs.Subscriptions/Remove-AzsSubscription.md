---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e6588eed555062aaf6dbb4075dffd9506c05503
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93908994"
---
# <span data-ttu-id="ed68b-101">Remove-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="ed68b-101">Remove-AzsSubscription</span></span>

## <span data-ttu-id="ed68b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ed68b-102">SYNOPSIS</span></span>
<span data-ttu-id="ed68b-103">Удаление указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="ed68b-103">Delete the specifed subscription.</span></span>

## <span data-ttu-id="ed68b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ed68b-104">SYNTAX</span></span>

```
Remove-AzsSubscription [-SubscriptionId] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed68b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed68b-105">DESCRIPTION</span></span>
<span data-ttu-id="ed68b-106">Удаление указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="ed68b-106">Delete the specifed subscription.</span></span>

## <span data-ttu-id="ed68b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ed68b-107">EXAMPLES</span></span>

### <span data-ttu-id="ed68b-108">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="ed68b-108">EXAMPLE 1</span></span>
```
Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9
```

<span data-ttu-id="ed68b-109">Удаление указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="ed68b-109">Delete the specifed subscription.</span></span>

## <span data-ttu-id="ed68b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ed68b-110">PARAMETERS</span></span>

### <span data-ttu-id="ed68b-111">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ed68b-111">-SubscriptionId</span></span>
<span data-ttu-id="ed68b-112">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="ed68b-112">Id of the subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed68b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ed68b-113">-Force</span></span>
<span data-ttu-id="ed68b-114">Удаление подписки без запроса</span><span class="sxs-lookup"><span data-stu-id="ed68b-114">Remove subscription without prompting</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed68b-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed68b-115">-WhatIf</span></span>
<span data-ttu-id="ed68b-116">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ed68b-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed68b-117">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ed68b-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed68b-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed68b-118">-Confirm</span></span>
<span data-ttu-id="ed68b-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ed68b-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed68b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed68b-120">CommonParameters</span></span>
<span data-ttu-id="ed68b-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ed68b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed68b-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed68b-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed68b-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ed68b-123">INPUTS</span></span>

## <span data-ttu-id="ed68b-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed68b-124">OUTPUTS</span></span>

## <span data-ttu-id="ed68b-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="ed68b-125">NOTES</span></span>

## <span data-ttu-id="ed68b-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed68b-126">RELATED LINKS</span></span>
