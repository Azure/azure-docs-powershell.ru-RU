---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: aa4bd73f9300daf8ca17e3a11d884e06e9852234
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556179"
---
# <span data-ttu-id="a3dc0-101">Remove-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="a3dc0-101">Remove-AzsPlan</span></span>

## <span data-ttu-id="a3dc0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a3dc0-102">SYNOPSIS</span></span>
<span data-ttu-id="a3dc0-103">Удаляет указанный план</span><span class="sxs-lookup"><span data-stu-id="a3dc0-103">Removes the specified plan</span></span>

## <span data-ttu-id="a3dc0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a3dc0-104">SYNTAX</span></span>

### <span data-ttu-id="a3dc0-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a3dc0-105">Delete (Default)</span></span>
```
Remove-AzsPlan -Name <String> -ResourceGroupName <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3dc0-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3dc0-106">ResourceId</span></span>
```
Remove-AzsPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3dc0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3dc0-107">DESCRIPTION</span></span>
<span data-ttu-id="a3dc0-108">Удаляет указанный план</span><span class="sxs-lookup"><span data-stu-id="a3dc0-108">Removes the specified plan</span></span>

## <span data-ttu-id="a3dc0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a3dc0-109">EXAMPLES</span></span>

### <span data-ttu-id="a3dc0-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a3dc0-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlan -Name plan1 -ResourceGroupName "rg1"
```

<span data-ttu-id="a3dc0-111">Удаляет указанный план</span><span class="sxs-lookup"><span data-stu-id="a3dc0-111">Removes the specified plan</span></span>

## <span data-ttu-id="a3dc0-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a3dc0-112">PARAMETERS</span></span>

### <span data-ttu-id="a3dc0-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a3dc0-113">-Force</span></span>
<span data-ttu-id="a3dc0-114">Пометка для удаления элемента без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="a3dc0-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="a3dc0-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a3dc0-115">-Name</span></span>
<span data-ttu-id="a3dc0-116">Название плана.</span><span class="sxs-lookup"><span data-stu-id="a3dc0-116">Name of the plan.</span></span>

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

### <span data-ttu-id="a3dc0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3dc0-117">-ResourceGroupName</span></span>
<span data-ttu-id="a3dc0-118">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="a3dc0-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="a3dc0-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3dc0-119">-ResourceId</span></span>
<span data-ttu-id="a3dc0-120">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="a3dc0-120">The resource id.</span></span>

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

### <span data-ttu-id="a3dc0-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3dc0-121">-Confirm</span></span>
<span data-ttu-id="a3dc0-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a3dc0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3dc0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3dc0-123">-WhatIf</span></span>
<span data-ttu-id="a3dc0-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a3dc0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3dc0-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a3dc0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3dc0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3dc0-126">CommonParameters</span></span>
<span data-ttu-id="a3dc0-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a3dc0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3dc0-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3dc0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3dc0-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a3dc0-129">INPUTS</span></span>

## <span data-ttu-id="a3dc0-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3dc0-130">OUTPUTS</span></span>

## <span data-ttu-id="a3dc0-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="a3dc0-131">NOTES</span></span>

## <span data-ttu-id="a3dc0-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a3dc0-132">RELATED LINKS</span></span>

