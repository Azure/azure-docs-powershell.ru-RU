---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 19c8f8fce7c3711c5002f9588900e6bdf8efcbb0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731768"
---
# <span data-ttu-id="bbdf6-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="bbdf6-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="bbdf6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bbdf6-102">SYNOPSIS</span></span>
<span data-ttu-id="bbdf6-103">Возобновляет Запущенный ранее прогон обновления, который завершился сбоем.</span><span class="sxs-lookup"><span data-stu-id="bbdf6-103">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="bbdf6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bbdf6-104">SYNTAX</span></span>

### <span data-ttu-id="bbdf6-105">UpdateRuns_Rerun (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bbdf6-105">UpdateRuns_Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> [-Location <String>] [-ResourceGroupName <String>] -UpdateName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbdf6-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="bbdf6-106">ResourceId</span></span>
```
Resume-AzsUpdateRun [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbdf6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbdf6-107">DESCRIPTION</span></span>
<span data-ttu-id="bbdf6-108">Возобновляет Запущенный ранее прогон обновления, который завершился сбоем.</span><span class="sxs-lookup"><span data-stu-id="bbdf6-108">Resumes a previously started update run that failed.</span></span> <span data-ttu-id="bbdf6-109">Возобновление прогонов обновления возобновится на момент последнего сбоя.</span><span class="sxs-lookup"><span data-stu-id="bbdf6-109">Resumeed update runs will resume at the point they last failed.</span></span>

## <span data-ttu-id="bbdf6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bbdf6-110">EXAMPLES</span></span>

### <span data-ttu-id="bbdf6-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="bbdf6-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdateRun -Name 5173e9f4-3040-494f-b7a7-738a6331d55c -UpdateName Microsoft1.0.180305.1 | Resume-AzsUpdateRun
```

<span data-ttu-id="bbdf6-112">Возобновляет Запущенный ранее прогон обновления, который завершился сбоем.</span><span class="sxs-lookup"><span data-stu-id="bbdf6-112">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="bbdf6-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bbdf6-113">PARAMETERS</span></span>

### <span data-ttu-id="bbdf6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bbdf6-114">-AsJob</span></span>
<span data-ttu-id="bbdf6-115">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="bbdf6-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="bbdf6-116">-Force</span><span class="sxs-lookup"><span data-stu-id="bbdf6-116">-Force</span></span>
<span data-ttu-id="bbdf6-117">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="bbdf6-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="bbdf6-118">-Location</span><span class="sxs-lookup"><span data-stu-id="bbdf6-118">-Location</span></span>
<span data-ttu-id="bbdf6-119">Имя расположения обновления.</span><span class="sxs-lookup"><span data-stu-id="bbdf6-119">The name of the update location.</span></span>

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

### <span data-ttu-id="bbdf6-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bbdf6-120">-Name</span></span>
<span data-ttu-id="bbdf6-121">Обновите идентификатор выполнения.</span><span class="sxs-lookup"><span data-stu-id="bbdf6-121">Update run identifier.</span></span>

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

### <span data-ttu-id="bbdf6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbdf6-122">-ResourceGroupName</span></span>
<span data-ttu-id="bbdf6-123">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="bbdf6-123">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="bbdf6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bbdf6-124">-ResourceId</span></span>
<span data-ttu-id="bbdf6-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="bbdf6-125">The resource id.</span></span>

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

### <span data-ttu-id="bbdf6-126">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="bbdf6-126">-UpdateName</span></span>
<span data-ttu-id="bbdf6-127">Отображаемое имя обновления.</span><span class="sxs-lookup"><span data-stu-id="bbdf6-127">Display name of the update.</span></span>

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

### <span data-ttu-id="bbdf6-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bbdf6-128">-Confirm</span></span>
<span data-ttu-id="bbdf6-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bbdf6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbdf6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbdf6-130">-WhatIf</span></span>
<span data-ttu-id="bbdf6-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bbdf6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbdf6-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bbdf6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbdf6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbdf6-133">CommonParameters</span></span>
<span data-ttu-id="bbdf6-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bbdf6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbdf6-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbdf6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbdf6-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bbdf6-136">INPUTS</span></span>

## <span data-ttu-id="bbdf6-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbdf6-137">OUTPUTS</span></span>

## <span data-ttu-id="bbdf6-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="bbdf6-138">NOTES</span></span>

## <span data-ttu-id="bbdf6-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bbdf6-139">RELATED LINKS</span></span>

