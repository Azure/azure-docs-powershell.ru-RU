---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9ff6532cb43d7ece7460651eb4493201de4734b1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077002"
---
# <span data-ttu-id="3e497-101">Set-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="3e497-101">Set-AzsPlan</span></span>

## <span data-ttu-id="3e497-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e497-102">SYNOPSIS</span></span>
<span data-ttu-id="3e497-103">Обновляет указанный план</span><span class="sxs-lookup"><span data-stu-id="3e497-103">Updates the specified plan</span></span>

## <span data-ttu-id="3e497-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e497-104">SYNTAX</span></span>

### <span data-ttu-id="3e497-105">Обновление (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3e497-105">Update (Default)</span></span>
```
Set-AzsPlan -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-QuotaIds <String[]>]
 [-SkuIds <String[]>] [-ExternalReferenceId <String>] [-Description <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e497-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="3e497-106">InputObject</span></span>
```
Set-AzsPlan [-ResourceGroupName <String>] -InputObject <Plan> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e497-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e497-107">ResourceId</span></span>
```
Set-AzsPlan -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e497-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e497-108">DESCRIPTION</span></span>
<span data-ttu-id="3e497-109">Обновляет указанный план</span><span class="sxs-lookup"><span data-stu-id="3e497-109">Updates the specified plan</span></span>

## <span data-ttu-id="3e497-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e497-110">EXAMPLES</span></span>

### <span data-ttu-id="3e497-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3e497-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -Description "This plan is meant to be used by accounting only."
```

<span data-ttu-id="3e497-112">Обновляет указанный план</span><span class="sxs-lookup"><span data-stu-id="3e497-112">Updates the specified plan</span></span>

## <span data-ttu-id="3e497-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e497-113">PARAMETERS</span></span>

### <span data-ttu-id="3e497-114">-Описание</span><span class="sxs-lookup"><span data-stu-id="3e497-114">-Description</span></span>
<span data-ttu-id="3e497-115">Описание плана.</span><span class="sxs-lookup"><span data-stu-id="3e497-115">Description of the plan.</span></span>

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

### <span data-ttu-id="3e497-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3e497-116">-DisplayName</span></span>
<span data-ttu-id="3e497-117">Отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="3e497-117">Display name.</span></span>

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

### <span data-ttu-id="3e497-118">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="3e497-118">-ExternalReferenceId</span></span>
<span data-ttu-id="3e497-119">Идентификатор внешней ссылки.</span><span class="sxs-lookup"><span data-stu-id="3e497-119">External reference identifier.</span></span>

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

### <span data-ttu-id="3e497-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e497-120">-InputObject</span></span>
<span data-ttu-id="3e497-121">Входной объект типа Microsoft. AzureStack. Management. Subscriptions. admin. Models. Plan.</span><span class="sxs-lookup"><span data-stu-id="3e497-121">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan.</span></span>

```yaml
Type: Plan
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e497-122">-Location</span><span class="sxs-lookup"><span data-stu-id="3e497-122">-Location</span></span>
<span data-ttu-id="3e497-123">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="3e497-123">Location of the resource.</span></span>

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

### <span data-ttu-id="3e497-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3e497-124">-Name</span></span>
<span data-ttu-id="3e497-125">Название плана.</span><span class="sxs-lookup"><span data-stu-id="3e497-125">Name of the plan.</span></span>

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

### <span data-ttu-id="3e497-126">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="3e497-126">-QuotaIds</span></span>
<span data-ttu-id="3e497-127">Идентификаторы квот в плане.</span><span class="sxs-lookup"><span data-stu-id="3e497-127">Quota identifiers under the plan.</span></span>

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

### <span data-ttu-id="3e497-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e497-128">-ResourceGroupName</span></span>
<span data-ttu-id="3e497-129">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="3e497-129">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="3e497-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e497-130">-ResourceId</span></span>
<span data-ttu-id="3e497-131">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="3e497-131">The resource id.</span></span>

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

### <span data-ttu-id="3e497-132">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="3e497-132">-SkuIds</span></span>
<span data-ttu-id="3e497-133">Идентификаторы SKU.</span><span class="sxs-lookup"><span data-stu-id="3e497-133">SKU identifiers.</span></span>

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

### <span data-ttu-id="3e497-134">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="3e497-134">-SubscriptionCount</span></span>
<span data-ttu-id="3e497-135">Число подписок.</span><span class="sxs-lookup"><span data-stu-id="3e497-135">Subscription count.</span></span>

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

### <span data-ttu-id="3e497-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e497-136">-Confirm</span></span>
<span data-ttu-id="3e497-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3e497-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e497-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e497-138">-WhatIf</span></span>
<span data-ttu-id="3e497-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3e497-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e497-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3e497-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e497-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e497-141">CommonParameters</span></span>
<span data-ttu-id="3e497-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e497-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e497-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e497-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e497-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e497-144">INPUTS</span></span>

## <span data-ttu-id="3e497-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e497-145">OUTPUTS</span></span>

### <span data-ttu-id="3e497-146">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Plan</span><span class="sxs-lookup"><span data-stu-id="3e497-146">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="3e497-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e497-147">NOTES</span></span>

## <span data-ttu-id="3e497-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e497-148">RELATED LINKS</span></span>

