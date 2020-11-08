---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3e7d51bef12f0f7808aff3fda819ac614e0bb1c9
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076613"
---
# <span data-ttu-id="62663-101">Add-AzsPlanToOffer</span><span class="sxs-lookup"><span data-stu-id="62663-101">Add-AzsPlanToOffer</span></span>

## <span data-ttu-id="62663-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="62663-102">SYNOPSIS</span></span>
<span data-ttu-id="62663-103">Связывание плана с предложением.</span><span class="sxs-lookup"><span data-stu-id="62663-103">Links a plan to an offer.</span></span>

## <span data-ttu-id="62663-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="62663-104">SYNTAX</span></span>

```
Add-AzsPlanToOffer [-PlanName] <String> [-OfferName] <String> [-ResourceGroupName] <String>
 [[-PlanLinkType] <String>] [[-MaxAcquisitionCount] <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62663-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62663-105">DESCRIPTION</span></span>
<span data-ttu-id="62663-106">Связывание плана с предложением.</span><span class="sxs-lookup"><span data-stu-id="62663-106">Links a plan to an offer.</span></span>

## <span data-ttu-id="62663-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="62663-107">EXAMPLES</span></span>

### <span data-ttu-id="62663-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="62663-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsPlanToOffer -PlanLinkType Addon -Offer offer1 -PlanName plan1 -ResourceGroupName rg1 -MaxAcquisitionCount 2
```

## <span data-ttu-id="62663-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="62663-109">PARAMETERS</span></span>

### <span data-ttu-id="62663-110">-Force</span><span class="sxs-lookup"><span data-stu-id="62663-110">-Force</span></span>
<span data-ttu-id="62663-111">Пометка для удаления элемента без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="62663-111">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="62663-112">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="62663-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="62663-113">Максимальное количество приобретений для подписчиков</span><span class="sxs-lookup"><span data-stu-id="62663-113">The maximum acquisition count by subscribers</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62663-114">-OfferName</span><span class="sxs-lookup"><span data-stu-id="62663-114">-OfferName</span></span>
<span data-ttu-id="62663-115">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="62663-115">Name of an offer.</span></span>

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

### <span data-ttu-id="62663-116">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="62663-116">-PlanLinkType</span></span>
<span data-ttu-id="62663-117">Тип ссылки на план.</span><span class="sxs-lookup"><span data-stu-id="62663-117">Type of the plan link.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62663-118">-PlanName</span><span class="sxs-lookup"><span data-stu-id="62663-118">-PlanName</span></span>
<span data-ttu-id="62663-119">Название плана.</span><span class="sxs-lookup"><span data-stu-id="62663-119">Name of the plan.</span></span>

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

### <span data-ttu-id="62663-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62663-120">-ResourceGroupName</span></span>
<span data-ttu-id="62663-121">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="62663-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="62663-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62663-122">-Confirm</span></span>
<span data-ttu-id="62663-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="62663-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62663-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62663-124">-WhatIf</span></span>
<span data-ttu-id="62663-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="62663-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62663-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="62663-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62663-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62663-127">CommonParameters</span></span>
<span data-ttu-id="62663-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="62663-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62663-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62663-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62663-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="62663-130">INPUTS</span></span>

## <span data-ttu-id="62663-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="62663-131">OUTPUTS</span></span>

## <span data-ttu-id="62663-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="62663-132">NOTES</span></span>

## <span data-ttu-id="62663-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62663-133">RELATED LINKS</span></span>

