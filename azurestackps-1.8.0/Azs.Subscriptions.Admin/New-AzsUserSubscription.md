---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d4b7abdeb085c7cfee6444c4afeeb6a3e79d99e9
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908085"
---
# <span data-ttu-id="05746-101">New-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="05746-101">New-AzsUserSubscription</span></span>

## <span data-ttu-id="05746-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="05746-102">SYNOPSIS</span></span>
<span data-ttu-id="05746-103">Создайте новую подписку.</span><span class="sxs-lookup"><span data-stu-id="05746-103">Create a new subscription.</span></span>

## <span data-ttu-id="05746-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="05746-104">SYNTAX</span></span>

```
New-AzsUserSubscription [-Owner] <String> [-OfferId] <String> [[-TenantId] <String>] [[-DisplayName] <String>]
 [[-DelegatedProviderSubscriptionId] <String>] [[-RoutingResourceManagerType] <String>]
 [[-ExternalReferenceId] <String>] [[-State] <String>] [[-SubscriptionId] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="05746-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05746-105">DESCRIPTION</span></span>
<span data-ttu-id="05746-106">Создайте новую подписку.</span><span class="sxs-lookup"><span data-stu-id="05746-106">Create a new subscription.</span></span>

## <span data-ttu-id="05746-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="05746-107">EXAMPLES</span></span>

### <span data-ttu-id="05746-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="05746-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsUserSubscription -Owner user@contoso.com -OfferId "/subscriptions/302d0fcd-5263-4f4d-82ba-383ad95a3e53/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/offers/offer1"
```

<span data-ttu-id="05746-109">Создает новую подписку пользователя</span><span class="sxs-lookup"><span data-stu-id="05746-109">Creates a new user subscription</span></span>

## <span data-ttu-id="05746-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="05746-110">PARAMETERS</span></span>

### <span data-ttu-id="05746-111">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="05746-111">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="05746-112">Идентификатор родительской подписки на DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="05746-112">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="05746-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="05746-113">-DisplayName</span></span>
<span data-ttu-id="05746-114">Название подписки.</span><span class="sxs-lookup"><span data-stu-id="05746-114">Subscription name.</span></span>

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

### <span data-ttu-id="05746-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="05746-115">-ExternalReferenceId</span></span>
<span data-ttu-id="05746-116">Идентификатор внешней ссылки.</span><span class="sxs-lookup"><span data-stu-id="05746-116">External reference identifier.</span></span>

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

### <span data-ttu-id="05746-117">-OfferId</span><span class="sxs-lookup"><span data-stu-id="05746-117">-OfferId</span></span>
<span data-ttu-id="05746-118">Идентификатор предложения в рамках области поставщика делегированных данных.</span><span class="sxs-lookup"><span data-stu-id="05746-118">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="05746-119">-Владелец</span><span class="sxs-lookup"><span data-stu-id="05746-119">-Owner</span></span>
<span data-ttu-id="05746-120">Владелец подписки.</span><span class="sxs-lookup"><span data-stu-id="05746-120">Subscription owner.</span></span>

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

### <span data-ttu-id="05746-121">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="05746-121">-RoutingResourceManagerType</span></span>
<span data-ttu-id="05746-122">Тип диспетчера ресурсов маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="05746-122">Routing resource manager type.</span></span>

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

### <span data-ttu-id="05746-123">-State</span><span class="sxs-lookup"><span data-stu-id="05746-123">-State</span></span>
<span data-ttu-id="05746-124">Состояние подписки.</span><span class="sxs-lookup"><span data-stu-id="05746-124">Subscription state.</span></span>

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

### <span data-ttu-id="05746-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="05746-125">-SubscriptionId</span></span>
<span data-ttu-id="05746-126">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="05746-126">Subscription identifier.</span></span>

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

### <span data-ttu-id="05746-127">-TenantId</span><span class="sxs-lookup"><span data-stu-id="05746-127">-TenantId</span></span>
<span data-ttu-id="05746-128">Идентификатор клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="05746-128">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="05746-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05746-129">-Confirm</span></span>
<span data-ttu-id="05746-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="05746-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05746-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05746-131">-WhatIf</span></span>
<span data-ttu-id="05746-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="05746-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05746-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="05746-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05746-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05746-134">CommonParameters</span></span>
<span data-ttu-id="05746-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="05746-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05746-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05746-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05746-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="05746-137">INPUTS</span></span>

## <span data-ttu-id="05746-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="05746-138">OUTPUTS</span></span>

### <span data-ttu-id="05746-139">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="05746-139">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="05746-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="05746-140">NOTES</span></span>

## <span data-ttu-id="05746-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05746-141">RELATED LINKS</span></span>

