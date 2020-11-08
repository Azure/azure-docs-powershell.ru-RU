---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75010b9591b4211f32c5665aa969bae28d69aaea
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076685"
---
# <span data-ttu-id="17c27-101">Remove-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="17c27-101">Remove-AzsPlan</span></span>

## <span data-ttu-id="17c27-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="17c27-102">SYNOPSIS</span></span>
<span data-ttu-id="17c27-103">Удаляет указанный план</span><span class="sxs-lookup"><span data-stu-id="17c27-103">Removes the specified plan</span></span>

## <span data-ttu-id="17c27-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="17c27-104">SYNTAX</span></span>

### <span data-ttu-id="17c27-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="17c27-105">Delete (Default)</span></span>
```
Remove-AzsPlan -Name <String> -ResourceGroupName <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17c27-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="17c27-106">ResourceId</span></span>
```
Remove-AzsPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17c27-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="17c27-107">DESCRIPTION</span></span>
<span data-ttu-id="17c27-108">Удаляет указанный план</span><span class="sxs-lookup"><span data-stu-id="17c27-108">Removes the specified plan</span></span>

## <span data-ttu-id="17c27-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="17c27-109">EXAMPLES</span></span>

### <span data-ttu-id="17c27-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="17c27-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlan -Name plan1 -ResourceGroupName "rg1"
```

<span data-ttu-id="17c27-111">Удаляет указанный план</span><span class="sxs-lookup"><span data-stu-id="17c27-111">Removes the specified plan</span></span>

## <span data-ttu-id="17c27-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="17c27-112">PARAMETERS</span></span>

### <span data-ttu-id="17c27-113">-Force</span><span class="sxs-lookup"><span data-stu-id="17c27-113">-Force</span></span>
<span data-ttu-id="17c27-114">Пометка для удаления элемента без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="17c27-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="17c27-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="17c27-115">-Name</span></span>
<span data-ttu-id="17c27-116">Название плана.</span><span class="sxs-lookup"><span data-stu-id="17c27-116">Name of the plan.</span></span>

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

### <span data-ttu-id="17c27-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17c27-117">-ResourceGroupName</span></span>
<span data-ttu-id="17c27-118">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="17c27-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="17c27-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17c27-119">-ResourceId</span></span>
<span data-ttu-id="17c27-120">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="17c27-120">The resource id.</span></span>

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

### <span data-ttu-id="17c27-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17c27-121">-Confirm</span></span>
<span data-ttu-id="17c27-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="17c27-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17c27-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17c27-123">-WhatIf</span></span>
<span data-ttu-id="17c27-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="17c27-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17c27-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="17c27-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17c27-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17c27-126">CommonParameters</span></span>
<span data-ttu-id="17c27-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="17c27-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17c27-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17c27-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17c27-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="17c27-129">INPUTS</span></span>

## <span data-ttu-id="17c27-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="17c27-130">OUTPUTS</span></span>

## <span data-ttu-id="17c27-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="17c27-131">NOTES</span></span>

## <span data-ttu-id="17c27-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="17c27-132">RELATED LINKS</span></span>
