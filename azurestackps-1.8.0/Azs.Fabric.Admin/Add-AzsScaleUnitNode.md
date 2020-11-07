---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ced1207f07360c0a18674d6f8ae4170be9b87beb
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908209"
---
# <span data-ttu-id="c3a93-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="c3a93-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="c3a93-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c3a93-102">SYNOPSIS</span></span>
<span data-ttu-id="c3a93-103">Добавьте новую единицу измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="c3a93-103">Add a new scale unit.</span></span>

## <span data-ttu-id="c3a93-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c3a93-104">SYNTAX</span></span>

### <span data-ttu-id="c3a93-105">Масштабирование (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c3a93-105">ScaleOut (Default)</span></span>
```
Add-AzsScaleUnitNode -Name <String> -NodeList <ScaleOutScaleUnitParameters[]> [-AwaitStorageConvergence]
 [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3a93-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3a93-106">ResourceId</span></span>
```
Add-AzsScaleUnitNode -NodeList <ScaleOutScaleUnitParameters[]> [-AwaitStorageConvergence] -ResourceId <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3a93-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3a93-107">DESCRIPTION</span></span>
<span data-ttu-id="c3a93-108">Добавьте новую единицу измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="c3a93-108">Add a new scale unit.</span></span>

## <span data-ttu-id="c3a93-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c3a93-109">EXAMPLES</span></span>

### <span data-ttu-id="c3a93-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c3a93-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsScaleUnitNode -ScaleUnitName "Azs-ERC03" -NodeList $nodeList
```

<span data-ttu-id="c3a93-111">Добавьте новый узел шкалы измерения.</span><span class="sxs-lookup"><span data-stu-id="c3a93-111">Add a new scale unit node.</span></span>

## <span data-ttu-id="c3a93-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c3a93-112">PARAMETERS</span></span>

### <span data-ttu-id="c3a93-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3a93-113">-AsJob</span></span>
<span data-ttu-id="c3a93-114">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="c3a93-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="c3a93-115">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="c3a93-115">-AwaitStorageConvergence</span></span>
<span data-ttu-id="c3a93-116">Флаг указывает, должна ли операция ждать, пока хранилище не будет получено, прежде чем возвращать его.</span><span class="sxs-lookup"><span data-stu-id="c3a93-116">Flag indicates if the operation should wait for storage to converge before returning.</span></span>

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

### <span data-ttu-id="c3a93-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c3a93-117">-Force</span></span>
<span data-ttu-id="c3a93-118">Не запрашивать подтверждение</span><span class="sxs-lookup"><span data-stu-id="c3a93-118">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="c3a93-119">-Location</span><span class="sxs-lookup"><span data-stu-id="c3a93-119">-Location</span></span>
<span data-ttu-id="c3a93-120">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="c3a93-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ScaleOut
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3a93-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c3a93-121">-Name</span></span>
<span data-ttu-id="c3a93-122">{{Описание имени заливки}}</span><span class="sxs-lookup"><span data-stu-id="c3a93-122">{{Fill Name Description}}</span></span>

```yaml
Type: String
Parameter Sets: ScaleOut
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3a93-123">-NodeList</span><span class="sxs-lookup"><span data-stu-id="c3a93-123">-NodeList</span></span>
<span data-ttu-id="c3a93-124">Список узлов в единице масштабирования.</span><span class="sxs-lookup"><span data-stu-id="c3a93-124">List of nodes in the scale unit.</span></span>

```yaml
Type: ScaleOutScaleUnitParameters[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3a93-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3a93-125">-ResourceGroupName</span></span>
<span data-ttu-id="c3a93-126">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c3a93-126">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: ScaleOut
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3a93-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3a93-127">-ResourceId</span></span>
<span data-ttu-id="c3a93-128">Идентификатор ресурса узла единицы масштабирования.</span><span class="sxs-lookup"><span data-stu-id="c3a93-128">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="c3a93-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c3a93-129">-Confirm</span></span>
<span data-ttu-id="c3a93-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c3a93-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3a93-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3a93-131">-WhatIf</span></span>
<span data-ttu-id="c3a93-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c3a93-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3a93-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c3a93-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3a93-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3a93-134">CommonParameters</span></span>
<span data-ttu-id="c3a93-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c3a93-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3a93-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3a93-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3a93-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c3a93-137">INPUTS</span></span>

## <span data-ttu-id="c3a93-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3a93-138">OUTPUTS</span></span>

## <span data-ttu-id="c3a93-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="c3a93-139">NOTES</span></span>

## <span data-ttu-id="c3a93-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c3a93-140">RELATED LINKS</span></span>

