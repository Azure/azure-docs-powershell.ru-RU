---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0ec978cebfaa12f574ce20638347839fd70099df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556036"
---
# <span data-ttu-id="f576b-101">Remove-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="f576b-101">Remove-AzsOfferDelegation</span></span>

## <span data-ttu-id="f576b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f576b-102">SYNOPSIS</span></span>
<span data-ttu-id="f576b-103">Удаление делегирования предложения</span><span class="sxs-lookup"><span data-stu-id="f576b-103">Removes the offer delegation</span></span>

## <span data-ttu-id="f576b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f576b-104">SYNTAX</span></span>

### <span data-ttu-id="f576b-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f576b-105">Delete (Default)</span></span>
```
Remove-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f576b-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f576b-106">ResourceId</span></span>
```
Remove-AzsOfferDelegation -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f576b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f576b-107">DESCRIPTION</span></span>
<span data-ttu-id="f576b-108">Удаление делегирования предложения</span><span class="sxs-lookup"><span data-stu-id="f576b-108">Removes the offer delegation</span></span>

## <span data-ttu-id="f576b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f576b-109">EXAMPLES</span></span>

### <span data-ttu-id="f576b-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f576b-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegation1
```

<span data-ttu-id="f576b-111">Удаление делегирования предложения</span><span class="sxs-lookup"><span data-stu-id="f576b-111">Removes the offer delegation</span></span>

## <span data-ttu-id="f576b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f576b-112">PARAMETERS</span></span>

### <span data-ttu-id="f576b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f576b-113">-Force</span></span>
<span data-ttu-id="f576b-114">Пометка для удаления элемента без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="f576b-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="f576b-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f576b-115">-Name</span></span>
<span data-ttu-id="f576b-116">Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="f576b-116">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="f576b-117">-OfferName</span><span class="sxs-lookup"><span data-stu-id="f576b-117">-OfferName</span></span>
<span data-ttu-id="f576b-118">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="f576b-118">Name of an offer.</span></span>

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

### <span data-ttu-id="f576b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f576b-119">-ResourceGroupName</span></span>
<span data-ttu-id="f576b-120">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="f576b-120">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="f576b-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f576b-121">-ResourceId</span></span>
<span data-ttu-id="f576b-122">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="f576b-122">The resource id.</span></span>

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

### <span data-ttu-id="f576b-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f576b-123">-Confirm</span></span>
<span data-ttu-id="f576b-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f576b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f576b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f576b-125">-WhatIf</span></span>
<span data-ttu-id="f576b-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f576b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f576b-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f576b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f576b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f576b-128">CommonParameters</span></span>
<span data-ttu-id="f576b-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f576b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f576b-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f576b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f576b-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f576b-131">INPUTS</span></span>

## <span data-ttu-id="f576b-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f576b-132">OUTPUTS</span></span>

## <span data-ttu-id="f576b-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="f576b-133">NOTES</span></span>

## <span data-ttu-id="f576b-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f576b-134">RELATED LINKS</span></span>

