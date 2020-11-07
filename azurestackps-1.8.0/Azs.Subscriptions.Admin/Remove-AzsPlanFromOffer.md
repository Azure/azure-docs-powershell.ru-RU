---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5f5c0050f6a1e226f5b5513e11d70fac1844ecda
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908401"
---
# <span data-ttu-id="9c55a-101">Remove-AzsPlanFromOffer</span><span class="sxs-lookup"><span data-stu-id="9c55a-101">Remove-AzsPlanFromOffer</span></span>

## <span data-ttu-id="9c55a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9c55a-102">SYNOPSIS</span></span>
<span data-ttu-id="9c55a-103">Удаление связи плана с предложением.</span><span class="sxs-lookup"><span data-stu-id="9c55a-103">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="9c55a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9c55a-104">SYNTAX</span></span>

```
Remove-AzsPlanFromOffer -PlanName <String> -OfferName <String> -ResourceGroupName <String>
 [-PlanLinkType <String>] [-MaxAcquisitionCount <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c55a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c55a-105">DESCRIPTION</span></span>
<span data-ttu-id="9c55a-106">Удаление связи плана с предложением.</span><span class="sxs-lookup"><span data-stu-id="9c55a-106">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="9c55a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9c55a-107">EXAMPLES</span></span>

### <span data-ttu-id="9c55a-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9c55a-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlanToOffer -Offer offer1 -PlanName plan1 -ResourceGroup rg1
```

## <span data-ttu-id="9c55a-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9c55a-109">PARAMETERS</span></span>

### <span data-ttu-id="9c55a-110">-Force</span><span class="sxs-lookup"><span data-stu-id="9c55a-110">-Force</span></span>
<span data-ttu-id="9c55a-111">Пометка для удаления элемента без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="9c55a-111">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="9c55a-112">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="9c55a-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="9c55a-113">Максимальное количество приобретений для подписчиков</span><span class="sxs-lookup"><span data-stu-id="9c55a-113">The maximum acquisition count by subscribers</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c55a-114">-OfferName</span><span class="sxs-lookup"><span data-stu-id="9c55a-114">-OfferName</span></span>
<span data-ttu-id="9c55a-115">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="9c55a-115">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c55a-116">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="9c55a-116">-PlanLinkType</span></span>
<span data-ttu-id="9c55a-117">Тип ссылки на план.</span><span class="sxs-lookup"><span data-stu-id="9c55a-117">Type of the plan link.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c55a-118">-PlanName</span><span class="sxs-lookup"><span data-stu-id="9c55a-118">-PlanName</span></span>
<span data-ttu-id="9c55a-119">Название плана.</span><span class="sxs-lookup"><span data-stu-id="9c55a-119">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c55a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c55a-120">-ResourceGroupName</span></span>
<span data-ttu-id="9c55a-121">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="9c55a-121">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c55a-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c55a-122">-Confirm</span></span>
<span data-ttu-id="9c55a-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9c55a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c55a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c55a-124">-WhatIf</span></span>
<span data-ttu-id="9c55a-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9c55a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c55a-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9c55a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c55a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c55a-127">CommonParameters</span></span>
<span data-ttu-id="9c55a-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9c55a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c55a-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c55a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c55a-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9c55a-130">INPUTS</span></span>

## <span data-ttu-id="9c55a-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c55a-131">OUTPUTS</span></span>

## <span data-ttu-id="9c55a-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="9c55a-132">NOTES</span></span>

## <span data-ttu-id="9c55a-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c55a-133">RELATED LINKS</span></span>

