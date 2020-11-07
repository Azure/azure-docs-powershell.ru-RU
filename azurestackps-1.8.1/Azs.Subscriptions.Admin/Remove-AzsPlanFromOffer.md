---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5f5c0050f6a1e226f5b5513e11d70fac1844ecda
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93908661"
---
# <span data-ttu-id="aac73-101">Remove-AzsPlanFromOffer</span><span class="sxs-lookup"><span data-stu-id="aac73-101">Remove-AzsPlanFromOffer</span></span>

## <span data-ttu-id="aac73-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aac73-102">SYNOPSIS</span></span>
<span data-ttu-id="aac73-103">Удаление связи плана с предложением.</span><span class="sxs-lookup"><span data-stu-id="aac73-103">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="aac73-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aac73-104">SYNTAX</span></span>

```
Remove-AzsPlanFromOffer -PlanName <String> -OfferName <String> -ResourceGroupName <String>
 [-PlanLinkType <String>] [-MaxAcquisitionCount <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aac73-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aac73-105">DESCRIPTION</span></span>
<span data-ttu-id="aac73-106">Удаление связи плана с предложением.</span><span class="sxs-lookup"><span data-stu-id="aac73-106">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="aac73-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aac73-107">EXAMPLES</span></span>

### <span data-ttu-id="aac73-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="aac73-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlanToOffer -Offer offer1 -PlanName plan1 -ResourceGroup rg1
```

## <span data-ttu-id="aac73-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aac73-109">PARAMETERS</span></span>

### <span data-ttu-id="aac73-110">-Force</span><span class="sxs-lookup"><span data-stu-id="aac73-110">-Force</span></span>
<span data-ttu-id="aac73-111">Пометка для удаления элемента без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="aac73-111">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="aac73-112">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="aac73-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="aac73-113">Максимальное количество приобретений для подписчиков</span><span class="sxs-lookup"><span data-stu-id="aac73-113">The maximum acquisition count by subscribers</span></span>

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

### <span data-ttu-id="aac73-114">-OfferName</span><span class="sxs-lookup"><span data-stu-id="aac73-114">-OfferName</span></span>
<span data-ttu-id="aac73-115">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="aac73-115">Name of an offer.</span></span>

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

### <span data-ttu-id="aac73-116">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="aac73-116">-PlanLinkType</span></span>
<span data-ttu-id="aac73-117">Тип ссылки на план.</span><span class="sxs-lookup"><span data-stu-id="aac73-117">Type of the plan link.</span></span>

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

### <span data-ttu-id="aac73-118">-PlanName</span><span class="sxs-lookup"><span data-stu-id="aac73-118">-PlanName</span></span>
<span data-ttu-id="aac73-119">Название плана.</span><span class="sxs-lookup"><span data-stu-id="aac73-119">Name of the plan.</span></span>

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

### <span data-ttu-id="aac73-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aac73-120">-ResourceGroupName</span></span>
<span data-ttu-id="aac73-121">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="aac73-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="aac73-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aac73-122">-Confirm</span></span>
<span data-ttu-id="aac73-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aac73-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aac73-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aac73-124">-WhatIf</span></span>
<span data-ttu-id="aac73-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aac73-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aac73-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aac73-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aac73-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aac73-127">CommonParameters</span></span>
<span data-ttu-id="aac73-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aac73-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aac73-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aac73-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aac73-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aac73-130">INPUTS</span></span>

## <span data-ttu-id="aac73-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aac73-131">OUTPUTS</span></span>

## <span data-ttu-id="aac73-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="aac73-132">NOTES</span></span>

## <span data-ttu-id="aac73-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aac73-133">RELATED LINKS</span></span>

