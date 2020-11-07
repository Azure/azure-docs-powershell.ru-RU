---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 617a7ac7d949eb54ab08b0d0cb06c0fca3ba79bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907965"
---
# <span data-ttu-id="bde31-101">New-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="bde31-101">New-AzsSubscription</span></span>

## <span data-ttu-id="bde31-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bde31-102">SYNOPSIS</span></span>
<span data-ttu-id="bde31-103">Создайте подписку.</span><span class="sxs-lookup"><span data-stu-id="bde31-103">Create a subscription.</span></span>

## <span data-ttu-id="bde31-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bde31-104">SYNTAX</span></span>

```
New-AzsSubscription [-OfferId] <String> [[-DisplayName] <String>] [[-TenantId] <String>]
 [[-SubscriptionId] <String>] [[-State] <String>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bde31-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bde31-105">DESCRIPTION</span></span>
<span data-ttu-id="bde31-106">Создайте подписку.</span><span class="sxs-lookup"><span data-stu-id="bde31-106">Create a subscription.</span></span>

## <span data-ttu-id="bde31-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bde31-107">EXAMPLES</span></span>

### <span data-ttu-id="bde31-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="bde31-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsSubscription -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="bde31-109">Создайте подписку.</span><span class="sxs-lookup"><span data-stu-id="bde31-109">Create a subscription.</span></span>

## <span data-ttu-id="bde31-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bde31-110">PARAMETERS</span></span>

### <span data-ttu-id="bde31-111">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bde31-111">-DisplayName</span></span>
<span data-ttu-id="bde31-112">Название подписки.</span><span class="sxs-lookup"><span data-stu-id="bde31-112">Subscription name.</span></span>

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

### <span data-ttu-id="bde31-113">-Location</span><span class="sxs-lookup"><span data-stu-id="bde31-113">-Location</span></span>
<span data-ttu-id="bde31-114">Расположение, в котором расположен ресурс.</span><span class="sxs-lookup"><span data-stu-id="bde31-114">Location where resource is location.</span></span>

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

### <span data-ttu-id="bde31-115">-OfferId</span><span class="sxs-lookup"><span data-stu-id="bde31-115">-OfferId</span></span>
<span data-ttu-id="bde31-116">Идентификатор предложения в рамках области поставщика делегированных данных.</span><span class="sxs-lookup"><span data-stu-id="bde31-116">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="bde31-117">-State</span><span class="sxs-lookup"><span data-stu-id="bde31-117">-State</span></span>
<span data-ttu-id="bde31-118">Состояние подписки.</span><span class="sxs-lookup"><span data-stu-id="bde31-118">Subscription state.</span></span>

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

### <span data-ttu-id="bde31-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bde31-119">-SubscriptionId</span></span>
<span data-ttu-id="bde31-120">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="bde31-120">Subscription identifier.</span></span>

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

### <span data-ttu-id="bde31-121">-TenantId</span><span class="sxs-lookup"><span data-stu-id="bde31-121">-TenantId</span></span>
<span data-ttu-id="bde31-122">Идентификатор клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="bde31-122">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="bde31-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bde31-123">-Confirm</span></span>
<span data-ttu-id="bde31-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bde31-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bde31-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bde31-125">-WhatIf</span></span>
<span data-ttu-id="bde31-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bde31-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bde31-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bde31-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bde31-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bde31-128">CommonParameters</span></span>
<span data-ttu-id="bde31-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bde31-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bde31-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bde31-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bde31-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bde31-131">INPUTS</span></span>

## <span data-ttu-id="bde31-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bde31-132">OUTPUTS</span></span>

### <span data-ttu-id="bde31-133">Microsoft. AzureStack. Management. Subscription. Models. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="bde31-133">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="bde31-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="bde31-134">NOTES</span></span>

## <span data-ttu-id="bde31-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bde31-135">RELATED LINKS</span></span>

