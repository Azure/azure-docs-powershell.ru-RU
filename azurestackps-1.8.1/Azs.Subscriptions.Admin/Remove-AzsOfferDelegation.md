---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e9fc37b5f99a9ad38e92ce1efc730718882b533d
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93908670"
---
# <span data-ttu-id="a086f-101">Remove-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="a086f-101">Remove-AzsOfferDelegation</span></span>

## <span data-ttu-id="a086f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a086f-102">SYNOPSIS</span></span>
<span data-ttu-id="a086f-103">Удаление делегирования предложения</span><span class="sxs-lookup"><span data-stu-id="a086f-103">Removes the offer delegation</span></span>

## <span data-ttu-id="a086f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a086f-104">SYNTAX</span></span>

### <span data-ttu-id="a086f-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a086f-105">Delete (Default)</span></span>
```
Remove-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a086f-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a086f-106">ResourceId</span></span>
```
Remove-AzsOfferDelegation -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a086f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a086f-107">DESCRIPTION</span></span>
<span data-ttu-id="a086f-108">Удаление делегирования предложения</span><span class="sxs-lookup"><span data-stu-id="a086f-108">Removes the offer delegation</span></span>

## <span data-ttu-id="a086f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a086f-109">EXAMPLES</span></span>

### <span data-ttu-id="a086f-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a086f-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegation1
```

<span data-ttu-id="a086f-111">Удаление делегирования предложения</span><span class="sxs-lookup"><span data-stu-id="a086f-111">Removes the offer delegation</span></span>

## <span data-ttu-id="a086f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a086f-112">PARAMETERS</span></span>

### <span data-ttu-id="a086f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a086f-113">-Force</span></span>
<span data-ttu-id="a086f-114">Пометка для удаления элемента без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="a086f-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="a086f-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a086f-115">-Name</span></span>
<span data-ttu-id="a086f-116">Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="a086f-116">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="a086f-117">-OfferName</span><span class="sxs-lookup"><span data-stu-id="a086f-117">-OfferName</span></span>
<span data-ttu-id="a086f-118">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="a086f-118">Name of an offer.</span></span>

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

### <span data-ttu-id="a086f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a086f-119">-ResourceGroupName</span></span>
<span data-ttu-id="a086f-120">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="a086f-120">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="a086f-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a086f-121">-ResourceId</span></span>
<span data-ttu-id="a086f-122">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="a086f-122">The resource id.</span></span>

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

### <span data-ttu-id="a086f-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a086f-123">-Confirm</span></span>
<span data-ttu-id="a086f-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a086f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a086f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a086f-125">-WhatIf</span></span>
<span data-ttu-id="a086f-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a086f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a086f-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a086f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a086f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a086f-128">CommonParameters</span></span>
<span data-ttu-id="a086f-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a086f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a086f-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a086f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a086f-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a086f-131">INPUTS</span></span>

## <span data-ttu-id="a086f-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a086f-132">OUTPUTS</span></span>

## <span data-ttu-id="a086f-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="a086f-133">NOTES</span></span>

## <span data-ttu-id="a086f-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a086f-134">RELATED LINKS</span></span>

