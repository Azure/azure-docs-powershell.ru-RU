---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d77229892da63973513dd8870a949ff296f5538
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908197"
---
# <span data-ttu-id="ba440-101">Enable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="ba440-101">Enable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="ba440-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ba440-102">SYNOPSIS</span></span>
<span data-ttu-id="ba440-103">Отключение режима обслуживания для узла масштабируемой единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="ba440-103">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="ba440-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ba440-104">SYNTAX</span></span>

### <span data-ttu-id="ba440-105">Включить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ba440-105">Enable (Default)</span></span>
```
Enable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba440-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba440-106">ResourceId</span></span>
```
Enable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba440-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba440-107">DESCRIPTION</span></span>
<span data-ttu-id="ba440-108">Отключение режима обслуживания для узла масштабируемой единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="ba440-108">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="ba440-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ba440-109">EXAMPLES</span></span>

### <span data-ttu-id="ba440-110">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="ba440-110">EXAMPLE 1</span></span>
```
Enable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="ba440-111">Остановка режима обслуживания на узле шкалы.</span><span class="sxs-lookup"><span data-stu-id="ba440-111">Stop maintenance mode on a scale unit node.</span></span>

## <span data-ttu-id="ba440-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ba440-112">PARAMETERS</span></span>

### <span data-ttu-id="ba440-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ba440-113">-Name</span></span>
<span data-ttu-id="ba440-114">Имя узла единиц масштабирования.</span><span class="sxs-lookup"><span data-stu-id="ba440-114">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="ba440-115">-Location</span><span class="sxs-lookup"><span data-stu-id="ba440-115">-Location</span></span>
<span data-ttu-id="ba440-116">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="ba440-116">Location of the resource.</span></span>

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

### <span data-ttu-id="ba440-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba440-117">-ResourceGroupName</span></span>
<span data-ttu-id="ba440-118">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ba440-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="ba440-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba440-119">-ResourceId</span></span>
<span data-ttu-id="ba440-120">Идентификатор ресурса узла единицы масштабирования.</span><span class="sxs-lookup"><span data-stu-id="ba440-120">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="ba440-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba440-121">-AsJob</span></span>
<span data-ttu-id="ba440-122">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="ba440-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="ba440-123">-Force</span><span class="sxs-lookup"><span data-stu-id="ba440-123">-Force</span></span>
<span data-ttu-id="ba440-124">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ba440-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="ba440-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba440-125">-WhatIf</span></span>
<span data-ttu-id="ba440-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ba440-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba440-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ba440-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba440-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba440-128">-Confirm</span></span>
<span data-ttu-id="ba440-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ba440-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba440-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba440-130">CommonParameters</span></span>
<span data-ttu-id="ba440-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ba440-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba440-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba440-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba440-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ba440-133">INPUTS</span></span>

## <span data-ttu-id="ba440-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba440-134">OUTPUTS</span></span>

## <span data-ttu-id="ba440-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="ba440-135">NOTES</span></span>

## <span data-ttu-id="ba440-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba440-136">RELATED LINKS</span></span>
