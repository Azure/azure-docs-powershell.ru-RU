---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4c51249856d9cd8c8fc47d4968b1bc011040610e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076839"
---
# <span data-ttu-id="487af-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="487af-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="487af-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="487af-102">SYNOPSIS</span></span>
<span data-ttu-id="487af-103">Постепенное масштабирование на узле единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="487af-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="487af-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="487af-104">SYNTAX</span></span>

### <span data-ttu-id="487af-105">PowerOn (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="487af-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="487af-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="487af-106">ResourceId</span></span>
```
Start-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="487af-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="487af-107">DESCRIPTION</span></span>
<span data-ttu-id="487af-108">Постепенное масштабирование на узле единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="487af-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="487af-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="487af-109">EXAMPLES</span></span>

### <span data-ttu-id="487af-110">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="487af-110">EXAMPLE 1</span></span>
```
Start-AzsScaleUnitNode -Name "AzS-ACS01"
```

<span data-ttu-id="487af-111">ProvisioningState: выполнено успешно</span><span class="sxs-lookup"><span data-stu-id="487af-111">ProvisioningState : Succeeded</span></span>

<span data-ttu-id="487af-112">Постепенное масштабирование на узле единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="487af-112">Power on a scale unit node.</span></span>

## <span data-ttu-id="487af-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="487af-113">PARAMETERS</span></span>

### <span data-ttu-id="487af-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="487af-114">-Name</span></span>
<span data-ttu-id="487af-115">Имя узла единиц масштабирования.</span><span class="sxs-lookup"><span data-stu-id="487af-115">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="487af-116">-Location</span><span class="sxs-lookup"><span data-stu-id="487af-116">-Location</span></span>
<span data-ttu-id="487af-117">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="487af-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="487af-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="487af-118">-ResourceGroupName</span></span>
<span data-ttu-id="487af-119">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="487af-119">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="487af-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="487af-120">-ResourceId</span></span>
<span data-ttu-id="487af-121">Идентификатор ресурса узла единицы масштабирования.</span><span class="sxs-lookup"><span data-stu-id="487af-121">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="487af-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="487af-122">-AsJob</span></span>
<span data-ttu-id="487af-123">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="487af-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="487af-124">-Force</span><span class="sxs-lookup"><span data-stu-id="487af-124">-Force</span></span>
<span data-ttu-id="487af-125">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="487af-125">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="487af-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="487af-126">-WhatIf</span></span>
<span data-ttu-id="487af-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="487af-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="487af-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="487af-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="487af-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="487af-129">-Confirm</span></span>
<span data-ttu-id="487af-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="487af-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="487af-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="487af-131">CommonParameters</span></span>
<span data-ttu-id="487af-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="487af-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="487af-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="487af-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="487af-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="487af-134">INPUTS</span></span>

## <span data-ttu-id="487af-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="487af-135">OUTPUTS</span></span>

## <span data-ttu-id="487af-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="487af-136">NOTES</span></span>

## <span data-ttu-id="487af-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="487af-137">RELATED LINKS</span></span>
