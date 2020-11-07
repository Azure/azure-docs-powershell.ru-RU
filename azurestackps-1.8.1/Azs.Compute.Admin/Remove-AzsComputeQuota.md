---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ebc1ebae40d6d1726ee6c23def6f82ff1efc8517
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93908906"
---
# <span data-ttu-id="04afb-101">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="04afb-101">Remove-AzsComputeQuota</span></span>

## <span data-ttu-id="04afb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="04afb-102">SYNOPSIS</span></span>
<span data-ttu-id="04afb-103">Удаляет указанную вычислительную квоту.</span><span class="sxs-lookup"><span data-stu-id="04afb-103">Deletes specified compute quota.</span></span>

## <span data-ttu-id="04afb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="04afb-104">SYNTAX</span></span>

### <span data-ttu-id="04afb-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="04afb-105">Delete (Default)</span></span>
```
Remove-AzsComputeQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04afb-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="04afb-106">ResourceId</span></span>
```
Remove-AzsComputeQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04afb-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="04afb-107">DESCRIPTION</span></span>
<span data-ttu-id="04afb-108">Удаление существующей квоты.</span><span class="sxs-lookup"><span data-stu-id="04afb-108">Delete an existing quota.</span></span>

## <span data-ttu-id="04afb-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="04afb-109">EXAMPLES</span></span>

### <span data-ttu-id="04afb-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="04afb-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsComputeQuota -Name ComputeQuota
```

<span data-ttu-id="04afb-111">Удаление вычислительной квоты с учетом всех параметров.</span><span class="sxs-lookup"><span data-stu-id="04afb-111">Remove a compute quota given all the parameters.</span></span>

## <span data-ttu-id="04afb-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="04afb-112">PARAMETERS</span></span>

### <span data-ttu-id="04afb-113">-Force</span><span class="sxs-lookup"><span data-stu-id="04afb-113">-Force</span></span>
<span data-ttu-id="04afb-114">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="04afb-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="04afb-115">-Location</span><span class="sxs-lookup"><span data-stu-id="04afb-115">-Location</span></span>
<span data-ttu-id="04afb-116">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="04afb-116">Location of the resource.</span></span> <span data-ttu-id="04afb-117">Если это значение не задано, по умолчанию используется расположение, связанное с подпиской на Tenat.</span><span class="sxs-lookup"><span data-stu-id="04afb-117">If not given we default to the location bound to the tenat's subscription.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04afb-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="04afb-118">-Name</span></span>
<span data-ttu-id="04afb-119">Имя квоты.</span><span class="sxs-lookup"><span data-stu-id="04afb-119">Name of the quota.</span></span>

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

### <span data-ttu-id="04afb-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04afb-120">-ResourceId</span></span>
<span data-ttu-id="04afb-121">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="04afb-121">The resource id.</span></span>

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

### <span data-ttu-id="04afb-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04afb-122">-Confirm</span></span>
<span data-ttu-id="04afb-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="04afb-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04afb-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04afb-124">-WhatIf</span></span>
<span data-ttu-id="04afb-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="04afb-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04afb-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="04afb-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04afb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04afb-127">CommonParameters</span></span>
<span data-ttu-id="04afb-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="04afb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04afb-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04afb-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04afb-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="04afb-130">INPUTS</span></span>

## <span data-ttu-id="04afb-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="04afb-131">OUTPUTS</span></span>

## <span data-ttu-id="04afb-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="04afb-132">NOTES</span></span>

## <span data-ttu-id="04afb-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="04afb-133">RELATED LINKS</span></span>

