---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: d905159ca62f34584f045a699621f6672507ffe1
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908030"
---
# <span data-ttu-id="22440-101">New-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="22440-101">New-AzsSubscription</span></span>

## <span data-ttu-id="22440-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="22440-102">SYNOPSIS</span></span>
<span data-ttu-id="22440-103">Создайте подписку.</span><span class="sxs-lookup"><span data-stu-id="22440-103">Create a subscription.</span></span>

## <span data-ttu-id="22440-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="22440-104">SYNTAX</span></span>

```
New-AzsSubscription [-OfferId] <String> [[-DisplayName] <String>] [[-TenantId] <String>]
 [[-SubscriptionId] <String>] [[-State] <String>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22440-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="22440-105">DESCRIPTION</span></span>
<span data-ttu-id="22440-106">Создайте подписку.</span><span class="sxs-lookup"><span data-stu-id="22440-106">Create a subscription.</span></span>

## <span data-ttu-id="22440-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="22440-107">EXAMPLES</span></span>

### <span data-ttu-id="22440-108">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="22440-108">EXAMPLE 1</span></span>
```
New-AzsSubscription -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="22440-109">Создайте подписку.</span><span class="sxs-lookup"><span data-stu-id="22440-109">Create a subscription.</span></span>

## <span data-ttu-id="22440-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="22440-110">PARAMETERS</span></span>

### <span data-ttu-id="22440-111">-OfferId</span><span class="sxs-lookup"><span data-stu-id="22440-111">-OfferId</span></span>
<span data-ttu-id="22440-112">Идентификатор предложения в рамках области поставщика делегированных данных.</span><span class="sxs-lookup"><span data-stu-id="22440-112">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="22440-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="22440-113">-DisplayName</span></span>
<span data-ttu-id="22440-114">Название подписки.</span><span class="sxs-lookup"><span data-stu-id="22440-114">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22440-115">-TenantId</span><span class="sxs-lookup"><span data-stu-id="22440-115">-TenantId</span></span>
<span data-ttu-id="22440-116">Идентификатор клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="22440-116">Directory tenant identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22440-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="22440-117">-SubscriptionId</span></span>
<span data-ttu-id="22440-118">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="22440-118">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22440-119">-State</span><span class="sxs-lookup"><span data-stu-id="22440-119">-State</span></span>
<span data-ttu-id="22440-120">Состояние подписки.</span><span class="sxs-lookup"><span data-stu-id="22440-120">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22440-121">-Location</span><span class="sxs-lookup"><span data-stu-id="22440-121">-Location</span></span>
<span data-ttu-id="22440-122">Расположение, в котором расположен ресурс.</span><span class="sxs-lookup"><span data-stu-id="22440-122">Location where resource is location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ArmLocation

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22440-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22440-123">-WhatIf</span></span>
<span data-ttu-id="22440-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="22440-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22440-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="22440-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22440-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22440-126">-Confirm</span></span>
<span data-ttu-id="22440-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="22440-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22440-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22440-128">CommonParameters</span></span>
<span data-ttu-id="22440-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="22440-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22440-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22440-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22440-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="22440-131">INPUTS</span></span>

## <span data-ttu-id="22440-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="22440-132">OUTPUTS</span></span>

### <span data-ttu-id="22440-133">Microsoft. AzureStack. Management. Subscription. Models. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="22440-133">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="22440-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="22440-134">NOTES</span></span>

## <span data-ttu-id="22440-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="22440-135">RELATED LINKS</span></span>
