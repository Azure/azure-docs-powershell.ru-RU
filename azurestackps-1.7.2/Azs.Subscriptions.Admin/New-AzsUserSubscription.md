---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 33544da0c95e6b53da2a0dc189ca0dfe538da270
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907946"
---
# <span data-ttu-id="61eb7-101">New-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="61eb7-101">New-AzsUserSubscription</span></span>

## <span data-ttu-id="61eb7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="61eb7-102">SYNOPSIS</span></span>
<span data-ttu-id="61eb7-103">Создайте новую подписку.</span><span class="sxs-lookup"><span data-stu-id="61eb7-103">Create a new subscription.</span></span>

## <span data-ttu-id="61eb7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="61eb7-104">SYNTAX</span></span>

```
New-AzsUserSubscription [-Owner] <String> [-OfferId] <String> [[-TenantId] <String>] [[-DisplayName] <String>]
 [[-DelegatedProviderSubscriptionId] <String>] [[-RoutingResourceManagerType] <String>]
 [[-ExternalReferenceId] <String>] [[-State] <String>] [[-SubscriptionId] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61eb7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61eb7-105">DESCRIPTION</span></span>
<span data-ttu-id="61eb7-106">Создайте новую подписку.</span><span class="sxs-lookup"><span data-stu-id="61eb7-106">Create a new subscription.</span></span>

## <span data-ttu-id="61eb7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="61eb7-107">EXAMPLES</span></span>

### <span data-ttu-id="61eb7-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="61eb7-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsUserSubscription -Owner user@contoso.com -OfferId "/subscriptions/302d0fcd-5263-4f4d-82ba-383ad95a3e53/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/offers/offer1"
```

<span data-ttu-id="61eb7-109">Создает новую подписку пользователя</span><span class="sxs-lookup"><span data-stu-id="61eb7-109">Creates a new user subscription</span></span>

## <span data-ttu-id="61eb7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="61eb7-110">PARAMETERS</span></span>

### <span data-ttu-id="61eb7-111">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="61eb7-111">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="61eb7-112">Идентификатор родительской подписки на DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="61eb7-112">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61eb7-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="61eb7-113">-DisplayName</span></span>
<span data-ttu-id="61eb7-114">Название подписки.</span><span class="sxs-lookup"><span data-stu-id="61eb7-114">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61eb7-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="61eb7-115">-ExternalReferenceId</span></span>
<span data-ttu-id="61eb7-116">Идентификатор внешней ссылки.</span><span class="sxs-lookup"><span data-stu-id="61eb7-116">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61eb7-117">-OfferId</span><span class="sxs-lookup"><span data-stu-id="61eb7-117">-OfferId</span></span>
<span data-ttu-id="61eb7-118">Идентификатор предложения в рамках области поставщика делегированных данных.</span><span class="sxs-lookup"><span data-stu-id="61eb7-118">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61eb7-119">-Владелец</span><span class="sxs-lookup"><span data-stu-id="61eb7-119">-Owner</span></span>
<span data-ttu-id="61eb7-120">Владелец подписки.</span><span class="sxs-lookup"><span data-stu-id="61eb7-120">Subscription owner.</span></span>

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

### <span data-ttu-id="61eb7-121">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="61eb7-121">-RoutingResourceManagerType</span></span>
<span data-ttu-id="61eb7-122">Тип диспетчера ресурсов маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="61eb7-122">Routing resource manager type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: Default
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61eb7-123">-State</span><span class="sxs-lookup"><span data-stu-id="61eb7-123">-State</span></span>
<span data-ttu-id="61eb7-124">Состояние подписки.</span><span class="sxs-lookup"><span data-stu-id="61eb7-124">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61eb7-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="61eb7-125">-SubscriptionId</span></span>
<span data-ttu-id="61eb7-126">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="61eb7-126">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61eb7-127">-TenantId</span><span class="sxs-lookup"><span data-stu-id="61eb7-127">-TenantId</span></span>
<span data-ttu-id="61eb7-128">Идентификатор клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="61eb7-128">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="61eb7-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61eb7-129">-Confirm</span></span>
<span data-ttu-id="61eb7-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="61eb7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61eb7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61eb7-131">-WhatIf</span></span>
<span data-ttu-id="61eb7-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="61eb7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61eb7-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="61eb7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61eb7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61eb7-134">CommonParameters</span></span>
<span data-ttu-id="61eb7-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="61eb7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61eb7-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61eb7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61eb7-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="61eb7-137">INPUTS</span></span>

## <span data-ttu-id="61eb7-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="61eb7-138">OUTPUTS</span></span>

### <span data-ttu-id="61eb7-139">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="61eb7-139">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="61eb7-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="61eb7-140">NOTES</span></span>

## <span data-ttu-id="61eb7-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61eb7-141">RELATED LINKS</span></span>

