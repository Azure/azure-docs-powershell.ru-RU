---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 348f7dc1f4719e70a73902b59cf335bb22015bec
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908090"
---
# <span data-ttu-id="3a735-101">New-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="3a735-101">New-AzsPlan</span></span>

## <span data-ttu-id="3a735-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3a735-102">SYNOPSIS</span></span>
<span data-ttu-id="3a735-103">Создание нового плана</span><span class="sxs-lookup"><span data-stu-id="3a735-103">Creates a new plan</span></span>

## <span data-ttu-id="3a735-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3a735-104">SYNTAX</span></span>

```
New-AzsPlan [-Name] <String> [-ResourceGroupName] <String> [-DisplayName] <String> [-QuotaIds] <String[]>
 [[-Description] <String>] [[-SkuIds] <String[]>] [[-ExternalReferenceId] <String>] [[-Location] <String>]
 [[-SubscriptionCount] <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a735-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a735-105">DESCRIPTION</span></span>
<span data-ttu-id="3a735-106">Создание нового плана</span><span class="sxs-lookup"><span data-stu-id="3a735-106">Creates a new plan</span></span>

## <span data-ttu-id="3a735-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3a735-107">EXAMPLES</span></span>

### <span data-ttu-id="3a735-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3a735-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -QuotaIds "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/providers/Microsoft.Subscriptions.Admin/locations/local/quotas/delegatedProviderQuota" -Location "local" -DisplayName "plan1" -Description "asda"
```

<span data-ttu-id="3a735-109">Создание нового плана</span><span class="sxs-lookup"><span data-stu-id="3a735-109">Creates a new plan</span></span>

## <span data-ttu-id="3a735-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3a735-110">PARAMETERS</span></span>

### <span data-ttu-id="3a735-111">-Описание</span><span class="sxs-lookup"><span data-stu-id="3a735-111">-Description</span></span>
<span data-ttu-id="3a735-112">Описание плана.</span><span class="sxs-lookup"><span data-stu-id="3a735-112">Description of the plan.</span></span>

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

### <span data-ttu-id="3a735-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3a735-113">-DisplayName</span></span>
<span data-ttu-id="3a735-114">Отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="3a735-114">Display name.</span></span>

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

### <span data-ttu-id="3a735-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="3a735-115">-ExternalReferenceId</span></span>
<span data-ttu-id="3a735-116">Идентификатор внешней ссылки.</span><span class="sxs-lookup"><span data-stu-id="3a735-116">External reference identifier.</span></span>

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

### <span data-ttu-id="3a735-117">-Location</span><span class="sxs-lookup"><span data-stu-id="3a735-117">-Location</span></span>
<span data-ttu-id="3a735-118">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="3a735-118">Location of the resource.</span></span>

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

### <span data-ttu-id="3a735-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3a735-119">-Name</span></span>
<span data-ttu-id="3a735-120">Название плана.</span><span class="sxs-lookup"><span data-stu-id="3a735-120">Name of the plan.</span></span>

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

### <span data-ttu-id="3a735-121">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="3a735-121">-QuotaIds</span></span>
<span data-ttu-id="3a735-122">Идентификаторы квот в плане.</span><span class="sxs-lookup"><span data-stu-id="3a735-122">Quota identifiers under the plan.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a735-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a735-123">-ResourceGroupName</span></span>
<span data-ttu-id="3a735-124">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="3a735-124">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="3a735-125">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="3a735-125">-SkuIds</span></span>
<span data-ttu-id="3a735-126">Идентификаторы SKU.</span><span class="sxs-lookup"><span data-stu-id="3a735-126">SKU identifiers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a735-127">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="3a735-127">-SubscriptionCount</span></span>
<span data-ttu-id="3a735-128">Число подписок.</span><span class="sxs-lookup"><span data-stu-id="3a735-128">Subscription count.</span></span>

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

### <span data-ttu-id="3a735-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a735-129">-Confirm</span></span>
<span data-ttu-id="3a735-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3a735-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a735-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a735-131">-WhatIf</span></span>
<span data-ttu-id="3a735-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3a735-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a735-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3a735-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a735-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a735-134">CommonParameters</span></span>
<span data-ttu-id="3a735-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3a735-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a735-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a735-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a735-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3a735-137">INPUTS</span></span>

## <span data-ttu-id="3a735-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a735-138">OUTPUTS</span></span>

### <span data-ttu-id="3a735-139">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Plan</span><span class="sxs-lookup"><span data-stu-id="3a735-139">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="3a735-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="3a735-140">NOTES</span></span>

## <span data-ttu-id="3a735-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3a735-141">RELATED LINKS</span></span>

