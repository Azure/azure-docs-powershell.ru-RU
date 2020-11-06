---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6de990526330cdd192cd99707aacc1e06ad49c5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556335"
---
# <span data-ttu-id="6b007-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="6b007-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="6b007-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6b007-102">SYNOPSIS</span></span>
<span data-ttu-id="6b007-103">Включите или выключите узел шкалной единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="6b007-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="6b007-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6b007-104">SYNTAX</span></span>

### <span data-ttu-id="6b007-105">Остановить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6b007-105">Stop (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Shutdown] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b007-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b007-106">ResourceId</span></span>
```
Stop-AzsScaleUnitNode -ResourceId <String> [-Shutdown] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6b007-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b007-107">DESCRIPTION</span></span>
<span data-ttu-id="6b007-108">Включите или выключите узел шкалной единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="6b007-108">Power off a scale unit node.</span></span>

## <span data-ttu-id="6b007-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6b007-109">EXAMPLES</span></span>

### <span data-ttu-id="6b007-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6b007-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236" -Shutdown
```

<span data-ttu-id="6b007-111">Завершение работы узла масштабируемой единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="6b007-111">Shutdown a scale unit node.</span></span>

### <span data-ttu-id="6b007-112">--------------------------ПРИМЕР 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="6b007-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="6b007-113">Включите или выключите узел масштабируемой единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="6b007-113">Power down a scale unit node.</span></span>

## <span data-ttu-id="6b007-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6b007-114">PARAMETERS</span></span>

### <span data-ttu-id="6b007-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b007-115">-AsJob</span></span>
<span data-ttu-id="6b007-116">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="6b007-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="6b007-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6b007-117">-Force</span></span>
<span data-ttu-id="6b007-118">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="6b007-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="6b007-119">-Location</span><span class="sxs-lookup"><span data-stu-id="6b007-119">-Location</span></span>
<span data-ttu-id="6b007-120">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="6b007-120">Location of the resource.</span></span>

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

### <span data-ttu-id="6b007-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6b007-121">-Name</span></span>
<span data-ttu-id="6b007-122">Имя узла единиц масштабирования.</span><span class="sxs-lookup"><span data-stu-id="6b007-122">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="6b007-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b007-123">-ResourceGroupName</span></span>
<span data-ttu-id="6b007-124">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6b007-124">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="6b007-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b007-125">-ResourceId</span></span>
<span data-ttu-id="6b007-126">Идентификатор ресурса узла единицы масштабирования.</span><span class="sxs-lookup"><span data-stu-id="6b007-126">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="6b007-127">-Shutdown</span><span class="sxs-lookup"><span data-stu-id="6b007-127">-Shutdown</span></span>
<span data-ttu-id="6b007-128">Если вы установили мягкое завершение работы узла масштабирования, выберите элемент. в противном случае не заключайте элемент масштабирования на узел единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="6b007-128">If set gracefully shutdown the scale unit node; otherwise hard power off the scale unit node.</span></span>

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

### <span data-ttu-id="6b007-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b007-129">-Confirm</span></span>
<span data-ttu-id="6b007-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6b007-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b007-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b007-131">-WhatIf</span></span>
<span data-ttu-id="6b007-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6b007-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b007-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6b007-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b007-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b007-134">CommonParameters</span></span>
<span data-ttu-id="6b007-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6b007-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b007-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b007-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b007-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6b007-137">INPUTS</span></span>

## <span data-ttu-id="6b007-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b007-138">OUTPUTS</span></span>

## <span data-ttu-id="6b007-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="6b007-139">NOTES</span></span>

## <span data-ttu-id="6b007-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b007-140">RELATED LINKS</span></span>

