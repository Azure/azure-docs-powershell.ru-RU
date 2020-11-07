---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25411a71a6d8233be55ab25ac99487da0b44bd0b
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93908653"
---
# <span data-ttu-id="98b45-101">Remove-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="98b45-101">Remove-AzsUserSubscription</span></span>

## <span data-ttu-id="98b45-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="98b45-102">SYNOPSIS</span></span>
<span data-ttu-id="98b45-103">Удаляет указанную подписку клиента.</span><span class="sxs-lookup"><span data-stu-id="98b45-103">Removes the specified tenant subscription.</span></span>

## <span data-ttu-id="98b45-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="98b45-104">SYNTAX</span></span>

```
Remove-AzsUserSubscription [-SubscriptionId] <Guid> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98b45-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98b45-105">DESCRIPTION</span></span>
<span data-ttu-id="98b45-106">Удаляет указанную подписку клиента.</span><span class="sxs-lookup"><span data-stu-id="98b45-106">Removes the specified tenant subscription.</span></span>

## <span data-ttu-id="98b45-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="98b45-107">EXAMPLES</span></span>

### <span data-ttu-id="98b45-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="98b45-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsUserSubscription -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="98b45-109">Удалите указанную подписку клиента.</span><span class="sxs-lookup"><span data-stu-id="98b45-109">Remove the specified tenant subscription.</span></span>

## <span data-ttu-id="98b45-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="98b45-110">PARAMETERS</span></span>

### <span data-ttu-id="98b45-111">-Force</span><span class="sxs-lookup"><span data-stu-id="98b45-111">-Force</span></span>
<span data-ttu-id="98b45-112">Пометка для удаления элемента без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="98b45-112">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="98b45-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="98b45-113">-SubscriptionId</span></span>
<span data-ttu-id="98b45-114">Параметр идентификатора подписки.</span><span class="sxs-lookup"><span data-stu-id="98b45-114">Subscription Id parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98b45-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98b45-115">-Confirm</span></span>
<span data-ttu-id="98b45-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="98b45-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98b45-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98b45-117">-WhatIf</span></span>
<span data-ttu-id="98b45-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="98b45-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98b45-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="98b45-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98b45-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98b45-120">CommonParameters</span></span>
<span data-ttu-id="98b45-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="98b45-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98b45-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98b45-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98b45-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="98b45-123">INPUTS</span></span>

## <span data-ttu-id="98b45-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="98b45-124">OUTPUTS</span></span>

## <span data-ttu-id="98b45-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="98b45-125">NOTES</span></span>

## <span data-ttu-id="98b45-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98b45-126">RELATED LINKS</span></span>

