---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3a4c99f48087dcbac17dc10da3c647525670fe90
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908410"
---
# <span data-ttu-id="f57c3-101">New-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="f57c3-101">New-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="f57c3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f57c3-102">SYNOPSIS</span></span>
<span data-ttu-id="f57c3-103">Создание плана подписки.</span><span class="sxs-lookup"><span data-stu-id="f57c3-103">Creates a subscription plan.</span></span>

## <span data-ttu-id="f57c3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f57c3-104">SYNTAX</span></span>

```
New-AzsSubscriptionPlan [[-AcquisitionId] <Guid>] [-PlanId] <String> [-TargetSubscriptionId] <Guid> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f57c3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f57c3-105">DESCRIPTION</span></span>
<span data-ttu-id="f57c3-106">Создание плана подписки.</span><span class="sxs-lookup"><span data-stu-id="f57c3-106">Creates a subscription plan.</span></span>

## <span data-ttu-id="f57c3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f57c3-107">EXAMPLES</span></span>

### <span data-ttu-id="f57c3-108">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f57c3-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsSubscriptionPlan -PlanId "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/plans/plan1" -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="f57c3-109">Создание плана подписки.</span><span class="sxs-lookup"><span data-stu-id="f57c3-109">Create an subscription plan.</span></span>

## <span data-ttu-id="f57c3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f57c3-110">PARAMETERS</span></span>

### <span data-ttu-id="f57c3-111">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="f57c3-111">-AcquisitionId</span></span>
<span data-ttu-id="f57c3-112">Идентификатор приобретения.</span><span class="sxs-lookup"><span data-stu-id="f57c3-112">Acquisition identifier.</span></span>

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

### <span data-ttu-id="f57c3-113">-PlanId</span><span class="sxs-lookup"><span data-stu-id="f57c3-113">-PlanId</span></span>
<span data-ttu-id="f57c3-114">Идентификатор плана в контексте подписки клиента.</span><span class="sxs-lookup"><span data-stu-id="f57c3-114">Plan identifier in the tenant subscription context.</span></span>

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

### <span data-ttu-id="f57c3-115">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f57c3-115">-TargetSubscriptionId</span></span>
<span data-ttu-id="f57c3-116">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="f57c3-116">The target subscription ID.</span></span>

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

### <span data-ttu-id="f57c3-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f57c3-117">-Confirm</span></span>
<span data-ttu-id="f57c3-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f57c3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f57c3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f57c3-119">-WhatIf</span></span>
<span data-ttu-id="f57c3-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f57c3-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f57c3-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f57c3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f57c3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f57c3-122">CommonParameters</span></span>
<span data-ttu-id="f57c3-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f57c3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f57c3-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f57c3-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f57c3-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f57c3-125">INPUTS</span></span>

## <span data-ttu-id="f57c3-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f57c3-126">OUTPUTS</span></span>

### <span data-ttu-id="f57c3-127">Microsoft. AzureStack. Management. Subscriptions. admin. Models. PlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="f57c3-127">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.PlanAcquisition</span></span>

## <span data-ttu-id="f57c3-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="f57c3-128">NOTES</span></span>

## <span data-ttu-id="f57c3-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f57c3-129">RELATED LINKS</span></span>

