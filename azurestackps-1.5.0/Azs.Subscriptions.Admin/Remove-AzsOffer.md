---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2ac9f85896c1ae0a8eb7e060600ba5b4eb0e792
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731753"
---
# <span data-ttu-id="9de35-101">Remove-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="9de35-101">Remove-AzsOffer</span></span>

## <span data-ttu-id="9de35-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9de35-102">SYNOPSIS</span></span>
<span data-ttu-id="9de35-103">Удаление указанного предложения.</span><span class="sxs-lookup"><span data-stu-id="9de35-103">Delete the specified offer.</span></span>

## <span data-ttu-id="9de35-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9de35-104">SYNTAX</span></span>

### <span data-ttu-id="9de35-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9de35-105">Delete (Default)</span></span>
```
Remove-AzsOffer -Name <String> -ResourceGroupName <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9de35-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9de35-106">ResourceId</span></span>
```
Remove-AzsOffer -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9de35-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9de35-107">DESCRIPTION</span></span>
<span data-ttu-id="9de35-108">Удаление указанного предложения.</span><span class="sxs-lookup"><span data-stu-id="9de35-108">Delete the specified offer.</span></span>

## <span data-ttu-id="9de35-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9de35-109">EXAMPLES</span></span>

### <span data-ttu-id="9de35-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9de35-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsOffer -Name offername1 -ResourceGroupName rg1
```

<span data-ttu-id="9de35-111">Удаление указанного предложения.</span><span class="sxs-lookup"><span data-stu-id="9de35-111">Delete the specified offer.</span></span>

## <span data-ttu-id="9de35-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9de35-112">PARAMETERS</span></span>

### <span data-ttu-id="9de35-113">-Force</span><span class="sxs-lookup"><span data-stu-id="9de35-113">-Force</span></span>
<span data-ttu-id="9de35-114">Пометка для удаления элемента без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="9de35-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="9de35-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9de35-115">-Name</span></span>
<span data-ttu-id="9de35-116">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="9de35-116">Name of an offer.</span></span>

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

### <span data-ttu-id="9de35-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9de35-117">-ResourceGroupName</span></span>
<span data-ttu-id="9de35-118">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="9de35-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="9de35-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9de35-119">-ResourceId</span></span>
<span data-ttu-id="9de35-120">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="9de35-120">The resource id.</span></span>

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

### <span data-ttu-id="9de35-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9de35-121">-Confirm</span></span>
<span data-ttu-id="9de35-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9de35-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9de35-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9de35-123">-WhatIf</span></span>
<span data-ttu-id="9de35-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9de35-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9de35-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9de35-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9de35-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9de35-126">CommonParameters</span></span>
<span data-ttu-id="9de35-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9de35-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9de35-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9de35-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9de35-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9de35-129">INPUTS</span></span>

## <span data-ttu-id="9de35-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9de35-130">OUTPUTS</span></span>

## <span data-ttu-id="9de35-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="9de35-131">NOTES</span></span>

## <span data-ttu-id="9de35-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9de35-132">RELATED LINKS</span></span>

