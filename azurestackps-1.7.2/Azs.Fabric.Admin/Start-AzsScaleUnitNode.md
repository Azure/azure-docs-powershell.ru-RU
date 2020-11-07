---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c5de84b66283d683d121c99c0cf2e0ea27a4a66
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907826"
---
# <span data-ttu-id="90bed-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="90bed-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="90bed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="90bed-102">SYNOPSIS</span></span>
<span data-ttu-id="90bed-103">Постепенное масштабирование на узле единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="90bed-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="90bed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="90bed-104">SYNTAX</span></span>

### <span data-ttu-id="90bed-105">PowerOn (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="90bed-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90bed-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="90bed-106">ResourceId</span></span>
```
Start-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90bed-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="90bed-107">DESCRIPTION</span></span>
<span data-ttu-id="90bed-108">Постепенное масштабирование на узле единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="90bed-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="90bed-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="90bed-109">EXAMPLES</span></span>

### <span data-ttu-id="90bed-110">--------------------------ПРИМЕР 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="90bed-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsScaleUnitNode -Name "AzS-ACS01"
```

<span data-ttu-id="90bed-111">ProvisioningState: выполнено успешно</span><span class="sxs-lookup"><span data-stu-id="90bed-111">ProvisioningState : Succeeded</span></span>

<span data-ttu-id="90bed-112">Постепенное масштабирование на узле единиц измерения.</span><span class="sxs-lookup"><span data-stu-id="90bed-112">Power on a scale unit node.</span></span>

## <span data-ttu-id="90bed-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="90bed-113">PARAMETERS</span></span>

### <span data-ttu-id="90bed-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90bed-114">-AsJob</span></span>
<span data-ttu-id="90bed-115">Запустите асинхронно как задание и верните объект задания.</span><span class="sxs-lookup"><span data-stu-id="90bed-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="90bed-116">-Force</span><span class="sxs-lookup"><span data-stu-id="90bed-116">-Force</span></span>
<span data-ttu-id="90bed-117">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="90bed-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="90bed-118">-Location</span><span class="sxs-lookup"><span data-stu-id="90bed-118">-Location</span></span>
<span data-ttu-id="90bed-119">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="90bed-119">Location of the resource.</span></span>

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

### <span data-ttu-id="90bed-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="90bed-120">-Name</span></span>
<span data-ttu-id="90bed-121">Имя узла единиц масштабирования.</span><span class="sxs-lookup"><span data-stu-id="90bed-121">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="90bed-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90bed-122">-ResourceGroupName</span></span>
<span data-ttu-id="90bed-123">Группа ресурсов, в которой зарегистрирован поставщик ресурсов.</span><span class="sxs-lookup"><span data-stu-id="90bed-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="90bed-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90bed-124">-ResourceId</span></span>
<span data-ttu-id="90bed-125">Идентификатор ресурса узла единицы масштабирования.</span><span class="sxs-lookup"><span data-stu-id="90bed-125">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="90bed-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90bed-126">-Confirm</span></span>
<span data-ttu-id="90bed-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="90bed-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90bed-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90bed-128">-WhatIf</span></span>
<span data-ttu-id="90bed-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="90bed-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90bed-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="90bed-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90bed-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90bed-131">CommonParameters</span></span>
<span data-ttu-id="90bed-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="90bed-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90bed-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90bed-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90bed-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="90bed-134">INPUTS</span></span>

## <span data-ttu-id="90bed-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="90bed-135">OUTPUTS</span></span>

## <span data-ttu-id="90bed-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="90bed-136">NOTES</span></span>

## <span data-ttu-id="90bed-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="90bed-137">RELATED LINKS</span></span>

