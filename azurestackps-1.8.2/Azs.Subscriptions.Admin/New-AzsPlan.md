---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 348f7dc1f4719e70a73902b59cf335bb22015bec
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077136"
---
# <span data-ttu-id="04314-101">New-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="04314-101">New-AzsPlan</span></span>

## <span data-ttu-id="04314-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="04314-102">SYNOPSIS</span></span>
<span data-ttu-id="04314-103">Создание нового плана</span><span class="sxs-lookup"><span data-stu-id="04314-103">Creates a new plan</span></span>

## <span data-ttu-id="04314-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="04314-104">SYNTAX</span></span>

```
New-AzsPlan [-Name] <String> [-ResourceGroupName] <String> [-DisplayName] <String> [-QuotaIds] <String[]>
 [[-Description] <String>] [[-SkuIds] <String[]>] [[-ExternalReferenceId] <String>] [[-Location] <String>]
 [[-SubscriptionCount] <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04314-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="04314-105">DESCRIPTION</span></span>
<span data-ttu-id="04314-106">Создание нового плана</span><span class="sxs-lookup"><span data-stu-id="04314-106">Creates a new plan</span></span>

## <span data-ttu-id="04314-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="04314-107">EXAMPLES</span></span>

### <span data-ttu-id="04314-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="04314-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -QuotaIds "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/providers/Microsoft.Subscriptions.Admin/locations/local/quotas/delegatedProviderQuota" -Location "local" -DisplayName "plan1" -Description "asda"
```

<span data-ttu-id="04314-109">Создание нового плана</span><span class="sxs-lookup"><span data-stu-id="04314-109">Creates a new plan</span></span>

## <span data-ttu-id="04314-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="04314-110">PARAMETERS</span></span>

### <span data-ttu-id="04314-111">-Описание</span><span class="sxs-lookup"><span data-stu-id="04314-111">-Description</span></span>
<span data-ttu-id="04314-112">Описание плана.</span><span class="sxs-lookup"><span data-stu-id="04314-112">Description of the plan.</span></span>

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

### <span data-ttu-id="04314-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="04314-113">-DisplayName</span></span>
<span data-ttu-id="04314-114">Отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="04314-114">Display name.</span></span>

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

### <span data-ttu-id="04314-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="04314-115">-ExternalReferenceId</span></span>
<span data-ttu-id="04314-116">Идентификатор внешней ссылки.</span><span class="sxs-lookup"><span data-stu-id="04314-116">External reference identifier.</span></span>

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

### <span data-ttu-id="04314-117">-Location</span><span class="sxs-lookup"><span data-stu-id="04314-117">-Location</span></span>
<span data-ttu-id="04314-118">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="04314-118">Location of the resource.</span></span>

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

### <span data-ttu-id="04314-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="04314-119">-Name</span></span>
<span data-ttu-id="04314-120">Название плана.</span><span class="sxs-lookup"><span data-stu-id="04314-120">Name of the plan.</span></span>

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

### <span data-ttu-id="04314-121">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="04314-121">-QuotaIds</span></span>
<span data-ttu-id="04314-122">Идентификаторы квот в плане.</span><span class="sxs-lookup"><span data-stu-id="04314-122">Quota identifiers under the plan.</span></span>

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

### <span data-ttu-id="04314-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04314-123">-ResourceGroupName</span></span>
<span data-ttu-id="04314-124">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="04314-124">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="04314-125">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="04314-125">-SkuIds</span></span>
<span data-ttu-id="04314-126">Идентификаторы SKU.</span><span class="sxs-lookup"><span data-stu-id="04314-126">SKU identifiers.</span></span>

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

### <span data-ttu-id="04314-127">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="04314-127">-SubscriptionCount</span></span>
<span data-ttu-id="04314-128">Число подписок.</span><span class="sxs-lookup"><span data-stu-id="04314-128">Subscription count.</span></span>

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

### <span data-ttu-id="04314-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04314-129">-Confirm</span></span>
<span data-ttu-id="04314-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="04314-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04314-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04314-131">-WhatIf</span></span>
<span data-ttu-id="04314-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="04314-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04314-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="04314-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04314-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04314-134">CommonParameters</span></span>
<span data-ttu-id="04314-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="04314-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04314-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04314-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04314-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="04314-137">INPUTS</span></span>

## <span data-ttu-id="04314-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="04314-138">OUTPUTS</span></span>

### <span data-ttu-id="04314-139">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Plan</span><span class="sxs-lookup"><span data-stu-id="04314-139">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="04314-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="04314-140">NOTES</span></span>

## <span data-ttu-id="04314-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="04314-141">RELATED LINKS</span></span>

