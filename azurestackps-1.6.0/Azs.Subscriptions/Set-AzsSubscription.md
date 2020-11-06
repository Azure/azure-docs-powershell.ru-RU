---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb23765090b0edfd14fa355b9809a2385900396e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556099"
---
# <span data-ttu-id="e1df0-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="e1df0-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="e1df0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e1df0-102">SYNOPSIS</span></span>
<span data-ttu-id="e1df0-103">Создание или обновление подписки.</span><span class="sxs-lookup"><span data-stu-id="e1df0-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="e1df0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e1df0-104">SYNTAX</span></span>

### <span data-ttu-id="e1df0-105">Set (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e1df0-105">Set (Default)</span></span>
```
Set-AzsSubscription [-OfferId <String>] [-Type <String>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -SubscriptionId <String>
 [-State <String>] [-TenantId <String>] [-DisplayName <String>] [-Location <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1df0-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1df0-106">ResourceId</span></span>
```
Set-AzsSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1df0-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="e1df0-107">InputObject</span></span>
```
Set-AzsSubscription -InputObject <SubscriptionModel> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1df0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1df0-108">DESCRIPTION</span></span>
<span data-ttu-id="e1df0-109">Создание или обновление подписки.</span><span class="sxs-lookup"><span data-stu-id="e1df0-109">Create or updates a subscription.</span></span>

## <span data-ttu-id="e1df0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e1df0-110">EXAMPLES</span></span>

### <span data-ttu-id="e1df0-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e1df0-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsSubscription -SubscriptionId 2d9f5af9-3397-44fb-8700-d98762c2422a -DisplayName MyTestSub -State Enabled -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="e1df0-112">Создание или обновление подписки.</span><span class="sxs-lookup"><span data-stu-id="e1df0-112">Create or updates a subscription.</span></span>

## <span data-ttu-id="e1df0-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e1df0-113">PARAMETERS</span></span>

### <span data-ttu-id="e1df0-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e1df0-114">-DisplayName</span></span>
<span data-ttu-id="e1df0-115">Название подписки.</span><span class="sxs-lookup"><span data-stu-id="e1df0-115">Subscription name.</span></span>

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

### <span data-ttu-id="e1df0-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1df0-116">-InputObject</span></span>
<span data-ttu-id="e1df0-117">Posbbily изменена сетевая квота, возвращенная командой Get-AzsNetworkQuota.</span><span class="sxs-lookup"><span data-stu-id="e1df0-117">Posbbily modified network quota returned by Get-AzsNetworkQuota.</span></span>

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

### <span data-ttu-id="e1df0-118">-Location</span><span class="sxs-lookup"><span data-stu-id="e1df0-118">-Location</span></span>
<span data-ttu-id="e1df0-119">Расположение, в котором расположен ресурс.</span><span class="sxs-lookup"><span data-stu-id="e1df0-119">Location where resource is location.</span></span>

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

### <span data-ttu-id="e1df0-120">-OfferId</span><span class="sxs-lookup"><span data-stu-id="e1df0-120">-OfferId</span></span>
<span data-ttu-id="e1df0-121">Идентификатор предложения в рамках области поставщика делегированных данных.</span><span class="sxs-lookup"><span data-stu-id="e1df0-121">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="e1df0-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1df0-122">-ResourceId</span></span>
<span data-ttu-id="e1df0-123">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="e1df0-123">The resource ID.</span></span>

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

### <span data-ttu-id="e1df0-124">-State</span><span class="sxs-lookup"><span data-stu-id="e1df0-124">-State</span></span>
<span data-ttu-id="e1df0-125">Состояние подписки.</span><span class="sxs-lookup"><span data-stu-id="e1df0-125">Subscription state.</span></span>

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

### <span data-ttu-id="e1df0-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e1df0-126">-SubscriptionId</span></span>
<span data-ttu-id="e1df0-127">Идентификатор подписки.</span><span class="sxs-lookup"><span data-stu-id="e1df0-127">Subscription identifier.</span></span>

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

### <span data-ttu-id="e1df0-128">-Теги</span><span class="sxs-lookup"><span data-stu-id="e1df0-128">-Tags</span></span>
<span data-ttu-id="e1df0-129">Список пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="e1df0-129">List of key-value pairs.</span></span>

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

### <span data-ttu-id="e1df0-130">-TenantId</span><span class="sxs-lookup"><span data-stu-id="e1df0-130">-TenantId</span></span>
<span data-ttu-id="e1df0-131">Идентификатор клиента службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="e1df0-131">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="e1df0-132">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="e1df0-132">-Type</span></span>
<span data-ttu-id="e1df0-133">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="e1df0-133">Type of resource.</span></span>

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

### <span data-ttu-id="e1df0-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1df0-134">-Confirm</span></span>
<span data-ttu-id="e1df0-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e1df0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1df0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1df0-136">-WhatIf</span></span>
<span data-ttu-id="e1df0-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e1df0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1df0-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e1df0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1df0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1df0-139">CommonParameters</span></span>
<span data-ttu-id="e1df0-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e1df0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1df0-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1df0-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1df0-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e1df0-142">INPUTS</span></span>

## <span data-ttu-id="e1df0-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1df0-143">OUTPUTS</span></span>

### <span data-ttu-id="e1df0-144">Microsoft. AzureStack. Management. Subscription. Models. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="e1df0-144">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="e1df0-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="e1df0-145">NOTES</span></span>

## <span data-ttu-id="e1df0-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e1df0-146">RELATED LINKS</span></span>

