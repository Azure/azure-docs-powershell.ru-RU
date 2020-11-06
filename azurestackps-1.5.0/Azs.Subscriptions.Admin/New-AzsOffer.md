---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87ad48de1fa4ae05f90f067e8a0a2eac2c4fdd0d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555496"
---
# <span data-ttu-id="0e504-101">New-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="0e504-101">New-AzsOffer</span></span>

## <span data-ttu-id="0e504-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0e504-102">SYNOPSIS</span></span>
<span data-ttu-id="0e504-103">Создание нового предложения.</span><span class="sxs-lookup"><span data-stu-id="0e504-103">Creates a new offer.</span></span>

## <span data-ttu-id="0e504-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0e504-104">SYNTAX</span></span>

```
New-AzsOffer [-Name] <String> [-DisplayName] <String> [-ResourceGroupName] <String> [[-BasePlanIds] <String[]>]
 [[-Description] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>] [[-Location] <String>]
 [[-MaxSubscriptionsPerAccount] <Int64>] [[-SubscriptionCount] <Int64>]
 [[-AddonPlanDefinition] <AddonPlanDefinition[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e504-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e504-105">DESCRIPTION</span></span>
<span data-ttu-id="0e504-106">Создание или обновление предложения.</span><span class="sxs-lookup"><span data-stu-id="0e504-106">Create or update the offer.</span></span>

## <span data-ttu-id="0e504-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0e504-107">EXAMPLES</span></span>

### <span data-ttu-id="0e504-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0e504-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsOffer -Name offer1 -ResourceGroupName rg1 -State Public -DisplayName "offer1" -BasePlanIds "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/plans/plan1"
```

<span data-ttu-id="0e504-109">Создание нового предложения.</span><span class="sxs-lookup"><span data-stu-id="0e504-109">Creates a new offer.</span></span>

## <span data-ttu-id="0e504-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0e504-110">PARAMETERS</span></span>

### <span data-ttu-id="0e504-111">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="0e504-111">-AddonPlanDefinition</span></span>
<span data-ttu-id="0e504-112">Ссылки на планы надстроек, с помощью которых клиент может дополнительно получить как часть предложения.</span><span class="sxs-lookup"><span data-stu-id="0e504-112">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

```yaml
Type: AddonPlanDefinition[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e504-113">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="0e504-113">-BasePlanIds</span></span>
<span data-ttu-id="0e504-114">Идентификаторы базовых планов, которые будут доступны клиенту немедленно, когда клиент подписывается на предложение.</span><span class="sxs-lookup"><span data-stu-id="0e504-114">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e504-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="0e504-115">-Description</span></span>
<span data-ttu-id="0e504-116">Описание предложения.</span><span class="sxs-lookup"><span data-stu-id="0e504-116">Description of offer.</span></span>

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

### <span data-ttu-id="0e504-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0e504-117">-DisplayName</span></span>
<span data-ttu-id="0e504-118">Отображаемое имя предложения.</span><span class="sxs-lookup"><span data-stu-id="0e504-118">Display name of offer.</span></span>

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

### <span data-ttu-id="0e504-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="0e504-119">-ExternalReferenceId</span></span>
<span data-ttu-id="0e504-120">Идентификатор внешней ссылки.</span><span class="sxs-lookup"><span data-stu-id="0e504-120">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e504-121">-Location</span><span class="sxs-lookup"><span data-stu-id="0e504-121">-Location</span></span>
<span data-ttu-id="0e504-122">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="0e504-122">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ArmLocation

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e504-123">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="0e504-123">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="0e504-124">Максимальное количество подписок на одну учетную запись.</span><span class="sxs-lookup"><span data-stu-id="0e504-124">Maximum subscriptions per account.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e504-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0e504-125">-Name</span></span>
<span data-ttu-id="0e504-126">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="0e504-126">Name of an offer.</span></span>

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

### <span data-ttu-id="0e504-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e504-127">-ResourceGroupName</span></span>
<span data-ttu-id="0e504-128">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="0e504-128">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e504-129">-State</span><span class="sxs-lookup"><span data-stu-id="0e504-129">-State</span></span>
<span data-ttu-id="0e504-130">Предоставление поддержки специальных возможностей.</span><span class="sxs-lookup"><span data-stu-id="0e504-130">Offer accessibility state.</span></span>
<span data-ttu-id="0e504-131">Значение по умолчанию — Private.</span><span class="sxs-lookup"><span data-stu-id="0e504-131">Default value is Private.</span></span>
<span data-ttu-id="0e504-132">Этот параметр будет устаревшим в следующем выпуске</span><span class="sxs-lookup"><span data-stu-id="0e504-132">This parameter will be deprecated in a future release</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: Private
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e504-133">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="0e504-133">-SubscriptionCount</span></span>
<span data-ttu-id="0e504-134">Текущее число подписок.</span><span class="sxs-lookup"><span data-stu-id="0e504-134">Current subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e504-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0e504-135">-Confirm</span></span>
<span data-ttu-id="0e504-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0e504-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e504-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e504-137">-WhatIf</span></span>
<span data-ttu-id="0e504-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0e504-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e504-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0e504-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e504-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e504-140">CommonParameters</span></span>
<span data-ttu-id="0e504-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0e504-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e504-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e504-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e504-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0e504-143">INPUTS</span></span>

## <span data-ttu-id="0e504-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e504-144">OUTPUTS</span></span>

### <span data-ttu-id="0e504-145">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Offer</span><span class="sxs-lookup"><span data-stu-id="0e504-145">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="0e504-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="0e504-146">NOTES</span></span>

## <span data-ttu-id="0e504-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0e504-147">RELATED LINKS</span></span>

