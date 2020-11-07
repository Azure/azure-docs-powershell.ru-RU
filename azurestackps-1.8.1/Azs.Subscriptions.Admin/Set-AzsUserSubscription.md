---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ef53ac2d32d71a68b7fe342f5d2d0cafc2a193f8
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93908682"
---
# <span data-ttu-id="bdda6-101">Set-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="bdda6-101">Set-AzsUserSubscription</span></span>

## <span data-ttu-id="bdda6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bdda6-102">SYNOPSIS</span></span>
<span data-ttu-id="bdda6-103">Обновляет указанную подписку пользователя</span><span class="sxs-lookup"><span data-stu-id="bdda6-103">Updates the specified user subscription</span></span>

## <span data-ttu-id="bdda6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bdda6-104">SYNTAX</span></span>

### <span data-ttu-id="bdda6-105">Set (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bdda6-105">Set (Default)</span></span>
```
Set-AzsUserSubscription -SubscriptionId <Guid> [-DisplayName <String>]
 [-DelegatedProviderSubscriptionId <String>] [-Owner <String>] [-TenantId <String>]
 [-RoutingResourceManagerType <String>] [-ExternalReferenceId <String>] [-State <String>] [-Location <String>]
 [-OfferId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdda6-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdda6-106">ResourceId</span></span>
```
Set-AzsUserSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdda6-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="bdda6-107">InputObject</span></span>
```
Set-AzsUserSubscription -InputObject <Subscription> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdda6-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bdda6-108">DESCRIPTION</span></span>
<span data-ttu-id="bdda6-109">Обновляет указанную подписку пользователя</span><span class="sxs-lookup"><span data-stu-id="bdda6-109">Updates the specified user subscription</span></span>

## <span data-ttu-id="bdda6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bdda6-110">EXAMPLES</span></span>

### <span data-ttu-id="bdda6-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="bdda6-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsUserSubscription -SubscriptionId 8e425478-c7f0-49ca-bb92-b42889ec3642 -DisplayName "NewName"
```

<span data-ttu-id="bdda6-112">Обновляет подписку</span><span class="sxs-lookup"><span data-stu-id="bdda6-112">Updates a subscription</span></span>

## <span data-ttu-id="bdda6-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bdda6-113">PARAMETERS</span></span>

### <span data-ttu-id="bdda6-114">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bdda6-114">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="bdda6-115">Идентификатор родительской подписки на DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="bdda6-115">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdda6-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bdda6-116">-DisplayName</span></span>
<span data-ttu-id="bdda6-117">Название подписки.</span><span class="sxs-lookup"><span data-stu-id="bdda6-117">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdda6-118">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="bdda6-118">-ExternalReferenceId</span></span>
<span data-ttu-id="bdda6-119">Идентификатор внешней ссылки.</span><span class="sxs-lookup"><span data-stu-id="bdda6-119">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdda6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bdda6-120">-InputObject</span></span>
<span data-ttu-id="bdda6-121">Входной объект типа Microsoft. AzureStack. Management. Network. admin. Models. Quota.</span><span class="sxs-lookup"><span data-stu-id="bdda6-121">The input object of type Microsoft.AzureStack.Management.Network.Admin.Models.Quota.</span></span>

```yaml
Type: Subscription
Parameter Sets: InputObject
Aliases: Subscription

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdda6-122">-Location</span><span class="sxs-lookup"><span data-stu-id="bdda6-122">-Location</span></span>
<span data-ttu-id="bdda6-123">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="bdda6-123">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdda6-124">-OfferId</span><span class="sxs-lookup"><span data-stu-id="bdda6-124">-OfferId</span></span>
<span data-ttu-id="bdda6-125">Идентификатор предложения в рамках области поставщика делегированных данных.</span><span class="sxs-lookup"><span data-stu-id="bdda6-125">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdda6-126">-Владелец</span><span class="sxs-lookup"><span data-stu-id="bdda6-126">-Owner</span></span>
<span data-ttu-id="bdda6-127">Владелец подписки.</span><span class="sxs-lookup"><span data-stu-id="bdda6-127">Subscription owner.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdda6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdda6-128">-ResourceId</span></span>
<span data-ttu-id="bdda6-129">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="bdda6-129">The resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdda6-130">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="bdda6-130">-RoutingResourceManagerType</span></span>
<span data-ttu-id="bdda6-131">Тип диспетчера ресурсов маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="bdda6-131">Routing resource manager type.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdda6-132">-State</span><span class="sxs-lookup"><span data-stu-id="bdda6-132">-State</span></span>
<span data-ttu-id="bdda6-133">Состояние подписки.</span><span class="sxs-lookup"><span data-stu-id="bdda6-133">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdda6-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bdda6-134">-SubscriptionId</span></span>
<span data-ttu-id="bdda6-135">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="bdda6-135">Subscription identifier.</span></span>

```yaml
Type: Guid
Parameter Sets: Set
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdda6-136">-TenantId</span><span class="sxs-lookup"><span data-stu-id="bdda6-136">-TenantId</span></span>
<span data-ttu-id="bdda6-137">Идентификатор клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="bdda6-137">Directory tenant identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdda6-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bdda6-138">-Confirm</span></span>
<span data-ttu-id="bdda6-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bdda6-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdda6-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdda6-140">-WhatIf</span></span>
<span data-ttu-id="bdda6-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bdda6-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdda6-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bdda6-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdda6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdda6-143">CommonParameters</span></span>
<span data-ttu-id="bdda6-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bdda6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdda6-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdda6-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdda6-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bdda6-146">INPUTS</span></span>

## <span data-ttu-id="bdda6-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bdda6-147">OUTPUTS</span></span>

### <span data-ttu-id="bdda6-148">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="bdda6-148">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="bdda6-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="bdda6-149">NOTES</span></span>

## <span data-ttu-id="bdda6-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bdda6-150">RELATED LINKS</span></span>

