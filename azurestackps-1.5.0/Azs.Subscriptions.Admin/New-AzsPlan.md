---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cddc7e5b3e0d9c7181248e024982293d1418e680
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555488"
---
# <span data-ttu-id="27ad7-101">New-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="27ad7-101">New-AzsPlan</span></span>

## <span data-ttu-id="27ad7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="27ad7-102">SYNOPSIS</span></span>
<span data-ttu-id="27ad7-103">Создание нового плана</span><span class="sxs-lookup"><span data-stu-id="27ad7-103">Creates a new plan</span></span>

## <span data-ttu-id="27ad7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="27ad7-104">SYNTAX</span></span>

```
New-AzsPlan [-Name] <String> [-ResourceGroupName] <String> [-DisplayName] <String> [-QuotaIds] <String[]>
 [[-Description] <String>] [[-SkuIds] <String[]>] [[-ExternalReferenceId] <String>] [[-Location] <String>]
 [[-SubscriptionCount] <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27ad7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27ad7-105">DESCRIPTION</span></span>
<span data-ttu-id="27ad7-106">Создание нового плана</span><span class="sxs-lookup"><span data-stu-id="27ad7-106">Creates a new plan</span></span>

## <span data-ttu-id="27ad7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="27ad7-107">EXAMPLES</span></span>

### <span data-ttu-id="27ad7-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="27ad7-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -QuotaIds "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/providers/Microsoft.Subscriptions.Admin/locations/local/quotas/delegatedProviderQuota" -Location "local" -DisplayName "plan1" -Description "asda"
```

<span data-ttu-id="27ad7-109">Создание нового плана</span><span class="sxs-lookup"><span data-stu-id="27ad7-109">Creates a new plan</span></span>

## <span data-ttu-id="27ad7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="27ad7-110">PARAMETERS</span></span>

### <span data-ttu-id="27ad7-111">-Описание</span><span class="sxs-lookup"><span data-stu-id="27ad7-111">-Description</span></span>
<span data-ttu-id="27ad7-112">Описание плана.</span><span class="sxs-lookup"><span data-stu-id="27ad7-112">Description of the plan.</span></span>

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

### <span data-ttu-id="27ad7-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="27ad7-113">-DisplayName</span></span>
<span data-ttu-id="27ad7-114">Отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="27ad7-114">Display name.</span></span>

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

### <span data-ttu-id="27ad7-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="27ad7-115">-ExternalReferenceId</span></span>
<span data-ttu-id="27ad7-116">Идентификатор внешней ссылки.</span><span class="sxs-lookup"><span data-stu-id="27ad7-116">External reference identifier.</span></span>

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

### <span data-ttu-id="27ad7-117">-Location</span><span class="sxs-lookup"><span data-stu-id="27ad7-117">-Location</span></span>
<span data-ttu-id="27ad7-118">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="27ad7-118">Location of the resource.</span></span>

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

### <span data-ttu-id="27ad7-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="27ad7-119">-Name</span></span>
<span data-ttu-id="27ad7-120">Название плана.</span><span class="sxs-lookup"><span data-stu-id="27ad7-120">Name of the plan.</span></span>

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

### <span data-ttu-id="27ad7-121">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="27ad7-121">-QuotaIds</span></span>
<span data-ttu-id="27ad7-122">Идентификаторы квот в плане.</span><span class="sxs-lookup"><span data-stu-id="27ad7-122">Quota identifiers under the plan.</span></span>

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

### <span data-ttu-id="27ad7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27ad7-123">-ResourceGroupName</span></span>
<span data-ttu-id="27ad7-124">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="27ad7-124">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="27ad7-125">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="27ad7-125">-SkuIds</span></span>
<span data-ttu-id="27ad7-126">Идентификаторы SKU.</span><span class="sxs-lookup"><span data-stu-id="27ad7-126">SKU identifiers.</span></span>

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

### <span data-ttu-id="27ad7-127">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="27ad7-127">-SubscriptionCount</span></span>
<span data-ttu-id="27ad7-128">Число подписок.</span><span class="sxs-lookup"><span data-stu-id="27ad7-128">Subscription count.</span></span>

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

### <span data-ttu-id="27ad7-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27ad7-129">-Confirm</span></span>
<span data-ttu-id="27ad7-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="27ad7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27ad7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27ad7-131">-WhatIf</span></span>
<span data-ttu-id="27ad7-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="27ad7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27ad7-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="27ad7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27ad7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27ad7-134">CommonParameters</span></span>
<span data-ttu-id="27ad7-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="27ad7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27ad7-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27ad7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27ad7-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="27ad7-137">INPUTS</span></span>

## <span data-ttu-id="27ad7-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="27ad7-138">OUTPUTS</span></span>

### <span data-ttu-id="27ad7-139">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Plan</span><span class="sxs-lookup"><span data-stu-id="27ad7-139">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="27ad7-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="27ad7-140">NOTES</span></span>

## <span data-ttu-id="27ad7-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27ad7-141">RELATED LINKS</span></span>

