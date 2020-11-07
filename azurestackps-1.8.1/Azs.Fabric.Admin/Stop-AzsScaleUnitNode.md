---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f1a26c22b5714fc7db448935b31b0af685301217
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93909246"
---
# <span data-ttu-id="81d89-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="81d89-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="81d89-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="81d89-102">SYNOPSIS</span></span>
<span data-ttu-id="81d89-103">Включите или выключите узел шкалной единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="81d89-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="81d89-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="81d89-104">SYNTAX</span></span>

### <span data-ttu-id="81d89-105">Остановить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="81d89-105">Stop (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Shutdown] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81d89-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="81d89-106">ResourceId</span></span>
```
Stop-AzsScaleUnitNode -ResourceId <String> [-Shutdown] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81d89-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="81d89-107">DESCRIPTION</span></span>
<span data-ttu-id="81d89-108">Включите или выключите узел шкалной единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="81d89-108">Power off a scale unit node.</span></span>

## <span data-ttu-id="81d89-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="81d89-109">EXAMPLES</span></span>

### <span data-ttu-id="81d89-110">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="81d89-110">EXAMPLE 1</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236" -Shutdown
```

<span data-ttu-id="81d89-111">Завершение работы узла масштабируемой единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="81d89-111">Shutdown a scale unit node.</span></span>

### <span data-ttu-id="81d89-112">ПРИМЕР 2</span><span class="sxs-lookup"><span data-stu-id="81d89-112">EXAMPLE 2</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="81d89-113">Включите или выключите узел масштабируемой единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="81d89-113">Power down a scale unit node.</span></span>

## <span data-ttu-id="81d89-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="81d89-114">PARAMETERS</span></span>

### <span data-ttu-id="81d89-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="81d89-115">-Name</span></span>
<span data-ttu-id="81d89-116">Имя узла единиц масштабирования.</span><span class="sxs-lookup"><span data-stu-id="81d89-116">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d89-117">-Location</span><span class="sxs-lookup"><span data-stu-id="81d89-117">-Location</span></span>
<span data-ttu-id="81d89-118">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="81d89-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d89-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81d89-119">-ResourceGroupName</span></span>
<span data-ttu-id="81d89-120">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="81d89-120">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81d89-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81d89-121">-ResourceId</span></span>
<span data-ttu-id="81d89-122">Идентификатор ресурса узла единицы масштабирования.</span><span class="sxs-lookup"><span data-stu-id="81d89-122">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="81d89-123">-Shutdown</span><span class="sxs-lookup"><span data-stu-id="81d89-123">-Shutdown</span></span>
<span data-ttu-id="81d89-124">Если вы установили мягкое завершение работы узла масштабирования, выберите элемент. в противном случае не заключайте элемент масштабирования на узел единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="81d89-124">If set gracefully shutdown the scale unit node; otherwise hard power off the scale unit node.</span></span>

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

### <span data-ttu-id="81d89-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81d89-125">-AsJob</span></span>
<span data-ttu-id="81d89-126">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="81d89-126">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="81d89-127">-Force</span><span class="sxs-lookup"><span data-stu-id="81d89-127">-Force</span></span>
<span data-ttu-id="81d89-128">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="81d89-128">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="81d89-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81d89-129">-WhatIf</span></span>
<span data-ttu-id="81d89-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="81d89-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81d89-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="81d89-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81d89-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81d89-132">-Confirm</span></span>
<span data-ttu-id="81d89-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="81d89-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81d89-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81d89-134">CommonParameters</span></span>
<span data-ttu-id="81d89-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="81d89-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81d89-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81d89-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81d89-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="81d89-137">INPUTS</span></span>

## <span data-ttu-id="81d89-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="81d89-138">OUTPUTS</span></span>

## <span data-ttu-id="81d89-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="81d89-139">NOTES</span></span>

## <span data-ttu-id="81d89-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="81d89-140">RELATED LINKS</span></span>
