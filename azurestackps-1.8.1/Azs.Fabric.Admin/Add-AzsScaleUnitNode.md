---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ced1207f07360c0a18674d6f8ae4170be9b87beb
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93909258"
---
# <span data-ttu-id="b3de9-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="b3de9-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="b3de9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b3de9-102">SYNOPSIS</span></span>
<span data-ttu-id="b3de9-103">Добавьте новую единицу измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="b3de9-103">Add a new scale unit.</span></span>

## <span data-ttu-id="b3de9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b3de9-104">SYNTAX</span></span>

### <span data-ttu-id="b3de9-105">Масштабирование (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b3de9-105">ScaleOut (Default)</span></span>
```
Add-AzsScaleUnitNode -Name <String> -NodeList <ScaleOutScaleUnitParameters[]> [-AwaitStorageConvergence]
 [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3de9-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3de9-106">ResourceId</span></span>
```
Add-AzsScaleUnitNode -NodeList <ScaleOutScaleUnitParameters[]> [-AwaitStorageConvergence] -ResourceId <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3de9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3de9-107">DESCRIPTION</span></span>
<span data-ttu-id="b3de9-108">Добавьте новую единицу измерения шкалы.</span><span class="sxs-lookup"><span data-stu-id="b3de9-108">Add a new scale unit.</span></span>

## <span data-ttu-id="b3de9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b3de9-109">EXAMPLES</span></span>

### <span data-ttu-id="b3de9-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b3de9-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsScaleUnitNode -ScaleUnitName "Azs-ERC03" -NodeList $nodeList
```

<span data-ttu-id="b3de9-111">Добавьте новый узел шкалы измерения.</span><span class="sxs-lookup"><span data-stu-id="b3de9-111">Add a new scale unit node.</span></span>

## <span data-ttu-id="b3de9-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b3de9-112">PARAMETERS</span></span>

### <span data-ttu-id="b3de9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3de9-113">-AsJob</span></span>
<span data-ttu-id="b3de9-114">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="b3de9-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="b3de9-115">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="b3de9-115">-AwaitStorageConvergence</span></span>
<span data-ttu-id="b3de9-116">Флаг указывает, должна ли операция ждать, пока хранилище не будет получено, прежде чем возвращать его.</span><span class="sxs-lookup"><span data-stu-id="b3de9-116">Flag indicates if the operation should wait for storage to converge before returning.</span></span>

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

### <span data-ttu-id="b3de9-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b3de9-117">-Force</span></span>
<span data-ttu-id="b3de9-118">Не запрашивать подтверждение</span><span class="sxs-lookup"><span data-stu-id="b3de9-118">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="b3de9-119">-Location</span><span class="sxs-lookup"><span data-stu-id="b3de9-119">-Location</span></span>
<span data-ttu-id="b3de9-120">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="b3de9-120">Location of the resource.</span></span>

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

### <span data-ttu-id="b3de9-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b3de9-121">-Name</span></span>
<span data-ttu-id="b3de9-122">{{Описание имени заливки}}</span><span class="sxs-lookup"><span data-stu-id="b3de9-122">{{Fill Name Description}}</span></span>

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

### <span data-ttu-id="b3de9-123">-NodeList</span><span class="sxs-lookup"><span data-stu-id="b3de9-123">-NodeList</span></span>
<span data-ttu-id="b3de9-124">Список узлов в единице масштабирования.</span><span class="sxs-lookup"><span data-stu-id="b3de9-124">List of nodes in the scale unit.</span></span>

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

### <span data-ttu-id="b3de9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3de9-125">-ResourceGroupName</span></span>
<span data-ttu-id="b3de9-126">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b3de9-126">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="b3de9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3de9-127">-ResourceId</span></span>
<span data-ttu-id="b3de9-128">Идентификатор ресурса узла единицы масштабирования.</span><span class="sxs-lookup"><span data-stu-id="b3de9-128">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="b3de9-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3de9-129">-Confirm</span></span>
<span data-ttu-id="b3de9-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b3de9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3de9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3de9-131">-WhatIf</span></span>
<span data-ttu-id="b3de9-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b3de9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3de9-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b3de9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3de9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3de9-134">CommonParameters</span></span>
<span data-ttu-id="b3de9-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b3de9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3de9-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3de9-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3de9-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b3de9-137">INPUTS</span></span>

## <span data-ttu-id="b3de9-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3de9-138">OUTPUTS</span></span>

## <span data-ttu-id="b3de9-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="b3de9-139">NOTES</span></span>

## <span data-ttu-id="b3de9-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3de9-140">RELATED LINKS</span></span>

