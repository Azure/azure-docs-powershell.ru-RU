---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4c51249856d9cd8c8fc47d4968b1bc011040610e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2020
ms.locfileid: "93909253"
---
# <span data-ttu-id="1852b-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="1852b-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="1852b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1852b-102">SYNOPSIS</span></span>
<span data-ttu-id="1852b-103">Постепенное масштабирование на узле единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="1852b-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="1852b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1852b-104">SYNTAX</span></span>

### <span data-ttu-id="1852b-105">PowerOn (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1852b-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1852b-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1852b-106">ResourceId</span></span>
```
Start-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1852b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1852b-107">DESCRIPTION</span></span>
<span data-ttu-id="1852b-108">Постепенное масштабирование на узле единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="1852b-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="1852b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1852b-109">EXAMPLES</span></span>

### <span data-ttu-id="1852b-110">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="1852b-110">EXAMPLE 1</span></span>
```
Start-AzsScaleUnitNode -Name "AzS-ACS01"
```

<span data-ttu-id="1852b-111">ProvisioningState: выполнено успешно</span><span class="sxs-lookup"><span data-stu-id="1852b-111">ProvisioningState : Succeeded</span></span>

<span data-ttu-id="1852b-112">Постепенное масштабирование на узле единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="1852b-112">Power on a scale unit node.</span></span>

## <span data-ttu-id="1852b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1852b-113">PARAMETERS</span></span>

### <span data-ttu-id="1852b-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1852b-114">-Name</span></span>
<span data-ttu-id="1852b-115">Имя узла единиц масштабирования.</span><span class="sxs-lookup"><span data-stu-id="1852b-115">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="1852b-116">-Location</span><span class="sxs-lookup"><span data-stu-id="1852b-116">-Location</span></span>
<span data-ttu-id="1852b-117">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="1852b-117">Location of the resource.</span></span>

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

### <span data-ttu-id="1852b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1852b-118">-ResourceGroupName</span></span>
<span data-ttu-id="1852b-119">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1852b-119">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="1852b-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1852b-120">-ResourceId</span></span>
<span data-ttu-id="1852b-121">Идентификатор ресурса узла единицы масштабирования.</span><span class="sxs-lookup"><span data-stu-id="1852b-121">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="1852b-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1852b-122">-AsJob</span></span>
<span data-ttu-id="1852b-123">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="1852b-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="1852b-124">-Force</span><span class="sxs-lookup"><span data-stu-id="1852b-124">-Force</span></span>
<span data-ttu-id="1852b-125">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="1852b-125">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="1852b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1852b-126">-WhatIf</span></span>
<span data-ttu-id="1852b-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1852b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1852b-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1852b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1852b-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1852b-129">-Confirm</span></span>
<span data-ttu-id="1852b-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1852b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1852b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1852b-131">CommonParameters</span></span>
<span data-ttu-id="1852b-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1852b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1852b-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1852b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1852b-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1852b-134">INPUTS</span></span>

## <span data-ttu-id="1852b-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1852b-135">OUTPUTS</span></span>

## <span data-ttu-id="1852b-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="1852b-136">NOTES</span></span>

## <span data-ttu-id="1852b-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1852b-137">RELATED LINKS</span></span>
