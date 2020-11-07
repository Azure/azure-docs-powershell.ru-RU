---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c60245b9e6b8d44d8c465427c41c69e5cd442bb0
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93908874"
---
# <span data-ttu-id="13349-101">Disable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="13349-101">Disable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="13349-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="13349-102">SYNOPSIS</span></span>
<span data-ttu-id="13349-103">Запуск режима обслуживания для узла масштабируемой единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="13349-103">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="13349-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="13349-104">SYNTAX</span></span>

### <span data-ttu-id="13349-105">Отключить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="13349-105">Disable (Default)</span></span>
```
Disable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13349-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="13349-106">ResourceId</span></span>
```
Disable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13349-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13349-107">DESCRIPTION</span></span>
<span data-ttu-id="13349-108">Запуск режима обслуживания для узла масштабируемой единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="13349-108">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="13349-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="13349-109">EXAMPLES</span></span>

### <span data-ttu-id="13349-110">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="13349-110">EXAMPLE 1</span></span>
```
Disable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="13349-111">Включение режима обслуживания для узла масштабируемой единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="13349-111">Enable maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="13349-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="13349-112">PARAMETERS</span></span>

### <span data-ttu-id="13349-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="13349-113">-Name</span></span>
<span data-ttu-id="13349-114">Имя узла единиц масштабирования.</span><span class="sxs-lookup"><span data-stu-id="13349-114">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13349-115">-Location</span><span class="sxs-lookup"><span data-stu-id="13349-115">-Location</span></span>
<span data-ttu-id="13349-116">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="13349-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13349-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13349-117">-ResourceGroupName</span></span>
<span data-ttu-id="13349-118">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="13349-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13349-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13349-119">-ResourceId</span></span>
<span data-ttu-id="13349-120">Идентификатор ресурса узла единицы масштабирования.</span><span class="sxs-lookup"><span data-stu-id="13349-120">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="13349-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13349-121">-AsJob</span></span>
<span data-ttu-id="13349-122">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="13349-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="13349-123">-Force</span><span class="sxs-lookup"><span data-stu-id="13349-123">-Force</span></span>
<span data-ttu-id="13349-124">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="13349-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="13349-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13349-125">-WhatIf</span></span>
<span data-ttu-id="13349-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="13349-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13349-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="13349-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13349-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13349-128">-Confirm</span></span>
<span data-ttu-id="13349-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="13349-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13349-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13349-130">CommonParameters</span></span>
<span data-ttu-id="13349-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="13349-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13349-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13349-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13349-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="13349-133">INPUTS</span></span>

## <span data-ttu-id="13349-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="13349-134">OUTPUTS</span></span>

## <span data-ttu-id="13349-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="13349-135">NOTES</span></span>

## <span data-ttu-id="13349-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13349-136">RELATED LINKS</span></span>
