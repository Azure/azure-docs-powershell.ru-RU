---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9b08aed00a4c16bd2031608ff795a4dde8491859
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077071"
---
# <span data-ttu-id="291f5-101">Set-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="291f5-101">Set-AzsOffer</span></span>

## <span data-ttu-id="291f5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="291f5-102">SYNOPSIS</span></span>
<span data-ttu-id="291f5-103">Обновите предложение.</span><span class="sxs-lookup"><span data-stu-id="291f5-103">Update the offer.</span></span>

## <span data-ttu-id="291f5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="291f5-104">SYNTAX</span></span>

### <span data-ttu-id="291f5-105">Обновление (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="291f5-105">Update (Default)</span></span>
```
Set-AzsOffer -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-BasePlanIds <String[]>]
 [-Description <String>] [-ExternalReferenceId <String>] [-State <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-MaxSubscriptionsPerAccount <Int64>]
 [-AddonPlanDefinition <AddonPlanDefinition[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="291f5-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="291f5-106">InputObject</span></span>
```
Set-AzsOffer [-ResourceGroupName <String>] -InputObject <Offer> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="291f5-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="291f5-107">ResourceId</span></span>
```
Set-AzsOffer -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="291f5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="291f5-108">DESCRIPTION</span></span>
<span data-ttu-id="291f5-109">Обновите предложение.</span><span class="sxs-lookup"><span data-stu-id="291f5-109">Update the offer.</span></span>

## <span data-ttu-id="291f5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="291f5-110">EXAMPLES</span></span>

### <span data-ttu-id="291f5-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="291f5-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsOffer -Name offer1 -ResourceGroupName rg1 -State Private
```

<span data-ttu-id="291f5-112">Обновите предложение.</span><span class="sxs-lookup"><span data-stu-id="291f5-112">Update the offer.</span></span>

## <span data-ttu-id="291f5-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="291f5-113">PARAMETERS</span></span>

### <span data-ttu-id="291f5-114">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="291f5-114">-AddonPlanDefinition</span></span>
<span data-ttu-id="291f5-115">Ссылки на планы надстроек, с помощью которых клиент может дополнительно получить как часть предложения.</span><span class="sxs-lookup"><span data-stu-id="291f5-115">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

```yaml
Type: AddonPlanDefinition[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291f5-116">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="291f5-116">-BasePlanIds</span></span>
<span data-ttu-id="291f5-117">Идентификаторы базовых планов, которые будут доступны клиенту немедленно, когда клиент подписывается на предложение.</span><span class="sxs-lookup"><span data-stu-id="291f5-117">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: String[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291f5-118">-Описание</span><span class="sxs-lookup"><span data-stu-id="291f5-118">-Description</span></span>
<span data-ttu-id="291f5-119">Описание предложения.</span><span class="sxs-lookup"><span data-stu-id="291f5-119">Description of offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291f5-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="291f5-120">-DisplayName</span></span>
<span data-ttu-id="291f5-121">Отображаемое имя предложения.</span><span class="sxs-lookup"><span data-stu-id="291f5-121">Display name of offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291f5-122">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="291f5-122">-ExternalReferenceId</span></span>
<span data-ttu-id="291f5-123">Идентификатор внешней ссылки.</span><span class="sxs-lookup"><span data-stu-id="291f5-123">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291f5-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="291f5-124">-InputObject</span></span>
<span data-ttu-id="291f5-125">Входной объект типа Microsoft. AzureStack. Management. Subscriptions. admin. Models. offer.</span><span class="sxs-lookup"><span data-stu-id="291f5-125">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer.</span></span>

```yaml
Type: Offer
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="291f5-126">-Location</span><span class="sxs-lookup"><span data-stu-id="291f5-126">-Location</span></span>
<span data-ttu-id="291f5-127">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="291f5-127">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291f5-128">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="291f5-128">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="291f5-129">Максимальное количество подписок на одну учетную запись.</span><span class="sxs-lookup"><span data-stu-id="291f5-129">Maximum subscriptions per account.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291f5-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="291f5-130">-Name</span></span>
<span data-ttu-id="291f5-131">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="291f5-131">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291f5-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="291f5-132">-ResourceGroupName</span></span>
<span data-ttu-id="291f5-133">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="291f5-133">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InputObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291f5-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="291f5-134">-ResourceId</span></span>
<span data-ttu-id="291f5-135">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="291f5-135">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="291f5-136">-State</span><span class="sxs-lookup"><span data-stu-id="291f5-136">-State</span></span>
<span data-ttu-id="291f5-137">Предоставление поддержки специальных возможностей.</span><span class="sxs-lookup"><span data-stu-id="291f5-137">Offer accessibility state.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291f5-138">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="291f5-138">-SubscriptionCount</span></span>
<span data-ttu-id="291f5-139">Текущее число подписок.</span><span class="sxs-lookup"><span data-stu-id="291f5-139">Current subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="291f5-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="291f5-140">-Confirm</span></span>
<span data-ttu-id="291f5-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="291f5-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="291f5-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="291f5-142">-WhatIf</span></span>
<span data-ttu-id="291f5-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="291f5-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="291f5-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="291f5-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="291f5-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="291f5-145">CommonParameters</span></span>
<span data-ttu-id="291f5-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="291f5-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="291f5-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="291f5-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="291f5-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="291f5-148">INPUTS</span></span>

## <span data-ttu-id="291f5-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="291f5-149">OUTPUTS</span></span>

### <span data-ttu-id="291f5-150">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Offer</span><span class="sxs-lookup"><span data-stu-id="291f5-150">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="291f5-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="291f5-151">NOTES</span></span>

## <span data-ttu-id="291f5-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="291f5-152">RELATED LINKS</span></span>

