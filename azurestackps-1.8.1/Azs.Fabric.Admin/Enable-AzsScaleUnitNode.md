---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d77229892da63973513dd8870a949ff296f5538
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93909257"
---
# <span data-ttu-id="d0516-101">Enable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="d0516-101">Enable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="d0516-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d0516-102">SYNOPSIS</span></span>
<span data-ttu-id="d0516-103">Отключение режима обслуживания для узла масштабируемой единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="d0516-103">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="d0516-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d0516-104">SYNTAX</span></span>

### <span data-ttu-id="d0516-105">Включить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d0516-105">Enable (Default)</span></span>
```
Enable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0516-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0516-106">ResourceId</span></span>
```
Enable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0516-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0516-107">DESCRIPTION</span></span>
<span data-ttu-id="d0516-108">Отключение режима обслуживания для узла масштабируемой единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="d0516-108">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="d0516-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d0516-109">EXAMPLES</span></span>

### <span data-ttu-id="d0516-110">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="d0516-110">EXAMPLE 1</span></span>
```
Enable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="d0516-111">Остановка режима обслуживания на узле шкалы.</span><span class="sxs-lookup"><span data-stu-id="d0516-111">Stop maintenance mode on a scale unit node.</span></span>

## <span data-ttu-id="d0516-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d0516-112">PARAMETERS</span></span>

### <span data-ttu-id="d0516-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d0516-113">-Name</span></span>
<span data-ttu-id="d0516-114">Имя узла единиц масштабирования.</span><span class="sxs-lookup"><span data-stu-id="d0516-114">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Enable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0516-115">-Location</span><span class="sxs-lookup"><span data-stu-id="d0516-115">-Location</span></span>
<span data-ttu-id="d0516-116">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="d0516-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Enable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0516-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0516-117">-ResourceGroupName</span></span>
<span data-ttu-id="d0516-118">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d0516-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Enable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0516-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0516-119">-ResourceId</span></span>
<span data-ttu-id="d0516-120">Идентификатор ресурса узла единицы масштабирования.</span><span class="sxs-lookup"><span data-stu-id="d0516-120">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="d0516-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0516-121">-AsJob</span></span>
<span data-ttu-id="d0516-122">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="d0516-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="d0516-123">-Force</span><span class="sxs-lookup"><span data-stu-id="d0516-123">-Force</span></span>
<span data-ttu-id="d0516-124">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="d0516-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="d0516-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0516-125">-WhatIf</span></span>
<span data-ttu-id="d0516-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d0516-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0516-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d0516-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0516-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0516-128">-Confirm</span></span>
<span data-ttu-id="d0516-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d0516-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0516-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0516-130">CommonParameters</span></span>
<span data-ttu-id="d0516-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d0516-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0516-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0516-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0516-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d0516-133">INPUTS</span></span>

## <span data-ttu-id="d0516-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0516-134">OUTPUTS</span></span>

## <span data-ttu-id="d0516-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="d0516-135">NOTES</span></span>

## <span data-ttu-id="d0516-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d0516-136">RELATED LINKS</span></span>
