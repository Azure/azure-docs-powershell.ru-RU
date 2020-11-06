---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 106293e9d959aefe25ae3e4b27519639a39193d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555655"
---
# <span data-ttu-id="ba800-101">Set-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="ba800-101">Set-AzsUserSubscription</span></span>

## <span data-ttu-id="ba800-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ba800-102">SYNOPSIS</span></span>
<span data-ttu-id="ba800-103">Обновляет указанную подписку пользователя</span><span class="sxs-lookup"><span data-stu-id="ba800-103">Updates the specified user subscription</span></span>

## <span data-ttu-id="ba800-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ba800-104">SYNTAX</span></span>

### <span data-ttu-id="ba800-105">Set (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ba800-105">Set (Default)</span></span>
```
Set-AzsUserSubscription -SubscriptionId <Guid> [-DisplayName <String>]
 [-DelegatedProviderSubscriptionId <String>] [-Owner <String>] [-TenantId <String>]
 [-RoutingResourceManagerType <String>] [-ExternalReferenceId <String>] [-State <String>] [-Location <String>]
 [-OfferId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba800-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba800-106">ResourceId</span></span>
```
Set-AzsUserSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba800-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="ba800-107">InputObject</span></span>
```
Set-AzsUserSubscription -InputObject <Subscription> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba800-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba800-108">DESCRIPTION</span></span>
<span data-ttu-id="ba800-109">Обновляет указанную подписку пользователя</span><span class="sxs-lookup"><span data-stu-id="ba800-109">Updates the specified user subscription</span></span>

## <span data-ttu-id="ba800-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ba800-110">EXAMPLES</span></span>

### <span data-ttu-id="ba800-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ba800-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsUserSubscription -SubscriptionId 8e425478-c7f0-49ca-bb92-b42889ec3642 -DisplayName "NewName"
```

<span data-ttu-id="ba800-112">Обновляет подписку</span><span class="sxs-lookup"><span data-stu-id="ba800-112">Updates a subscription</span></span>

## <span data-ttu-id="ba800-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ba800-113">PARAMETERS</span></span>

### <span data-ttu-id="ba800-114">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ba800-114">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="ba800-115">Идентификатор родительской подписки на DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="ba800-115">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="ba800-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ba800-116">-DisplayName</span></span>
<span data-ttu-id="ba800-117">Название подписки.</span><span class="sxs-lookup"><span data-stu-id="ba800-117">Subscription name.</span></span>

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

### <span data-ttu-id="ba800-118">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="ba800-118">-ExternalReferenceId</span></span>
<span data-ttu-id="ba800-119">Идентификатор внешней ссылки.</span><span class="sxs-lookup"><span data-stu-id="ba800-119">External reference identifier.</span></span>

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

### <span data-ttu-id="ba800-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba800-120">-InputObject</span></span>
<span data-ttu-id="ba800-121">Входной объект типа Microsoft. AzureStack. Management. Network. admin. Models. Quota.</span><span class="sxs-lookup"><span data-stu-id="ba800-121">The input object of type Microsoft.AzureStack.Management.Network.Admin.Models.Quota.</span></span>

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

### <span data-ttu-id="ba800-122">-Location</span><span class="sxs-lookup"><span data-stu-id="ba800-122">-Location</span></span>
<span data-ttu-id="ba800-123">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="ba800-123">Location of the resource.</span></span>

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

### <span data-ttu-id="ba800-124">-OfferId</span><span class="sxs-lookup"><span data-stu-id="ba800-124">-OfferId</span></span>
<span data-ttu-id="ba800-125">Идентификатор предложения в рамках области поставщика делегированных данных.</span><span class="sxs-lookup"><span data-stu-id="ba800-125">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="ba800-126">-Владелец</span><span class="sxs-lookup"><span data-stu-id="ba800-126">-Owner</span></span>
<span data-ttu-id="ba800-127">Владелец подписки.</span><span class="sxs-lookup"><span data-stu-id="ba800-127">Subscription owner.</span></span>

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

### <span data-ttu-id="ba800-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba800-128">-ResourceId</span></span>
<span data-ttu-id="ba800-129">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="ba800-129">The resource ID.</span></span>

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

### <span data-ttu-id="ba800-130">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="ba800-130">-RoutingResourceManagerType</span></span>
<span data-ttu-id="ba800-131">Тип диспетчера ресурсов маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="ba800-131">Routing resource manager type.</span></span>

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

### <span data-ttu-id="ba800-132">-State</span><span class="sxs-lookup"><span data-stu-id="ba800-132">-State</span></span>
<span data-ttu-id="ba800-133">Состояние подписки.</span><span class="sxs-lookup"><span data-stu-id="ba800-133">Subscription state.</span></span>

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

### <span data-ttu-id="ba800-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ba800-134">-SubscriptionId</span></span>
<span data-ttu-id="ba800-135">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="ba800-135">Subscription identifier.</span></span>

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

### <span data-ttu-id="ba800-136">-TenantId</span><span class="sxs-lookup"><span data-stu-id="ba800-136">-TenantId</span></span>
<span data-ttu-id="ba800-137">Идентификатор клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="ba800-137">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="ba800-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba800-138">-Confirm</span></span>
<span data-ttu-id="ba800-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ba800-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba800-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba800-140">-WhatIf</span></span>
<span data-ttu-id="ba800-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ba800-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba800-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ba800-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba800-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba800-143">CommonParameters</span></span>
<span data-ttu-id="ba800-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ba800-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba800-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba800-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba800-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ba800-146">INPUTS</span></span>

## <span data-ttu-id="ba800-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba800-147">OUTPUTS</span></span>

### <span data-ttu-id="ba800-148">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="ba800-148">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="ba800-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="ba800-149">NOTES</span></span>

## <span data-ttu-id="ba800-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba800-150">RELATED LINKS</span></span>

