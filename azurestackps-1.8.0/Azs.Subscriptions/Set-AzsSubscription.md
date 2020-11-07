---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25bd0c892c8c5978493d855246be994bc96158db
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908029"
---
# <span data-ttu-id="7fb9e-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="7fb9e-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="7fb9e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7fb9e-102">SYNOPSIS</span></span>
<span data-ttu-id="7fb9e-103">Создание или обновление подписки.</span><span class="sxs-lookup"><span data-stu-id="7fb9e-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="7fb9e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7fb9e-104">SYNTAX</span></span>

### <span data-ttu-id="7fb9e-105">Set (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7fb9e-105">Set (Default)</span></span>
```
Set-AzsSubscription [-OfferId <String>] [-Type <String>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -SubscriptionId <String>
 [-State <String>] [-TenantId <String>] [-DisplayName <String>] [-Location <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7fb9e-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fb9e-106">ResourceId</span></span>
```
Set-AzsSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fb9e-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="7fb9e-107">InputObject</span></span>
```
Set-AzsSubscription -InputObject <SubscriptionModel> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fb9e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fb9e-108">DESCRIPTION</span></span>
<span data-ttu-id="7fb9e-109">Создание или обновление подписки.</span><span class="sxs-lookup"><span data-stu-id="7fb9e-109">Create or updates a subscription.</span></span>

## <span data-ttu-id="7fb9e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7fb9e-110">EXAMPLES</span></span>

### <span data-ttu-id="7fb9e-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="7fb9e-111">EXAMPLE 1</span></span>
```
Set-AzsSubscription -SubscriptionId 2d9f5af9-3397-44fb-8700-d98762c2422a -DisplayName MyTestSub -State Enabled -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="7fb9e-112">Создание или обновление подписки.</span><span class="sxs-lookup"><span data-stu-id="7fb9e-112">Create or updates a subscription.</span></span>

## <span data-ttu-id="7fb9e-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7fb9e-113">PARAMETERS</span></span>

### <span data-ttu-id="7fb9e-114">-OfferId</span><span class="sxs-lookup"><span data-stu-id="7fb9e-114">-OfferId</span></span>
<span data-ttu-id="7fb9e-115">Идентификатор предложения в рамках области поставщика делегированных данных.</span><span class="sxs-lookup"><span data-stu-id="7fb9e-115">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="7fb9e-116">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="7fb9e-116">-Type</span></span>
<span data-ttu-id="7fb9e-117">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="7fb9e-117">Type of resource.</span></span>

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

### <span data-ttu-id="7fb9e-118">-Теги</span><span class="sxs-lookup"><span data-stu-id="7fb9e-118">-Tags</span></span>
<span data-ttu-id="7fb9e-119">Список пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="7fb9e-119">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb9e-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7fb9e-120">-SubscriptionId</span></span>
<span data-ttu-id="7fb9e-121">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="7fb9e-121">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb9e-122">-State</span><span class="sxs-lookup"><span data-stu-id="7fb9e-122">-State</span></span>
<span data-ttu-id="7fb9e-123">Состояние подписки.</span><span class="sxs-lookup"><span data-stu-id="7fb9e-123">Subscription state.</span></span>

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

### <span data-ttu-id="7fb9e-124">-TenantId</span><span class="sxs-lookup"><span data-stu-id="7fb9e-124">-TenantId</span></span>
<span data-ttu-id="7fb9e-125">Идентификатор клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="7fb9e-125">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="7fb9e-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7fb9e-126">-DisplayName</span></span>
<span data-ttu-id="7fb9e-127">Название подписки.</span><span class="sxs-lookup"><span data-stu-id="7fb9e-127">Subscription name.</span></span>

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

### <span data-ttu-id="7fb9e-128">-Location</span><span class="sxs-lookup"><span data-stu-id="7fb9e-128">-Location</span></span>
<span data-ttu-id="7fb9e-129">Расположение, в котором расположен ресурс.</span><span class="sxs-lookup"><span data-stu-id="7fb9e-129">Location where resource is location.</span></span>

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

### <span data-ttu-id="7fb9e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fb9e-130">-ResourceId</span></span>
<span data-ttu-id="7fb9e-131">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="7fb9e-131">The resource ID.</span></span>

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

### <span data-ttu-id="7fb9e-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fb9e-132">-InputObject</span></span>
<span data-ttu-id="7fb9e-133">Posbbily изменена сетевая квота, возвращенная командой Get-AzsNetworkQuota.</span><span class="sxs-lookup"><span data-stu-id="7fb9e-133">Posbbily modified network quota returned by Get-AzsNetworkQuota.</span></span>

```yaml
Type: SubscriptionModel
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fb9e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fb9e-134">-WhatIf</span></span>
<span data-ttu-id="7fb9e-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7fb9e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fb9e-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7fb9e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fb9e-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7fb9e-137">-Confirm</span></span>
<span data-ttu-id="7fb9e-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7fb9e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fb9e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fb9e-139">CommonParameters</span></span>
<span data-ttu-id="7fb9e-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7fb9e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fb9e-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fb9e-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fb9e-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7fb9e-142">INPUTS</span></span>

## <span data-ttu-id="7fb9e-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fb9e-143">OUTPUTS</span></span>

### <span data-ttu-id="7fb9e-144">Microsoft. AzureStack. Management. Subscription. Models. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="7fb9e-144">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="7fb9e-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="7fb9e-145">NOTES</span></span>

## <span data-ttu-id="7fb9e-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7fb9e-146">RELATED LINKS</span></span>
