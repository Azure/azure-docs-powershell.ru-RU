---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb3b784d079d1de3cec1d4fe3ec50a2853a4b054
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908006"
---
# <span data-ttu-id="38dea-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="38dea-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="38dea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="38dea-102">SYNOPSIS</span></span>
<span data-ttu-id="38dea-103">Возобновляет Запущенный ранее прогон обновления, который завершился сбоем.</span><span class="sxs-lookup"><span data-stu-id="38dea-103">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="38dea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="38dea-104">SYNTAX</span></span>

### <span data-ttu-id="38dea-105">UpdateRuns_Rerun (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="38dea-105">UpdateRuns_Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> [-Location <String>] [-ResourceGroupName <String>] -UpdateName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38dea-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="38dea-106">ResourceId</span></span>
```
Resume-AzsUpdateRun [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38dea-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="38dea-107">DESCRIPTION</span></span>
<span data-ttu-id="38dea-108">Возобновляет Запущенный ранее прогон обновления, который завершился сбоем.</span><span class="sxs-lookup"><span data-stu-id="38dea-108">Resumes a previously started update run that failed.</span></span> <span data-ttu-id="38dea-109">Возобновление прогонов обновления возобновится на момент последнего сбоя.</span><span class="sxs-lookup"><span data-stu-id="38dea-109">Resumeed update runs will resume at the point they last failed.</span></span>

## <span data-ttu-id="38dea-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="38dea-110">EXAMPLES</span></span>

### <span data-ttu-id="38dea-111">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="38dea-111">EXAMPLE 1</span></span>
```
Get-AzsUpdateRun -Name 5173e9f4-3040-494f-b7a7-738a6331d55c -UpdateName Microsoft1.0.180305.1 | Resume-AzsUpdateRun
```

<span data-ttu-id="38dea-112">Возобновляет Запущенный ранее прогон обновления, который завершился сбоем.</span><span class="sxs-lookup"><span data-stu-id="38dea-112">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="38dea-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="38dea-113">PARAMETERS</span></span>

### <span data-ttu-id="38dea-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="38dea-114">-Name</span></span>
<span data-ttu-id="38dea-115">Обновите идентификатор выполнения.</span><span class="sxs-lookup"><span data-stu-id="38dea-115">Update run identifier.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38dea-116">-Location</span><span class="sxs-lookup"><span data-stu-id="38dea-116">-Location</span></span>
<span data-ttu-id="38dea-117">Имя расположения обновления.</span><span class="sxs-lookup"><span data-stu-id="38dea-117">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38dea-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38dea-118">-ResourceGroupName</span></span>
<span data-ttu-id="38dea-119">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="38dea-119">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38dea-120">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="38dea-120">-UpdateName</span></span>
<span data-ttu-id="38dea-121">Отображаемое имя обновления.</span><span class="sxs-lookup"><span data-stu-id="38dea-121">Display name of the update.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38dea-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38dea-122">-AsJob</span></span>
<span data-ttu-id="38dea-123">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="38dea-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="38dea-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38dea-124">-ResourceId</span></span>
<span data-ttu-id="38dea-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="38dea-125">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38dea-126">-Force</span><span class="sxs-lookup"><span data-stu-id="38dea-126">-Force</span></span>
<span data-ttu-id="38dea-127">Пометка для удаления элемента без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="38dea-127">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="38dea-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38dea-128">-WhatIf</span></span>
<span data-ttu-id="38dea-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="38dea-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38dea-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="38dea-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38dea-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38dea-131">-Confirm</span></span>
<span data-ttu-id="38dea-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="38dea-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38dea-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38dea-133">CommonParameters</span></span>
<span data-ttu-id="38dea-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="38dea-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38dea-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38dea-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38dea-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="38dea-136">INPUTS</span></span>

## <span data-ttu-id="38dea-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="38dea-137">OUTPUTS</span></span>

## <span data-ttu-id="38dea-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="38dea-138">NOTES</span></span>

## <span data-ttu-id="38dea-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="38dea-139">RELATED LINKS</span></span>
