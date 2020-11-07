---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e6588eed555062aaf6dbb4075dffd9506c05503
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908362"
---
# <span data-ttu-id="3e1ca-101">Remove-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="3e1ca-101">Remove-AzsSubscription</span></span>

## <span data-ttu-id="3e1ca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e1ca-102">SYNOPSIS</span></span>
<span data-ttu-id="3e1ca-103">Удаление указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="3e1ca-103">Delete the specifed subscription.</span></span>

## <span data-ttu-id="3e1ca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e1ca-104">SYNTAX</span></span>

```
Remove-AzsSubscription [-SubscriptionId] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e1ca-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e1ca-105">DESCRIPTION</span></span>
<span data-ttu-id="3e1ca-106">Удаление указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="3e1ca-106">Delete the specifed subscription.</span></span>

## <span data-ttu-id="3e1ca-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e1ca-107">EXAMPLES</span></span>

### <span data-ttu-id="3e1ca-108">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="3e1ca-108">EXAMPLE 1</span></span>
```
Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9
```

<span data-ttu-id="3e1ca-109">Удаление указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="3e1ca-109">Delete the specifed subscription.</span></span>

## <span data-ttu-id="3e1ca-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e1ca-110">PARAMETERS</span></span>

### <span data-ttu-id="3e1ca-111">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3e1ca-111">-SubscriptionId</span></span>
<span data-ttu-id="3e1ca-112">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="3e1ca-112">Id of the subscription.</span></span>

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

### <span data-ttu-id="3e1ca-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3e1ca-113">-Force</span></span>
<span data-ttu-id="3e1ca-114">Удаление подписки без запроса</span><span class="sxs-lookup"><span data-stu-id="3e1ca-114">Remove subscription without prompting</span></span>

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

### <span data-ttu-id="3e1ca-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e1ca-115">-WhatIf</span></span>
<span data-ttu-id="3e1ca-116">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3e1ca-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e1ca-117">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3e1ca-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e1ca-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e1ca-118">-Confirm</span></span>
<span data-ttu-id="3e1ca-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3e1ca-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e1ca-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e1ca-120">CommonParameters</span></span>
<span data-ttu-id="3e1ca-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e1ca-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e1ca-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e1ca-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e1ca-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e1ca-123">INPUTS</span></span>

## <span data-ttu-id="3e1ca-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e1ca-124">OUTPUTS</span></span>

## <span data-ttu-id="3e1ca-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e1ca-125">NOTES</span></span>

## <span data-ttu-id="3e1ca-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e1ca-126">RELATED LINKS</span></span>
