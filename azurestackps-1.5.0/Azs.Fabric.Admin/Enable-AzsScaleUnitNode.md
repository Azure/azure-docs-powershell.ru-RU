---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 932d0b77fc6df9a88a2ee13ad92856727db82f06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555539"
---
# <span data-ttu-id="80e2f-101">Enable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="80e2f-101">Enable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="80e2f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="80e2f-102">SYNOPSIS</span></span>
<span data-ttu-id="80e2f-103">Отключение режима обслуживания для узла масштабируемой единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="80e2f-103">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="80e2f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="80e2f-104">SYNTAX</span></span>

### <span data-ttu-id="80e2f-105">Включить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="80e2f-105">Enable (Default)</span></span>
```
Enable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80e2f-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="80e2f-106">ResourceId</span></span>
```
Enable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80e2f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="80e2f-107">DESCRIPTION</span></span>
<span data-ttu-id="80e2f-108">Отключение режима обслуживания для узла масштабируемой единицы измерения.</span><span class="sxs-lookup"><span data-stu-id="80e2f-108">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="80e2f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="80e2f-109">EXAMPLES</span></span>

### <span data-ttu-id="80e2f-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="80e2f-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Enable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="80e2f-111">Остановка режима обслуживания на узле шкалы.</span><span class="sxs-lookup"><span data-stu-id="80e2f-111">Stop maintenance mode on a scale unit node.</span></span>

## <span data-ttu-id="80e2f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="80e2f-112">PARAMETERS</span></span>

### <span data-ttu-id="80e2f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80e2f-113">-AsJob</span></span>
<span data-ttu-id="80e2f-114">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="80e2f-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="80e2f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="80e2f-115">-Force</span></span>
<span data-ttu-id="80e2f-116">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="80e2f-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="80e2f-117">-Location</span><span class="sxs-lookup"><span data-stu-id="80e2f-117">-Location</span></span>
<span data-ttu-id="80e2f-118">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="80e2f-118">Location of the resource.</span></span>

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

### <span data-ttu-id="80e2f-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="80e2f-119">-Name</span></span>
<span data-ttu-id="80e2f-120">Имя узла единиц масштабирования.</span><span class="sxs-lookup"><span data-stu-id="80e2f-120">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="80e2f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80e2f-121">-ResourceGroupName</span></span>
<span data-ttu-id="80e2f-122">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="80e2f-122">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="80e2f-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80e2f-123">-ResourceId</span></span>
<span data-ttu-id="80e2f-124">Идентификатор ресурса узла единицы масштабирования.</span><span class="sxs-lookup"><span data-stu-id="80e2f-124">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="80e2f-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80e2f-125">-Confirm</span></span>
<span data-ttu-id="80e2f-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="80e2f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80e2f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80e2f-127">-WhatIf</span></span>
<span data-ttu-id="80e2f-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="80e2f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80e2f-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="80e2f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80e2f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80e2f-130">CommonParameters</span></span>
<span data-ttu-id="80e2f-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="80e2f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80e2f-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80e2f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80e2f-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="80e2f-133">INPUTS</span></span>

## <span data-ttu-id="80e2f-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="80e2f-134">OUTPUTS</span></span>

## <span data-ttu-id="80e2f-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="80e2f-135">NOTES</span></span>

## <span data-ttu-id="80e2f-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="80e2f-136">RELATED LINKS</span></span>

