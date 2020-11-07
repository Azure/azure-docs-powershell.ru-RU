---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: aee9eab2ce04c1b9454fcf133edc290e887caf50
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731717"
---
# <span data-ttu-id="7ff80-101">New-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="7ff80-101">New-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="7ff80-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7ff80-102">SYNOPSIS</span></span>
<span data-ttu-id="7ff80-103">Создание плана подписки.</span><span class="sxs-lookup"><span data-stu-id="7ff80-103">Creates a subscription plan.</span></span>

## <span data-ttu-id="7ff80-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7ff80-104">SYNTAX</span></span>

```
New-AzsSubscriptionPlan [[-AcquisitionId] <Guid>] [-PlanId] <String> [-TargetSubscriptionId] <Guid> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ff80-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ff80-105">DESCRIPTION</span></span>
<span data-ttu-id="7ff80-106">Создание плана подписки.</span><span class="sxs-lookup"><span data-stu-id="7ff80-106">Creates a subscription plan.</span></span>

## <span data-ttu-id="7ff80-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7ff80-107">EXAMPLES</span></span>

### <span data-ttu-id="7ff80-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7ff80-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsSubscriptionPlan -PlanId "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/plans/plan1" -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="7ff80-109">Создание плана подписки.</span><span class="sxs-lookup"><span data-stu-id="7ff80-109">Create an subscription plan.</span></span>

## <span data-ttu-id="7ff80-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7ff80-110">PARAMETERS</span></span>

### <span data-ttu-id="7ff80-111">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="7ff80-111">-AcquisitionId</span></span>
<span data-ttu-id="7ff80-112">Идентификатор приобретения.</span><span class="sxs-lookup"><span data-stu-id="7ff80-112">Acquisition identifier.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: $([Guid]::NewGuid())
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ff80-113">-PlanId</span><span class="sxs-lookup"><span data-stu-id="7ff80-113">-PlanId</span></span>
<span data-ttu-id="7ff80-114">Идентификатор плана в контексте подписки клиента.</span><span class="sxs-lookup"><span data-stu-id="7ff80-114">Plan identifier in the tenant subscription context.</span></span>

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

### <span data-ttu-id="7ff80-115">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7ff80-115">-TargetSubscriptionId</span></span>
<span data-ttu-id="7ff80-116">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="7ff80-116">The target subscription ID.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ff80-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ff80-117">-Confirm</span></span>
<span data-ttu-id="7ff80-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7ff80-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ff80-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ff80-119">-WhatIf</span></span>
<span data-ttu-id="7ff80-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7ff80-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ff80-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7ff80-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ff80-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ff80-122">CommonParameters</span></span>
<span data-ttu-id="7ff80-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7ff80-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ff80-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ff80-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ff80-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7ff80-125">INPUTS</span></span>

## <span data-ttu-id="7ff80-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ff80-126">OUTPUTS</span></span>

### <span data-ttu-id="7ff80-127">Microsoft. AzureStack. Management. Subscriptions. admin. Models. PlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="7ff80-127">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.PlanAcquisition</span></span>

## <span data-ttu-id="7ff80-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="7ff80-128">NOTES</span></span>

## <span data-ttu-id="7ff80-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7ff80-129">RELATED LINKS</span></span>

