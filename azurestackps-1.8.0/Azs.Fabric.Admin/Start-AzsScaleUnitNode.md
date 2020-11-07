---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4c51249856d9cd8c8fc47d4968b1bc011040610e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "93908101"
---
# <span data-ttu-id="d5a4c-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="d5a4c-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="d5a4c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d5a4c-102">SYNOPSIS</span></span>
<span data-ttu-id="d5a4c-103">Постепенное масштабирование на узле единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="d5a4c-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="d5a4c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d5a4c-104">SYNTAX</span></span>

### <span data-ttu-id="d5a4c-105">PowerOn (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d5a4c-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5a4c-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5a4c-106">ResourceId</span></span>
```
Start-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5a4c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5a4c-107">DESCRIPTION</span></span>
<span data-ttu-id="d5a4c-108">Постепенное масштабирование на узле единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="d5a4c-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="d5a4c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d5a4c-109">EXAMPLES</span></span>

### <span data-ttu-id="d5a4c-110">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="d5a4c-110">EXAMPLE 1</span></span>
```
Start-AzsScaleUnitNode -Name "AzS-ACS01"
```

<span data-ttu-id="d5a4c-111">ProvisioningState: выполнено успешно</span><span class="sxs-lookup"><span data-stu-id="d5a4c-111">ProvisioningState : Succeeded</span></span>

<span data-ttu-id="d5a4c-112">Постепенное масштабирование на узле единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="d5a4c-112">Power on a scale unit node.</span></span>

## <span data-ttu-id="d5a4c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d5a4c-113">PARAMETERS</span></span>

### <span data-ttu-id="d5a4c-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d5a4c-114">-Name</span></span>
<span data-ttu-id="d5a4c-115">Имя узла единиц масштабирования.</span><span class="sxs-lookup"><span data-stu-id="d5a4c-115">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="d5a4c-116">-Location</span><span class="sxs-lookup"><span data-stu-id="d5a4c-116">-Location</span></span>
<span data-ttu-id="d5a4c-117">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="d5a4c-117">Location of the resource.</span></span>

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

### <span data-ttu-id="d5a4c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5a4c-118">-ResourceGroupName</span></span>
<span data-ttu-id="d5a4c-119">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d5a4c-119">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="d5a4c-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5a4c-120">-ResourceId</span></span>
<span data-ttu-id="d5a4c-121">Идентификатор ресурса узла единицы масштабирования.</span><span class="sxs-lookup"><span data-stu-id="d5a4c-121">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="d5a4c-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d5a4c-122">-AsJob</span></span>
<span data-ttu-id="d5a4c-123">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="d5a4c-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="d5a4c-124">-Force</span><span class="sxs-lookup"><span data-stu-id="d5a4c-124">-Force</span></span>
<span data-ttu-id="d5a4c-125">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="d5a4c-125">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="d5a4c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5a4c-126">-WhatIf</span></span>
<span data-ttu-id="d5a4c-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d5a4c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5a4c-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d5a4c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5a4c-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d5a4c-129">-Confirm</span></span>
<span data-ttu-id="d5a4c-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d5a4c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5a4c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5a4c-131">CommonParameters</span></span>
<span data-ttu-id="d5a4c-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d5a4c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5a4c-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5a4c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5a4c-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d5a4c-134">INPUTS</span></span>

## <span data-ttu-id="d5a4c-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5a4c-135">OUTPUTS</span></span>

## <span data-ttu-id="d5a4c-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="d5a4c-136">NOTES</span></span>

## <span data-ttu-id="d5a4c-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5a4c-137">RELATED LINKS</span></span>
