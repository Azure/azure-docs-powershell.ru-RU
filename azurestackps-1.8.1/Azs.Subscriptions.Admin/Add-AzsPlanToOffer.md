---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3e7d51bef12f0f7808aff3fda819ac614e0bb1c9
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93908646"
---
# <span data-ttu-id="ece0e-101">Add-AzsPlanToOffer</span><span class="sxs-lookup"><span data-stu-id="ece0e-101">Add-AzsPlanToOffer</span></span>

## <span data-ttu-id="ece0e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ece0e-102">SYNOPSIS</span></span>
<span data-ttu-id="ece0e-103">Связывание плана с предложением.</span><span class="sxs-lookup"><span data-stu-id="ece0e-103">Links a plan to an offer.</span></span>

## <span data-ttu-id="ece0e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ece0e-104">SYNTAX</span></span>

```
Add-AzsPlanToOffer [-PlanName] <String> [-OfferName] <String> [-ResourceGroupName] <String>
 [[-PlanLinkType] <String>] [[-MaxAcquisitionCount] <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ece0e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ece0e-105">DESCRIPTION</span></span>
<span data-ttu-id="ece0e-106">Связывание плана с предложением.</span><span class="sxs-lookup"><span data-stu-id="ece0e-106">Links a plan to an offer.</span></span>

## <span data-ttu-id="ece0e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ece0e-107">EXAMPLES</span></span>

### <span data-ttu-id="ece0e-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ece0e-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsPlanToOffer -PlanLinkType Addon -Offer offer1 -PlanName plan1 -ResourceGroupName rg1 -MaxAcquisitionCount 2
```

## <span data-ttu-id="ece0e-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ece0e-109">PARAMETERS</span></span>

### <span data-ttu-id="ece0e-110">-Force</span><span class="sxs-lookup"><span data-stu-id="ece0e-110">-Force</span></span>
<span data-ttu-id="ece0e-111">Пометка для удаления элемента без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="ece0e-111">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="ece0e-112">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="ece0e-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="ece0e-113">Максимальное количество приобретений для подписчиков</span><span class="sxs-lookup"><span data-stu-id="ece0e-113">The maximum acquisition count by subscribers</span></span>

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

### <span data-ttu-id="ece0e-114">-OfferName</span><span class="sxs-lookup"><span data-stu-id="ece0e-114">-OfferName</span></span>
<span data-ttu-id="ece0e-115">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="ece0e-115">Name of an offer.</span></span>

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

### <span data-ttu-id="ece0e-116">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="ece0e-116">-PlanLinkType</span></span>
<span data-ttu-id="ece0e-117">Тип ссылки на план.</span><span class="sxs-lookup"><span data-stu-id="ece0e-117">Type of the plan link.</span></span>

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

### <span data-ttu-id="ece0e-118">-PlanName</span><span class="sxs-lookup"><span data-stu-id="ece0e-118">-PlanName</span></span>
<span data-ttu-id="ece0e-119">Название плана.</span><span class="sxs-lookup"><span data-stu-id="ece0e-119">Name of the plan.</span></span>

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

### <span data-ttu-id="ece0e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ece0e-120">-ResourceGroupName</span></span>
<span data-ttu-id="ece0e-121">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="ece0e-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="ece0e-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ece0e-122">-Confirm</span></span>
<span data-ttu-id="ece0e-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ece0e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ece0e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ece0e-124">-WhatIf</span></span>
<span data-ttu-id="ece0e-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ece0e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ece0e-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ece0e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ece0e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ece0e-127">CommonParameters</span></span>
<span data-ttu-id="ece0e-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ece0e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ece0e-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ece0e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ece0e-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ece0e-130">INPUTS</span></span>

## <span data-ttu-id="ece0e-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ece0e-131">OUTPUTS</span></span>

## <span data-ttu-id="ece0e-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="ece0e-132">NOTES</span></span>

## <span data-ttu-id="ece0e-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ece0e-133">RELATED LINKS</span></span>

