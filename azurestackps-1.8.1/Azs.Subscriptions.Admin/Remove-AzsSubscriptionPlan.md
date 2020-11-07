---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b2f5117224318eae53b8b11f4af58c736ac800b
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93908657"
---
# <span data-ttu-id="3c8aa-101">Remove-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="3c8aa-101">Remove-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="3c8aa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3c8aa-102">SYNOPSIS</span></span>
<span data-ttu-id="3c8aa-103">Удаление плана подписки.</span><span class="sxs-lookup"><span data-stu-id="3c8aa-103">Deletes a subscription plan.</span></span>

## <span data-ttu-id="3c8aa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3c8aa-104">SYNTAX</span></span>

### <span data-ttu-id="3c8aa-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3c8aa-105">Delete (Default)</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId <Guid> -TargetSubscriptionId <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c8aa-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c8aa-106">ResourceId</span></span>
```
Remove-AzsSubscriptionPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c8aa-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c8aa-107">DESCRIPTION</span></span>
<span data-ttu-id="3c8aa-108">Удаление плана подписки.</span><span class="sxs-lookup"><span data-stu-id="3c8aa-108">Deletes a subscription plan.</span></span>

## <span data-ttu-id="3c8aa-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3c8aa-109">EXAMPLES</span></span>

### <span data-ttu-id="3c8aa-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3c8aa-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="3c8aa-111">Удаление плана подписки.</span><span class="sxs-lookup"><span data-stu-id="3c8aa-111">Delete a subscription plan.</span></span>

## <span data-ttu-id="3c8aa-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3c8aa-112">PARAMETERS</span></span>

### <span data-ttu-id="3c8aa-113">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="3c8aa-113">-AcquisitionId</span></span>
<span data-ttu-id="3c8aa-114">Идентификатор приобретения плана</span><span class="sxs-lookup"><span data-stu-id="3c8aa-114">The plan acquisition Identifier</span></span>

```yaml
Type: Guid
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c8aa-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3c8aa-115">-Force</span></span>
<span data-ttu-id="3c8aa-116">Пометка для удаления элемента без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="3c8aa-116">Flag to remove the item without confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c8aa-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c8aa-117">-ResourceId</span></span>
<span data-ttu-id="3c8aa-118">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="3c8aa-118">The resource id.</span></span>

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

### <span data-ttu-id="3c8aa-119">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3c8aa-119">-TargetSubscriptionId</span></span>
<span data-ttu-id="3c8aa-120">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="3c8aa-120">The target subscription ID.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c8aa-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c8aa-121">-Confirm</span></span>
<span data-ttu-id="3c8aa-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3c8aa-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c8aa-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c8aa-123">-WhatIf</span></span>
<span data-ttu-id="3c8aa-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3c8aa-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c8aa-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3c8aa-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c8aa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c8aa-126">CommonParameters</span></span>
<span data-ttu-id="3c8aa-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3c8aa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c8aa-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c8aa-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c8aa-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3c8aa-129">INPUTS</span></span>

## <span data-ttu-id="3c8aa-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c8aa-130">OUTPUTS</span></span>

## <span data-ttu-id="3c8aa-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="3c8aa-131">NOTES</span></span>

## <span data-ttu-id="3c8aa-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c8aa-132">RELATED LINKS</span></span>

