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
ms.locfileid: "93731702"
---
# <span data-ttu-id="2e079-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="2e079-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="2e079-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2e079-102">SYNOPSIS</span></span>
<span data-ttu-id="2e079-103">Возобновляет Запущенный ранее прогон обновления, который завершился сбоем.</span><span class="sxs-lookup"><span data-stu-id="2e079-103">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="2e079-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2e079-104">SYNTAX</span></span>

### <span data-ttu-id="2e079-105">UpdateRuns_Rerun (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2e079-105">UpdateRuns_Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> [-Location <String>] [-ResourceGroupName <String>] -UpdateName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e079-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e079-106">ResourceId</span></span>
```
Resume-AzsUpdateRun [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e079-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e079-107">DESCRIPTION</span></span>
<span data-ttu-id="2e079-108">Возобновляет Запущенный ранее прогон обновления, который завершился сбоем.</span><span class="sxs-lookup"><span data-stu-id="2e079-108">Resumes a previously started update run that failed.</span></span> <span data-ttu-id="2e079-109">Возобновление прогонов обновления возобновится на момент последнего сбоя.</span><span class="sxs-lookup"><span data-stu-id="2e079-109">Resumeed update runs will resume at the point they last failed.</span></span>

## <span data-ttu-id="2e079-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2e079-110">EXAMPLES</span></span>

### <span data-ttu-id="2e079-111">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2e079-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdateRun -Name 5173e9f4-3040-494f-b7a7-738a6331d55c -UpdateName Microsoft1.0.180305.1 | Resume-AzsUpdateRun
```

<span data-ttu-id="2e079-112">Возобновляет Запущенный ранее прогон обновления, который завершился сбоем.</span><span class="sxs-lookup"><span data-stu-id="2e079-112">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="2e079-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2e079-113">PARAMETERS</span></span>

### <span data-ttu-id="2e079-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e079-114">-AsJob</span></span>
<span data-ttu-id="2e079-115">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="2e079-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="2e079-116">-Force</span><span class="sxs-lookup"><span data-stu-id="2e079-116">-Force</span></span>
<span data-ttu-id="2e079-117">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="2e079-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="2e079-118">-Location</span><span class="sxs-lookup"><span data-stu-id="2e079-118">-Location</span></span>
<span data-ttu-id="2e079-119">Имя расположения обновления.</span><span class="sxs-lookup"><span data-stu-id="2e079-119">The name of the update location.</span></span>

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

### <span data-ttu-id="2e079-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2e079-120">-Name</span></span>
<span data-ttu-id="2e079-121">Обновите идентификатор выполнения.</span><span class="sxs-lookup"><span data-stu-id="2e079-121">Update run identifier.</span></span>

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

### <span data-ttu-id="2e079-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e079-122">-ResourceGroupName</span></span>
<span data-ttu-id="2e079-123">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="2e079-123">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="2e079-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e079-124">-ResourceId</span></span>
<span data-ttu-id="2e079-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="2e079-125">The resource id.</span></span>

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

### <span data-ttu-id="2e079-126">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="2e079-126">-UpdateName</span></span>
<span data-ttu-id="2e079-127">Отображаемое имя обновления.</span><span class="sxs-lookup"><span data-stu-id="2e079-127">Display name of the update.</span></span>

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

### <span data-ttu-id="2e079-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e079-128">-Confirm</span></span>
<span data-ttu-id="2e079-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2e079-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e079-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e079-130">-WhatIf</span></span>
<span data-ttu-id="2e079-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2e079-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e079-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2e079-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e079-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e079-133">CommonParameters</span></span>
<span data-ttu-id="2e079-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2e079-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e079-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e079-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e079-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2e079-136">INPUTS</span></span>

## <span data-ttu-id="2e079-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e079-137">OUTPUTS</span></span>

## <span data-ttu-id="2e079-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="2e079-138">NOTES</span></span>

## <span data-ttu-id="2e079-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2e079-139">RELATED LINKS</span></span>

