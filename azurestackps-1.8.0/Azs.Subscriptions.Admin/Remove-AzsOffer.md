---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 74772615551979a9ab0cdba3603305489698e212
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908058"
---
# <span data-ttu-id="1fc8b-101">Remove-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="1fc8b-101">Remove-AzsOffer</span></span>

## <span data-ttu-id="1fc8b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1fc8b-102">SYNOPSIS</span></span>
<span data-ttu-id="1fc8b-103">Удаление указанного предложения.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-103">Delete the specified offer.</span></span>

## <span data-ttu-id="1fc8b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1fc8b-104">SYNTAX</span></span>

### <span data-ttu-id="1fc8b-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1fc8b-105">Delete (Default)</span></span>
```
Remove-AzsOffer -Name <String> -ResourceGroupName <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fc8b-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fc8b-106">ResourceId</span></span>
```
Remove-AzsOffer -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fc8b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fc8b-107">DESCRIPTION</span></span>
<span data-ttu-id="1fc8b-108">Удаление указанного предложения.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-108">Delete the specified offer.</span></span>

## <span data-ttu-id="1fc8b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1fc8b-109">EXAMPLES</span></span>

### <span data-ttu-id="1fc8b-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1fc8b-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsOffer -Name offername1 -ResourceGroupName rg1
```

<span data-ttu-id="1fc8b-111">Удаление указанного предложения.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-111">Delete the specified offer.</span></span>

## <span data-ttu-id="1fc8b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1fc8b-112">PARAMETERS</span></span>

### <span data-ttu-id="1fc8b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1fc8b-113">-Force</span></span>
<span data-ttu-id="1fc8b-114">Пометка для удаления элемента без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="1fc8b-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1fc8b-115">-Name</span></span>
<span data-ttu-id="1fc8b-116">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-116">Name of an offer.</span></span>

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

### <span data-ttu-id="1fc8b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fc8b-117">-ResourceGroupName</span></span>
<span data-ttu-id="1fc8b-118">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="1fc8b-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fc8b-119">-ResourceId</span></span>
<span data-ttu-id="1fc8b-120">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-120">The resource id.</span></span>

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

### <span data-ttu-id="1fc8b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1fc8b-121">-Confirm</span></span>
<span data-ttu-id="1fc8b-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fc8b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fc8b-123">-WhatIf</span></span>
<span data-ttu-id="1fc8b-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fc8b-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fc8b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fc8b-126">CommonParameters</span></span>
<span data-ttu-id="1fc8b-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1fc8b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fc8b-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fc8b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fc8b-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1fc8b-129">INPUTS</span></span>

## <span data-ttu-id="1fc8b-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fc8b-130">OUTPUTS</span></span>

## <span data-ttu-id="1fc8b-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="1fc8b-131">NOTES</span></span>

## <span data-ttu-id="1fc8b-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1fc8b-132">RELATED LINKS</span></span>

